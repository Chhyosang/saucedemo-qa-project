# SauceDemo — Manual QA Testing Project

Manual QA testing project performed on **SauceDemo** (https://www.saucedemo.com), a public e-commerce web application maintained specifically for QA and test-automation practice. This project documents a full manual testing lifecycle — test planning, requirement traceability, test case design, execution, defect logging, and reporting — built as a second portfolio piece to complement my [Doko QA project](https://github.com/Chhyosang/doko-qa-project).

## 🧾 Project Summary
- **Application under test:** SauceDemo (public QA practice e-commerce app)
- **Testing type:** Manual (Functional, Negative, Boundary, Exploratory/Persona-based, UI, Cross-Browser)
- **Modules covered:** Login, Product Listing, Product Detail, Shopping Cart, Checkout (3 steps), Logout/Session, Persona-based Bug Hunting, Cross-Browser, Responsive
- **Test cases designed:** 50
- **Unique angle:** SauceDemo ships with intentionally "broken" test personas (`problem_user`, `error_user`, `visual_user`, `performance_glitch_user`) that simulate real bugs — this project systematically compares each against a `standard_user` baseline to uncover and document genuine, reproducible defects.

## 🛠️ Tools Used
| Purpose | Tool |
|---|---|
| Test documentation | Excel / Google Sheets |
| Bug tracking | Excel log (adaptable to GitHub Issues / Jira) |
| Test execution evidence | Screenshots (before/after persona comparisons) |
| Version control | Git & GitHub |

## 📂 Repository Structure
```
saucedemo-qa-project/
├── README.md
├── docs/
│   ├── test-plan.md
│   └── requirement-traceability-matrix.xlsx
├── test-cases/
│   └── test-cases.xlsx
├── bug-reports/
│   └── bug-log.xlsx
├── test-summary-report/
│   └── summary-report.md
└── screenshots/
    └── (baseline & persona comparison evidence)
```

## 📄 Deliverables
- **[Test Plan](docs/test-plan.md)** — scope, approach, environment, entry/exit criteria
- **[Requirement Traceability Matrix](docs/requirement-traceability-matrix.xlsx)** — 25 requirements mapped to test cases
- **[Test Cases](test-cases/test-cases.xlsx)** — 50 manual test cases across 13 module categories
- **[Bug Log](bug-reports/bug-log.xlsx)** — real defects found via persona comparison, with severity/priority and repro steps
- **[Test Summary Report](test-summary-report/summary-report.md)** — execution metrics, defect summary, recommendations

## ✅ Testing Approach
- **Functional Testing** — validated core flows using the `standard_user` baseline: login, browse, sort, add to cart, checkout, logout
- **Negative Testing** — invalid credentials, locked-out account, blank required fields
- **Persona-Based Bug Hunting** — compared `problem_user`, `error_user`, `visual_user`, and `performance_glitch_user` against the baseline to find real, reproducible defects
- **Boundary Testing** — duplicate cart additions, special characters, empty cart states
- **Cross-Browser & Responsive Testing** — Chrome vs. Firefox, mobile-width layout checks

## 🐞 Key Defects Found
See [`bug-reports/bug-log.xlsx`](bug-reports/bug-log.xlsx) for the full list with screenshots and severity classification.

## 📈 Result Snapshot
*(Update once execution is complete)*
- 50 test cases executed across 13 module categories
- [X] Passed / [X] Failed / [X] Blocked
- [X] real defects identified via persona-based bug hunting

## 🙋 About Me
This project was created to practice and demonstrate manual QA testing skills for my resume and portfolio, using a publicly available, purpose-built QA practice application.

**Chhyosang Lepcha**
www.linkedin.com/in/chhyosang-lepcha-088182215 | chhyosanglepcha@gmail.com | [Portfolio]
