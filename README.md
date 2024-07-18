## Introduction 
The project includes a Sales Performance Dashboard for a B2B company selling computer hardware. This dashboard is implemented using PowerBI and designed to reflect the sales team's performance during the year 2017. It provides a comprehensive overview of total sales, regional performance, individual sales agents' performance within each team, and the customers targeted throughout the year.

<div align="center">
  <img src="https://github.com/maissaladjimi/Sales_Opportunities_Dashboard_PowerBI/assets/94018321/370935cf-ca9d-471f-9f2f-b7bbc1c5c199" width="800">
</div>

The project was developed through four phases: Preparing Data, Modeling Data, Visualizing Data, and Deployment.

## 1. Prepare Data ( ETL Process ) 
### Extract: get data from data sources
The initial data was downloaded from Maven Analytics' free datasets. The data was retrieved from local CSV files using the import mode. 
### Transform: clean and transform data to be suitable for analysis
- Clean Data
    * Changed data types to ensure consistency and accuracy.
    * Removed duplicate records to maintain data integrity.
    * Reviewed data distribution, quality, and profile to identify and address any anomalies or issues.
  
- Transform Data:
  * Replaced null values.
  * Renamed column headers for more readability.
  * Added a conditional column to categorize company size based on the number of employees.
  * Extracted the first name of sales agents from the sales_agent column.
  * Created a date table with columns for Date, Year, Quarter, Month, MonthName, and Day to support time-based analysis.

### Load: load data in PowerBI Desktop 
As data is now ready for analysis, we loaded it in PowerBI Desktop using "Close & Apply".

## 2. Model Data
- The model was built using a Star Schema with sales_pipeline as the Fact table and accounts, sales_team, products, and Date as Dimension Tables.
  <p align="center">
    <img src="https://github.com/user-attachments/assets/39c148e7-fc8a-4fa4-9791-348bf7341fb6" alt="Model Data" width="700"/>
  </p>

 
## 3. Visualize Data
- Sales 2017
- Regional Offices Sales
- Sales Team
- Customers
  
## 4. Deployment 
After completing the report, the dashboard was published in PowerBI Service. 
