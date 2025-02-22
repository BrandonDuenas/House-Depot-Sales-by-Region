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

The exploratory data Analysis aimed to answer the following questions:

- Which 10 cities generated the most revenue for the Company?
- What was the total revenue from customers in each of these top 10 cities?
- What was the total number of sales in each of the top 10 Cities?
- How many products were delivered to each of the top 10 cities?
- How many products were installed in customers' homes in each the top 10 cities?

### Data Analysis

 I used calculated fields within Tableau to analyze the data
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

A. The cities included in the top revenue generators, listed from highest to lowest revenue, are:  Manteca, Stockton, Tracy, Modesto, Lathrop, Ceres, Patterson, Lodi, Delhi, and Roseville.

B. The revenue and sales for each of the top cities are:
   1. Manteca: $62,737 (91 sales)
   2. Stockton: $35,037 (50 sales)
   3. Tracy: $22,304 (33 sales)
   4. Modesto: $19,610 (25 sales)
   5. Lathrop: $18,827 (25 sales)
   6. Ceres: $6,009 (8 sales)
   7. Patterson: $5,929 with
   8. Lodi: $4,553 (5 sales)
   9. Delhi $4,011 (4 sales)
   10. Roseville: $3,656 (8 sales)

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



