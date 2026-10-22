# Exploratory Testing & Product Immersion Notes

## 1. Context & Objective
- **Activity:** First-week product immersion and exploratory testing on [Automation Exercise] (https://automationexercise.com).
- **Goal:** Understand user journeys, uncover hidden business rules, document initial observations, and identify core "Money Paths" before writing test cases and automation scripts.

---

## 2. Session Notes & Observations

### A. Signup and login flow
- **Signup Journey (`\signup`):**
 - Successfully navigated user registration by entering Name and Email.
 - Form validation correctly enforces mandatory fields during the subsequent contact information setup.
 - Reached successful completion state (`ACCOUNT CREATED`).
- **Login Journey (`\login`):**
 - Authenticated successfully using registered credentials.
 - *Observation/UI Note:* Noticed that the profile viewing button is unresponsive on hover/click and requires further verification.

### B. Checkout flow (Registered User)
- **Journey Path:** Add items to cart, proceed to checkout, fill payment details, order placement.
- **Outcome:** successfully directed to the confirmation/payment done page (`payment_done`).
- **Significance:** Verified as the core revenue-generating **Money Path**. This serves as the primary candidate for critical path automated smoke testing.

### C. Checkout flow (Guest/Unregistered user)
- **Journey Path:** Add items to cart, Click "proceed to checkout".
- **Discovery/Business Rule:**
 - The system **does not allow guest checkout**.
 - Clicking checkout without a registered account triggers a pop-up window, prompting the user to log in or register.
 - *QA Impact* Automation scripts targeting checkout must either use a pre-created test user setup or handle dynamic registration via API/UI fixtures.

---

## 3. Key takeaways and next steps
- **Next phase:** Transition exploratory findings and test analysis into formal **Test cases** (Test Design phase).
- 