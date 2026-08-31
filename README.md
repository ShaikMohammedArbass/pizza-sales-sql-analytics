# Pizza Sales Insights Pipeline: Business Analytics via Advanced SQL

This project delivers an end-to-end relational database analysis of a high-volume pizza restaurant chain. Using MySQL, complex SQL techniques—including CTEs, Window Functions (`RANK()`, `ROW_NUMBER()`), and Partitioning—were applied to evaluate operational performance, menu revenue distribution, and sales growth over time.

---

## Database Schema & Analytics Pipeline

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


