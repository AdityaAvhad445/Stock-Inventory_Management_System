# Test Cases — Stock Inventory Management System

## Smoke Test Cases

| TC ID | Module | Description | Steps | Expected Result | Priority |
|---|---|---|---|---|---|
| TC_SM_01 | Purchases | Verify user can create a purchase order | 1. Login 2. Go to Purchases > Create Purchase Order 3. Select vendor, add products & quantities 4. Save | Purchase order is created with status 'Ordered' | High |
| TC_SM_02 | Purchases | Verify stock increases on receiving a purchase order | 1. Open an 'Ordered' purchase order 2. Mark as Received 3. Check product stock | Stock quantity increases by the received amount | High |
| TC_SM_03 | Sales | Verify user can create a POS sale | 1. Go to Sales/POS 2. Select customer & products 3. Apply payment 4. Complete sale | Sale is recorded and invoice is generated | High |
| TC_SM_04 | Sales | Verify stock decreases after a completed sale | 1. Note stock before sale 2. Complete a sale for a product 3. Check stock after | Stock quantity decreases by sold quantity | High |
| TC_SM_05 | Customers | Verify user can add a new customer | 1. Go to Customers > Add Customer 2. Enter details 3. Save | Customer is created and appears in customer list | High |
| TC_SM_06 | Dashboard | Verify dashboard loads with correct summary data | 1. Login 2. Navigate to Dashboard | Dashboard displays income/expenses, top products, and charts without errors | High |
| TC_SM_07 | Reports | Verify stock report reflects current inventory | 1. Go to Reports > Stock Report 2. Select a center | Report shows current stock quantities matching product records | High |

## Sanity Test Cases

| TC ID | Module | Description | Steps | Expected Result | Priority |
|---|---|---|---|---|---|
| TC_SN_01 | Purchases | Verify purchase return decreases stock correctly | 1. Create a purchase return for a received item 2. Check stock | Stock decreases by the returned quantity | High |
| TC_SN_02 | Sales | Verify sales return increases stock correctly | 1. Process a sales return for a completed sale 2. Check stock | Stock increases by the returned quantity | High |
| TC_SN_03 | Customers | Verify top 5 customers widget reflects correct sales data | 1. Complete sales for multiple customers with varying totals 2. Check 'Top 5 Customers' on dashboard | Customers are ranked correctly by sales value | Medium |
| TC_SN_04 | Dashboard/Charts | Verify chart data matches underlying report for a given center | 1. Select a specific center on the dashboard 2. Compare chart values with the detailed report for that center | Chart values match report values (no discrepancy) | High |
| TC_SN_05 | Dashboard/Charts | Verify date range filter updates dashboard charts correctly | 1. Apply a custom date range filter on dashboard 2. Observe chart update | Charts refresh and reflect data only within the selected range | Medium |
| TC_SN_06 | Stock Transfer | Verify stock transfer between centers updates both locations | 1. Transfer stock of a product from Center A to Center B 2. Check stock at both centers | Center A stock decreases, Center B stock increases by transferred quantity | High |
| TC_SN_07 | Stock Adjustment | Verify manual stock adjustment updates quantity correctly | 1. Go to Stock Adjustment 2. Adjust quantity for a product with a reason 3. Save | Product stock reflects the adjusted quantity | Medium |
| TC_SN_08 | Reports | Verify report export (PDF/Excel) contains correct data | 1. Generate a sales or stock report 2. Export as PDF and Excel | Exported file data matches on-screen report data | Medium |
| TC_SN_09 | Validation | Verify system prevents sale when stock is insufficient | 1. Attempt to sell more quantity than available stock | System blocks the sale or shows a warning | High |
| TC_SN_10 | Low Stock Alert | Verify low-stock alert triggers correctly | 1. Reduce product stock below the defined threshold | System displays a low-stock warning/report entry for that product | Medium |

## Notes
- Add `Actual Result` and `Status (Pass/Fail)` columns during execution.
- Adjust module/field names above to match the exact application UI/terminology once you've explored the live demo.
