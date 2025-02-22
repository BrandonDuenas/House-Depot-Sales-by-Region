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
---
This project analyzes House Depot's 2023 regional sales data to provide actionable insights. By examining sales, delivery, and installation data for household appliances in California, we identify top-performing cities and uncover regional trends. The resulting visualizations and analysis will inform data-driven recommendations, enabling House Depot to understand its markets and  optimize resource allocation.

![Dashboard 1](https://github.com/user-attachments/assets/eee21768-0e8d-4a27-802f-24a5c673ac27)


### Data Sources

Sales Data: Sales record files for 2023 were provided by House Depot. These records were then consolidated into a comprehensive spreadsheet to facilitate the regional analysis.

### Tools Used

- Google Sheets - Data collection and Cleaning and analysis
   - [Download Here](https://github.com/BrandonDuenas/House-Depot-Sales-by-Region/blob/main/House%20Depot%20Regional%20-%20Sheet1.csv)

- Tableau Public - Data Analysis
   - [Download here](https://public.tableau.com/views/HousedepotsalesbyRegion/Dashboard1?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

### Data Preperation

For the preperation I did the following
1. Sales data from each file was manually entered into a spreadsheet.
2. Missing values were noted but included in the sales data.
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



