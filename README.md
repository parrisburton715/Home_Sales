# Home Sales Analysis

This project involves analyzing home sales data using Apache Spark. Below is a step-by-step guide on how to execute the analysis.

## Setup

1. **Install Spark and Java**:
   - Install the required Spark version and Java Development Kit.
   - Set environment variables for Spark and Java.
   - Initialize Spark with the necessary configuration.

2. **Create a Spark Session**:
   - Import necessary libraries and start a Spark session for the analysis.

## Data Handling

1. **Download and Read Data**:
   - Download the home sales data from an S3 bucket.
   - Load the data into a Spark DataFrame and verify its contents.

2. **Create Temporary View**:
   - Create a temporary SQL view of the DataFrame to run SQL queries on the data.

## Data Analysis

1. **Calculate Average Price for Four-Bedroom Houses**:
   - Determine the average price of four-bedroom houses sold each year.

2. **Average Price by Year Built (3 Bedrooms, 3 Bathrooms)**:
   - Calculate the average price for homes with 3 bedrooms and 3 bathrooms, grouped by the year they were built.

3. **Average Price by Year Built (Additional Criteria)**:
   - Find the average price for homes with 3 bedrooms, 3 bathrooms, two floors, and at least 2,000 square feet, grouped by the year built.

4. **Average Price Per View Rating**:
   - Compute the average price of homes per view rating where the average price is at least $350,000. Measure and print the query runtime.

## Performance Optimization

1. **Cache Data**:
   - Cache the temporary view of the home sales data to improve query performance.

2. **Re-run Query Using Cached Data**:
   - Execute the same query on the cached data and measure the runtime to compare with the uncached version.

3. **Partition Data and Save as Parquet**:
   - Partition the data by the year built and save it in Parquet format.

4. **Read Parquet Data**:
   - Load the data from the Parquet file.

5. **Create Temporary View for Parquet Data**:
   - Create a temporary SQL view for the parquet-formatted data.

6. **Run Query on Parquet Data**:
   - Execute the query on the parquet-formatted data and compare the runtime with the cached data.

## Final Steps

1. **Uncache the Temporary Table**:
   - Remove the cached data from Spark’s memory.

2. **Check Cache Status**:
   - Verify that the temporary table is no longer cached.