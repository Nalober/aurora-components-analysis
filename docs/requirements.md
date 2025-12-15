

***

# Aurora Components – Requirements

## 1. Purpose

This document captures the business and analytical requirements for the **Aurora Components Manufacturing Analytics & Data Foundation** project.  
It translates stakeholder needs into concrete capabilities, user stories, and high-level data/analytic requirements that will guide design and development.

***

## 2. Stakeholder summary

**Sponsors**

- **CEO** – Needs a clear view of growth, product mix, and plant performance.  
- **COO** – Needs visibility into throughput, on-time delivery, and bottlenecks across plants.

**Core stakeholders**

- **CFO** – Focused on product and customer profitability, inventory carrying cost, and payment behavior.  
- **Plant Managers (Midwest, Eastern Europe)** – Focused on schedule adherence, utilization, overtime, and scrap.  
- **Supply Chain Manager / Procurement** – Focused on stockouts, days of supply, supplier performance, and lead times.  
- **Sales Director** – Focused on customer performance, revenue concentration, and service levels.

***

## 3. Business requirements (by area)

### 3.1 Sales & customers

**BR-S1** – The system must provide monthly revenue and order volume by region, plant, product line, and customer segment.  
**BR-S2** – The system must identify the top customers (by revenue and margin) over configurable time periods.  
**BR-S3** – The system must distinguish new vs existing customers based on first order date.  
**BR-S4** – The system must provide customer-level profitability, including revenue, discounts, cost of goods, and payment behavior (DSO).

### 3.2 Orders & fulfillment

**BR-O1** – The system must list all open orders, with due dates and assigned plant, to support weekly production planning.  
**BR-O2** – The system must calculate on-time delivery rate by plant, product line, and key customer.  
**BR-O3** – The system must support scenario analyses on demand changes (e.g., +10% demand) and show resulting order and capacity impact.

### 3.3 Inventory & stock

**BR-I1** – The system must provide current inventory levels by product and plant.  
**BR-I2** – The system must calculate Days of Supply per product/plant using recent demand history.  
**BR-I3** – The system must flag products at risk of stockout in the next configurable number of days.  
**BR-I4** – The system must support safety stock thresholds per product/plant and categorize items as “Critical / Warning / OK”.

### 3.4 Suppliers & purchasing

**BR-P1** – The system must aggregate purchase orders and receipts by supplier, product, and plant.  
**BR-P2** – The system must measure on-time delivery rate per supplier.  
**BR-P3** – The system must compute average unit cost by supplier and product.  
**BR-P4** – The system must rank suppliers by cost and reliability (on-time rate) for key components.

### 3.5 Production & operations

**BR-M1** – The system must record production orders, planned vs actual dates, and quantities by plant and product.  
**BR-M2** – The system must calculate schedule adherence and yield for each production order, product, and plant.  
**BR-M3** – The system must summarize utilization and performance by plant and (optionally) work center/line.  
**BR-M4** – The system must enable comparison of throughput, on-time delivery, and scrap across plants.

### 3.6 Profitability & finance-lite

**BR-F1** – The system must compute fully loaded product cost using bills of materials (components) plus labor/overhead allocations.  
**BR-F2** – The system must calculate gross margin by product and product line.  
**BR-F3** – The system must calculate customer-level profitability, including effects of discounts and returns (if modeled).  
**BR-F4** – The system must compute Days Sales Outstanding (DSO) and payment aging per customer.

### 3.7 Executive & cross-system views

**BR-X1** – The system must provide an executive summary view combining revenue, on-time delivery, and margin by product line.  
**BR-X2** – The system must provide a plant comparison view showing throughput, on-time delivery, and scrap for each plant.  
**BR-X3** – The system must support “what if” scenarios (demand and lead-time changes) and expose the impact on key KPIs.

***


## 4. High-level data requirements

- Ability to store and query: customers, products, product lines, plants.  
- Sales entities: orders, order_items, order status, dates, and amounts.  
- Inventory entities: inventory snapshots by product and plant, safety stock levels.  
- Supply chain entities: suppliers, purchase_orders, purchase_order_items, expected vs actual receipts.  
- Production entities: production_orders (planned vs actual), quantities, and (optionally) work centers.  
- BOM: parent and component product relationships and quantities.  
- Finance-lite entities: invoices, payments, discounts, and payment dates.

***

## 5. Non-functional requirements (lightweight)

- **NFR-1** – Queries supporting core dashboards (sales summary, inventory risk, supplier scorecard, profitability) should return in a reasonable time for interactive use on a laptop-scale environment.  
- **NFR-2** – All analytical outputs should be reproducible from version-controlled SQL scripts and documented schemas.  
- **NFR-3** – Metric definitions and logic should be documented so that another analyst could understand and extend the model.

***
