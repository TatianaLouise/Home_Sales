# Home_Sales

This challenge uses SparkSQL to determine key metrics about home sales data. Spark is used to create temporary views, partition the data, cache and uncache a temporary table, and verify that the table has been uncached.

# Results

## Average price for a four bedroom house sold for each year: 
<img width="233" alt="Screenshot 2024-03-16 at 11 56 33 AM" src="https://github.com/TatianaLouise/Home_Sales/assets/143769037/10757365-c2c2-4935-b343-bb0d01a22a3d">


## Average price of a home for each year the home was built, that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet:
<img width="201" alt="Screenshot 2024-03-16 at 11 57 16 AM" src="https://github.com/TatianaLouise/Home_Sales/assets/143769037/b17b85bb-7f67-43a8-ae84-f548d04102ea">


## Average price of a home per "view" rating having an average home price greater than or equal to $350,000
<img width="236" alt="Screenshot 2024-03-16 at 11 57 32 AM" src="https://github.com/TatianaLouise/Home_Sales/assets/143769037/2fe2639b-2b6b-4ba0-a66a-a15bad4255a6">

# Summary 
When the home_sales data table is cached and the query to identify the avg_price of a home per "view" rating with an avg home price greater or equal to $350,000 is created, the runtime decreases from 1.3591489791870117 seconds (uncached) to 0.717524528503418 seconds (cached).
Once the data is parqueted, the same query runs at a speed of 0.6125171184539795 seconds. The decrease in runtime for this data set indicates that it might be more efficient to parquet the data before working with larger and more complicated queries and data sets.

# Data Source
https://2u-data-curriculum-team.s3.amazonaws.com/dataviz-classroom/v1.2/22-big-data/home_sales_revised.csv
