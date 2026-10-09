# Security and Privacy

## Data policy

- All names, emails, phone numbers, messages, and business scenarios in this project are synthetic or redacted.
- No employer, client, customer, banking, production, or confidential data is used.
- This project is an independent portfolio demonstration.

## Credentials and secrets

- Credentials are stored only in n8n credential storage.
- No API keys, OAuth tokens, passwords, private webhook URLs, private execution URLs, or credential exports are committed to GitHub.
- Google Sheets integration uses a personal test account only.

## AI safety

- AI receives synthetic lead content only.
- Lead messages are treated as untrusted input.
- AI output is constrained to structured fields: intent, priority, aiConfidence, and aiReason.
- AI cannot send customer messages or take irreversible actions.
- High-priority or low-confidence leads require human approval.

## Workflow safety

- Incoming requests are validated before storage or processing.
- Duplicate requests are handled using a stable leadKey.
- Final outcomes are stored in the lead ledger and synced to a synthetic Demo CRM.
- Workflow errors are recorded in p1_error_log for review.

## Project limitations

This project is not a production deployment, security audit, compliance certification, or representation of any employer system.
