---
type: haz_soe_usability
id: HAZ-US-001
title: User interface causes confusion during critical workflow
status: approved
author: rune@ords.io
reviewers:
  - product
approvers:
  - quality
use_error: User selects wrong action from similar-looking buttons
task_context: Signing off on release documents
leads_to:
  - HS-001
---

# Hazard: User Interface Causes Confusion During Critical Workflow

## Description

The electronic signature workflow contains buttons with similar visual appearance that may cause users to select incorrect actions, potentially leading to unsigned releases or incorrect approvals.

## Use Error Analysis

- **Task**: Signing off on release documentation
- **User Error**: Clicking "Save Draft" instead of "Sign & Approve"
- **Contributing Factors**: Similar button styling, proximity of actions

## Sequence of Events

1. User reviews release documentation
2. User intends to sign and approve the release
3. User clicks wrong button due to visual similarity
4. Document is saved as draft instead of signed
5. Release process is delayed or incorrect version ships

## Detection Methods

- Usability testing with representative users
- Click tracking analytics
- User feedback and support tickets
