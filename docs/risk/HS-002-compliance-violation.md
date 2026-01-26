---
type: hazardous_situation
id: HS-002
title: Organization operates with non-compliant documentation
status: approved
probability: 4
results_in:
  - HARM-002
---

# Hazardous Situation: Organization Operates with Non-Compliant Documentation

## Description

Due to synchronization failures or gaps in the audit trail, the organization's quality management system contains outdated or incomplete documentation, putting FDA compliance at risk.

## Probability Assessment

**Rating: 4 (Likely)**

- Sync failures can occur with any network disruption
- Audit gaps may accumulate over time unnoticed
- Compliance issues often discovered only during audits
- Multiple dependent systems increase failure points

## Exposure Frequency

- Document changes occur daily
- Audit requirements are continuous
- Regulatory inspections occur periodically

## Contributing Factors

- Reliance on automated synchronization
- Distributed team making concurrent changes
- Complex integration between GitHub and QMS
