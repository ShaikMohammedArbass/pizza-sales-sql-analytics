# Pizza Sales Insights Pipeline: Business Analytics via Advanced SQL

This project delivers an end-to-end relational database analysis of a high-volume pizza restaurant chain. Using MySQL, complex SQL techniques—including CTEs, Window Functions (`RANK()`, `ROW_NUMBER()`), and Partitioning—were applied to evaluate operational performance, menu revenue distribution, and sales growth over time.

---

```text
  +-------------------+       +-------------------+
  |      orders       |       |    pizza_types    |
  +-------------------+       +-------------------+
  | order_id (PK)     |       | pizza_type_id(PK) |
  | date, time        |       | name, category    |
  +---------+---------+       +---------+---------+
            |                           |
            v                           v
  +-------------------+       +-------------------+
  |   order_details   |  -->  |      pizzas       |
  +-------------------+       +-------------------+
  | order_details_id  |       | pizza_id (PK)     |
  | order_id (FK)     |       | pizza_type_id(FK) |
  | pizza_id (FK)     |       | size, price       |
  | quantity          |       +-------------------+
  +-------------------+

Key Business Analytics & SQL Techniques
Revenue & Sales Growth Analysis: Calculated total gross revenue, daily order volumes, and cumulative revenue over time using aggregate window functions.

Menu & Category Performance: Evaluated sales performance by category and pinpointed top 3 revenue-generating pizzas per category using RANK() OVER (PARTITION BY category).

Percentage Contribution Analysis: Used CTEs paired with SUM() OVER() to determine the exact percentage revenue contribution of each pizza item relative to total sales.

Peak Demand Identification: Analyzed hourly order distributions and calculated average daily pizza consumption through nested subqueries and CTE aggregations.

Project Structure
Pizza_Sales_Analytics_Queries.sql - Complete SQL script containing schema exploration, basic KPI queries, intermediate menu analysis, and advanced window functions.

Technical Stack
Language: SQL

Database Engine: MySQL Server / MySQL Workbench

Analytical Techniques: Common Table Expressions (CTEs), Window Functions (RANK, ROW_NUMBER, Unbounded Preceding), Dynamic Percentages, Data Aggregations, Multi-Table Joins
