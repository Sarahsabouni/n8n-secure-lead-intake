# Operator Runbook

## 1. A request is rejected

If the API returns HTTP `400`:

- Confirm the request includes `fullName`, `email`, and `source`.
- Confirm the request uses the `POST` method.
- Review the `Required Fields Present?` node.

## 2. A lead is waiting for approval

If a lead status is `awaiting_human_approval`:

- Open the related execution in n8n.
- Open the private reviewer form URL.
- Select `Approved` or `Denied`.
- Add an optional reviewer note.
- Confirm the final status is saved in the lead ledger.

## 3. A lead does not appear in the Demo CRM

- Find the lead using its `leadKey` in `p1_lead_ledger`.
- Review the related n8n execution.
- Check the `P1 — Sync Demo CRM` workflow.
- Confirm the Google Sheets credential is connected.
- Review retry attempts and error records before testing again.

## 4. A workflow fails

- Open the `p1_error_log` Data Table.
- Review the workflow name, failed node, error message, and timestamp.
- Fix the configuration or test-data issue.
- Re-run the workflow with synthetic data only.

## 5. Duplicate lead delivery

- Search the lead using its `leadKey`.
- Confirm one record exists for the same email and source.
- Confirm the existing record was updated instead of creating a duplicate.

## Safety reminder

- Do not use real customer, employer, banking, or confidential data.
- Do not publish private webhook URLs, execution URLs, API keys, credentials, or tokens.
- This project creates simulated follow-up outcomes only. It does not send real customer messages.
