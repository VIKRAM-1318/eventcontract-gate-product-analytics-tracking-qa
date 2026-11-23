# Manual Acceptance Test Scenarios

These cases specify expected agent behaviour. They are not a claim that automated tests have been executed.

| Scenario | Input / condition | Expected behaviour |
|---|---|---|
| Missing implementation | Tracking plan supplied without implementation evidence. | Return INCOMPLETE_EVIDENCE; never PASS. |
| Required type drift | Spec requires account_id string; implementation declares number. | Report blocker with evidence locations and remediation test. |
| Dynamic event names | Events are generated dynamically. | Mark coverage unverified and request safe fixtures or manifest. |

## Global assertions
- Missing required evidence never produces a confident positive conclusion.
- Conflicts are preserved and escalated.
- Facts, assumptions, inferences and unknowns are distinguished.
- Sensitive data is minimised.
- No external side effect occurs without separate explicit authorisation and a supported integration.
