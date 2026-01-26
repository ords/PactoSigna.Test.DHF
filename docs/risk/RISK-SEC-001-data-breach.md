---
type: security_risk
id: RISK-SEC-001
title: Patient data breach via unauthorized access
status: approved
analyzes: HAZ-SEC-001
hazardous_situation: HS-002
harm: HARM-002
inherent_severity: 5
inherent_probability: 3
inherent_exploitability: 3
mitigations:
  - control: SRS-001
    reduces: sequence_probability
residual_severity: 5
residual_probability: 1
residual_exploitability: 1
---

# Risk Analysis: Patient Data Breach via Unauthorized Access

## Risk Path

**Hazard**: HAZ-SEC-001 - Unauthorized access to patient data
**Situation**: HS-002 - Organization operates with non-compliant documentation
**Harm**: HARM-002 - Regulatory enforcement action (plus HIPAA violations)

## Inherent Risk Assessment

| Factor | Rating | Justification |
|--------|--------|---------------|
| Severity | 5 (Catastrophic) | HIPAA violation, patient privacy breach |
| Exploitability | 3 (Moderate) | Requires some technical skill |
| **Inherent Risk** | **Unacceptable** | Requires strong controls |

## Risk Controls

### Control 1: Authentication System (SRS-001)

- **Reduces**: Sequence probability (exploitability)
- **Mechanism**: Multi-factor authentication, session management
- **Verification**: Penetration testing, security audit

## Residual Risk Assessment

| Factor | Rating | Justification |
|--------|--------|---------------|
| Severity | 5 (Catastrophic) | Unchanged if breach occurs |
| Exploitability | 1 (Theoretical) | MFA makes attack very difficult |
| **Residual Risk** | **Acceptable** | Strong authentication controls |

## Security Testing Evidence

- Penetration test: No critical findings
- MFA bypass attempts: All failed
- Session security: Tokens expire appropriately
