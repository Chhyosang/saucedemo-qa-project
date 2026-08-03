# Test Plan — SauceDemo E-Commerce Web Application

## 1. Document Control
| Field | Detail |
|---|---|
| Project Name | SauceDemo — Public QA Practice E-Commerce Application |
| Application URL | https://www.saucedemo.com |
| Document Version | 1.0 |
| Prepared By | [Your Name] |
| Role | QA Engineer (Manual Testing) |
| Date | [Insert Date] |

## 2. Introduction
SauceDemo is a publicly available demo e-commerce web application maintained specifically for QA and test-automation practice. It simulates a small storefront (login, product browsing, cart, checkout) and ships with multiple test user personas that intentionally exhibit different bugs. This project documents a full manual QA testing cycle performed against SauceDemo, including test planning, test case design, execution, defect logging, and reporting.

## 3. Objectives
- Verify core e-commerce functionality (login, browsing, cart, checkout) behaves correctly for a standard user.
- Use SauceDemo's built-in "problem" personas to systematically uncover and document real, reproducible defects.
- Produce a complete, portfolio-ready QA artifact set demonstrating manual testing skills.

## 4. Scope

### 4.1 In Scope
| Module | Key Features to Test |
|---|---|
| Login | Valid login, locked-out user, invalid credentials, empty fields |
| Product Listing (Inventory) | Product display, sorting (name/price asc-desc), cart icon badge |
| Product Detail | Product info accuracy, add/remove from cart |
| Shopping Cart | Add/remove items, cart contents accuracy, navigation |
| Checkout (Step 1 – Information) | Field validation (first name, last name, zip) |
| Checkout (Step 2 – Overview) | Order summary accuracy, price/tax/total calculation |
| Checkout (Step 3 – Complete) | Confirmation message, cart reset |
| Logout / Session | Logout flow, direct URL access after logout |
| Persona-based bug hunting | `problem_user`, `error_user`, `visual_user`, `performance_glitch_user` compared against `standard_user` baseline |

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
- **UI/Visual Testing** — layout, alignment, and image-consistency checks.
- **Cross-Browser Testing** — Chrome and Firefox, key flows only.
- **Regression Testing** — re-verify related cases after any noted defect.

## 6. Test Environment
| Item | Detail |
|---|---|
| Application URL | https://www.saucedemo.com |
| Test Accounts | standard_user, locked_out_user, problem_user, error_user, visual_user, performance_glitch_user (password: secret_sauce) |
| Browsers | Chrome, Firefox (latest versions) |
| Devices | Desktop; mobile-width browser resize for responsive check |
| Tools | Browser DevTools, Excel/Google Sheets, GitHub Issues |

## 7. Roles & Responsibilities
| Role | Responsibility |
|---|---|
| QA Tester (You) | Test planning, test case design, execution, bug logging, reporting |

## 8. Entry Criteria
- SauceDemo application is accessible at the URL above.
- All test personas' credentials are confirmed working.
- Test cases have been written and reviewed.

## 9. Exit Criteria
- All planned test cases have been executed at least once, across all relevant personas.
- All discrepancies between persona behavior and the `standard_user` baseline have been logged as bugs.
- Test summary report has been prepared.

## 10. Test Deliverables
1. Test Plan (this document)
2. Requirement Traceability Matrix (RTM)
3. Test Case Document (baseline + negative + persona-based bug hunting)
4. Bug Reports (with screenshots)
5. Test Summary Report
6. Execution evidence (screenshots comparing personas to baseline)

## 11. Risk & Mitigation
| Risk | Mitigation |
|---|---|
| SauceDemo's known bugs may change over time as it's updated | Document the date of testing; note application version/state if visible |
| Solo tester, limited time | Prioritize baseline (`standard_user`) and persona bug-hunting cases first |
| Some "bugs" may be intentional demo features, not real defects | Cross-check against `standard_user` baseline before logging; note uncertainty in the bug report if unsure |

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
| [Your Name] | QA Engineer | |
