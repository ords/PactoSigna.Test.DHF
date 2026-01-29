---
id: FMEA-001
title: Sync Engine FMEA
status: approved
author: rune@ords.io
reviewers:
  - engineering
  - quality
approvers:
  - product
links:
  - SDD-002
  - SRS-002
---

# Sync Engine Failure Mode Effects Analysis

## 1. FMEA Table

| ID | Failure Mode | Effect | Severity | Occurrence | Detection | RPN | Mitigation |
|----|--------------|--------|----------|------------|-----------|-----|------------|
| FM-01 | Webhook not received | Documents not synced | 7 | 3 | 5 | 105 | Manual sync, monitoring |
| FM-02 | Parse error in frontmatter | Document skipped | 4 | 5 | 2 | 40 | Validation, clear errors |
| FM-03 | GitHub API rate limit | Sync delayed | 5 | 4 | 3 | 60 | Caching, backoff |
| FM-04 | Firestore write failure | Data loss | 8 | 2 | 4 | 64 | Retries, transactions |
| FM-05 | Duplicate sync jobs | Wasted resources | 3 | 4 | 5 | 60 | Idempotency keys |

## 2. Severity Scale

| Score | Description |
|-------|-------------|
| 1-3 | Minor impact, workaround exists |
| 4-6 | Moderate impact, degraded functionality |
| 7-9 | Major impact, feature unusable |
| 10 | Critical, system failure or data loss |

## 3. High Priority Items (RPN > 80)

### FM-01: Webhook Not Received

**Root Causes:**
- GitHub outage
- Network issues
- Function timeout

**Mitigations:**
1. Implement manual sync button
2. Monitor webhook delivery in GitHub
3. Alert on sync gaps > 1 hour
