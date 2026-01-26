---
id: HLD-001
title: High-Level Design - System Context
status: approved
links:
  - SDD-001
---

# High-Level Design: System Context

## 1. System Context Diagram

```mermaid
C4Context
    title System Context Diagram for PactoSigna
    
    Person(user, "QMS User", "Regulatory or quality team member")
    Person(admin, "Admin", "Organization administrator")
    
    System(pactosigna, "PactoSigna", "QMS document viewing and traceability platform")
    
    System_Ext(github, "GitHub", "Source code and document repository")
    System_Ext(email, "Email Service", "Sends notifications")
    
    Rel(user, pactosigna, "Views documents, checks traceability")
    Rel(admin, pactosigna, "Manages organization, connects repos")
    Rel(pactosigna, github, "Syncs documents via API")
    Rel(github, pactosigna, "Sends webhooks on changes")
    Rel(pactosigna, email, "Sends invitations")
```

## 2. Key Actors

### QMS User
- Views synced documents
- Navigates traceability matrix
- Exports reports

### Administrator
- Creates organization
- Invites team members
- Connects GitHub repositories
- Manages settings

## 3. External Integrations

### GitHub
- OAuth App for user authentication (org connection)
- GitHub App for repository access
- Webhooks for real-time sync

### Email
- Firebase Auth email templates
- Custom invitation emails
