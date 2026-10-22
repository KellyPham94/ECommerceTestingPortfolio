# Test Execution Report - Smoke & Functional Testing

- **Execution Date:** October 22, 2026
- **Environment:** Production / Staging ([Automation Exercise](https://automationexercise.com))
- **Executed By:** Kelly Pham
- **Overall Status:** **PASSED** (Ready for Automation Phase)

---

## Summary Metrics
- **Total Test Cases Executed:** 5
- **Passed:** 5
- **Failed:** 0
- **Blocked:** 0

---

## Detailed Execution Results

| Test Case ID | Test Case Title | Priority | Status | Execution Notes / Defects Found |
|:-------------| :--- | :--- | :--- | :--- |
| **TC_001**   | Successful User Registration | High | **PASS** | Account created successfully. Redirected to success page cleanly. |
| **TC_002**   | Successful User Login | High | **PASS** | Authenticated successfully; username displayed in top nav. |
| **TC_003**   | Unsuccessful Login (Invalid Credentials) | Medium | **PASS** | Error message *"Your email or password is incorrect!"* appeared as expected. |
| **TC_004**   | Successful Registered User Checkout | High | **PASS** | Order placed successfully (`ORDER PLACED!`). Invoice download works. |
| **TC_005**   | Guest Checkout Restriction | Medium | **PASS** | System correctly forced redirect/modal to login before checkout. |

—

