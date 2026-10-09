# Secure Lead Intake and Human-Reviewed AI Qualification

An independent n8n portfolio project that demonstrates a safe lead-intake workflow using synthetic data only.

## Business problem

Businesses receive leads from websites and forms. Some requests may be incomplete, duplicated, urgent, or require a human decision before any follow-up.

## What this project demonstrates

- Webhook-based lead intake
- Required-field validation
- Duplicate-safe lead storage
- Structured AI lead classification
- Human approval for high-risk or low-confidence leads
- Google Sheets Mock CRM integration
- Error logging and safe workflow design
- Testing, documentation, and privacy controls

## Workflow overview

Webhook

  → Validate request
  → Store lead safely
  → Return 202 Accepted
  → AI classification
  → Human approval when required
  → Save final outcome
  → Sync final result to a Demo CRM

## Privacy and security
- All leads, names, emails, phone numbers, messages, and screenshots use synthetic or redacted data.
- No employer, client, customer, banking, or production data is used.
- No API keys, OAuth tokens, credentials, private webhook URLs, or private execution URLs are committed to this repository.
- This is an independent portfolio demonstration, not a production deployment or compliance certification.
