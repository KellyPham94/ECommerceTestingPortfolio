# Test Cases: User Authentication (Signup & Login)

## 1. Module Overview
- **Feature:** User Authentication & Account Management
- **Target Application:** [Automation Exercise](https://automationexercise.com)
- **Objective:** Verify that users can successfully register a new account and log into the system with valid credentials, while properly handling invalid inputs.

---

## 2. Test Cases List

### TC_001: Successful User Registration (Signup)
- **Priority:** High (Smoke Test)
- **Pre-conditions:** 
  - User is on the Home Page (`https://automationexercise.com`).
  - User is not logged in.
- **Test Steps:**
  1. Click on the "Signup / Login" menu item in the top navigation bar.
  2. Enter valid Name and unique Email address in the "New User Signup!" section.
  3. Click the "Signup" button.
  4. Verify navigation to the account information page (`ENTER ACCOUNT INFORMATION`).
  5. Fill in all mandatory fields (Password, Date of Birth, First Name, Last Name, Address, Country, State, City, Zipcode, Mobile Number).
  6. Click the "Create Account" button.
- **Expected Result:** 
  - System successfully creates the account.
  - Displays the `ACCOUNT CREATED!` success message and a "Continue" button.
  - Top navigation shows "Logged in as [Username]".

---

### TC_002: Successful User Login (Valid Credentials)
- **Priority:** High (Smoke Test)
- **Pre-conditions:** 
  - An active user account already exists in the system.
  - User is on the Login page (`/login`).
- **Test Steps:**
  1. Enter a registered Email address in the "Login to your account" section.
  2. Enter the correct Password.
  3. Click the "Login" button.
- **Expected Result:** 
  - User is successfully authenticated.
  - Redirected to the home page or account dashboard.
  - Top navigation displays "Logged in as [Username]" and the "Delete Account" option becomes visible.

---

### TC_003: Unsuccessful Login (Invalid Credentials / Negative Test)
- **Priority:** Medium
- **Pre-conditions:** User is on the Login page (`/login`).
- **Test Steps:**
  1. Enter an unregistered or incorrect Email address.
  2. Enter an incorrect Password.
  3. Click the "Login" button.
- **Expected Result:** 
  - System denies access.
  - Displays an error message: *"Your email or password is incorrect!"*.
  - User remains on the login page.

