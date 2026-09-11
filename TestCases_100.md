# Test Cases (100) — Stock Inventory Management System

| TC ID | Module | Description | Steps | Expected Result | Priority |
|---|---|---|---|---|---|
| TC_001 | Login | Verify user can login with valid credentials | 1. Go to login page 2. Enter valid email/password 3. Click Sign In | User is logged in and redirected to Dashboard | High |
| TC_002 | Login | Verify login fails with invalid password | 1. Enter valid email, wrong password 2. Click Sign In | Error message shown, user not logged in | High |
| TC_003 | Login | Verify login fails with unregistered email | 1. Enter unregistered email 2. Click Sign In | Error message shown, login blocked | Medium |
| TC_004 | Login | Verify 'Remember Me' keeps user logged in | 1. Check 'Remember Me' 2. Login 3. Close and reopen browser | User session persists | Low |
| TC_005 | Login | Verify 'Forgot Password' sends reset link | 1. Click 'Forgot Password' 2. Enter registered email 3. Submit | Password reset email is sent | Medium |
| TC_006 | Login | Verify mandatory field validation on login form | 1. Leave email/password blank 2. Click Sign In | Validation error shown for empty fields | Medium |
| TC_007 | Login | Verify password field masks input | 1. Type password in password field | Characters are masked (dots/asterisks) | Low |
| TC_008 | Login | Verify logout functionality | 1. Login 2. Click Logout | User is logged out and redirected to login page | High |
| TC_009 | Dashboard | Verify dashboard loads all widgets without error | 1. Login 2. Navigate to Dashboard | All widgets (income, expenses, top products, top customers) load correctly | High |
| TC_010 | Dashboard | Verify live snapshot widget shows current data | 1. Open Dashboard 2. Check live snapshot section | Data reflects most recent transactions | High |
| TC_011 | Dashboard | Verify Income vs Expenses chart renders correctly | 1. Open Dashboard 2. View Income/Expenses chart | Chart displays accurate income and expense values | High |
| TC_012 | Dashboard | Verify Top Selling Products (Month) widget | 1. Open Dashboard 2. Check Top Selling Products - Month | Correct products listed based on monthly sales volume | Medium |
| TC_013 | Dashboard | Verify Top Selling Products (Year) widget | 1. Open Dashboard 2. Check Top Selling Products - Year | Correct products listed based on yearly sales volume | Medium |
| TC_014 | Dashboard | Verify Top 5 Customers widget accuracy | 1. Complete sales for multiple customers 2. Check Top 5 Customers | Customers ranked correctly by sales value | High |
| TC_015 | Dashboard | Verify data filter on dashboard updates widgets | 1. Apply a date range filter 2. Observe widgets | All widgets refresh to reflect filtered range only | High |
| TC_016 | Dashboard | Verify center/location filter updates dashboard | 1. Select a specific center from filter 2. Observe dashboard | Data shown is specific to the selected center only | High |
| TC_017 | Dashboard | Verify dashboard chart values match detailed reports | 1. Note chart value for a metric 2. Compare with corresponding report | Values match with no discrepancy | High |
| TC_018 | Dashboard | Verify dashboard works correctly in Dark Mode | 1. Switch to Dark Version 2. Navigate dashboard | UI renders correctly with no visual/data issues | Low |
| TC_019 | Dashboard | Verify dashboard is responsive on smaller screen sizes | 1. Resize browser/viewport 2. Check dashboard layout | Layout adjusts responsively without breaking | Low |
| TC_020 | Purchases | Verify user can create a new purchase order | 1. Go to Purchases > Create 2. Select vendor, add products/quantities 3. Save | Purchase order created with status 'Ordered' | High |
| TC_021 | Purchases | Verify mandatory fields are validated on purchase order form | 1. Leave vendor/product blank 2. Try to save | Validation error shown, order not saved | Medium |
| TC_022 | Purchases | Verify stock increases when purchase order is fully received | 1. Mark a purchase order as fully received 2. Check product stock | Stock increases by the full ordered quantity | High |
| TC_023 | Purchases | Verify stock increases correctly on partial receipt | 1. Mark only part of the order as received 2. Check stock | Stock increases only by the received quantity | High |
| TC_024 | Purchases | Verify purchase order status updates to 'Completed' after full receipt | 1. Receive all items on a PO 2. Check PO status | Status changes to 'Completed' | Medium |
| TC_025 | Purchases | Verify purchase order can be edited before receiving | 1. Open an 'Ordered' PO 2. Edit quantity 3. Save | Changes are saved successfully | Medium |
| TC_026 | Purchases | Verify purchase order cannot be edited after completion | 1. Open a 'Completed' PO 2. Attempt to edit | Edit is disabled or blocked with a message | Medium |
| TC_027 | Purchases | Verify purchase order can be cancelled | 1. Open an 'Ordered' PO 2. Click Cancel | PO status changes to 'Cancelled', no stock impact | Medium |
| TC_028 | Purchases | Verify purchase return decreases stock correctly | 1. Create a return for a received item 2. Check stock | Stock decreases by returned quantity | High |
| TC_029 | Purchases | Verify purchase return updates vendor payment records | 1. Process a purchase return 2. Check vendor ledger | Vendor balance adjusts to reflect the return | Medium |
| TC_030 | Purchases | Verify purchase order tax and total calculate correctly | 1. Add products with tax rates 2. Check total | Total = (unit cost × qty) + tax, calculated correctly | High |
| TC_031 | Purchases | Verify duplicate purchase order number is not allowed | 1. Attempt to create PO with an existing PO number (if manual) | System blocks duplicate or auto-generates unique number | Low |
| TC_032 | Purchases | Verify vendor selection dropdown loads all active vendors | 1. Open Create PO 2. Click vendor dropdown | All active vendors are listed | Low |
| TC_033 | Purchases | Verify purchase order list can be filtered by status | 1. Go to Purchases list 2. Filter by 'Ordered'/'Completed' | List updates to show only matching POs | Medium |
| TC_034 | Purchases | Verify purchase order can be exported as PDF | 1. Open a PO 2. Click Export/Print PDF | PDF generated with correct PO details | Low |
| TC_035 | Sales | Verify user can create a POS sale | 1. Go to Sales/POS 2. Select customer & products 3. Complete payment | Sale recorded, invoice generated | High |
| TC_036 | Sales | Verify stock decreases after a completed sale | 1. Note stock before sale 2. Complete sale 3. Check stock after | Stock decreases by sold quantity | High |
| TC_037 | Sales | Verify sale cannot be completed with insufficient stock | 1. Attempt to sell more than available stock | System blocks sale or shows warning | High |
| TC_038 | Sales | Verify discount is applied correctly on a sale | 1. Add a discount (%/flat) to a sale 2. Check total | Total reflects discount accurately | High |
| TC_039 | Sales | Verify tax is applied correctly on a sale | 1. Complete a sale with taxable products 2. Check invoice total | Tax calculated and added correctly | High |
| TC_040 | Sales | Verify multiple payment methods can be applied to one sale | 1. Split payment between cash & card 2. Complete sale | Sale completes with both payment amounts recorded | Medium |
| TC_041 | Sales | Verify sale can be generated from a quotation | 1. Open an existing quotation 2. Convert to sale | Sale created with quotation's product/quantity data carried over | Medium |
| TC_042 | Sales | Verify invoice is generated with correct design/details | 1. Complete a sale 2. Open/print invoice | Invoice shows correct items, totals, and business branding | Medium |
| TC_043 | Sales | Verify sales return increases stock correctly | 1. Process a return for a completed sale 2. Check stock | Stock increases by returned quantity | High |
| TC_044 | Sales | Verify sales return adjusts customer payment/refund records | 1. Process a sales return 2. Check customer ledger/payment | Refund or credit is recorded correctly | Medium |
| TC_045 | Sales | Verify barcode scanning adds correct product to sale | 1. Scan a product barcode in POS | Correct product is added to the cart with correct price | High |
| TC_046 | Sales | Verify quantity can be updated in POS cart before checkout | 1. Add product to cart 2. Change quantity | Cart total updates accordingly | Medium |
| TC_047 | Sales | Verify product can be removed from POS cart | 1. Add product to cart 2. Remove it | Product removed, total recalculated | Medium |
| TC_048 | Sales | Verify sale cannot be completed without selecting a payment method | 1. Attempt checkout without payment method | System blocks completion with a validation message | Medium |
| TC_049 | Sales | Verify walk-in/guest sale (without customer) is allowed | 1. Complete a sale without selecting a customer | Sale completes successfully as a guest/walk-in sale | Low |
| TC_050 | Sales | Verify sales list can be filtered by date range | 1. Go to Sales list 2. Apply date filter | Only sales within the range are shown | Medium |
| TC_051 | Sales | Verify quotation can be created and saved as draft | 1. Create a quotation 2. Save without converting to sale | Quotation saved with 'Pending' status | Low |
| TC_052 | Customers | Verify user can add a new customer | 1. Go to Customers > Add 2. Enter details 3. Save | Customer created and appears in list | High |
| TC_053 | Customers | Verify mandatory fields validated on customer form | 1. Leave required fields blank 2. Save | Validation error shown | Medium |
| TC_054 | Customers | Verify customer details can be edited | 1. Open existing customer 2. Edit info 3. Save | Updated details are saved and reflected | Medium |
| TC_055 | Customers | Verify customer purchase/sales history displays correctly | 1. Open a customer profile 2. Check history tab | All past sales linked to this customer are listed accurately | High |
| TC_056 | Customers | Verify customer can be deleted/deactivated | 1. Open customer 2. Click Delete/Deactivate | Customer is removed or marked inactive | Low |
| TC_057 | Customers | Verify duplicate customer entries are flagged | 1. Add a customer with an existing email/phone | System warns of duplicate or blocks creation | Low |
| TC_058 | Customers | Verify customer search functionality | 1. Go to Customers list 2. Search by name/phone | Matching customer(s) displayed | Medium |
| TC_059 | Customers | Verify Top 5 Customers excludes fully-returned (net-zero) sales | 1. Fully return a customer's only sale 2. Check Top 5 Customers | Customer does not appear in the widget | Medium |
| TC_060 | Vendors | Verify user can add a new vendor/supplier | 1. Go to Vendors > Add 2. Enter details 3. Save | Vendor is created and appears in list | High |
| TC_061 | Vendors | Verify vendor details can be edited | 1. Open a vendor 2. Edit info 3. Save | Updated details are saved | Medium |
| TC_062 | Vendors | Verify vendor purchase history is accurate | 1. Open a vendor profile 2. Check purchase history | All POs linked to this vendor are listed correctly | Medium |
| TC_063 | Vendors | Verify vendor balance/payment ledger updates correctly | 1. Make a payment against a PO 2. Check vendor ledger | Balance reflects the payment made | Medium |
| TC_064 | Vendors | Verify vendor can be filtered/searched in vendor list | 1. Search vendor by name | Correct vendor(s) shown | Low |
| TC_065 | Products | Verify user can add a new product | 1. Go to Products > Add 2. Enter name, SKU, price, tax, category 3. Save | Product created and appears in product list | High |
| TC_066 | Products | Verify mandatory fields validated on product form | 1. Leave required fields blank 2. Save | Validation error shown | Medium |
| TC_067 | Products | Verify product can be edited | 1. Open product 2. Edit price/details 3. Save | Updated product data is saved and reflected everywhere it's used | Medium |
| TC_068 | Products | Verify product barcode can be generated/printed | 1. Open product 2. Click Print Barcode | Barcode is generated correctly for the product | Low |
| TC_069 | Products | Verify product list can be exported as PDF | 1. Go to Products list 2. Click Export PDF | PDF generated with correct product data | Low |
| TC_070 | Products | Verify product list can be exported as Excel | 1. Go to Products list 2. Click Export Excel | Excel file generated with correct product data | Low |
| TC_071 | Products | Verify product category filter works correctly | 1. Select a category filter on Products list | Only products in that category are displayed | Medium |
| TC_072 | Products | Verify inactive/disabled product does not appear in POS | 1. Deactivate a product 2. Go to POS and search for it | Product does not appear as sellable in POS | Medium |
| TC_073 | Stock Management | Verify manual stock adjustment updates quantity correctly | 1. Go to Stock Adjustment 2. Adjust quantity with a reason 3. Save | Product stock reflects adjusted quantity | High |
| TC_074 | Stock Management | Verify stock adjustment requires a reason/note | 1. Attempt adjustment without entering a reason | System blocks save or shows validation error | Medium |
| TC_075 | Stock Management | Verify stock transfer between centers updates both locations | 1. Transfer stock of a product from Center A to Center B 2. Check stock at both | Center A decreases, Center B increases by transferred qty | High |
| TC_076 | Stock Management | Verify stock transfer cannot exceed available stock at source | 1. Attempt to transfer more than available stock | System blocks transfer or shows error | High |
| TC_077 | Stock Management | Verify stock transfer history/log is recorded | 1. Complete a transfer 2. Check transfer history/report | Transfer entry is logged with correct date, quantity, and centers | Medium |
| TC_078 | Stock Management | Verify low-stock alert triggers when stock falls below threshold | 1. Reduce stock below defined threshold | Product appears in Low Stock report/alert | High |
| TC_079 | Stock Management | Verify low-stock threshold can be configured per product | 1. Open product settings 2. Set custom low-stock threshold 3. Save | Threshold is saved and used for alerting | Medium |
| TC_080 | Stock Management | Verify stock tracking option can be enabled/disabled per product | 1. Open product 2. Toggle stock tracking 3. Save | Setting is saved; stock is/isn't tracked accordingly | Low |
| TC_081 | Reports | Verify Stock Report reflects current inventory accurately | 1. Go to Reports > Stock Report 2. Select a center | Report shows stock quantities matching actual product records | High |
| TC_082 | Reports | Verify Sales Report totals match individual sales records | 1. Generate Sales Report for a date range 2. Cross-check with Sales list | Totals match with no discrepancy | High |
| TC_083 | Reports | Verify Purchase Report totals match individual PO records | 1. Generate Purchase Report for a date range 2. Cross-check with Purchases list | Totals match with no discrepancy | High |
| TC_084 | Reports | Verify Payments Report reflects all recorded payments | 1. Generate Payments Report 2. Cross-check with transaction records | All payments (sales & purchases) are accurately listed | Medium |
| TC_085 | Reports | Verify report can be filtered by vendor | 1. Apply vendor filter on Purchase Report | Report shows only data for the selected vendor | Medium |
| TC_086 | Reports | Verify report can be filtered by product | 1. Apply product filter on a report | Report shows only data for the selected product | Medium |
| TC_087 | Reports | Verify report can be filtered by date range | 1. Apply a custom date range on any report | Report shows only data within that range | High |
| TC_088 | Reports | Verify report export as PDF contains correct data | 1. Generate a report 2. Export as PDF | PDF data matches on-screen report | Medium |
| TC_089 | Reports | Verify report export as Excel contains correct data | 1. Generate a report 2. Export as Excel | Excel data matches on-screen report | Medium |
| TC_090 | Reports | Verify empty report state displays correctly | 1. Apply filters that return no data | A clear 'No data found' message is shown, not an error | Low |
| TC_091 | Settings | Verify tax rates can be created and edited | 1. Go to Settings > Tax 2. Add/edit a tax rate 3. Save | Tax rate is saved and available for use in Sales/Purchases | Medium |
| TC_092 | Settings | Verify currency setting reflects across the application | 1. Change currency in Settings 2. Check Sales/Purchases/Reports | Currency symbol/format updates consistently | Low |
| TC_093 | Settings | Verify payment modes can be added/edited | 1. Go to Settings > Payment Modes 2. Add a new mode 3. Save | New payment mode is available for selection during checkout | Low |
| TC_094 | Settings | Verify company/business details update correctly on invoices | 1. Update company info in Settings 2. Generate a new invoice | Invoice reflects updated company details | Low |
| TC_095 | Roles & Permissions | Verify a restricted-role user cannot access unauthorized modules | 1. Login as a limited-permission user 2. Attempt to access a restricted module | Access is denied / module is hidden | High |
| TC_096 | Roles & Permissions | Verify admin can assign/edit roles for staff users | 1. Go to Users > Roles 2. Edit a user's role 3. Save | Role updates and permissions apply on next login | Medium |
| TC_097 | Notifications | Verify email notification is sent for a completed purchase order | 1. Complete a PO (receive it) 2. Check configured notification email | Notification email is received with correct PO details | Low |
| TC_098 | Multilingual | Verify UI text changes correctly when switching language | 1. Go to Settings > Language 2. Switch language 3. Browse the app | UI labels update to the selected language without missing/broken text | Low |
| TC_099 | UI/Usability | Verify all mandatory fields across modules are clearly marked | 1. Open forms across Purchases, Sales, Customers, Products | Required fields are visibly indicated (e.g., asterisk) | Low |
| TC_100 | Data Integrity | Verify deleting a product does not break historical sales/purchase records | 1. Delete/deactivate a product that has past transactions 2. Open an old sale/PO referencing it | Historical records still display correctly with the product's original data | High |

## Notes
- Add `Actual Result` and `Status (Pass/Fail)` columns during execution.
- IDs and module groupings can be renumbered/resequenced to match your test management tool (Excel/Jira/TestRail).
- Adjust field/module names once you've explored the live demo to match exact UI terminology.
