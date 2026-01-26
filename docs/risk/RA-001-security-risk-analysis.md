---
id: RA-001
title: Security Risk Analysis
status: approved
links:
  - SDD-001
  - SRS-001
---

# Security Risk Analysis

## 1. Scope

Identify and assess security risks for PactoSigna platform.

## 2. Risk Assessment Matrix

| ID | Risk | Likelihood | Impact | Score | Mitigation |
|----|------|------------|--------|-------|------------|
| SEC-01 | Unauthorized data access | Medium | High | 12 | Firestore rules, auth checks |
| SEC-02 | GitHub token exposure | Low | Critical | 10 | Secret Manager, no client exposure |
| SEC-03 | XSS in markdown rendering | Medium | Medium | 9 | DOMPurify, CSP headers |
| SEC-04 | CSRF attacks | Low | Medium | 6 | SameSite cookies, CSRF tokens |
| SEC-05 | Webhook spoofing | Medium | High | 12 | HMAC signature validation |

## 3. Risk Details

### SEC-01: Unauthorized Data Access

**Description:** User accesses documents from another organization.

**Controls:**
- Firestore security rules require `organizationId` match
- All queries scoped to user's organization
- Unit tests verify rule enforcement

### SEC-02: GitHub Token Exposure

**Description:** GitHub App private key or tokens exposed.

**Controls:**
- Private key in Cloud Secret Manager
- Installation tokens never sent to client
- Tokens have minimal required scopes

### SEC-05: Webhook Spoofing

**Description:** Attacker sends fake webhook events.

**Controls:**
- HMAC-SHA256 signature validation
- Webhook secret in Secret Manager
- IP allowlisting (optional)
