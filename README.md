# Home_Sales

# Big Data Analysis of Home Sales Using Apache Spark

**Overview**

This project demonstrates the analysis of a large dataset of home sales using Apache Spark. The primary objective was to perform various SQL-like operations, 
optimize query performance through caching and partitioning, and extract insights about home prices based on multiple parameters.

**Project Highlights**

1. Data Exploration:

 - The dataset was loaded into a Spark DataFrame, and the schema was validated for accuracy.
 
2- SQL Queries:

 - Temporary views were created for SQL-based operations.
 - Queries were executed to calculate:
  - Average price of four-bedroom homes sold each year.
  - Average price of homes with specific configurations (e.g., three bedrooms, three bathrooms) based on the year built.
  - Price trends for homes with two floors and at least 2,000 square feet.
  - Average price per "view" rating for homes with prices ≥ $350,000.

3. Performance Optimization:

 - Caching and uncaching were implemented to compare query runtimes for optimized performance.
 - Partitioning by the date_built field was used to store the data in Parquet format and enhance query efficiency.

4. Insights:

 - Price trends showed clear patterns based on home configurations and view ratings.
 - Significant runtime improvements were observed with caching and Parquet partitioning.

**Tools Used**

 - Apache Spark: For distributed data processing and SQL operations.
 - PySpark: Python integration with Spark.
 - Jupyter Notebook: For documenting and executing queries.
 - Google Colab: Used as an alternative environment for replicating the analysis.

**How to Run the Analysis**

1. Set Up the Environment:

 - Install dependencies: Apache Spark and PySpark.
 - Download the dataset (home_sales_revised.csv) from the provided URL.

2. Run the Notebooks:

 - Execute the steps outlined in the Home_Sales.ipynb (Jupyter) or Home_Sales_colab.ipynb (Google Colab) notebooks.
 - Follow the instructions to load data, create views, and run queries.

3. Analyze the Outputs:

 - Review query results and runtime improvements in the notebook outputs.

**Key Results**

1. Price Trends:

 - Four-bedroom homes showed steady price growth across years.
 - Homes with specific configurations (three bedrooms, three bathrooms) had distinct price variations based on the year built.

2. View Rating Analysis:

 - Homes with a "view" rating of ≥ $350,000 had higher average prices.
 - Runtime for uncached vs. cached queries demonstrated noticeable performance improvements.

3. Partitioning Impact:

 - Using Parquet format and partitioning reduced query runtimes significantly compared to non-partitioned data.

**Performance Observations**
 - Caching: Reduced query runtime by approximately 50%.
 - Partitioning: Improved data organization and retrieval efficiency.

**Future Improvements**

 - Expand analysis to include additional parameters like location and property type.
 - Integrate visualizations to present insights more effectively.
