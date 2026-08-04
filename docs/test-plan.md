# Test Plan — SauceDemo E-Commerce Web Application

## 1. Document Control
| Field | Detail |
|---|---|
| Project Name | SauceDemo — Public QA Practice E-Commerce Application |
| Application URL | https://www.saucedemo.com |
| Document Version | 1.0 |
| Prepared By | Chhyosang Lepcha |
| Role | QA Engineer (Manual Testing) |
| Date | 2026-07-11 |

## 2. Introduction
SauceDemo is a publicly available demo e-commerce web application maintained specifically for QA and test-automation practice. It simulates a small storefront (login, product browsing, cart, checkout) and ships with multiple test user personas that intentionally exhibit different bugs. This project documents a full manual QA testing cycle performed against SauceDemo, including test planning, test case design, execution, defect logging and reporting.

## 3. Objectives
- Verify core e-commerce functionality (login, browsing, cart, checkout) behaves correctly for a standard user.
- Use SauceDemo's built-in "problem" personas to systematically uncover and document real, reproducible defects.
- Produce a complete, portfolio-ready QA artifact set demonstrating manual testing skills.

## 4. Scope

### 4.1 In Scope

### 4.1 In Scope

| Module | Key Features to Test |
|---|---|
| Login | Verify successful login, invalid login, locked-out user, empty required fields, and session handling. |
| Product Listing (Inventory) | Verify product display, product information, sorting options, cart badge updates, and navigation to product details. |
| Product Detail | Verify product information, product images, and Add to Cart/Remove functionality. |
| Shopping Cart | Verify adding/removing products, cart contents, quantity, and Continue Shopping/Checkout navigation. |
| Checkout (Step 1 – Information) | Verify required field validation, valid customer information, Cancel button, and form validation. |
| Checkout (Step 2 – Overview) | Verify order summary, payment information, shipping information, item prices, tax calculation, and total amount. |
| Checkout (Step 3 – Complete) | Verify successful order completion, confirmation message, Back Home navigation, and cart reset. |
| Logout / Session | Verify logout functionality, session termination, and prevention of unauthorized access after logout. |
| Cross-Browser Compatibility | Verify core functionality in supported browsers (Chrome and Firefox). |
| Responsive UI | Verify that pages remain usable on different screen sizes and mobile viewports. |
| Browser Navigation | Verify browser Back/Forward behavior during shopping and checkout. |
| Persona-Based Bug Hunting | Compare `problem_user`, `error_user`, `visual_user`, and `performance_glitch_user` with the `standard_user` baseline to identify persona-specific defects. |
| Regression Testing | Re-execute affected test cases after defect fixes to verify corrections and ensure no regression. |

### 4.2 Out of Scope
- Test automation / scripting
- Performance/load testing (beyond a basic observational check of `performance_glitch_user`)
- Security/penetration testing
- Payment gateway testing (SauceDemo checkout does not process real payments)
- Backend/API/database testing (no public API is exposed)

## 5. Test Approach / Strategy
- **Functional Testing** — verify each feature against expected behavior using `standard_user`.
- **Negative Testing** — invalid credentials, empty required fields, locked-out account.
- **Exploratory / Persona-Based Bug Hunting** — compare `problem_user`, `error_user`, `visual_user`, and `performance_glitch_user` against the `standard_user` baseline to uncover planted defects.
- **UI/Visual Testing** — layout, alignment and image-consistency checks.
- **Cross-Browser Testing** — Chrome and Firefox, key flows only.
- **Regression Testing** — re-verify related cases after any noted defect.

## 6. Test Environment
| Item | Detail |
|---|---|
| Application URL | https://www.saucedemo.com |
| Test Accounts | standard_user, locked_out_user, problem_user, error_user, visual_user, performance_glitch_user (password: secret_sauce) |
| Browsers | Chrome, Firefox |
| Devices | Desktop; mobile-width browser resize for responsive check |
| Tools | Browser DevTools, Excel/Google Sheets, GitHub Issues |

## 7. Roles & Responsibilities
| Role | Responsibility |
|---|---|
| QA Tester| Test planning, test case design, execution, bug logging, reporting |

## 8. Entry Criteria
- SauceDemo application is accessible at the URL above.
- All test personas' credentials are confirmed working.
- Test cases have been written and reviewed.

## 9. Exit Criteria
- All planned test cases have been executed at least once, across all relevant personas.
- All discrepancies between persona behavior and the `standard_user` baseline have been logged as bugs.
- Test summary report has been prepared.

## 10. Test Deliverables

1. **Test Plan** – Defines the testing scope, objectives, strategy, schedule, and deliverables.
2. **Requirement Traceability Matrix (RTM)** – Maps project requirements to corresponding test cases.
3. **Manual Test Case Document** – Contains 50 test cases covering positive, negative, boundary, exploratory, cross-browser, responsive UI, and regression testing.
4. **Bug Report Log** – Documents verified defects with reproduction steps, expected and actual results, severity, priority, environment, and status.
5. **Test Execution Summary Report** – Summarizes test execution results, pass/fail statistics, defect summary, key observations, and recommendations.
6. **Execution Evidence (Screenshots)** – Screenshots demonstrating successful test execution, validation messages, checkout flow, and documented defects.

## 11. Risk & Mitigation

| Risk | Mitigation |
|---|---|
| SauceDemo's intentionally buggy personas (`problem_user`, `error_user`, `visual_user`, `performance_glitch_user`) may change over time. | Record the testing date and compare results with the `standard_user` baseline before reporting defects. |
| Browser-specific behavior may affect test results. | Execute critical test cases in multiple browsers (Chrome and Firefox) and compare the results. |
| Limited testing time and a single tester may reduce overall test coverage. | Prioritize high-risk modules such as Login, Shopping Cart, Checkout, and Persona-Based Bug Hunting. |
| Some observed behaviors may be intentional demonstration features rather than genuine application defects. | Verify each issue against the `standard_user` account and document findings with screenshots before logging a defect. |
| Future application updates may impact existing test cases and defect reports. | Review and update test cases, RTM, and bug reports whenever the application changes. |

## 12. Schedule (Sample)
| Phase | Duration |
|---|---|
| Test Planning & RTM | 1 day |
| Test Case Design | 2 days |
| Baseline Execution (standard_user) | 1 day |
| Negative & Persona-Based Bug Hunting | 2 days |
| Cross-Browser / Responsive Check | 1 day |
| Bug Logging & Summary Report | 1 day |

## 13. Approval
| Name | Role | Signature/Date |
|---|---|---|
| Chhyosang Lepcha | QA Engineer |2026-07-11 |
