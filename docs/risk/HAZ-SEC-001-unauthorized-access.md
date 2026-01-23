---
type: haz_soe_security
id: HAZ-SEC-001
title: Unauthorized access to patient data
status: approved
threat_category: Spoofing
attack_vector: Session hijacking or credential theft
leads_to:
  - HS-002
created: 2025-01-13
updated: 2025-01-15
author: Security Team
reviewer: David Park
approver: Lisa Williams
---

# Hazard: Unauthorized Access to Patient Data

## STRIDE Analysis

**Threat Category**: Spoofing

An attacker could impersonate an authorized user through session hijacking, phishing attacks, or credential theft to gain unauthorized access to patient health information.

## Attack Vectors

1. **Session Hijacking**: Stealing session tokens through XSS or network interception
2. **Credential Theft**: Phishing attacks targeting user credentials
3. **Brute Force**: Attempting common passwords against user accounts

## Detection Methods

- Failed login attempt monitoring
- Anomalous session behavior detection
- Geographic/IP anomaly alerts
- Security audit logging

## Related Controls

- SRS-001: Authentication system with MFA
- Network security controls (out of scope for software)
