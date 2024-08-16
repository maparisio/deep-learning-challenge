# deep-learning-challenge

## Module 22 Challenge - Big-Data

# Home_Sales
In this challenge, I will use my knowledge of SparkSQL to determine key metrics about home sales data. Then I will use Spark to create temporary views, partition the data, cache and uncache a temporary table, and verify that the table has been uncached.

## INDEX

## Instructions
1. What is the average price for a four-bedroom house sold for each year? Round off your answer to two decimal places.
2. What is the average price of a home for each year the home was built, that has three bedrooms and three bathrooms? Round off your answer to two decimal places.
3. What is the average price of a home for each year the home was built, that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet? Round off your answer to two decimal places.
4. What is the average price of a home per "view" rating having an average home price greater than or equal to $350,000? Determine the run time for this query, and round off your answer to two decimal places.
5. Cache your temporary table home_sales.
6. Check if your temporary table is cached.
7. Using the cached data, run the last query that calculates the average price of a home per "view" rating having an average home price greater than or equal to $350,000. 8. 8. Determine the runtime and compare it to uncached runtime.
9. Partition by the "date_built" field on the formatted parquet home sales data.
10. Create a temporary table for the parquet data.
11. Run the last query that calculates the average price of a home per "view" rating having an average home price greater than or equal to $350,000. Determine the runtime and compare it to uncached runtime.
12. Uncache the home_sales temporary table.
13. Verify that the home_sales temporary table is uncached using PySpark.
14. Download your Home_Sales.ipynb file and upload it into your "Home_Sales" GitHub repository.

# Additional Requirements:
1. A Spark DataFrame is created from the dataset.
2. A temporary table of the original DataFrame is created.
3. A cache of the temporary "home_sales" table is created and validated.
4. The query is run on the cached temporary table, and the run time is computed.
5. A partition of the home sales dataset by the "date_built" field is created, and the formatted parquet data is read.
6. A temporary table of the parquet data is created.
7. The query is run on the parquet temporary table, and the run time is computed.
8. The "home_sales" temporary table is uncached and verified.
9. Cache your temporary table home_sales.
10. Check if your temporary table is cached.
11. Using the cached data, run the query that filters out the view ratings with an average price of greater than or equal to $350,000. Determine the runtime and compare it to uncached runtime.
12. Partition by the "date_built" field on the formatted parquet home sales data.
13. Create a temporary table for the parquet data.
14. Run the query that filters the view ratings with an average price of greater than or equal to $350,000. Determine the runtime and compare it to uncached runtime.
15. Uncache the home_sales temporary table.
16. Verify that the home_sales temporary table is uncached using PySpark.

# Repository Contents
- Home_Sales_colab.ipynb
- Read.me

# References
Data for this dataset was generated by edX Boot Camps LLC, and is intended for educational purposes only.
