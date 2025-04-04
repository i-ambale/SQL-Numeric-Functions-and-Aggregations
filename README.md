# SQL Numeric Functions and Aggregations
Exercise 5 — ExploreAI Academy

## 📚 Overview
This exercise demonstrates the use of SQL numeric functions and aggregations to compute the total price per order from a dataset. The query utilizes basic arithmetic operations within aggregate functions and is executed against the OrderDetails table from the Northwind sample database.

## 🧮 SQL Query Used
```sql
SELECT 
    OrderID, 
    SUM(UnitPrice * Quantity * (1 - Discount)) AS TotalPrice 
FROM 
    OrderDetails
GROUP BY 
    OrderID;
```
## 🗂️ Dataset
- Database: Northwind.db

- Table: OrderDetails

- Columns used:

    - OrderID: Identifier for the order.
    
    - UnitPrice: Price per unit of the item.
    
    - Quantity: Number of units ordered.
    
    - Discount: Discount applied (as a decimal).

## 🧠 Key Concepts
- Aggregation: The SUM() function is used to compute the total price for each OrderID.

- Arithmetic operations: The total price for each item is calculated by multiplying UnitPrice * Quantity * (1 - Discount).

- Grouping: The GROUP BY clause groups the data by OrderID to summarize total spending per order.

✅ Output
The output is a list of unique order IDs alongside their computed TotalPrice, reflecting how much each order is worth after discounts. Example output:

|        OrderID      |        TotalPrice      |
|---------------------|------------            |
|         10248       |         440.00         |
|         10249       |         1863.40        |
|         10250       |         1813.00        |
|         .....       |         .....          |


Note: The complete output contains all order totals from the OrderDetails table.

## 🔍 Insights
This query is helpful for:

- Summarizing financial performance per order.

- Creating reports for total sales.

- Analyzing the impact of discounts on revenue.

## 📦 Requirements
- SQLite (or any SQL interface that supports the Northwind database)

- Northwind.db database file available locally

## 💡 How to Run
Use a Jupyter Notebook cell with a SQL magic command (%%sql) or a database client like DB Browser for SQLite to execute the query on the Northwind.db database.


