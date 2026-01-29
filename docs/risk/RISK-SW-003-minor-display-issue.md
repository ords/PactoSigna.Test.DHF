---
type: software_risk
id: RISK-SW-003
title: Minor display formatting inconsistency
status: approved
author: rune@ords.io
reviewers:
  - product
approvers:
  - engineering
analyzes: HAZ-SW-002
hazardous_situation: HS-002
harm: HARM-002
inherent_severity: 2
inherent_probability: 2
residual_severity: 2
residual_probability: 2
---

# Risk Analysis: Minor Display Formatting Inconsistency

## Risk Path

**Hazard**: HAZ-SW-002 - Document sync fails silently
**Situation**: HS-002 - Organization operates with non-compliant documentation
**Harm**: HARM-002 - Regulatory enforcement action

## Inherent Risk Assessment

| Factor | Rating | Justification |
|--------|--------|---------------|
| Severity | 2 (Minor) | Cosmetic issue, no functional impact |
| Probability | 2 (Unlikely) | Occurs rarely with specific content |
| **Inherent Risk** | **Acceptable** | No mitigation required |

## Risk Evaluation

This risk represents minor formatting inconsistencies that may appear when markdown documents contain unusual character combinations. The impact is purely cosmetic and does not affect the accuracy or integrity of the underlying data.

## Decision

**Accept without additional controls** - The inherent risk is within acceptable limits. The effort to implement additional controls would be disproportionate to the minimal risk reduction achieved.

## Monitoring

- User feedback monitored for formatting complaints
- Periodic review of rendered documents
