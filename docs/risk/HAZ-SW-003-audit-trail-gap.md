---
type: haz_soe_software
id: HAZ-SW-003
title: Audit trail has temporal gaps
status: approved
failure_mode: Events not captured during high load
cause: Queue overflow under peak usage
detection_method: Log analysis, compliance audits
---

# Hazard: Audit Trail Has Temporal Gaps

## Description

During periods of high system load, the audit logging queue may overflow, resulting in lost audit entries. This creates gaps in the compliance trail required for Part 11.

## Sequence of Events

1. Multiple users perform simultaneous operations
2. Audit events queue faster than they can be processed
3. Queue buffer fills and oldest events are dropped
4. Audit trail has missing entries for the overflow period

## Detection Methods

- Queue depth monitoring
- Periodic audit log completeness checks
- Compliance audit reviews

## Note

This hazard intentionally has no `leads_to` links to demonstrate gap detection.
