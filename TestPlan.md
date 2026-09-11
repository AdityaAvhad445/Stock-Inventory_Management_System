# Test Plan — Stock Inventory Management System

## 1. Objective
To verify that the Stock Inventory Management System accurately manages stock levels, tracks purchases and sales, and generates correct reports/charts to prevent stockouts and overstock situations.

## 2. Scope

### In Scope
- Purchase order creation, receiving, and purchase returns
- Sales (POS) transactions, sales returns, quotations, and invoices
- Customer and vendor data accuracy
- Stock adjustments and stock transfers between centers/locations
- Dashboard graphical representations (charts) per stock center
- Reports: sales, purchase, stock, payment reports, and PDF/Excel export
- Low-stock / overstock alerting

### Out of Scope
- Payment gateway backend processing
- Performance/load testing
- Third-party integrations (accounting/ERP sync)
- Security/penetration testing

## 3. Test Approach
- **Smoke Testing** — verify critical flows (purchase → stock update → sale → stock update → report) before deeper testing
- **Sanity Testing** — verify targeted functionality after fixes/changes
- **Functional Testing** — validate each module against requirements
- **Data Accuracy Testing** — cross-check stakeholder data (Purchases, Customers, Sales) against dashboard/report output
- **UI/Chart Testing** — verify graphical representations render correctly and match underlying data, across filters and centers
- **Negative Testing** — invalid quantities, missing mandatory fields, duplicate entries

## 4. Test Environment
- Browser(s): Chrome, Firefox (latest versions)
- Test data: Sample vendors, customers, products, purchase orders, and sales transactions across at least 2 stock centers
- Environment: Staging/Demo environment
- Access: Test user accounts with admin/standard roles

## 5. Entry Criteria
- Build/demo environment accessible
- Test cases reviewed and ready
- Test data (products, vendors, customers) prepared

## 6. Exit Criteria
- All planned test cases executed
- No open Critical/High severity defects
- All Medium/Low defects logged in Jira and triaged

## 7. Roles & Responsibilities
| Role | Responsibility |
|---|---|
| QA Tester | Requirement analysis, test case design, execution, defect logging |
| Developer | Fix defects, support root cause analysis |
| Product Owner / BA | Clarify requirements, prioritize defects |

## 8. Deliverables
- Requirement analysis notes
- Test case document
- Bug reports (Jira & MS Word)
- Test summary report
