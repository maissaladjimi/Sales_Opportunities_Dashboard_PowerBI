## Introduction 
The project includes a Sales Performance Interactive Dashboard for a B2B company selling computer hardware. This dashboard was implemented using PowerBI and designed to reflect the sales team's performance in 2017. It provides a comprehensive overview of total sales, regional performance, individual sales agents' performance within each team, and the customers targeted throughout the year.

<div align="center">
  <img src="https://github.com/maissaladjimi/Sales_Opportunities_Dashboard_PowerBI/assets/94018321/370935cf-ca9d-471f-9f2f-b7bbc1c5c199" width="900">
</div>

The project was developed through four phases: Preparing Data, Modeling Data, Visualizing and Analyzing Data, and Deployment.
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
  * Created a date table using M Query with columns for Date, Year, Quarter, Month, MonthName, and Day to support time-based analysis.

### Load: load data in PowerBI Desktop 
As data is now ready for analysis, we loaded it in PowerBI Desktop using "Close & Apply".

## 2. Model Data
- The model was built using a **Star Schema** with sales_pipeline as the Fact table and accounts, sales_team, products, and Date as Dimension Tables. Relationships established are shown in the figure.
- New measures and calculated columns were created using DAX to enhance analysis capabilities
  <p align="center">
    <img src="https://github.com/user-attachments/assets/39c148e7-fc8a-4fa4-9791-348bf7341fb6" alt="Model Data" width="900"/>
  </p>

## 3. Visualize & Analyze Data
## Sales 2017
  ![saless](https://github.com/user-attachments/assets/8f407440-aa4e-42c4-942e-66e1585f2237)
#### Key Insights 
* **Total Sales:** $9.48M, with nearly 4,000 products sold. The most popular categories were GTX, with 854 GTXBasic and 695 GTXPro units sold, and MG, with 737 MG Special units sold.
* **Quarterly Performance:** Quarter 1 experienced the highest sales increase at 314.58%, driven by February's 85.57% growth, while Quarters 3 and 4 registered the lowest sales percentages, with Quarter 4 showing a significant drop of 44.48% due to a sales decrease of 61.52% in November and 60.18% in December.
* **Conversion Rates:** 48.2% of potential opportunities converted into won deals, representing 22.46% of engaging opportunities.
  
## Regional Offices Sales
  ![Regional Page](https://github.com/user-attachments/assets/90580127-883c-42a0-b929-38b361cf2ce6)
## Sales Team
  ![teams](https://github.com/user-attachments/assets/7733ea57-37d7-4bab-bed1-c66b7d367aee)
## Customers
  ![Customers](https://github.com/user-attachments/assets/499d3344-715f-492a-8096-ea6c54609823)
  
## 4. Deployment 
After completing the report, the dashboard was published in PowerBI Service. 
