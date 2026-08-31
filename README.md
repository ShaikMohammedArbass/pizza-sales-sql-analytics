# 🍕 Pizza Sales Analytics: Business Insights & Revenue Intelligence

A dynamic SQL relational analysis built to evaluate operational performance, sales volume, menu revenue distribution, and consumer demand patterns across a high-volume pizza chain.

---

## Short Description / Purpose

This project provides a database analysis of restaurant sales using MySQL. It transforms raw transaction records into structured business metrics covering peak ordering hours, top-performing menu items, category revenue shares, and cumulative growth[cite: 1]. Designed for restaurant operators and analytics professionals to optimize menu pricing, staffing, and inventory.

---

## Tech Stack

* 🛢️ **MySQL Server / Workbench** – Relational database management and schema design.
* 🧠 **Advanced SQL** – CTEs, Subqueries, and Aggregate Functions[cite: 1, 2].
* 📊 **Window Functions** – `RANK()`, `ROW_NUMBER()`, and `SUM() OVER()` for ranking and running totals[cite: 1, 2].
* 📐 **Data Modeling** – Multi-table schema (`orders`, `order_details`, `pizzas`, `pizza_types`)[cite: 1, 2].
* 📁 **File Format** – `.sql` scripts and `.csv` datasets[cite: 1, 2].

---

## Data Source

* **Source**: Relational Pizza Restaurant Dataset[cite: 1, 2].
* **Tables**: `orders` (timestamps), `order_details` (quantities), `pizzas` (sizes & prices), and `pizza_types` (names & categories)[cite: 1].

---

## Features / Highlights

### Business Problem
Raw transaction logs make it hard to evaluate peak rush hours, category margins, or item popularity needed for inventory and shift planning[cite: 1, 2].

### Goal of the Project
Deliver a SQL analytics suite that tracks total revenue, models consumer demand by hour and size, and ranks menu performance to guide operations[cite: 1, 2].

### Walkthrough of Key Analysis & Queries

* **Core KPIs**: Computed gross revenue, order volume, and sales counts by size[cite: 1].
* **Peak Demand**: Extracted hourly order trends (`HOUR(time)`) and calculated average daily pizza consumption using nested CTEs[cite: 1].
* **Category Rankings**: Used `RANK() OVER (PARTITION BY category)` to isolate the top 3 revenue-generating pizzas per category[cite: 1].
* **Revenue Share & Cumulative Growth**: Applied `SUM() OVER()` to calculate percentage revenue contribution per item and track running sales totals[cite: 1].

### Business Impact & Insights

* **Operations**: Hourly demand data improves kitchen shift scheduling and ingredient prep[cite: 1, 2].
* **Menu Strategy**: Revenue share analysis identifies items to re-price, promote, or discontinue[cite: 1, 2].
* **Marketing**: Highlights top sizes and items for targeted promo bundles[cite: 1, 2].

---

## How to Run

1. Clone this repository[cite: 2]:
   ```bash
   git clone [https://github.com/YOUR_USERNAME/pizza-sales-sql-analytics.git](https://github.com/YOUR_USERNAME/pizza-sales-sql-analytics.git)
