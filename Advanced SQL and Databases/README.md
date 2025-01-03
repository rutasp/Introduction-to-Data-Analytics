# Advanced SQL and Databases

This project is part of the Data Analytics course at Turing College. The goal is to work with the AdventureWorks 2005 database using SQL queries to solve various business questions. The database is accessible through the BigQuery account provided by Turing College.

## Tasks Overview

### 1. Customer Data Analysis

#### 1.1 Create a Detailed Overview of Individual Customers
- Extract customer identity information: `CustomerId`, `Firstname`, `Last Name`, `FullName`.
- Include `addressing_title` (e.g., "Mr. Achong", default to "Dear Achong" if missing).
- Contact information: `Email`, `Phone`, `AccountNumber`, `CustomerType`.
- Location information: `City`, `State`, `Country`, `Address`.
- Sales: number of orders, total amount (with Tax), and date of the last order.
- Limit the output to the top 200 rows ordered by total amount (with tax).

#### 1.2 Identify Customers Who Have Not Ordered in the Last 365 Days
- Using a temporary table, CTE, or subquery of 1.1, filter customers who haven't placed an order in the last 365 days.
- Output the top 200 customers with the highest total amount (with tax).

#### 1.3 Mark Active vs Inactive Customers
- Extend the 1.1 query by adding a column to mark active customers based on whether they’ve ordered within the last 365 days.
- Limit the output to the top 500 rows ordered by `CustomerId` in descending order.

#### 1.4 Extract Data for Active Customers from North America
- Customers who have either ordered more than 2500 in total amount (with Tax) or ordered 5+ times.
- Split their address line into two columns: `address_no` and `address_st`.
- Order the output by country, state, and `date_last_order`.

### 2. Reporting Sales Numbers

#### 2.1 Monthly Sales Numbers by Country and Region
- Query monthly sales data including the number of orders, customers, salespersons, and total amount (with tax) per country and region.

#### 2.2 Cumulative Sum of Total Amount Earned
- Extend the query from 2.1 by adding a cumulative sum of the total amount (with tax) per country and region using a CTE or subquery.

#### 2.3 Rank Sales by Total Amount Earned per Country
- Add a `sales_rank` column that ranks rows from best to worst based on the total amount earned each month per country/region.

#### 2.4 Add Tax Information at the Country Level
- Include the average tax rate (`mean_tax_rate`) for each country.
- Show the percentage of provinces with available tax rates (`perc_provinces_w_tax`).
- Only count the highest tax rate in provinces with multiple rates and ignore the `isonlystateprovinceFlag`.
