# Test plan and evidence log

Record the actual execution date, result and redacted screenshot for each scenario. Do not mark a test as passed until it is verified.

| ID | Workflow | Test | Expected outcome | Result |
|---|---|---|---|---|
| T01 | Application Intake | New `DEMO-001` application | One row added in Applications | Not tested in this package |
| T02 | Application Intake | Re-run `DEMO-001` | Existing row updated without duplication | Not tested in this package |
| T03 | Application Intake | Empty company | Validation branch runs; no row created | Not tested in this package |
| T04 | Gmail AI Intake | Fictional recruitment email | Log row, extracted fields and Pending Review_Queue entry | Not tested in this package |
| T05 | Gmail AI Intake | Non-recruitment message matching trigger | Logged; no Review_Queue entry | Not tested in this package |
| T06 | Gmail AI Intake | Duplicate processing of same message | Email_Log/Review_Queue do not duplicate `email_id` | Not tested in this package |
| T07 | Calendar Sync | Approved future deadline without event ID | All-day calendar event created, ID saved | Not tested in this package |
| T08 | Calendar Sync | Repeat execution | No second calendar event | Not tested in this package |
| T09 | Deadline Digest | Deadline tomorrow | One daily summary email sent | Not tested in this package |
| T10 | Deadline Digest | No deadlines within 3 days | No email sent | Not tested in this package |
| T11 | Runtime | Close browser, keep Docker running | Scheduled workflows still execute | Not tested in this package |
| T12 | Runtime | Stop Docker | No workflows execute until restarted | Not tested in this package |

## Debugging notes
- Inspect each workflow's **Executions** history for errors.
- Validate actual Google Sheets rows and Calendar event IDs after runs.
- Verify timezone (`Asia/Jakarta`) and dates near midnight.
- Avoid testing real internship correspondence or posting genuine emails in screenshots.
- For Gmail, trigger filters may intentionally skip messages. A missing execution may mean the filter did not match rather than a failed workflow.
