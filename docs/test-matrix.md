# Test Matrix

| Test ID | Scenario | Test File | Expected Result |
|---|---|---|---|
| T01 | Valid low-risk lead | `valid-low-risk-lead.json` | HTTP `202`; lead is processed; final result is saved to the Demo CRM |
| T02 | Valid high-risk lead | `valid-high-risk-lead.json` | HTTP `202`; lead status becomes `awaiting_human_approval`; reviewer form is required |
| T03 | Invalid request | `invalid-missing-source.json` | HTTP `400`; no lead is stored |
| T04 | Duplicate delivery | Send the same valid request twice | One record per `leadKey`; existing record is updated instead of duplicated |
| T05 | Reviewer approval | Submit `Approved` in the reviewer form | Final status becomes `approved_for_simulated_follow_up` |
| T06 | Reviewer denial | Submit `Denied` in the reviewer form | Final status becomes `review_denied` |
| T07 | Error handling | Run a synthetic failure test | An error record is saved in `p1_error_log` |

## Test data policy

All test data in this repository is synthetic. No employer, customer, client, banking, production, or confidential data is used.
