---
type: software_risk
id: RISK-SW-004
title: Data integrity loss during concurrent edits
status: draft
analyzes: HAZ-SW-002
hazardous_situation: HS-002
harm: HARM-002
inherent_severity: 5
inherent_probability: 3
mitigations:
  - control: SRS-099
    reduces: sequence_probability
residual_severity: 5
residual_probability: 2
created: 2025-01-14
updated: 2025-01-15
author: Quality Team
reviewer: Pending
approver: Pending
---

# Risk Analysis: Data Integrity Loss During Concurrent Edits

## Risk Path

**Hazard**: HAZ-SW-002 - Document sync fails silently
**Situation**: HS-002 - Organization operates with non-compliant documentation
**Harm**: HARM-002 - Regulatory enforcement action (elevated due to data loss)

## Inherent Risk Assessment

| Factor | Rating | Justification |
|--------|--------|---------------|
| Severity | 5 (Catastrophic) | Permanent data loss, compliance failure |
| Probability | 3 (Possible) | Race conditions can occur |
| **Inherent Risk** | **Unacceptable** | Requires mitigation |

## Risk Controls

### Control 1: Concurrent Edit Protection (SRS-099)

- **Reduces**: Sequence probability
- **Mechanism**: Optimistic locking, conflict detection
- **Verification**: TBD - requirement not yet implemented

**NOTE**: This control references SRS-099 which does not exist yet. This demonstrates gap detection for broken mitigation links.

## Residual Risk Assessment

| Factor | Rating | Justification |
|--------|--------|---------------|
| Severity | 5 (Catastrophic) | Unchanged |
| Probability | 2 (Unlikely) | With controls in place |
| **Residual Risk** | **Review Required** | Needs risk-benefit analysis |

## Status

**DRAFT** - Control SRS-099 needs to be created before this risk can be approved.
