# Test Plan

## 1. Introduction
This test plan describes the manual testing approach, scope, objectives, and deliverables for testing
the nopCommerce Demo Store (web application).

## 2. Application Under Test (AUT)
- Product: nopCommerce Demo Store
- Base URL: https://demo.nopcommerce.com/
- Key pages in scope:
  - Register: https://demo.nopcommerce.com/register
  - Login: https://demo.nopcommerce.com/login

## 3. Objective
The main objectives of testing are:
- Verify that core user account flows (registration and login) work as expected
- Validate form behavior, validation rules, and error messages
- Identify defects impacting usability and user experience

## 4. Scope of Testing

### In Scope
- User Registration (Create Account)
  - Required fields validation
  - Password & confirm password validation
  - Duplicate email behavior
- User Login
  - Valid/invalid credentials
  - Validation messages (empty fields, invalid email format)
  - Session behavior (basic checks)
- Navigation
  - Accessing Register/Login from header
  - Navigating categories and main pages
- Error messages & UI feedback
  - Validation messages
  - User-facing errors for incorrect input

### Out of Scope
- Performance testing
- Security testing (beyond basic negative scenarios)
- Backend/admin functionality
- Payment processing validation (no real payments)

## 5. Test Approach
Manual black-box testing using:
- Functional testing (happy path + negative)
- Exploratory testing (focused sessions)
- Basic regression checks after updates to test documentation

Test design techniques:
- Equivalence partitioning
- Boundary value checks (where applicable)

## 6. Test Environment
- OS: Windows
- Browser: Google Chrome (primary)
- Optional cross-check: Firefox / Edge

## 7. Test Data
- New user accounts will be created using unique emails (example: name+date@test.com)
- Passwords will follow typical complexity expectations (if enforced by AUT)

## 8. Test Deliverables
- Test Plan
- Test Cases (Markdown files per module)
- Bug Reports (Markdown files per defect)
- Exploratory Testing Notes
- Test Summary Report

## 9. Entry Criteria
- AUT is accessible
- Test environment is ready
- Test data strategy is defined (unique emails)

## 10. Exit Criteria
- All planned test cases are executed
- Critical/High severity defects are documented
- Test Summary Report is completed

## 11. Risks and Mitigation
| Risk | Mitigation |
|------|------------|
| Demo site data/state changes over time | Keep test data unique and document assumptions |
| Some flows may be restricted/unstable in demo | Focus on core account flows and document limitations |

## 12. Roles and Responsibilities
- QA Engineer (me): test planning, test execution, bug reporting, reporting
- Developers (demo owners): not in scope; defects are documented for portfolio purposes

## 13. Test Schedule
Testing will be performed incrementally with daily updates to test artifacts in GitHub.
