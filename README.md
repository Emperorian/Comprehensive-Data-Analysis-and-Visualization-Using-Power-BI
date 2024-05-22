# Comprehensive-Data-Analysis-and-Visualization-Using-Power-BI



## Introduction

In the rapidly evolving world of data analytics, the ability to transform raw data into actionable insights is crucial for decision-making and strategic planning. Power BI, a powerful business analytics service by Microsoft, provides a robust platform for data analysis, visualization, and sharing insights across an organization. This project aims to leverage the full spectrum of Power BI's capabilities to demonstrate a comprehensive data analysis process from sourcing data to creating interactive visualizations and deploying them on various platforms.

## Case study

Tailwind Traders requires a detailed report that outlines the company’s latest sales and profit overview. Tailwind Traders is a wholesaler company that is involved in the sales of housing and construction accessories. Ranging from Ultra grip hammer, luminous bulb 60w,        Oakwood shelf, protile cutter, garden glove set, and steel nails (1 inch) to mention a few.                    
The spreadsheet for this project contains about 55 unique product items, including the customer name, product descriptions, email address, etc. To achieve the sale and profit overview we are going to focus on the financial data like the gross product price, tax per product, quantity purchased, gross revenue, total tax, and net revenue, others are stocks, loyalty points, product category, and so on 

## Problem statement

Using MS Excel to obtain data from various sources and then clean, transform, and load the data for further analysis.

**Cleaning**, **transforming**, and **loading data** in Power BI

**Designing** a data model and modeling data in Power BI.

Creating model calculations using **DAX** and optimizing model performance

Creating and enhancing **dashboards** and reports for usability, storytelling, and identifying patterns and trends.

**Configuring alerts.**

## Data sourcing

All data used in this project was provided by the Coursera for the purpose of this project but the link for the dataset such as c.s.v, pbix and python script will be attached when necessary.

  ### Spreadsheet 

For starters, we have to do the following:
- Prepare the sales data worksheet to ensure accuracy before integration into Power BI.
- Understand the components of the sales data, such as individual sales per day and the corresponding gross amount.
- Implement formulas to determine the net amount by subtracting tax from the gross amount.

Tailwind Traders requires a detailed report that outlines the company’s latest sales data. The report must contain gross amounts and the difference between gross and net sales. Let’s create this report so it can shape its future sales strategies. 
A link to the c.s.v file for the first table for sales data can be downloaded [click](https://d3c33hcgiwev3.cloudfront.net/_2jXfvypQfuGZvUEtKJtXA_4f0aced6b1d94111a6eb81e85e3b00e1_Tailwind-Traders-Sales.xlsx?Expires=1716508800&Signature=B~uJ~d~tVewQqG~eKz7kBUM-RyK3~bWe0~wzhqcVsDbDlEqCMOhgs1EOEAMesHIH~asTPrnF2ZXy0JA7OIP0ry3wR5O~9Li~5FVsuumBMbW2oh5~wKfkqzlKeZ9H8vwE5qdoqIfZJi9HQ3OwYKcw2P0Dx-I5r9dABnqlU1nTnKM_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)
A sample of the downloaded table is pasted below 

![image](https://github.com/Emperorian/Comprehensive-Data-Analysis-and-Visualization-Using-Power-BI/assets/101293550/06c555f6-e2fa-4827-8f91-053f28bb9067)

This step is to calculate the gross revenue by using the formula =E2*G2 to calculate the revenue from each product. Which is to insert a column after Quantity Purchased and label it Gross Revenue. Next, calculate the Calculate Total Tax Create a Total Tax column next to Gross Revenue. Input the formula =F2*G2 to calculate the tax for each product. Calculate Net Revenue, Insert a Net Revenue column next to Total Tax. Use the formula =H2-I2 to determine the actual earnings post-tax for each product Observe the first 10 records and note the highest and lowest values for Net Revenue, Quantity Purchased, and Total Tax. In conjunction, observe neighboring columns like Sales Rep for trends.

## Configure data sources
   
### Load the sales data

At this stage of the project the sales data has been cleaned and structured, and additional columns has been added such as net revenue, quantity purchased, gross revenue, etc. Tailwind Traders needs to configure its data sources. The company has sought your help and needs you to add sales data, ensure the accuracy of its data types, and transform its historical currency exchange data. 

Load the Tailwind Traders Sales file into Power BI and select Transform. Begin by loading the Tailwind Traders Sales data file into Power BI.






