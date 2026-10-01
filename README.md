# n8n-secure-lead-intake
A documented n8n lead-intake workflow with validation, AI-ready routing, human approval, and resilient error handling.
# Secure Lead Intake — n8n Automation Portfolio Project

> A safe n8n workflow that receives a synthetic business lead, validates its data, and returns a clear API response.

## Status

**Phase 1 status:** In progress

## Business problem

Businesses receive leads from websites, forms, ads, and messaging channels. If incoming data is incomplete or duplicated, sales teams can waste time or miss important opportunities.

This workflow demonstrates a safe, testable lead-intake foundation before any AI or external message is added.

## Current workflow scope

```text
POST Webhook
    ↓
Normalize Lead
    ↓
Required Fields Present?
    ├── Valid   → Return 200 accepted response
    └── Invalid → Return 400 rejected response
