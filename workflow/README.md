# Redacted n8n Workflow Exports

This folder contains redacted exports of the completed n8n workflows used in this portfolio project.

## Workflow files

| File | Responsibility |
|---|---|
| `P1-lead-intake-api.redacted.json` | Receives webhook requests, validates required fields, stores the initial lead, returns HTTP `202`, and starts processing asynchronously. |
| `P1-lead-processor.redacted.json` | Runs structured AI classification and routes high-priority or low-confidence leads to human review. |
| `P1-store-lead.redacted.json` | Upserts lead state into the `p1_lead_ledger` Data Table using `leadKey`. |
| `P1-sync-demo-crm.redacted.json` | Upserts final synthetic lead outcomes to the Google Sheets Demo CRM. |
| `P1-error-handler.redacted.json` | Captures workflow failures and records error details in `p1_error_log`. |

## Redaction notes

All exports were reviewed before publication.

- No API keys, OAuth tokens, passwords, or credentials are included.
- No private webhook URLs, execution URLs, Google Sheet URLs, or internal n8n instance IDs are included.
- Child workflow, Data Table, Google Sheet, and credential references were replaced with import-time placeholders.
- Workflows are exported with `active: false`.
- Any user importing these files must connect their own credentials and select their own resources.

> All project data is synthetic or redacted. These files are independent portfolio examples, not production deployment files.
