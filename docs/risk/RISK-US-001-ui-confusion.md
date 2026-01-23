---
type: usability_risk
id: RISK-US-001
title: User selects wrong action due to UI confusion
status: approved
analyzes: HAZ-US-001
hazardous_situation: HS-001
harm: HARM-001
inherent_severity: 3
inherent_probability: 4
mitigations:
  - control: SRS-001
    reduces: harm_probability
residual_severity: 3
residual_probability: 2
created: 2025-01-11
updated: 2025-01-15
author: Quality Team
reviewer: Sarah Johnson
approver: Lisa Williams
---

# Risk Analysis: User Selects Wrong Action Due to UI Confusion

## Risk Path

**Hazard**: HAZ-US-001 - User interface causes confusion during critical workflow
**Situation**: HS-001 - Healthcare provider administers incorrect treatment
**Harm**: HARM-001 - Patient injury from incorrect treatment

## Inherent Risk Assessment

| Factor | Rating | Justification |
|--------|--------|---------------|
| Severity | 3 (Moderate) | Delayed or incorrect approval |
| Probability | 4 (Likely) | Similar buttons, high-stress environment |
| **Inherent Risk** | **Review Required** | Assess acceptability |

## Risk Controls

### Control 1: Authentication System (SRS-001)

- **Reduces**: Harm probability
- **Mechanism**: Confirmation dialogs, role-based access
- **Verification**: Usability testing, user acceptance testing

## Residual Risk Assessment

| Factor | Rating | Justification |
|--------|--------|---------------|
| Severity | 3 (Moderate) | Unchanged |
| Probability | 2 (Unlikely) | Confirmation reduces errors |
| **Residual Risk** | **Acceptable** | Within tolerance |

## Usability Validation

- Task completion rate: 95% on first attempt
- Error rate: < 5% selecting wrong action
- User satisfaction: 4.2/5.0 on signature workflow
