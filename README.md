# aurora-components-analysis


Aurora Components Manufacturing Analytics & Data Foundation is a fictional end-to-end analytics project for a mid-sized manufacturing company, designed to showcase SQL, data modeling, and systems analysis skills.

Project description
This project builds a MySQL-based data foundation and analytics layer for “Aurora Components,” a manufacturer of precision gear assemblies with multiple plants and a global customer base.
It covers the full lifecycle from requirements gathering and data modeling to SQL development and executive-style reporting, framed explicitly using an SDLC approach.

Business focus areas:

Sales and customers: revenue, customer performance, and plant-level demand

Operations: production orders, schedule adherence, yield, and capacity

Supply chain: inventory levels, stockout risk, suppliers, and purchase orders

Finance lite: product and customer profitability, discounts, and DSO

The project is structured into three “seasons” of SQL work:

Season 1 – Core reporting (sales, customers, plants)

Season 2 – Operations analytics (inventory, suppliers, production)

Season 3 – Profitability & scenarios (fully loaded margin, scenarios)

Tech stack
Database: MySQL

Language: SQL (ANSI-style with MySQL-specific syntax where needed)

Data: Public manufacturing / industrial datasets plus realistic synthetic extensions

Documentation: Notion (case study, requirements, metrics), Markdown files in this repo

Version control: Git & GitHub

SDLC phases
This project follows a simplified SDLC tailored to analytics and data projects:

Planning

Define business context, goals, scope, constraints, and success criteria.

Establish stakeholders and their high-level needs.

Requirements & Analysis

Capture stakeholder pain points and business questions.

Translate them into user stories and a metric catalog.

Design

Design the relational data model (ERD) for sales, production, inventory, suppliers, and finance-lite.

Define analytics views and reporting layer aligned to user stories.

Development – Season 1: Reporting

Implement core schema and load sales-related data.

Build queries and views for revenue, orders, and customer/plant views.

Development – Season 2: Operations

Extend schema for inventory, suppliers, and production.

Implement Days of Supply, stockout risk, supplier scorecards, and production KPIs.

Development – Season 3: Profitability & Scenarios

Implement BOM-based cost roll-ups and profitability views.

Add scenario simulations for demand and lead-time changes.

Testing & Validation

Validate totals, joins, and metric calculations with targeted test queries.

Document data quality checks and limitations.
