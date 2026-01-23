---
type: software_risk
id: RISK-SW-001
title: Incorrect dose due to calculation error
status: approved
analyzes: HAZ-SW-001
hazardous_situation: HS-001
harm: HARM-001
inherent_severity: 4
inherent_probability: 4
mitigations:
  - control: SRS-001
    reduces: sequence_probability
  - control: SRS-002
    reduces: harm_probability
residual_severity: 4
residual_probability: 1
created: 2025-01-10
updated: 2025-01-15
author: Quality Team
reviewer: Sarah Johnson
approver: Lisa Williams
---

# Risk Analysis: Incorrect Dose Due to Calculation Error

## Risk Path

**Hazard**: HAZ-SW-001 - Software displays incorrect medication dose
**Situation**: HS-001 - Healthcare provider administers incorrect treatment
**Harm**: HARM-001 - Patient injury from incorrect treatment

## Inherent Risk Assessment

| Factor | Rating | Justification |
|--------|--------|---------------|
| Severity | 4 (Major) | Patient injury requiring treatment |
| Probability | 4 (Likely) | Floating point errors common without controls |
| **Inherent Risk** | **Unacceptable** | Requires mitigation |

## Risk Controls

### Control 1: Authentication & Authorization (SRS-001)

- **Reduces**: Sequence probability
- **Mechanism**: Ensures only trained, authorized users can enter dose data
- **Verification**: Access control testing, user role validation

### Control 2: Document Synchronization (SRS-002)

- **Reduces**: Harm probability
- **Mechanism**: Ensures dose reference tables are always current
- **Verification**: Sync verification tests, timestamp validation

## Residual Risk Assessment

| Factor | Rating | Justification |
|--------|--------|---------------|
| Severity | 4 (Major) | Unchanged - harm severity if it occurs |
| Probability | 1 (Rare) | Multiple controls reduce likelihood |
| **Residual Risk** | **Acceptable** | Within tolerance |

## Verification Evidence

- Unit test results: 100% pass rate on dose calculations
- Integration test results: All boundary cases validated
- Clinical validation: Independent verification by pharmacist
