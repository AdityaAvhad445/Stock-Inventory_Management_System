# Stock Inventory Management System — Manual QA Project

## 📌 Overview
The Stock Inventory Management System is a web-based application designed to manage stock levels, track purchases and sales, and generate reports to help prevent stockouts and overstock situations. It includes dashboards with graphical/chart-based reporting across stock locations ("centers"), purchase & sales tracking, and customer/vendor management.

## 👤 My Role
Manual Tester

## 🧩 Responsibilities
- **Requirement Analysis** — Understanding application requirements to ensure data representation (Purchases, Customers, Sales) meets expected outcomes
- **Test Case Design** — Writing detailed test cases to verify the accuracy of stakeholder data (Purchases, Customers) and the proper functioning of graphical representations/charts for stock centers
- **Test Execution** — Manually executing test cases to check the integrity and correctness of data, ensuring stakeholder results are correctly processed and displayed
- **Test Documentation** — Creating and maintaining test plans, test cases, and test execution reports for tracking progress and results
- **Defect Reporting** — Reporting and tracking defects using Jira & MS Word, with proper severity and priority classification

## 🧩 Application Modules Covered
- Dashboard (live snapshot, income & expenses, top-selling products, top customers, charts by center/location)
- Purchases (purchase orders, purchase returns, vendor/supplier data)
- Sales (POS sales, sales returns, invoices, quotations)
- Customers & Vendors (stakeholder records)
- Stock Management (adjustments, stock transfer between centers/locations, tracking, low-stock alerts)
- Reports (purchase reports, sales reports, stock/inventory reports, payment reports, exports as PDF/Excel)

## 🛠️ Tools Used
- Bug tracking & reporting: Jira
- Test documentation & defect reports: MS Word
- Test case management: Excel / Google Sheets
- Browser DevTools for UI/data checks

## 📂 Repository Contents
| File | Description |
|---|---|
| `RequirementAnalysis.md` | Key requirement understanding & data representation notes |
| `TestPlan.md` | Scope, approach, entry/exit criteria |
| `TestCases.md` | Smoke & sanity test cases (Purchases, Sales, Customers, Reports, Dashboard) |
| `BugReports.md` | Sample defect reports (Jira/MS Word style) |
| `TestSummaryReport.md` | Execution summary & quality assessment

## 🎯 Key Testing Focus Areas
- Accuracy of stakeholder data — Purchases and Customers
- Correct functioning of dashboard graphs/charts across stock centers
- Stock quantity accuracy after purchases, sales, transfers, and adjustments
- Report accuracy (sales, purchase, stock, payment reports) and export functionality
- Low-stock / overstock alerting logic

## 📈 Outcome
Documented and executed smoke and sanity test suites covering the core inventory lifecycle — purchases, sales, stock adjustments/transfers, and dashboard reporting — identifying data-accuracy and chart-rendering issues across stock centers.
