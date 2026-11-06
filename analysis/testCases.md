# Website Functional Test Cases

| Test ID | Feature | Test Scenario | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|
| TC-NEWS-001 | Newsletter | Submit invalid email format | Reject invalid email | Browser validation works | PASS |
| TC-NEWS-002 | Newsletter | Submit valid-format email | Process subscription successfully | HTTP 503 SMTP error | FAIL |
| TC-NEWS-003 | Newsletter | Submit previously registered email | Display duplicate-subscription feedback | Duplicate message appears after reload | PARTIAL |
| TC-CON-001 | Contact | Submit contact form | Display successful submission confirmation | HTTP 503 SMTP error | FAIL |

**Status Definitions**
- PASS: Expected behaviour observed.
- FAIL: Expected behaviour not observed.
- PARTIAL: Some expected behaviour works, but usability or functionality remains incomplete.
- NOT TESTED: Test has not yet been performed.
