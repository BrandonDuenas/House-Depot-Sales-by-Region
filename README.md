# Regional Sales Analysis

## Table of contents
   - [Project Overview](#project-overview)
   - [Data Sources](#data-sources)
   - [Tools Used](#tools-used)
   - [Data Preperation](#data-preperation)
   - [Exploratory Data Analysis](#exploratory-data-analysis)
   - [Data Analysis](#data-analysis)
   - [Results](#results)
   - [Recommendations](#recommendations)
   - [Limitations](#limitations)

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
   
### Exploratory Data Analysis

Through the Exploratory Data Analysis i looked to answer the following questions:

- What were the top 10 cities that provided the most revenue for the Company?
- What was the amount of Total Sales made from customers in each of those top 10 cities?
- What was the number of sales made from each of the top 10 Cities?
- How many products were Delivered to the top 10 cities?
- How many products were installed in customers houses in the top 10 cities?

### Data Analysis

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

### Results

A. The cities included in the top revenue makers from most to least are:  Manteca, Stockton, Tracy, Modesto, Lathrop, Ceres, Patterson, Lodi, Delhi, and Roseville.

B. The Amount of sales and revenue for each of the Top Cities are:
   1. Manteca $62737 with 91 counted sales
   2. Stockton $35037 with 50 counted sales
   3. Tracy $22304 with 33 counted sales
   4. Modesto $19610 with 25 counted sales
   5. Lathrop $18827 with 25 counted sales
   6. Ceres $6009 with 8 counted sales
   7. Patterson $5929 with 8 counted sales
   8. Lodi $4553 with 5 counted sales
   9. Delhi $4011 with 4 counted sales
   10. Roseville $3656 with 8 counted sales

C.The amount of Deliverys and installations for the top 10 revenue cities are: 
   1. Manteca with 40 deliveries and 23 installations
   2. Stockton with 29 deliveries and 14 installations
   3. Tracy with 15 deliveries and 9 installations
   4. Modesto with 11 deliveries and 8 installations
   5. Lathrop with 10 deliveries and 8 installations
   6. Ceres with 3 deliveries and 3 installations
   7. Patterson with 5 deliveries and 2 installations
   8. Lodi with 1 delivery and 0 installations
   9. Delhi with 3 deliveries 3 installations
   10. Roseville with 2 deliveries and 0 installations

### Recommendations
Based on the analysis done through Regional Mapping I recommend the following:

- Invest more in marketing in cities in the middle and lower ranges of the list
- Strive to do Installations with every customer you are already delivering equipment to their household, to maximize profits and customer satisfaction.

### Limitations 

I had to remove null values  from the data analysis because not all files had information regarding customers residence. Those null values would have affected the accuracy of my end results.



