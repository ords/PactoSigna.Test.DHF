---
type: haz_soe_software
id: HAZ-SW-001
title: Software displays incorrect medication dose
status: approved
failure_mode: Calculation error in dose algorithm
cause: Rounding error in floating point arithmetic
detection_method: Unit tests, integration tests, clinical review
leads_to:
  - HS-001
created: 2025-01-10
updated: 2025-01-15
author: Quality Team
reviewer: Sarah Johnson
approver: Lisa Williams
---

# Hazard: Software Displays Incorrect Medication Dose

## Description

The dose calculation algorithm may produce incorrect results due to floating-point arithmetic precision issues, particularly when dealing with very small doses or complex unit conversions.

## Sequence of Events

1. User enters patient weight and prescribed dose rate
2. Software performs calculation using floating-point arithmetic
3. Rounding errors accumulate across multiple conversions
4. Displayed dose differs from intended value
5. Healthcare provider may administer incorrect dose

## Detection Methods

- Comprehensive unit test suite with boundary values
- Integration tests comparing against reference calculations
- Manual clinical review of calculated values
- Automated alerts for doses outside normal ranges

## Related Requirements

- SRS-001: Authentication ensures only authorized users can enter data
- SRS-002: Sync ensures dose tables are current
