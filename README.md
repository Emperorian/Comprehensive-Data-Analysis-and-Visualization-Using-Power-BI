# Comprehensive-Data-Analysis-and-Visualization-Using-Power-BI

[TAILWIND TRADERS](https://app.powerbi.com/links/RwRcHUdXtX?ctid=e715188b-7518-450d-a2c1-88ffafc16119&pbi_source=linkShare) 

## Table Of Content

- [Introduction](#introduction)

- [Case study](#case-study)

- [Problem statement](#problem-statement)

- [Data sourcing](#data-sourcing)

- [Configure data sources](#configure-data-sources)

- [Data Modelling](#data-modelling)

- [Visualization](#visualization)

- [Configuring alerts and subscriptions](#configuring-alerts-and-subscriptions)

- [Conclusion](#conclusion)





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

![image](https://github.com/Emperorian/Comprehensive-Data-Analysis-and-Visualization-Using-Power-BI/assets/101293550/c86fe58c-61ec-4026-812c-0ccdc2a1c3eb)

Clicking on the transform data button will lead you to the power query interface. Power Query is a data connection technology that enables you to discover, connect, combine, and refine data across a wide variety of sources for better analysis in Excel and Power BI.  Within the power query, find the OrderID column and set the data type to Whole Number. To complete optimization, assign the following data types for the columns:

- Gross Product Price = Fixed Decimal Number
- Tax Per Product = Fixed Decimal Number
- Quantity Purchased = Whole Number
- Loyalty Points = Whole Number
- Stock = Whole Number
- Product Category = Text
- Rating = Fixed Decimal Number

In the View tab, upon selecting the Column Quality, Column Distribution, and Column Profileboxes, ensure the Valid percentage is 100% for the OrderID column. Select the Gross Product Price column and note down the histogram frequency of distinct and unique values. Select the Quantity Purchased column and note down the MIN, MAX and AVERAGE values displayed on the additional statistical pane. Navigate to the View tab. Select the Column Quality, Column Distribution, and Column Profile checkboxes. Examining column quality, distribution, and profiles helps assess the data's health. It also allows for the early detection of issues, saving time and preventing errors in later stages of the analysis. Validate that the OrderID column achieves a 100% Valid rate, reflecting its data integrity. This confirms that there are no nulls, duplicates, or erroneous entries in this crucial column, which is vital for tracking individual sales accurately.

![data profiling](https://github.com/Emperorian/Comprehensive-Data-Analysis-and-Visualization-Using-Power-BI/assets/101293550/9f816443-52c8-42ed-bcd2-994fe2a4f09f)

Select the Warranty (Months) column and note down the MIN, MAX, and AVERAGE values displayed on the additional statistical pane. Tailwind Traders offers a minimum warranty duration of 6 months, a maximum of 48 months, and an average of 18.88 months. 
Since our aim is to generate the sales and profit overview, we will need the purchases data as well. To do that we are going to load the data below directly to Powerbi desktop from the downloaded Excel file: [purchases](https://d3c33hcgiwev3.cloudfront.net/XaBwJpnHRC6hxfZ79SrnWQ_1ea404989bb745d4bae0bc9a306d28e1_Purchases.xlsx?Expires=1716508800&Signature=BNyY9qjjVBQD772l5uBpivpXz1vuUlhx-U8wC2nUmeucECl6X6bybVltJRylBpu34rdlvOurI9F6enq-nYaa-R0Oj83WWqCOWKWj9xSqq0Dyl-adCqT-TkWkEXE3BHdHLk0gw5Wz3fe7ERUnG5RM5wSRquy-zzQVohxMLYj~vZM_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

### Load the Purchases data

Load the Purchases file into Power BI and select Transform. Select the Purchases data file and then select Load to load it into Power BI. Select Transform Data to access Power Query. To complete optimization, assign the following data types for the columns:

- PurchaseID = Whole Number
- OrderID = Whole Number
- Return Policy (Days) = Whole Number
- Purchase Date = Date
- Warranty (Months) = Whole Number
- Supplier = Text
- Last Visited = Date
- ReturnStatus = Text

  Carefully assign the appropriate data types for each column by selecting the column header and the correct data type from the list. Select the Warranty (Months) column and note down the MIN, MAX, and AVERAGE values displayed on the additional statistical pane.
Tailwind Traders offers a minimum warranty duration of 6 months, a maximum of 48 months, and an average of 18.88 months. Select the ReturnStatus column and observe the Column Quality pane to ensure the Valid percentage is 100%.
Observe the ReturnStatus column and confirm a 100% Valid rate via the Column Quality pane, indicating clean data. This is vital for financial reporting and understanding customer satisfaction. Filter the ReturnStatus column to ensure that only records with Not Returned are visible. Select the ReturnStatus column header to access the filter options. Select Not Returned from the list of filter options to ensure visibility of only those records.

### Load the Countries' data

Load the Countries file into Power BI and select Transform. Load the Countries data file into Power BI.Choose Transform Data to access the data manipulation tools in Power Query. However, your device (PC) must have a pre-installed Python application to run the countries data. If you have difficulty loading the countries' data, first download Python from the internet. For me I used the WINPYTHON64 -3.12.3.0 [download](https://winpython.github.io/) then go to the powerbi desktop and clicked file to option settings to configure the Python setting then Load the Historical currency exchange data, Select Get Data, choose Python script, and then paste the following code into the script window in Power BI

```
import pandas as pd
from io import StringIO

data = """Exchange ID;ExchangeRate;Exchange Currency
1;1;USD
2;0,75;GBP
3;0,85;EUR
4;3,67;AED
5;1,3;AUD"""
df = pd.read_csv(StringIO(data), sep=';')

# Return the transformed dataframe
df
```
This will integrate the data with powerbi platform, Save the Power BI project as Tailwind Traders Report.pbix.
Note: The Python script prepares the currency exchange data for analysis. It transforms the raw string data into a structured format that can be easily integrated with other datasets within Power BI. The core script elements are as follows:
- The pandas data analysis library is used for manipulating and analyzing data.
- StringIO is a module that lets you read and write strings like files.
- pd.read_csv() is a pandas function that reads a CSV file into a DataFrame.

![exchange id](https://github.com/Emperorian/Comprehensive-Data-Analysis-and-Visualization-Using-Power-BI/assets/101293550/a368c56f-c0df-41c4-b8f7-01777a3d7dc0)

To complete optimization, assign the following data types for the columns:
- Country ID = Whole Number
- Exchange ID = Whole Number
- Country = Text
To assign data types, select each column header to open the list of options. Then, select the correct data type from the list.

## Data Modelling

### Design and develop the data model


Designing and developing a data model involves creating a structured framework that defines how data is stored, connected, and accessed in a database system. This process includes identifying entities, attributes, and relationships, ensuring data integrity, and optimizing performance. A well-designed data model serves as a blueprint for efficient data management, supporting accurate analysis and decision-making in applications and businesses.
Open the Tailwind Traders Report.pbix Power BI file you have created in the previous exercise. Access Model View in Power BI to view the report's tables. Your Power BI environment should resemble the screenshot below. Follow the prompts to design and develop a data model from these tables.

![nonrelationship data model](https://github.com/Emperorian/Comprehensive-Data-Analysis-and-Visualization-Using-Power-BI/assets/101293550/1131014f-0d58-4217-b0ef-0a8ee249422e)

We are going to create a relationship between the Countries and Exchange Data tables this will be done with the Exchange ID field. Select the Model view option from the left-hand sidebar to view your data model. Then we set the Cardinality to One to One (1:1). Right-clicking on the relationship that you just created to access the Edit relationship menu. Navigate to the Cardinality options and set the cardinality of this relationship to One to One (1:1). Set the Cross filter direction to Both to be bi-directional. Navigate to the cross-filter direction options and select Both to enable a bi-directional flow.
Create a relationship on the Country ID field between the Sales and Countries tables. Like the previous task, establish a connection on the Country ID field between the Sales and Countries tables to allow for geographical analysis of sales data.

![countries and sales](https://github.com/Emperorian/Comprehensive-Data-Analysis-and-Visualization-Using-Power-BI/assets/101293550/d3aab94a-5ea0-41cd-8e92-aee18f1c2663)

1. Set the Cardinality to Many to One (1:1).
2. Set the Cross-filter direction to Both so that it’s bi-directional.
3. Ensure the Make this relationship active checkbox is selected.
Right-click the relationship, access the Edit relationship menu, and configure the above relationship settings as you did for the tables in the previous task. Inspect the relationship arrow in the Model View to ensure the arrows point in both directions and display a *:1 symbol on either end of the connector. Select OK to apply your settings and return to Model View. Your model should resemble the screenshot below. Inspect the relationship arrow to ensure that it illustrates a bi-directional connection, complete with a *:1 symbol correctly representing the many-to-one relationship inherent in the sales data structure.

#### Create a relationship between the Purchases and Sales tables
Create a relationship on the OrderID field between the Purchases and Sales tables. Create a relationship using the OrderID field as a bridge between the Purchases and Sales tables, linking procurement with sales. Set the Cardinality to One to One (1:1).
1. Set the Cross filter direction to Both to be bi-directional.
2. Ensure the Make this relationship active checkbox is selected.
Right-click the relationship, access the Edit relationship menu, and configure the above relationship settings as you did for the tables in the previous task. Inspect the relationship arrow in the Model View to ensure the arrows point in both directions and display a 1:1 symbol on either end of the connector. Select OK to apply your settings and return to Model View. Your model should resemble the screenshot below. Validate the relationship arrow in the Model View to check that it indicates a bidirectional flow, complete with a 1:1 symbol at both ends, affirming a one-to-one correspondence between each order and its sales outcome.

Through the use of dax (data analysis expression)  a calendar table will be created, Configure the Calendar table, Select New Table and add the following DAX code to create a new Calendar table
```
CalendarTable = 
ADDCOLUMNS(
CALENDAR(DATE(2020, 1, 1), DATE(2023, 12, 31)),
"Year", YEAR([Date]),
"Month Number", MONTH([Date]),
"Month", FORMAT([Date], "MMMM"),
"Quarter", QUARTER([Date]),
"Weekday", WEEKDAY([Date]),
"Day", DAY([Date])
)
```

Select New Table and input the provided DAX code to create a Calendar table, an indispensable tool for any time-based analysis. This table will become the backbone for time intelligence in the model, offering fields like Year, Month Number, Month, Quarter, Weekday, and Day, bringing a rich temporal dimension to the data landscape.

### Create a relationship between the Calendar and Purchasestables
Create a relationship on the Date field between the Calendar and the Purchase Date in the Purchases table. Create a relationship on the Date field that aligns the Calendar table and Purchase Date with Purchases. Set the Cardinality to Many to One (1:1).
Ensure the Make this relationship active checkbox is selected. Right-click the relationship, access the Edit relationship menu, and configure the above relationship settings as you did for the tables in the previous task. Inspect the relationship arrow in the Model View to ensure the arrows point in both directions and display a *:1 symbol on either end of the connector.
Select OK to apply your settings and return to Model View. Your model should resemble the screenshot below. Confirm that the relationship arrow correctly points in both directions and displays a *:1 symbol, validating the many-to-one relationship that connects Purchases to Dates.

### Create Sales in USD Calculated Table
Select New Table and add the following DAX code to create a new calculated table

```
Sales in USD = 
ADDCOLUMNS(
    Sales,
    "Country Name", RELATED(Countries[Country]),
    "Exchange Rate", RELATED('Exchange Data'[Exchange Rate]),
    "Exchange Currency", RELATED('Exchange Data'[Exchange Currency]),
    "Gross Revenue USD", [Gross Revenue] * RELATED('Exchange Data'[Exchange Rate]),
    "Net Revenue USD", [Net Revenue] * RELATED('Exchange Data'[Exchange Rate]),
    "Total Tax USD", [Total Tax] * RELATED('Exchange Data'[Exchange Rate])
)
```

Create a new calculated table named Sales in USD by selecting New Table and entering the DAX code provided. This adjusts the Sales values into a unified currency format. Note the Gross Revenue USD, Net Revenue USD, and Total Tax USD for the Order ID= 1035 on the Sales in USD table.
The Net Revenue for Order ID 1035 placed by Amelia Carter is precisely 682.62 USD. The Gross Revenue USD measures 734 USD, and the Total Tax USD is 51.38 USD. 

### Create a relationship between the Sales in USD and Sales tables
Create a relationship between the Sales in USD and Sales tables on the Order ID field. Link the Sales in USD table with the Sales table by creating a relationship based on the Order ID field, enabling Tailwind Traders to contrast the original sales data with its USD equivalent. Set the Cardinality to Many to One (1:1).
Ensuring the Make this relationship active checkbox is selected. Right-click the relationship, access the Edit relationship menu, and configure the above relationship settings as you did for the tables in the previous task. Your settings should resemble the following screenshot. Ensure the Make this relationship active checkbox is selected to prioritize this relationship as the default linkage for navigating between sales records and their USD counterparts. Inspect the relationship arrow in the Model View to ensure the arrows point in both directions and display a 1:1 symbol on either end of the connector. 
Select OK to apply your settings and return to Model View. Examine the relationship arrow to verify that it correctly illustrates a bi-directional relationship, with a *:1 symbol on either end, confirming the proper relationship structure for USD sales analysis.

![complete relationship](https://github.com/Emperorian/Comprehensive-Data-Analysis-and-Visualization-Using-Power-BI/assets/101293550/65b91fb9-c1a9-47a2-91d0-5d31a832b533)

### Configure aggregations using DAX
Configuring aggregations using Data Analysis Expressions (DAX) involves creating calculated measures to summarize and analyze data in Power BI and other analytics platforms. DAX functions like SUMX, AVERAGEX, and CALCULATE allow users to aggregate data dynamically based on specific criteria or conditions. By leveraging DAX, analysts can efficiently calculate and visualize key metrics to gain valuable insights into their datasets.
Tailwind Traders needs to generate insights into its financial performance to inform its strategic decisions for the upcoming business year. The insights it requires include time-based summaries that display quarterly and annual profits and year-to-date breakdowns. The company also requires its median sales volume to assess its financial performance.

### Calculate Yearly Profit.
For configuring aggregation using Dax, we are going to start with calculating the yearly profit margin.  Calculate Yearly Profit. Create a new measure for the Sales in USD table. Right-click on the Sales in USD table in the Fields pane and select New Column. In the formula bar, create a new column that represents the yearly profit margin. This margin should be derived by dividing the gross revenue by the total net revenue within the Sales in USD table.
Right-click on the Sales in USD table in the Fields pane and select New Column to set the stage for this calculation. Then, input the provided DAX formula into the formula bar.

```
Yearly Profit Margin = 'Sales in USD'[Gross Revenue USD] / 'Sales in USD'[Net Revenue USD]
```
This calculation divides the Gross Revenue by the Net Revenue and shows how much money is kept as profit from sales after costs. This measure provides an overarching view of Tailwind Traders’ financial efficiency throughout the year and is a key indicator of the company's financial health.

### Calculate Quarterly Profit
Create a new measure for quarterly profit. Consider using a function that aggregates data until the end of the current quarter. To achieve this, you must reference the calculated yearly profit and a calendar table. As you did in the previous task, right-click the Sales in USD table in the Fields pane and select New Column. Then, input the provided DAX formula into the formula bar:

```
Quarterly Profit = CALCULATE([Yearly Profit Margin], DATESQTD('CalendarTable'[Date]))
```

This calculation isolates the profit made in each quarter by using a time intelligence function, which filters the profit to each respective quarter. This data provides actionable insights for short-term planning and strategy.

### Calculate Year-to-Date Profit
Right-click on the Sales in USD table in the Fields pane and select New Measure. Create a new measure for the year-to-date profit. You'll need a function aggregating data from the start of the year to the current date.
As you did in the previous task, right-click the Sales in USD table in the Fields pane and select New Column. Then, input the provided DAX formula into the formula bar:
```
YTD Profit = TOTALYTD([Yearly Profit Margin], 'CalendarTable'[Date])
```

This measure accumulates the profit from the first day of the fiscal year to the current date, providing a running total of Tailwind Traders' profitability. This step provides a real-time snapshot of the company’s financial trajectory, allowing for comparison against the same period in previous years or projected targets.

### Calculate Median Sales
Right-click on the Sales in USD table in the Fields pane and choose New Measure. In the formula bar, create a new measure to represent the median sales. Consider the statistical functions in DAX that can help you find the middle value of gross revenue. Right-click on the Sales in USD table and choose New Measure. Input the provided DAX formula into the formula bar.
```
Median Sales = MEDIAN('Sales in USD'[Gross Revenue USD])
```

The median is a statistical measure that indicates the middle value in a set of numbers, which, in this case, represents sales volumes. Using the MEDIAN function on Gross Revenue identifies the sales value at the center of the dataset.

### Access the Performance Analyzer
Find and select the Performance Analyzer option within the View tab. Upon selecting the Report view icon, you must open the Performance Analyzer. Locate and select the View tab on the ribbon interface at the top of your Power BI report. Within the View tab, find and select the Performance Analyzer option. Create an empty Card visual and drag the Yearly Profit Margin field to the Fields well. Repeat this process for the Median Sales, Quarterly Profit, and YTD Profit.
Select the Card icon in the Visualizations pane. An empty Card visual appears on the canvas. Locate the Sales in USD table and drag the Yearly Profit Margin field to the Fields well in the Visualizations pane. Repeat this process for the Median Sales, Quarterly Profit and YTD Profit. Begin recording the performance of the card visuals using the Performance Analyzer’s recording feature. Locate and select the Start Recording button in the Performance Analyzer pane. Refresh your reports to test their performance.

### You can refresh a report using two methods: 
Select the Refresh button in the Home tab of the ribbon interface
or interact directly with the report.
As you interact with the report while the Performance Analyzer is recording, it tracks and documents the time taken to load each visual item. Observe the list of all visual items in your report and their respective load times. Ensure the DAX query time of visual items is < 200ms and note any slow-loading visuals.
Observe the list of all visual items in your report and their respective load times. Ensure the DAX query time of visual items is < 200ms and note down any slow-loading visuals. This step is important not only for data analysis accuracy but also for reports' performance optimization.
Select Stop and remove all Card visuals, resulting in a blank Canvas.
Select Stop and remove all Card visuals upon completion, resulting in a blank Canvas.

![proformance analyser](https://github.com/Emperorian/Comprehensive-Data-Analysis-and-Visualization-Using-Power-BI/assets/101293550/63e946f0-59bb-46f9-90d8-e42792f8fea3)

## Visualization 
Visualization involves representing data graphically to help users understand and interpret complex information. Techniques include charts, graphs, maps, and dashboards, which convert raw data into visual formats like bar charts, line graphs, and scatter plots. Effective visualization highlights patterns, trends, and outliers, making data more accessible and actionable. It aids in decision-making, storytelling, and communicating insights clearly and compellingly, enhancing comprehension and engagement across various audiences.

 ### Create Sales Report
We are going to start with the sales reports, A Power BI report is an interactive data visualization tool that combines charts, graphs, and tables to present insights, enabling users to explore and analyze data effectively.  To create a Sales Overview report,
Open the Tailwind Traders Report.pbix Power BI file. OpenPower BI Desktop and select the File menu in the top left corner. Navigate to the location where your Tailwind Traders Report.pbix file is saved. Select the Tailwind Traders Report.pbix file and select Open in the file explorer window. This action opens the saved project in the Power BI Desktop application. Rename the report Sales Overview.
Create a bar chart for loyalty points by country
Create a clustered bar chart that visualizes loyalty points by country using data from the Sales in USD table. Locate the Visualizations pane on the right-hand side of your screen. Select the Clustered bar chart icon to create an empty bar chart visualization on the canvas.
 Configure the chart as follows:
- Display the country names on the Y-Axis.
- Display the loyalty points on the X-Axis.
- Resize and position the chart to the left side of the canvas.
- Title the chart Loyalty Points by Country.
- Toggle on the data labels.
Drag the Country Name field from the Fields pane to the Y-Axis well in the Visualizations pane. Next, drag the Loyalty Points field from the Fields pane to the X-Axis well in the Visualizations pane. To format this visual, select the Format tab and title the chart Loyalty Points by Country. Note down the country with the highest Loyalty Points value. The UK leads the chart with 315 loyalty points.

![proformance analyser](https://github.com/Emperorian/Comprehensive-Data-Analysis-and-Visualization-Using-Power-BI/assets/101293550/6ea9c96c-8d1a-4ff4-a312-4105e5ca107a)

**Configure the chart as follows:**
- Display the product names on the Y-Axis.
- Display the quantity purchased on the X-Axis.
- Resize and position the chart to the right of the Loyalty Points by Country bar chart.
- Title the chart Quantity Sold by Product.
- Toggle on the data labels.

Locate the Sales in USD table on the right-hand side of the screen. Drag the Product Name field from the Fields pane to the X-Axis well in the Visualizations pane. Next, drag the Quantity Purchased field from the Fields pane to the Y-Axis well in the Visualizations pane.
 Create a pie chart for median sales distribution by country
Create a pie chart that visualizes median sales distribution by country using data from the Sales in USD table.
Select the Pie chart icon from the Visualizations pane to create an empty pie chart visualization on the canvas.

**Configure the chart as follows:**
- Display the country names in the Legend area.
- Display the median sales in the Values area.
- Adjust the chart size and position it below the Loyalty Points by Country bar chart.
- Title the chart Median Sales Distribution by Country.
- Display detailed labels.
Locate the Sales in USD table on the right-hand side of the screen and drag the Country Name field from the Fields pane to the Legend well in the Visualizations pane. Then, drag the Median Sales field from the Fields pane to the Values well in the Visualizations pane.

![visual  tiles](https://github.com/Emperorian/Comprehensive-Data-Analysis-and-Visualization-Using-Power-BI/assets/101293550/34f3f7d7-dc08-4a89-9273-7d6b0eb848ad)

**Create a line chart for median sales over time**
Create a line chart that visualizes median sales over time using data from the Sales in USD table. Select the Line chart icon from the Visualizations pane to create an empty line chart visualization on the canvas.
Configure the chart as follows:
- Display date data on the X-axis.
- Display median sales data on the Y-axis.
- Adjust and position the chart below the Quantity Sold by Product column chart.
- Title the chart Median Sales Over Time.
- Toggle on the data labels.
Locate the Calendar Table on the right-hand side of the screen. Drag the Date field from the Fields pane to the X-Axis well in the Visualizations pane.

![tile 4](https://github.com/Emperorian/Comprehensive-Data-Analysis-and-Visualization-Using-Power-BI/assets/101293550/1d15b8a2-ec9e-4654-9a0d-738cf514b511)

**Configure an analytics forecast as follows:**
Set Units to Days.
Set Forecast Length to 2.
Set the  Confidence interval to 99%.
Select the Analytics tab, represented by a magnifying glass icon. Locate the Forecast option and toggle the switch beside it to add a forecast line to your chart.

**Create cards to visualize your measures**
Create cards that visualize the following measures:
Stock.
Quantity Purchased.
Median Sales.
Select the Card icon in the Visualizations pane while ensuring nothing is selected on the canvas. An empty Card visual appears on the canvas.

**Position the cards as follows:**
Place the Stock and Quantity Purchased cards above the Loyalty Points by Country bar chart.
Place the Median Sales card above the Quantity Sold by Product column chart.
Select the edges of the Stock and Quantity Purchased cards on your canvas to resize them. Place both cards above the Loyalty Points by Country bar chart.

![cards](https://github.com/Emperorian/Comprehensive-Data-Analysis-and-Visualization-Using-Power-BI/assets/101293550/b0d3ee3c-4323-4ca8-871e-76f5dced9d0a)

Add a slicer to the report
Create a slicer that displays the Country Name data from the Sales in USD table. In the Visualizations pane, select the Slicer icon and drag the Country Name field from the Sales in USD table to the Field area.

### Create a Profit report
Create Profit Overview report
Open the Sales Overview report within Power BI. Create a new page in your existing Sales Overview report and name it Profit Overview. To add a new page, select the New Page option. Right-click the new page, select the Rename option, and title the report Profit Overview. Create a bar chart for Net Revenue by Product Create a clustered bar chart that visualizes Net Revenue using data from the Product Sales in USD table. Locate the Visualizations pane on the right-hand side of your screen. Select the Clustered bar chart icon to create an empty bar chart visualization on the canvas.

![profit overview](https://github.com/Emperorian/Comprehensive-Data-Analysis-and-Visualization-Using-Power-BI/assets/101293550/b28c1bfb-1687-411f-a96a-01f6778e181c)

**Configure the chart as follows:**
- Display the Product Name on the Y-Axis.
- Display the Net Revenue USD on the X-Axis.
- Resize and position the chart to the left side of the canvas.
- Title the chart Net Revenue by Product.
- Toggle on the data labels.
Locate the Product Name table on the right-hand side of the screen. Drag the Product Name field from the Fields pane to the Y-Axis well in the Visualizations pane. Next, drag the Net Revenue USD field from the Fields pane to the X-Axis well in the Visualizations pane. To format this visual, select the Format tab and title the chart Net Revenue by Product.
 
Note the product with the highest Net Revenue value. Note the product with the highest Net Revenue value: the Modular Sofa Set at 928.36 USD.

Sort the data in descending order. Select the ellipsis from the top right corner of the chart. Select the Sort Axis dropdown, then select Sort descending.
Create a donut chart for Yearly Profit Margin by Country
Create a donut chart that visualizes Yearly Profit Margin by Country using data from the Product Sales in USD table. Select the Donut chart icon from the Visualizations pane to create an empty donut chart visualization on the canvas. 

**Configure the chart as follows:**
- Display the Country Name in the Legend area.
- Display the Yearly Profit Margin in the Values area.
- Resize and position the chart to the right side of the canvas, next to the Net Revenue by Product chart.
- Title the chart Yearly Profit Margin by Country.
- Enable detailed labels for the Percentage of the total category.
Locate the Sales in USD table on the right-hand side of the screen and drag the Country Name field from the Fields pane to the Legend well in the Visualizations pane. Next, drag the Yearly Profit Margin field from the Fields pane to the Values well in the Visualizations pane.

Create an area chart for Yearly Profit Margin over Time
Create an area chart that visualizes the Yearly Profit Margin over Time. Select the Area Chart icon from the Visualizations pane to create an empty area chart visualization on the canvas.

![profit tiles](https://github.com/Emperorian/Comprehensive-Data-Analysis-and-Visualization-Using-Power-BI/assets/101293550/a0585920-8ba7-4e37-99bd-b5fa311abd2d)

Configure the chart as follows:
- Display the Date on the Y-axis.
- Display the Yearly Profit Margin on the X-axis.
- Resize and position the chart below the Net Revenue by Productbar chart and Yearly Profit Margin by Country Donut chart.
- Title the chart Yearly Profit Margin over Time.
- Toggle on the data labels.
Locate the Calendar Table on the right-hand side of the screen. Drag the Date field from the Fields pane to the X-axis well in the Visualizations pane.

![profit overview 3](https://github.com/Emperorian/Comprehensive-Data-Analysis-and-Visualization-Using-Power-BI/assets/101293550/3df0a564-5268-48a3-88e0-130be3d86884)

Select the Card icon in the Visualizations pane to create a second card visual for Net Revenue USD. Locate the Sales in USD table and drag the Net Revenue USD field to the Fields well in the Visualizations pane. Select the edges of the card on your canvas to resize it. Place it above the Net Revenue by Product bar chart.

**Create a KPI for Gross Revenue USD**
- Create a KPI for Gross Revenue USD.
- Select the KPI icon in the Visualizations pane, ensuring nothing else is selected on the canvas. An empty KPI visual appears on the canvas. Configure the KPI as follows:
- Display the Gross Revenue USD in the value area
- Display the Date in the Trend Axis area.
- Resize and position the KPI next to the Net Revenue USD card.
Locate the Sales in USD table and drag the Gross Revenue USD field to the Value well in the Visualizations pane.

![profit overview 4](https://github.com/Emperorian/Comprehensive-Data-Analysis-and-Visualization-Using-Power-BI/assets/101293550/f06d412e-861a-4f9e-afed-21ba90880028)

Save and publish your report.
Select File in the top-left corner of the Power BI Desktop interface, and then Save to save the report. In the dialog box, indicate where to save the report. Select My Workspace as your workspace and then the Select button.
![power bi service](https://github.com/Emperorian/Comprehensive-Data-Analysis-and-Visualization-Using-Power-BI/assets/101293550/bb2d8ade-31a0-4d33-854c-00f63dc7e907)

Once the destination is selected, Power BI publishes the report. Depending on the size of the report and your internet connection, this process could take a few moments. Once the report is published, a new window appears to confirm successful publication. It provides two options: 
Open the report in Power BI Service
Or Cancel and open it later.
In this case, select Open to launch the default web browser on your computer and view your report in Power BI service.

![power bi upload](https://github.com/Emperorian/Comprehensive-Data-Analysis-and-Visualization-Using-Power-BI/assets/101293550/84d9414b-ef5a-4125-b3a6-afb60b6b642c)

### Create an executive dashboard


**Create a new dashboard**
Navigate to your workspace and create a new dashboard called Tailwind Traders Executive Dashboard. In the Navigation view of My Workspace, locate and select the + New button on the top left corner of the screen.
![power bi workspace](https://github.com/Emperorian/Comprehensive-Data-Analysis-and-Visualization-Using-Power-BI/assets/101293550/0be5122a-8b2a-4bdf-a66e-555341ac67c6)

Select Dashboard from the list of options. A pop-up window titled Create a dashboard appears. Type Tailwind Traders Executive Dashboard in the Name field. Select Create. This action creates a new dashboard shell to which you can add content. Step 


Pin Sales Overview core visualizations
Navigate to your Workspace and access the Sales Overview tab of the Tailwind Traders Report. On the left side of your Power BI service screen, locate and select Workspaces > My Workspace again. Navigate to the Tailwind Traders Report in the list of reports within the workspace. Select the report’s Sales Overview tab. Within this tab, locate and select the pin icon on the Loyalty Points by Country bar chart. A Pin to dashboard dialog box appears onscreen. Select the Tailwind Traders Executive Dashboard and select Pin to confirm your choice.



Repeat this action for the following charts:
Quantity Sold by Product column chart.
Median Sales Distribution by Country pie chart.
Media Sales Over Time line chart.


Pin the Sales Overview card visualizations
Locate and pin the following Sales Overview card visualizations to the Tailwind Traders dashboard:
Sum of Stock card
Sum of Quantity Purchasedcard
Median sales card
Select the pin icon on the Sum of Stock card.


Pin the card to the Tailwind Traders Executive Dashboard.
Repeat this process for the Sum of Quantity Purchased card.
Repeat this process once again for the Median Sales card.




**Pin the Profit Overview core visualizations**
Select the Profit Overview tab. Select the Profit Overview tab from the Tailwind Traders Report. Locate and pin the following Profit Overview core visualization to the Tailwind Traders Executive Dashboard:
Net Revenue by Product bar chart
Yearly Profit Margin by Country donut chart
Year Profit Margin over Time area chart
Select the pin icon on the Net Revenue by Productbar chart and pin the visualization to the Tailwind Traders Executive Dashboard.

Repeat this process for the Yearly Profit Margin by Country donut chart.

Repeat the process for the Year profit Margin Over Time area chart.

Note the product with the highest value in the Net Revenue by Product bar chart.
The Modular Sofa Set has the highest Sum of Net Revenue USD, which is precisely 928.36.

**Pin Profit Overview Card and KPI Visualizations**
Locate and pin the following items to the Tailwind Traders Executive Dashboard:
YTD Profit card
- Sum of Net Revenue USD card
- Sum of Gross Revenue USD KPI
- Select and pin the YTD Profit Card to the Tailwind Traders Executive Dashboard.
- Repeat these actions for the Sum of Net Revenue USD Card.
- Repeat these actions for the Sum of Gross Revenue USD KPI.

Configure the Mobile View for the cards and KPI visuals
Locate and select the Tailwind Traders Executive Dashboard from the Dashboards list.
Select Workspaces, then My Workspace. Select the Tailwind Traders Executive Dashboard from the list of dashboards within the workspace.

![dashboard](https://github.com/Emperorian/Comprehensive-Data-Analysis-and-Visualization-Using-Power-BI/assets/101293550/b15804f3-56df-4c4a-bfed-30c298893d90)

Select Mobile Layout from the Edit menu and pin your card visuals to the dashboard in the following order:
- Sum of Net Revenue USD to the left and Sum of Quantity Purchased cards to the right.
- Median Sales to the left and YTD Profit cards to the right.
- Sum of Gross Revenue USD KPI across the full width of the layout
Select Edit from the main navigation bar. Select Mobile layout from the list of options to switch the view from desktop to mobile

### Mobile layout

Once you select the Mobile layout, your screen adjusts to a vertical layout to replicate a mobile device's screen size. This canvas is blank. You must decide which visuals to show on the mobile layout and where to place them. A list of all the visualizations in your dashboard is displayed on the right side of your screen. Each visualization has a pin icon next to it. 

![mobile layout](https://github.com/Emperorian/Comprehensive-Data-Analysis-and-Visualization-Using-Power-BI/assets/101293550/7cabadf3-37f3-47ae-8cd6-a812bd9642ce)

Select the Pin icon for the Sum of Net Revenue USD and the Sum of Quantity Purchased cards. Arrange the card visuals on the mobile canvas side-by-side for a balanced look.

Repeat this process for the Median Sales Card and YTD Profit Card. Finally, pin the Sum of Gross Revenue USD KPI so that it’s the full width of the layout of the mobile canvas.
Configure the Mobile View for the core visualizations
Configure the mobile view for the core visualizations by pinning the Sales Overview visualizations in the following order:
Loyalty Points by Country bar chart
Quantity Sold by Product column chart
Median Sales Distribution by Country pie chart
Median Sales over Time line chart
Select the Pin icon for the Loyalty Points by Country bar chart to pin it to the mobile view. Repeat this process for the Quantity Sold by Product column chart.

Pin the following Profit Overview visualizations in the following order:
Net Revenue by Product bar chart
Yearly Profit Margin by Country donut chart
Yearly Profit Margin over Time area chart
Select the Pin icons for the Net Revenue by Product bar chart and Yearly Profit Margin by Country bar chart.

![mobile layout 2](https://github.com/Emperorian/Comprehensive-Data-Analysis-and-Visualization-Using-Power-BI/assets/101293550/997cd2a8-d97c-4546-96ad-fdc8e91a366a)

## Configuring alerts and subscriptions

Configuring alerts and subscriptions in Power BI enables users to stay informed about important data changes and updates. Alerts can be set on specific metrics to notify users when thresholds are met. Subscriptions allow users to receive regular updates via email, ensuring they stay current with report changes. These features enhance proactive monitoring and timely decision-making, improving overall data management and responsiveness.

### Create a daily alert for Gross Revenue USD
Access the Mange Alerts menu for the Sum of Gross Revenue USD KPI tile.
On the Tailwind Traders Executive Dashboard, locate the Sum of Gross Revenue USD KPI tile and select the ellipses icon.

Select Manage Alerts from the list of options that appear.

![manage alert](https://github.com/Emperorian/Comprehensive-Data-Analysis-and-Visualization-Using-Power-BI/assets/101293550/9c8723c7-407e-4296-b8ff-b0e9adc439ec)

Create a new alert titled Gross Revenue USD below $400 with the following configurations:
In the Condition section, set the threshold at $400.
Set a frequency of at most every 24 hours.
Within the Manage alerts screen, locate and select the + New alert rule.
Enter Gross Revenue USD below $400 in the Alert title field.
In the Condition section, locate the dropdown menu and select Below. In the adjacent field, type in 400 to set the threshold at $400.Navigate to the Frequency section to decide how often Power BI checks this condition. For critical metrics, like Sum of Gross Revenue USD that might require daily checks, selecting the At most every 24 hours setting is appropriate.
Save and close the alert. Once you’ve set all required parameters, select Save and close to save your alert settings and activate the alert rule. 

### Create a subscription for Sales Overview
Access the report’s Sales Overview tab.
Locate and select Workspaces, then My Workspace. Find and select the Tailwind Traders Report in the list of reports within the workspace. Access the Median Sales Distribution by Country pie chart and note down the country with the highest Median Sales value.
Select the Median Sales Distribution by Country pie chart from the canvas. UAE is the country with the highest Median Sales, measuring 680.785 USD. Create a subscription for the Sales Overview report with the following configurations:
Select the ellipses next to the Edit button. Select Subscribe from the list of options that appear. This action opens the Subscription pane. Name your subscription Sales Weekly Summary. Set the Start date to the current date and the End date to 12/31/2025. For the frequency, select Weekly and select Monday. Set the Scheduled time to 5:00 AM.

![manage alert 2](https://github.com/Emperorian/Comprehensive-Data-Analysis-and-Visualization-Using-Power-BI/assets/101293550/904ca038-a073-4127-a731-ce8a3316abbd)

Access the Sales Overview report page in the Report page dropdown and ensure that the toggle switches for the following options are activated:
Permission to view the report in Power BI
Link to report in Power BI
Report page preview
Expand More options to view the Report page dropdown. Select the Sales Overview report page from the dropdown. Check that the toggle for each of the following options is activated:
Permission to view the report in Power BI
Link to report in Power BI
Report page preview
Activate the subscription.
Select Save to activate the Sales Overview subscription. You’ll receive a message confirming your subscription is now active.

**Create a subscription for Profit Overview**
Access the report’s Profit Overview tab.
Navigate to the Profit Overview tab and access the Subscribe to Report option.

**Create a subscription to the report with the following configurations:**
Name the subscription Profit Weekly Summary.
- Set the Start date to the current date and the End date to 12/31/2025.
- Set the frequency to Weekly and select Monday, Wednesday and Friday as the days of the week.
- Set the Scheduled time to 6:00 AM.
Name your report Profit Weekly Summary. Set the Start date to the current date and the End date to 12/31/2025. Select Weekly as your frequency, and select Monday, Wednesday, and Friday as the days of the week.

![manage alert 3](https://github.com/Emperorian/Comprehensive-Data-Analysis-and-Visualization-Using-Power-BI/assets/101293550/870194fc-1fca-4e69-8d8e-dc516c511189)

Set the Scheduled time to 6:00 AM.

Access the Profit Overview report page in the Report page dropdown and ensure that the toggle switches for the following options are switched on:
Permission to view the report in Power BI
Link to report in Power BI
Report page preview
Expand More options and select the Profit Overview report page in the Report page dropdown. Ensure that the toggle switches for the following options are switched on:
Permission to view the report in Power BI
Link to report in Power BI
Report page preview

**Activate the subscription.**

Select Save to activate the Profit Overview subscription.

![activate](https://github.com/Emperorian/Comprehensive-Data-Analysis-and-Visualization-Using-Power-BI/assets/101293550/cf049562-d8ab-4876-8198-2b2524303c70)

## links to the [POWER BI SERVICE- TAILWIND TRADERS](https://app.powerbi.com/links/RwRcHUdXtX?ctid=e715188b-7518-450d-a2c1-88ffafc16119&pbi_source=linkShare)  

## Conclusion
We finally created a sales and profit overview for the Tailwind Traders which includes a comprehension dashboard, report for sale, and profit for the period requested. In case some the stakeholders are not available, a mobile visualization, which hey can access through there mobile device for easy accessibility. Other features like the subscription and alert were also added to keep in check the activities of the company from time to time. 




