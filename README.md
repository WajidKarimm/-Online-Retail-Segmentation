# Online Retail Data Analysis

## Project Overview
This project focuses on analyzing an **online retail dataset** to extract actionable insights about customer behavior, product trends, and sales patterns. The dataset includes transactional data such as customer purchases, product details, and sales timestamps. Using SQL queries, various analyses have been performed, including customer segmentation, purchase patterns, and sales trends.

---

## Database Structure
### Schema
The dataset resides in the `online_retail` table under the `retailshop` schema. Key columns include:
- `CustomerID`: Unique identifier for customers.
- `InvoiceNo`: Unique transaction ID.
- `Description`: Product description.
- `Quantity`: Quantity purchased.
- `UnitPrice`: Price per unit.
- `InvoiceDate`: Date and time of purchase.
- `StockCode`: Unique product identifier.
- `Country`: Customer's country.

### Additional Column
- **Manufacturers**: A new column (`VARCHAR(50)`), added to classify products based on their manufacturers.

---

## SQL Queries

### 1. **Distribution of Order Values Across Customers**
Calculates the total order value for each customer.
```sql
SELECT CustomerID, SUM(Quantity * UnitPrice) AS TotalOrderValue
FROM online_retail
GROUP BY CustomerID;
