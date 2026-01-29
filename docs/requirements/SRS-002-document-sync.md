---
id: SRS-002
title: Document Synchronization Software Requirements
status: approved
author: rune@ords.io
reviewers:
  - engineering
  - quality
approvers:
  - product
links:
  - URS-002
---

# Document Synchronization Software Requirements

## 1. Introduction

Defines technical requirements for GitHub document synchronization.

## 2. Requirements

### SRS-002-01: GitHub Webhook Processing

**Traces to:** URS-002-01

The system shall:
- Receive webhook events on push to connected repositories
- Validate webhook signature using HMAC-SHA256
- Process events within 30 seconds

### SRS-002-02: Frontmatter Parsing

**Traces to:** URS-002-04

The system shall parse YAML frontmatter with fields:
- id (required, string)
- title (required, string)
- version (required, string)
- status (required, enum: draft|approved|obsolete)
- links (optional, array of strings)

### SRS-002-03: Document Type Inference

**Traces to:** URS-002-02

Document type shall be inferred from:
1. Frontmatter `type` field (if present)
2. File path pattern matching
3. Filename prefix (URS-, SRS-, etc.)

### SRS-002-04: Changelog Generation

**Traces to:** URS-002-04

On each sync, create changelog entry with:
- Previous version hash
- New version hash
- Changed fields
- Sync timestamp
- User who triggered (if manual)

## 3. Data Model

```typescript
interface Document {
  id: string;
  repositoryId: string;
  path: string;
  title: string;
  type: DocumentType;
  status: 'draft' | 'approved' | 'obsolete';
  version: string;
  links: string[];
  contentHash: string;
  lastSyncedAt: Timestamp;
}
```
