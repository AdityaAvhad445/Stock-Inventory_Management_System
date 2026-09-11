# Test Summary Report — Stock Inventory Management System

## 1. Summary
Manual testing was performed on the Stock Inventory Management System, covering purchases, sales, stock adjustments/transfers, customer data, and dashboard reporting across multiple stock centers. Testing included requirement validation, smoke, sanity, data-accuracy, and negative scenarios.

## 2. Test Execution Summary
| Metric | Count |
|---|---|
| Total Test Cases | 17 |
| Passed | 13 |
| Failed | 4 |
| Blocked | 0 |
| Not Executed | 0 |

*(Update with your actual execution results.)*

## 3. Defect Summary
| Severity | Count |
|---|---|
| Critical | 0 |
| High | 2 |
| Medium | 2 |
| Low | 0 |

## 4. Key Observations
- Core purchase → stock → sale flow works correctly under normal conditions
- Discrepancies found between dashboard charts and detailed reports for the same stock center
- Stock transfer between centers has a data-sync gap on the source location
- Dashboard widgets (Top Customers) don't always account for returns/net sales
- Low-stock alerting has a refresh-timing issue

## 5. Risk Assessment
Dashboard/report data mismatches (BUG-001) and the stock transfer sync issue (BUG-002) directly affect stakeholders' ability to trust reported stock levels — high risk for causing incorrect purchasing or overstock/stockout decisions if not fixed before release.

## 6. Recommendation
Recommend fixing both High severity defects (BUG-001, BUG-002) before sign-off, as they impact core data accuracy — the primary goal of the system. Medium severity issues can be tracked for a following release.

## 7. Sign-off
- QA Tester: [Your Name]
- Date: [Date]
