# Bug Reports — Stock Inventory Management System
*(Format used for both Jira tickets and MS Word defect reports)*

## BUG-001
- **Title:** Dashboard chart values do not match Stock Report for the same center
- **Module:** Dashboard / Reports
- **Severity:** High
- **Priority:** High
- **Steps to Reproduce:**
  1. Select "Center B" from the dashboard filter
  2. Note the stock value shown in the dashboard chart
  3. Navigate to Reports > Stock Report, filter by "Center B"
  4. Compare the two values
- **Expected Result:** Dashboard chart value should match the detailed Stock Report value for the same center
- **Actual Result:** Dashboard chart shows a lower stock value than the Stock Report
- **Environment:** Demo / Chrome
- **Attachment:** [screenshot placeholder]

---

## BUG-002
- **Title:** Stock not deducted from source center after inter-center transfer
- **Module:** Stock Transfer
- **Severity:** High
- **Priority:** High
- **Steps to Reproduce:**
  1. Transfer 10 units of Product X from Center A to Center B
  2. Check stock at Center A
- **Expected Result:** Center A stock should decrease by 10 units
- **Actual Result:** Center A stock remains unchanged while Center B correctly shows +10 units
- **Environment:** Demo / Firefox
- **Attachment:** [screenshot placeholder]

---

## BUG-003
- **Title:** Top 5 Customers widget includes a customer with zero completed sales
- **Module:** Dashboard — Customers
- **Severity:** Medium
- **Priority:** Medium
- **Steps to Reproduce:**
  1. Create a sale for a customer, then fully return it (sales return)
  2. Check the "Top 5 Customers" widget on the dashboard
- **Expected Result:** Customer with a fully returned (net-zero) sale should not appear in Top 5 Customers
- **Actual Result:** Customer still appears in the widget
- **Environment:** Demo / Chrome
- **Attachment:** [screenshot placeholder]

---

## BUG-004
- **Title:** Low-stock alert not triggered after manual stock adjustment
- **Module:** Stock Adjustment / Alerts
- **Severity:** Medium
- **Priority:** Low
- **Steps to Reproduce:**
  1. Manually adjust a product's stock to below its defined low-stock threshold
  2. Check Reports > Low Stock Report
- **Expected Result:** Product should appear in the Low Stock Report immediately
- **Actual Result:** Product appears only after a page refresh/re-login
- **Environment:** Demo / Chrome
- **Attachment:** [screenshot placeholder]

## Notes
These are illustrative sample defects for interview/portfolio purposes, written in Jira-ticket style so they can also be pasted into an MS Word defect log. Replace with real findings once you execute test cases on the live demo.
