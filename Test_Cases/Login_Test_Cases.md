# Login Test Cases

## Description
This document contains manual test cases for testing the Login functionality
of a demo web application.

---

### TC-01: Login with valid credentials
**Preconditions:**  
User is registered and on the login page

**Steps:**
1. Enter valid email
2. Enter valid password
3. Click Login button

**Expected Result:**  
User is successfully logged in and redirected to the dashboard

---

### TC-02: Login with invalid password
**Preconditions:**  
User is registered and on the login page

**Steps:**
1. Enter valid email
2. Enter invalid password
3. Click Login button

**Expected Result:**  
Error message is displayed indicating invalid credentials

---

### TC-03: Login with empty fields
**Preconditions:**  
User is on the login page

**Steps:**
1. Leave email field empty
2. Leave password field empty
3. Click Login button

**Expected Result:**  
Validation messages are displayed for required fields

---

### TC-04: Login with invalid email format
**Preconditions:**  
User is on the login page

**Steps:**
1. Enter invalid email format
2. Enter any password
3. Click Login button

**Expected Result:**  
Validation message is displayed for invalid email format
Add login test cases
