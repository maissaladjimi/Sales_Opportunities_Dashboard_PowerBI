## Introduction 
The project includes a Sales Performance Interactive Dashboard for a B2B company selling computer hardware. This dashboard was implemented using PowerBI and designed to reflect the sales team's performance in 2017. It provides a comprehensive overview of total sales, regional performance, individual sales agents' performance within each team, and the customers targeted throughout the year.

<div align="center">
  <img src="https://github.com/maissaladjimi/Sales_Opportunities_Dashboard_PowerBI/assets/94018321/370935cf-ca9d-471f-9f2f-b7bbc1c5c199">
</div>

---

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
    <img src="https://github.com/user-attachments/assets/39c148e7-fc8a-4fa4-9791-348bf7341fb6" alt="Model Data"/>
  </p>

## 3. Visualize & Analyze Data
## Sales 2017
  ![saless](https://github.com/user-attachments/assets/8f407440-aa4e-42c4-942e-66e1585f2237)
#### Key Insights 
* **Total Sales:** $9.48M, with nearly 4,000 products sold. The West region contributes the highest sales at $3,359,174.00, followed closely by the Central $3,163,215.00 and East $2,959,614.00 regions. The most popular categories were GTX, with 854 GTXBasic and 695 GTXPro units sold, and MG, with 737 MG Special units sold.
* **Quarterly Performance:** Quarter 1 experienced the highest sales increase at 314.58%, driven by February's 85.57% growth, while Quarters 3 and 4 registered the lowest sales percentages, with Quarter 4 showing a significant drop of 44.48% due to a sales decrease of 61.52% in November and 60.18% in December.
* **Conversion Rates:** 48.2% of potential opportunities converted into won deals, representing 22.46% of engaging opportunities.
  
## Regional Offices Sales
  ![Regional Page](https://github.com/user-attachments/assets/90580127-883c-42a0-b929-38b361cf2ce6)
#### Key Insights 
* **Regional Performance** The East region has the highest average basket value of $2.67k, indicating higher spending per order, The Central region has the highest average orders per month ( 128 orders/month), indicating higher sales volume, and The West region generates the highest total revenue of $3.36M, showcasing a balance between high average basket value and high order volume.
* **Sales Trends:** For the East and West Region, There is a steady increase in sales opportunities in the first half of the year, peaking around mid-year, followed by a decline in the latter months. The same goes for the Central region, However, there is a noticeable peak in mid-year, indicating a seasonal or promotional boost.
* **Products:** GTXPro/ GTX Plus Pro are the highest revenue-generating products across all regions. In terms of quantities, GTX Basic seems popular in all regions.
  
  In the East, GTXPro and MG Advanced are popular, while in the Central region, MG Special and GTX Plus Basic are most bought. Finally, for the West region, GTXPro and MG Special are the most sold. Additionally, GTK500 is only available in the West region, generating almost $380,000 in revenues.
## Sales Team
  ![teams](https://github.com/user-attachments/assets/7733ea57-37d7-4bab-bed1-c66b7d367aee)
#### Key Insights 
- Agents with moderate average times to sell (40-48 days) tend to have higher performance than others.
- Higher conversion rates don't necessarily correlate with better overall performance. An agent might have a lower conversion rate but better revenues generated due to the high average purchase value, respectively, an agent might have a high conversion rate but a weak performance due to low average purchase value.
- **Central Team** 
    * Melvin Marxen's team outperforms Dustin Brinkmann's team, generating a total of over $2.1M from 829 sales with an average purchase value of $2,569. In contrast, Dustin's team generates $1M from 702 sales with an average purchase value of $1,471.
    * Lajuana, Niesha, and Gladys struggle to successfully close deals, as their conversion rates are under 50%.
    * Niesha, Lajuana, and Versie lag behind compared to the rest of the team due to the lower average purchase value of their clients.
- **East Team**
    * Rocco Neubert's team leads in performance, achieving over $1.9M in revenue from 663 sales, with an average purchase value of $2,860. In comparison, Cara Losch's team has generated $1M from 445 sales, with an average purchase value of $2,388.
    * Except for agents Reed, Garret, and Donn, the rest of the team has a conversion rate below 50%.
    * Violet, Willburn, and Garret are the underperformers. Garret and Willburn have lower performance due to their smaller order volumes of 70 and 53, respectively. Despite Violet’s higher order volume of 111, her average purchase value of $1,000 is significantly lower, making her the least effective performer.
- **West Team**
    * The performance of both managers’ teams is quite close. Summer Sewald's team has generated $1.8M in revenue from 778 sales, with an average purchase value of $2,357. In comparison, Celia Rouche's team has earned $1.5M from 571 sales, with an average purchase value of $2,671.
    * With the exception of Maureen and Hayden, most agents have conversion rates below 50%.
    * Despite having one of the highest average purchase values, Rosalina’s performance is the weakest on the team due to a relatively low order count of only 67.
## Customer Segments
  ![Customers](https://github.com/user-attachments/assets/499d3344-715f-492a-8096-ea6c54609823)
#### Key Insights
* **Customer Overview:** The company has a total of 85 customers with an average number of approximately 47 orders per customer, an average lifespan of 380 days, and an average Customer Lifetime Value of $116K.
* **Customer Segments:** Most customers are categorized as frequent customers (64 out of 85). Loyal and top customers are relatively few, with 17 loyal customers and 4 top customers.
* **Sector Distribution:** Retail (753) and technology (642) sectors dominate the customer base, followed by medical (549) and software (428).
* **Business Size:** A substantial portion of customers (71.56%) are large-sized businesses. Medium-sized businesses represent 23.7%, while small-sized businesses account for only 4.74%.
* **Geographical Distribution:** The American continent is the top contributing continent taking over with 85%, out of which 95% belong to the United States.
* **Customer Retention:** Customer retention remains relatively stable throughout the year, but there is a significant drop in the final month.
* Top Customers are located in the United States and Korea.
* The Central office is the only team working with an African country, Kenya, bringing a revenue of $103,024.
  
## 4. Deployment 
After completing the report, the dashboard was published in PowerBI Service. 

---
## Recommendations 
* Focus on enhancing sales and increasing potential opportunities during Q3 and Q4 for all regions, specifically for August, November, and December. Work on customer engagement to maintain retention, targeted promotions and discounts, and seasonal campaigns such as holiday offers for the Christmas/Halloween season and summer season.
  
* Since GTXPro/GTX Plus Pro are the highest revenue-generating products across all regions, focus on boosting their availability and visibility and consider packing them with other products and introducing complementary products to drive additional sales.
  
* Customize marketing strategies to align with regional preferences, such as promoting MG Advanced more aggressively in the EAST region and MG Special in the CENTRAL region to match clients' needs.
  
* Although GTK500 is only available in the West region, it generates significant revenue. Promote it more in the WEST region and, if possible, expand its availability to other regional offices.
  
* For customer base expansion, focus on acquiring more customers in key sectors (retail, technology, and medical), attracting large-sized businesses for higher revenue and long-term contracts, and expanding into underrepresented continents such as Africa. Additionally, develop strategies to convert frequent customers into loyal and top clients by enhancing personalized engagement, offering exclusive benefits, and maintaining exceptional customer service.
  
* For sales agents like Lajuana, Versie, and Violet, who have high sales volumes but low average purchase values, provide workshops and training on targeting higher-value clients. For those with high average purchase values but low sales volumes, offer support to help increase their order quantities.
  
* Regional offices often have high-performing teams that generate most of the revenue and weaker teams with lower performance. The weaker teams should analyze the successful teams’ strategies for closing deals and handling high-value transactions to improve their performance.
  
