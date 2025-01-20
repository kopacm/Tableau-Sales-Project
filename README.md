# Tableau-Sales-Project
 

![amazon](/amazon_images.png)

  

## 📚 Table of Contents

- [Project Overview](#project-overview)

- [Objective](#objective)

- [Procedure](#procedure)


  

## **Project Overview**

This user story outlines the specifications for building two dashboards using tableau to help stakeholders, including sales managers and executives to analyze sales performance and customers.

  
## **User Requirements**

### Sales Dashboard | Requirements

#### Dashboard Purpose

The purpose of sales dashboard is to present an overview of the sales metrics and trends in order to analyze year-over-year sales performance and understand sales trends.

#### Key Requirements

##### KPI Overview

Display a summary of total sales, profits and quantity for the current year and the previous year.

##### Sales Trends

 – Present the data for each KPI on a monthly basis for both the current year and the previous year.

 – Identify months with highest and lowest sales and make them easy to recognize.

##### Product Subcategory Comparison

 – Compare sales performance by different product subcategories for the current year and the previous year.

 – Include a comparison of sales with profit.

##### Weekly Trends for Sales & Profit

 – Present weekly sales and profit data for the current year.

 – Display the average weekly values.

 – Highlight weeks that are above and below the average to draw attention to sales & profit performance.

### Customer Dashboard | Requirements

#### Dashboard Purpose

The customer dashboard aims to provide an overview of customer data, trends and behaviors. It will help marketing teams and management to understand customer segments and improve customer satisfaction.

#### Key Requirements

##### KPI Overview

Display a summary of total number of customers , total sales per customer and total number of orders for the current year and the previous year.

##### Customer Trends

 – Present the data for each KPI on a monthly basis for both the current year and the previous year.

 – Identify months with highest and lowest sales and make them easy to recognize.

##### Customer Distribution by Number of Orders

Represent the distribution of customers based on the number of orders they have placed to provide insights into customer behavior, loyalty and engagement.

##### Top 10 Customers By Profit

 – Present the top 10 customers who have generated the highest profits for the company.

 – Show additional information like rank, number of orders, current sales, current profit and the last order date.

### Design & Interactivity Requirements

##### Dashboard Dynamic

 – The Dashboard should allow users to check historical data by offering them the flexibility to select any desired year.

 – Provide users with the ability to navigate between the dashboards easily.

 – Make the charts and graphs interactive, enabling users to filter data using the charts.

##### Data Filters

Allow users to filter data by product information like category and subcategory and by location information like region, state and city.

## **Objective**

  Learn Dashboard Design process in Tableau by using specific framework. 


  

## **Procedure**


![image](/images/20250120121612.png)
1. STEP 1 - Analyse Requirements
	- Collect Requirements
	- Choose Right Chart
	- Draw Mockups
	- Choose Colors
2. STEP 2 - Build Data Source
	- Connect Data
	- Create Data Model
	- Rename Fields & Tables 
	- Check Data Types
	- Understand Data
3. STEP 3 - Build Charts
	- If we don't have all the data we need to create calculated fields & Test
	- Build Chart
	- Format 
		  - Remove Lines and grids
		  - Clean up Axis and Headers
		  - Coloring
		  - Tooltips
4. STEP 4 - Build Dashboard
	- Draw Mockup for Containers
	- Create Container Structure
	- Put All Charts Together
	- Format
		  - Distribute Object Evenly
		  - Format Colors, size... etc
		  - Fit "Entire View"
		  - Add Legends
		  - Add Spaces (inner/outer Padding)
	- Add Filters & Dynamic
	- Add Icons

### STEP 1 - Analyze Requirements

<details>
    <summary>Collect Requirements</summary>

    #### Collect Requirements 

    - [Tableau User Story Requirements](#user-requirements)
</details>

<details>
    <summary>Choose Right Chart</summary>

    #### Choose Right Chart

    I analyzed requirements and chose what chart I will use  

    Example: 

    ```
    KPI Overview

    - Display a summary of total sales, profits and quantity for the current year and the previous year
    ```

    > CHART: Numeric chart, BANS chart good for showing whole numbers
</details>

<details>
    <summary>Draw Mockups</summary>

    #### Draw Mockups

    ![image](/images/20250120121719.png)
    ![image](/images/20250120121745.png)
</details>

<details>
    <summary>Choose Colors</summary>

    #### Choose Colors

    **Choosing colors** at **start** of a project is important. Early selection of colors helps maintain **consistency** throughout the project

    **Maximum of 4 Colors**
    - 2 Basic Colors example: White background - #303030 dark gray & #b3b3b3 light gray 
    - 2 Custom Colors: User preferences/Logo color in this case #ff5500 orange #1da2d0 light blue
</details>

#### Connect Data

Opened new file and connect text file .csv
#### Create Data Model

Always start with the FACT table to build the data model
FACT table is table where are ID, dates, measures in my case is it orders.csv 
rest are dimensions 

![image](/images/20250114144836.png)
I need to make sure that connection are right in this case Order and Products tables are connected with Product ID 


#### Rename Fields & Tables 

In my case in changed Location.csv to Location so it's clean.

#### Check Data Types

Incorrect dat types can result in inaccurate visualizations 
Made sure that dates and measures in FACTS are not String data type 
#### Understand Data

Understanding the data is important to understand the business and build correct visualization 

### STEP 3 - Build Charts

#### If we don't have all the data we need to - Create calculated fields & Test them

- Display a summary of total sales, profits and quantity for the current year (CY Sales) and the previous year (PY Sales)
- The Dashboard should allow users to check historical data by offering them the flexibility to select any desired year
Sales for year 2023:
 New created field CY Sales, PY Sales:

![image](/images/20250114151226.png)


![image](/images/20250114151330.png)

For dynamic purpose I can use parameters in Tableau in order to be able to use it I needed to have years of order years in field which I named Order date (Year) 
![image](/images/20250114151138.png)
Created parameter "Select Year" 
![image](/images/20250114152255.png)

![image](/images/20250114152454.png)

Now in order to make it dynamic I need to change fields CY Sales and PY Sales 
```
IF YEAR([Order Date])= 2023 THEN [Sales]
END
```
to 
```
IF YEAR([Order Date])= [Select Year] THEN [Sales]
END
```
And PY Pales
to 
```
IF YEAR([Order Date])= [Select Year]-1 THEN [Sales]
END
```

#### Build Chart

##### Created BAN 

![image](/images/20250114153846.png)
Adjust formatting 
![image](/images/20250114154443.png)

In order to create clear indicator I used easy custom formatting ▲ 0.00%; ▼ -0.00%; which will show  ▲  in a case of positive number and ▼ negative number

![image](/images/20250114154613.png)

Sparkline 

to be able to compare two graph on each other I dragged PY Sales to CY Sales on Y-Axis 

![image](/images/20250114155648.png)


Next I needed to highlight lowest and highest value for that I needed new calculated field 
Min/Max Sales
```
IF SUM([CY Sales]) = WINDOW_MAX(SUM([CY Sales])) //WINDOW_MAX - max value in current window
THEN SUM([CY Sales])
ELSEIF SUM([CY Sales]) = WINDOW_MIN(SUM([CY Sales]))
THEN SUM([CY Sales])
END
```

Then I used this new calculated field in a row and to be able to show it in one graph I had to chose Dual Axis 
![image](/images/20250115095915.png)

I fixed this range which was caused by continuous graph by changing SUM values to "{}" brackets 

![image](/images/20250115100641.png)

![image](/images/20250115100930.png)

 Format 
  I Removed all Lines and grids  and cleaned up Axis and Headers because Minimalism is the key. Excessive Info on dashboard can distract users from the important data 
I left only X-Axis where instead of the numbers of month I made sure it's obvious what values are there even without Axis Title by showing moths abbreviation
![image](/images/20250115101914.png)

Instead of showing all months on Axis 
![image](/images/20250115102208.png)
I made it minimalist by showing only Jan and Dec so everyone who will look at it can see that it's from Jan to Dec. 
![image](/images/20250115103050.png)
![image](/images/20250115103208.png)


#### Coloring

I used colors mentioned above dark gray for CY Sales and light gray for PY Sales
To change color of MIN/MAX Sales I dragged "Min/Max Sales" from Rows by holding Ctrl on Colour

For MAX #1da2d0 and #ff5500 for MIN 

Tooltips 
Info showed while hovering on graph line

I create new calculated field Current Year and Previous year based on [Select Year]
![image](/images/20250115112033.png)
I formatted Tooltip so it showing clearly what I what to show
![image](/images/20250115112926.png)



Create Bar Chart


**When you merging two charts together don't forget to synchronize Axis !** 
![image](/images/20250116093006.png)

To be able easily identify in which subcategory KPI was worst than previous year I added icon 
![image](/images/20250116094056.png)
for that I created calculated field which compares CY Sales KPI with PY Sales result:
![image](/images/20250116094614.png)

For better overview I sorted subcategories based on CY sales
![image](/images/20250116094857.png)

#### Weekly Trends for Sales & Profit

 – Present weekly sales and profit data for the current year.

 – Display the average weekly values

 – Highlight weeks that are above and below the average to draw attention to sales & profit performance.

LINE Chart 


Weekly sales and profit data graph:
![image](/images/20250116100357.png)
To display average values I added reference line   
![image](/images/20250116100555.png)

For different coloring above and under I created calculated field with function WINDOW_AVG instead of AVG for reason that I only needed to reference to this year not all of them
```
IF SUM([CY Sales]) > WINDOW_AVG(SUM([CY Sales])) THEN 'Above'
ELSE 'Below'
END
```
![image](/images/20250116101859.png)

### STEP 4 - Build Dashboard


- Draw Mockup for Containers
- Create Container Structure
- Put All Charts Together
- Format
  - Distribute Object Evenly
  - Format Colors, size... etc
  - Fit "Entire View"
  - Add Legends
  - Add Spaces (inner/outer Padding)
- Add Filters & Dynamic
- Add Icons


Create Container Structure
I usually use fixed size of Dashboard 1200x800 px 
I'm starting with floating containers before tiled ones. By holding SHIFT and dragging it inside I created floating container 
![image](/images/20250116104420.png)

Then I created tiled main vertical container with horizontal containers in it. I used blank fields to see my structure first 
![image](/images/20250116110938.png)

Put All Charts Together
![image](/images/20250116111357.png)

Format

Distribute Object Evenly
![image](/images/20250116111334.png)

Outer padding 10 Inner padding 10

Filter Apply to all using this Data Source and then select in each graph which filter you want to be shown
![image](/images/20250116121851.png)

Number of Orders per Customer
`{FIXED [CY Customers Nr.]: COUNTD([CY Orders])}`
`{FIXED [CY Customers Nr.]:` all the customers who ordered this year then the aggregation `COUNTD([CY Orders])` number of orders

## **Final Dashboard Design**

![image](/images/20250120124311.png)

![image](/images/20250120124332.png)

![image](/images/20250120124400.png)

  
## **What I learned**
