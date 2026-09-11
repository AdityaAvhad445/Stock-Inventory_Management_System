# Requirement Analysis — Stock Inventory Management System

## 1. Purpose
To understand the application's requirements and ensure the data representation for key stakeholders (Purchases, Customers, Sales) matches expected business outcomes before test design begins.

## 2. Key Stakeholder Data Areas

### Purchases
- Purchase order creation: vendor, products, quantity, unit cost, tax, total
- Purchase status flow: Ordered → Received (partial/full) → Completed
- Stock quantity should increase correctly on receiving a purchase
- Purchase returns should decrease stock and reflect in vendor records

### Customers
- Customer profile data: name, contact info, purchase/sales history
- Top customers should be calculated correctly based on sales volume/value
- Customer-linked sales and invoices must map back to the correct customer record

### Sales
- Sales/POS transactions: product, quantity, price, discount, tax, payment method
- Stock quantity should decrease correctly on a completed sale
- Sales returns should increase stock back and adjust customer/payment records
- Quotation-to-sale conversion should carry over correct data

## 3. Graphical Representation Requirements (Dashboard / Centers)
- Each stock "center" (store/location/warehouse) should have its own accurate chart data — stock levels, sales, income/expenses
- Dashboard charts (e.g., top-selling products, income vs. expenses, stock value) must reflect real-time or correctly time-stamped data
- Filters (date range, center/location, vendor, product) must correctly update chart output
- Data on charts should reconcile with the underlying raw reports (no mismatch between graph and report numbers)

## 4. Assumptions
- "Centers" refers to individual store/warehouse locations within the system
- Stock values update in near real-time after purchase/sale/transfer actions
- Reports and dashboard charts pull from the same underlying data source

## 5. Open Questions (to raise with stakeholders/BA)
- What is the acceptable data refresh delay for dashboard charts?
- How are multi-center stock transfers reflected in each center's individual report?
- Is there a defined precision/rounding rule for currency and quantity values?
