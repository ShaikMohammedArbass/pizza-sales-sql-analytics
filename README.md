# 🍕 Pizza Sales Analytics: Business Insights & Revenue Intelligence

A dynamic SQL relational analysis built to evaluate operational performance, sales volume, menu revenue distribution, and consumer demand patterns across a high-volume pizza chain.

---

## Short Description / Purpose

This project provides a database analysis of restaurant sales using MySQL. It transforms raw transaction records into structured business metrics covering peak ordering hours, top-performing menu items, category revenue shares, and cumulative growth. Designed for restaurant operators and analytics professionals to optimize menu pricing, staffing, and inventory.

---

## Tech Stack

* 🛢️ **MySQL Server / Workbench** – Relational database management and schema design.
* 🧠 **Advanced SQL** – CTEs, Subqueries, and Aggregate Functions.
* 📊 **Window Functions** – `RANK()`, `ROW_NUMBER()`, and `SUM() OVER()` for ranking and running totals.
* 📐 **Data Modeling** – Multi-table schema (`orders`, `order_details`, `pizzas`, `pizza_types`).
* 📁 **File Format** – `.sql` scripts and `.csv` datasets.

---

## Data Source

* **Source**: Relational Pizza Restaurant Dataset.
* **Tables**: `orders` (timestamps), `order_details` (quantities), `pizzas` (sizes & prices), and `pizza_types` (names & categories).

---

## Features / Highlights

### Business Problem
Raw transaction logs make it hard to evaluate peak rush hours, category margins, or item popularity needed for inventory and shift planning.

### Goal of the Project
Deliver a SQL analytics suite that tracks total revenue, models consumer demand by hour and size, and ranks menu performance to guide operations.

### Walkthrough of Key Analysis & Queries

* **Core KPIs**: Computed gross revenue, order volume, and sales counts by size.
* **Peak Demand**: Extracted hourly order trends (`HOUR(time)`) and calculated average daily pizza consumption using nested CTEs.
* **Category Rankings**: Used `RANK() OVER (PARTITION BY category)` to isolate the top 3 revenue-generating pizzas per category.
* **Revenue Share & Cumulative Growth**: Applied `SUM() OVER()` to calculate percentage revenue contribution per item and track running sales totals.

### Business Impact & Insights

* **Operations**: Hourly demand data improves kitchen shift scheduling and ingredient prep.
* **Menu Strategy**: Revenue share analysis identifies items to re-price, promote, or discontinue.
* **Marketing**: Highlights top sizes and items for targeted promo bundles.

---

