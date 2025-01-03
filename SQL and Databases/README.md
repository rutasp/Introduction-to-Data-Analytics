
## Task: SQL and Databases

In this graded task, you will be asked to create queries to solve specific business questions. 

### Task Overview
You will explore the Adventureworks 2005 database, identify the required data, and determine how to retrieve/merge it from different tables. 

This project serves as a mid-way check-in while learning SQL and will involve 2 peer reviews. The next sprint will introduce more advanced SQL topics.

The database can be accessed using the BigQuery account provided by Turing College.

### Tasks

#### 1. An overview of Products
1.1 Extract data from the Product table where there exists a product subcategory and include the name of the ProductSubcategory.
- **Columns needed**: ProductId, Name, ProductNumber, size, color, ProductSubcategoryId, Subcategory name.
- **Order**: Results should be ordered by SubCategory name.

1.2 Modify the query from 1.1 to include the product category name, and order results by Category name.

1.3 Using the query from 1.2, select the most expensive bikes (price over 2000) that are still actively sold (no sales end date).
- **Order**: Results should be ordered from most to least expensive.

#### 2. Reviewing work orders
2.1 Create an aggregated query to select:
- Number of unique work orders.
- Number of unique products.
- Total actual cost.
For each location Id from the `workoderrouting` table for orders in January 2004.

2.2 Update the query from 2.1 to add the name of the location and the average number of days between the actual start date and actual end date for each location.

2.3 Select all expensive work orders (above 300 actual cost) that occurred throughout January 2004.

#### 3. Query Validation
3.1 Investigate and fix a query related to special offers. The query works but the numbers are off.

3.2 Investigate and fix a query collecting basic Vendor information. Provide feedback on how to improve its readability and debugability.


