# Registration Test Cases (nopCommerce Demo Store)

## AUT
- Register page: https://demo.nopcommerce.com/register

## Notes / Test Data
- Use a unique email for each “successful registration” test:
  - example: sunny.qa+20251219-01@test.com
- Company name is optional.
- Newsletter checkbox behavior may vary (checked by default).

---

### TC-REG-01: Successful registration with valid data
**Preconditions:** User is on Register page  
**Steps:**
1. Select Gender (any)
2. Enter First name (valid)
3. Enter Last name (valid)
4. Enter unique Email (valid format)
5. (Optional) Enter Company name
6. Enter Password (valid)
7. Enter Confirm password (same as Password)
8. Click **Register**
**Expected Result:** Registration succeeds and user sees a success confirmation message / is logged in.

---

### TC-REG-02: Register with all required fields empty
**Preconditions:** User is on Register page  
**Steps:**
1. Leave First name empty
2. Leave Last name empty
3. Leave Email empty
4. Leave Password empty
5. Leave Confirm password empty
6. Click **Register**
**Expected Result:** Validation messages appear for all required fields; registration does not proceed.

---

### TC-REG-03: Register with empty First name
**Preconditions:** User is on Register page  
**Steps:**
1. Leave First name empty
2. Fill Last name with valid value
3. Fill Email with valid unique email
4. Fill Password and Confirm password with valid matching values
5. Click **Register**
**Expected Result:** “First name is required” (or equivalent) is shown; registration does not proceed.

---

### TC-REG-04: Register with empty Last name
**Preconditions:** User is on Register page  
**Steps:**
1. Fill First name with valid value
2. Leave Last name empty
3. Fill Email with valid unique email
4. Fill Password and Confirm password with valid matching values
5. Click **Register**
**Expected Result:** “Last name is required” (or equivalent) is shown; registration does not proceed.

---

### TC-REG-05: Register with empty Email
**Preconditions:** User is on Register page  
**Steps:**
1. Fill First name and Last name with valid values
2. Leave Email empty
3. Fill Password and Confirm password with valid matching values
4. Click **Register**
**Expected Result:** Email required validation is shown; registration does not proceed.

---

### TC-REG-06: Register with invalid Email format
**Preconditions:** User is on Register page  
**Steps:**
1. Fill First name and Last name with valid values
2. Enter invalid email (e.g., sunny.qa-at-test.com)
3. Fill Password and Confirm password with valid matching values
4. Click **Register**
**Expected Result:** Email format validation is shown (e.g., “Wrong email” / equivalent); registration does not proceed.

---

### TC-REG-07: Register with mismatched passwords
**Preconditions:** User is on Register page  
**Steps:**
1. Fill First name, Last name with valid values
2. Fill Email with valid unique email
3. Enter Password = Value A
4. Enter Confirm password = Value B (different from A)
5. Click **Register**
**Expected Result:** Validation message about password mismatch is shown; registration does not proceed.

---

### TC-REG-08: Register with empty Password
**Preconditions:** User is on Register page  
**Steps:**
1. Fill First name, Last name with valid values
2. Fill Email with valid unique email
3. Leave Password empty
4. Fill Confirm password with any value (or leave empty)
5. Click **Register**
**Expected Result:** Password required validation is shown; registration does not proceed.

---

### TC-REG-09: Register with empty Confirm password
**Preconditions:** User is on Register page  
**Steps:**
1. Fill First name, Last name with valid values
2. Fill Email with valid unique email
3. Fill Password with a valid value
4. Leave Confirm password empty
5. Click **Register**
**Expected Result:** Confirm password required validation is shown; registration does not proceed.

---

### TC-REG-10: Register with already existing Email
**Preconditions:** An account already exists with the same email  
**Steps:**
1. Fill First name, Last name with valid values
2. Enter an email that is already registered
3. Fill Password and Confirm password with valid matching values
4. Click **Register**
**Expected Result:** Error message indicates the email already exists; registration does not proceed.

---

### TC-REG-11: Newsletter checkbox can be toggled
**Preconditions:** User is on Register page  
**Steps:**
1. Observe Newsletter checkbox default state
2. Toggle checkbox (check/uncheck)
3. Fill required fields with valid data (use unique email)
4. Click **Register**
**Expected Result:** Registration succeeds; newsletter preference is accepted (no UI errors / unexpected behavior).

---

### TC-REG-12: Gender selection works
**Preconditions:** User is on Register page  
**Steps:**
1. Select Gender = Male
2. Select Gender = Female
3. Leave page as-is (no submit)
**Expected Result:** Only one gender option can be selected at a time; UI behaves correctly.

---

## Optional (Nice-to-have) Checks
- Verify that user can access “Register” link from header navigation
- Verify validation messages are readable and positioned near the related field
