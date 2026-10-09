# Test Evidence

This folder contains redacted evidence from completed tests of the Secure Lead Intake and Human-Reviewed AI Qualification workflow.

## Evidence files

| File | What it proves |
|---|---|
| `01-valid-request-202.png` | A valid synthetic request receives HTTP `202 Accepted` and is queued for processing. |
| `02-invalid-request-400.png` | An incomplete request is rejected with HTTP `400 Bad Request` before it is stored or processed. |
| `03-main-workflow-canvas.png` | The Lead Intake API workflow includes validation, accepted and rejected paths, initial storage, HTTP response handling, and asynchronous processing. |
| `04-ai-structured-output.png` | AI classification returns structured fields: intent, priority, aiConfidence, and aiReason. |
| `05-human-approval-form.png` | High-priority or low-confidence leads pause for a human reviewer decision. |
| `06-final-demo-crm-row.png` | An approved synthetic lead is stored with its final status and synchronized to the Demo CRM. |
| `07-error-log-test.png` | A controlled production error is recorded by the Error Handler in `p1_error_log`. |

## Evidence policy

- All examples use synthetic or redacted data only.
- Browser URLs, webhook URLs, execution URLs, credentials, account information, and private identifiers are not shown.
- No employer, customer, banking, production, or confidential data is included.
- The error-handling evidence uses a temporary synthetic test workflow, which was deactivated after testing.
