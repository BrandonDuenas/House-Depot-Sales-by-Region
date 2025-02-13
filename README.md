# Regional Sales Analysis

### Project Overview

This data analysis is ment to provide insights of regional sales for the Company House Depot for the year of 2023. Through the collection and analysis of the sales data, we look to map out, what cities in Califonia have the most sales, deliveries, and Installations of Household appliances. Through the mapped out data we look to identify trends to make data driven recommendations, and to help the comapany understand where their products are selling the best.

### Data Sources

Sales Data: House Depot provided me with a box full of files which contained the information detailing each sale in 2023. I then built a spreadsheet containing all of needed information to preform the regional analysis. 

### Tools Used

- Google Sheets - Data collection and Cleaning and analysis
   - [Download Here](https://github.com/BrandonDuenas/House-Depot-Sales-by-Region/blob/main/House%20Depot%20Regional%20-%20Sheet1.csv)

- Tableau Public - Data Analysis
   - [Download here](https://public.tableau.com/views/HousedepotsalesbyRegion/Dashboard1?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

### Data Preperation

For the preperation I did the following
1. Added each file manually from paper to spreadsheet
2. Acknowledged missing values but still added them into sales data
3. Formatted Data to work seemless with Tableau
   
### Explorataory Data Analysis

Through the Exploratory Data Analysis i looked to answer the following questions:

- What were the top 20 cities that provided the most revenue for the Company?
- What was the amount of Total Sales made from customers in each city?
- What was the number of sales made from each city?
- How many products were Delivered to each city?
- How many products were installed in customers houses in each city?

### Data Analyis

I used some code to analyse the data in tableau by creating a Calculated Fields
   ``` Tableau
COUNT([Sale Price])<= WINDOW_AVG(COUNT([Sale Price]))
```
  ``` Tableau
SUM([Sale Price])<= WINDOW_AVG(SUM([Sale Price]))
```
``` Tableau
COUNT(
IF [Installation]= "Y" then [order ID] end)
```
``` Tableau
COUNT(
IF [Delivery] = "Y" then [order ID] END)
```
