# Test Cases: Registered User Checkout Flow

## 1. Module Overview
- **Feature:** E-commerce Checkout & Payment Process (Registered User)
- **Target Application:** [Automation Exercise](https://automationexercise.com)
- **Objective:** Verify that a registered user can successfully add products to the cart, complete the checkout process, submit payment details, and place an order successfully.

---

## 2. Test Cases List

### TC_004: Successful Registered User Checkout and Order Placement
- **Priority:** High (Critical / Smoke Test)
- **Pre-conditions:** 
  - User has an active account and is logged into the system (`Logged in as [Username]`).
  - Catalog contains available products.
- **Test Steps:**
  1. Navigate to the Products page and add at least one product to the cart.
  2. Click on the "Cart" menu item in the top navigation bar to view cart contents.
  3. Verify that the added product is correctly displayed in the cart table.
  4. Click the "Proceed To Checkout" button.
  5. Review the Address Details and Order Review sections on the checkout page.
  6. Enter a description/comment in the comment text area (optional).
  7. Click the "Place Order" button.
  8. Enter valid Payment Details (Name on Card, Card Number, CVC, Expiration Month/Year) on the payment page.
  9. Click the "Pay and Confirm Order" button.
- **Expected Result:** 
  - System successfully processes the payment.
  - Displays the order success confirmation message (`ORDER PLACED!`) along with a success notification (`Your order has been placed successfully!`).
  - Options to "Download Invoice" and "Continue" are available.

---

### TC_005: Guest Checkout Restriction (Business Rule Validation)
- **Priority:** Medium (Negative Test / Boundary Rule)
- **Pre-conditions:** 
  - User is **not** logged in (Guest state).
  - At least one product has been added to the cart.
- **Test Steps:**
  1. Navigate to the Cart page.
  2. Click the "Proceed To Checkout" button.
  3. Observe the system's reaction regarding authentication.
- **Expected Result:** 
  - System restricts direct access to the checkout page.
  - A modal or pop-up appears prompting the user to "Register / Login" before proceeding to checkout, enforcing the application's mandatory authentication rule.

