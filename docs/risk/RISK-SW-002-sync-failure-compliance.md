---
type: software_risk
id: RISK-SW-002
title: Compliance gap due to sync failure
status: approved
analyzes: HAZ-SW-002
hazardous_situation: HS-002
harm: HARM-002
inherent_severity: 3
inherent_probability: 3
mitigations:
  - control: SRS-002
    reduces: sequence_probability
residual_severity: 3
residual_probability: 2
---

# Risk Analysis: Compliance Gap Due to Sync Failure

## Risk Path

**Hazard**: HAZ-SW-002 - Document sync fails silently
**Situation**: HS-002 - Organization operates with non-compliant documentation
**Harm**: HARM-002 - Regulatory enforcement action

## Inherent Risk Assessment

| Factor | Rating | Justification |
|--------|--------|---------------|
| Severity | 3 (Moderate) | Business impact, no direct patient harm |
| Probability | 3 (Possible) | Network issues occur regularly |
| **Inherent Risk** | **Review Required** | Assess acceptability |

## Risk Controls

### Control 1: Document Synchronization Requirements (SRS-002)

- **Reduces**: Sequence probability
- **Mechanism**: Retry logic, monitoring, manual sync capability
- **Verification**: Failure injection testing, recovery validation

## Residual Risk Assessment

| Factor | Rating | Justification |
|--------|--------|---------------|
| Severity | 3 (Moderate) | Unchanged |
| Probability | 2 (Unlikely) | Monitoring catches most failures |
| **Residual Risk** | **Acceptable** | Within tolerance |

## Verification Evidence

- Sync monitoring dashboard active
- Manual sync tested monthly
- Recovery procedure documented and tested
