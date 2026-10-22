# Test Analysis & Business Rules Discovery - Automation Exercise

## 1. Project Overview & Scope
- **Target Application:** [Automation Exercise](https://automationexercise.com)
- **Domain:** E-commerce / SaaS
- **Objective:** Perform end-to-end test analysis on core user journeys (Money Paths) to identify business rules, functional requirements, and potential risk areas before test design and automation execution.

---

## 2. Core User Journeys (Money Paths) Analysis

### A. User Authentication & Profile Management
- **Signup Flow:** 
  - Users must provide valid credentials (Name, Email).
  - System enforces mandatory field validation during contact info filling.
  - Successful registration leads to the `ACCOUNT CREATED!` confirmation state.
- **Login Flow:** 
  - Authentication via registered email and password.
  - *Identified UI/UX Observation:* The profile viewing elements require verification during test design to ensure proper DOM element state handling.

### B. Checkout Process (Registered Account)
- **Flow Sequence:** Add items to cart $\rightarrow$ Proceed to checkout $\rightarrow$ Enter payment/card info $\rightarrow$ Order placed successfully (`payment_done`).
- **Significance:** This is the primary revenue-generating path. Any failure here directly impacts business operations, making it the highest priority candidate for automated Smoke Testing.

### C. Checkout Process (Guest / Unregistered User)
- **Flow Sequence:** Add items to cart $\rightarrow$ Go to cart $\rightarrow$ Click "Proceed to Checkout".
- **Business Rule Discovery / Constraint:** 
  - The application **does not support Guest Checkout**. 
  - Attempting to checkout without an account triggers a modal/pop-up forcing the user to Login or Signup.
  - *Testing Impact:* Test automation scripts for the checkout flow must explicitly handle user session states (either pre-authenticating or registering an account via API/UI setup).

---

## 3. Risk Identification & Test Focus Areas
1. **State Dependency:** Checkout heavily depends on valid cart contents and user session authentication. Test data management must ensure valid states before execution.
2. **Form Validation:** Mandatory field restrictions across Signup and Payment forms require robust negative test coverage.
