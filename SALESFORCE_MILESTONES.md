# Skill Wallet — Salesforce Milestone Progress

Salesforce org: `orgfarm-99ea52e025-dev-ed.develop.my.salesforce.com`

## Phase 2 — Completed

| Milestone | Status | Notes |
|-----------|--------|-------|
| 1. Salesforce Account | Done | Developer Edition org provisioned and logged in |
| 2. Objects Creation | Done | `Job_Opening__c`, `Candidate_Application__c` (Auto Number `CA - {0000}`) |
| 3. Tabs | Done | Custom tabs for Job Opening and Candidate Application |
| 4. Fields & Relationships | Done | Contact candidate fields, Job Opening salary/vacancy/status, Candidate Application lookups |
| 5. Validation Rules | Done | Salary and application validation rules configured |
| 6. Approval Process | Done | Candidate offer approval with profiles/roles prerequisites |
| 7. Email Templates | Done | Recruitment notification templates created |
| 8. Email Alerts | Done | Alerts linked to approval and notification flows |
| 9. Flows | Done | Four flows: High Priority Notification, Submit Offer for Approval, Pending Reminder, Candidate Application Screen Flow |
| 10. Agentforce AI | Partial | Agentforce & AI Trust enabled; Candidate Application Summary Prompt saved |

## Phase 3 — In Progress

| Milestone | Status | Notes |
|-----------|--------|-------|
| 11. Lightning App | In progress | App: AI-Powered Recruitment & Candidate Management System |
| 12. Page Layouts | Pending | |
| 13. Dynamic Forms | Pending | |
| 14. Users | Pending | Recruiter, Hiring Manager profiles |

## Flows Created (Org UI)

1. **High Priority Candidate Application Notification** — record-triggered alert for high-priority applications
2. **Submit Candidate Offer for Approval** — submits offer records into approval process
3. **Pending Application Reminder** — scheduled reminder for pending applications
4. **Candidate Application Screen Flow** — guided screen flow: Candidate Details → Offer Details → Create Record → Confirmation

## Prompt Templates (Org UI)

- **Candidate Application Summary Prompt** — Record Summary for `Candidate_Application__c`
- **Account Executive Summary Prompt** — Flex prompt for Account with opportunity/case flow resources (in progress)

## Deploy from This Repo

The metadata in `force-app/` can be deployed to any Salesforce org via Salesforce CLI:

```bash
sf org login web --alias aircmsOrg --set-default
sf project deploy start --source-dir force-app --target-org aircmsOrg
```

Org-specific UI configuration (page layouts, dynamic forms, prompt templates) must be completed manually in Setup or retrieved with `sf project retrieve start`.
