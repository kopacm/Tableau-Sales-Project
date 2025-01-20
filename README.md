# Tableau-Sales-Project
 

![tableau](/images/Tableau.png){: width="600" height="400"}

  
## 📚 Table of Contents

- [Project Overview](#project-overview)
- [Objective](#objective)
- [User Requirements](#user-requirements)
- [Procedure](#procedure)
    - [STEP 1 - Analyze Requirements](#step-1---analyze-requirements)
        - [Collect Requirements](#collect-requirements)
        - [Choose Right Chart](#choose-right-chart)
        - [Draw Mockups](#draw-mockups)
        - [Choose Colors](#choose-colors)
    - [STEP 2 - Build Data Source](#step-2---build-data-source)
        - [Connect Data](#connect-data)
        - [Create Data Model](#create-data-model)
        - [Rename Fields & Tables](#rename-fields--tables)
        - [Check Data Types](#check-data-types)
        - [Understand Data](#understand-data)
    - [STEP 3 - Build Charts](#step-3---build-charts)
        - [Create Calculated Fields & Test Them](#create-calculated-fields--test-them)
        - [Build Chart](#build-chart)
    - [STEP 4 - Build Dashboard](#step-4---build-dashboard)
        - [Create Container Structure](#create-container-structure)
        - [Put All Charts Together](#put-all-charts-together)
        - [Format](#format)
        - [Filter](#filter)
- [Final Dashboard Design](#final-dashboard-design)
- [What have I learned](#what-have-i-learned)


  

## **Project Overview**

This user story outlines the specifications for building two dashboards using tableau to help stakeholders, including sales managers and executives to analyze sales performance and customers.
## **Objective**

Learn Dashboard Design process in Tableau by using specific framework. 
<font color="blue">**This project was only created for design purpose not for presenting project**</font>
  
## **User Requirements**

### Sales Dashboard | Requirements

#### Dashboard Purpose

The purpose of sales dashboard is to present an overview of the sales metrics and trends in order to analyze year-over-year sales performance and understand sales trends.


<details>
<summary><h4>Key Requirements</h4></summary>

<h5>KPI Overview</h5>
<p>Display a summary of total sales, profits and quantity for the current year and the previous year.</p>

<h5>Sales Trends</h5>
<ul>
    <li>Present the data for each KPI on a monthly basis for both the current year and the previous year.</li>
    <li>Identify months with highest and lowest sales and make them easy to recognize.</li>
</ul>

<h5>Product Subcategory Comparison</h5>
<ul>
    <li>Compare sales performance by different product subcategories for the current year and the previous year.</li>
    <li>Include a comparison of sales with profit.</li>
</ul>

<h5>Weekly Trends for Sales & Profit</h5>
<ul>
    <li>Present weekly sales and profit data for the current year.</li>
    <li>Display the average weekly values.</li>
    <li>Highlight weeks that are above and below the average to draw attention to sales & profit performance.</li>
</ul>
</details>


<h3>Customer Dashboard | Requirements</h3>

<h4>Dashboard Purpose</h4>
<p>The customer dashboard aims to provide an overview of customer data, trends and behaviors. It will help marketing teams and management to understand customer segments and improve customer satisfaction.</p>

<details>
<summary><h4>Key Requirements</h4></summary>

<h5>KPI Overview</h5>
<p>Display a summary of total number of customers, total sales per customer and total number of orders for the current year and the previous year.</p>

<h5>Customer Trends</h5>
<ul>
    <li>Present the data for each KPI on a monthly basis for both the current year and the previous year.</li>
    <li>Identify months with highest and lowest sales and make them easy to recognize.</li>
</ul>

<h5>Customer Distribution by Number of Orders</h5>
<p>Represent the distribution of customers based on the number of orders they have placed to provide insights into customer behavior, loyalty and engagement.</p>

<h5>Top 10 Customers By Profit</h5>
<ul>
    <li>Present the top 10 customers who have generated the highest profits for the company.</li>
    <li>Show additional information like rank, number of orders, current sales, current profit and the last order date.</li>
</ul>

<h3>Design & Interactivity Requirements</h3>

<h5>Dashboard Dynamic</h5>
<ul>
    <li>The Dashboard should allow users to check historical data by offering them the flexibility to select any desired year.</li>
    <li>Provide users with the ability to navigate between the dashboards easily.</li>
    <li>Make the charts and graphs interactive, enabling users to filter data using the charts.</li>
</ul>

<h5>Data Filters</h5>
<p>Allow users to filter data by product information like category and subcategory and by location information like region, state and city.</p>

</details>



  

## **Procedure**


![image](/images/20250120121612.png)

## Framework for this project

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

My approach and notes:

<details>
<summary><h4>Collect Requirements</h4></summary>
<ul>
    <li><a href="#user-requirements">Tableau User Story Requirements</a></li>
</ul>
</details>

<details>
<summary><h4>Choose Right Chart</h4></summary>
<p>I analyzed requirements and chose what chart I will use</p>
<p>Example:</p>
<pre>
KPI Overview

- Display a summary of total sales, profits and quantity for the current year and the previous year
</pre>
<blockquote>CHART: Numeric chart, BANS chart good for showing whole numbers</blockquote>
</details>

<details>
<summary><h4>Draw Mockups</h4></summary>
<img src="/images/20250120121719.png" alt="Mockup 1">
<img src="/images/20250120121745.png" alt="Mockup 2">
</details>

<details>
<summary><h4>Choose Colors</h4></summary>
<p><strong>Choosing colors</strong> at <strong>start</strong> of a project is important. Early selection of colors helps maintain <strong>consistency</strong> throughout the project</p>
<p><strong>Maximum of 4 Colors</strong></p>
<ul>
    <li>2 Basic Colors example: White background - #303030 dark gray & #b3b3b3 light gray</li>
    <li>2 Custom Colors: User preferences/Logo color in this case #ff5500 orange #1da2d0 light blue</li>
</ul>
</details>

### STEP 2 - Build Data Source

My approach and notes:

<details>
<summary><h4>Connect Data</h4></summary>
<p>Opened new file and connect text file .csv</p>
</details>

<details>
<summary><h4>Create Data Model</h4></summary>
<p>Always start with the FACT table to build the data model. FACT table is the table where there are ID, dates, measures; in my case, it is orders.csv. The rest are dimensions.</p>
<img src="/images/20250114144836.png" alt="Data Model">
<p>I need to make sure that connections are right; in this case, Order and Products tables are connected with Product ID.</p>
</details>

<details>
<summary><h4>Rename Fields & Tables</h4></summary>
<p>In my case, I changed Location.csv to Location so it's clean.</p>
</details>

<details>
<summary><h4>Check Data Types</h4></summary>
<p>Incorrect data types can result in inaccurate visualizations. Made sure that dates and measures in FACTS are not String data type.</p>
</details>

<details>
<summary><h4>Understand Data</h4></summary>
<p>Understanding the data is important to understand the business and build correct visualization.</p>
</details>

### STEP 3 - Build Charts

My approach and notes:

<details>
<summary><h4>Create Calculated Fields & Test Them</h4></summary>

<p>Display a summary of total sales, profits and quantity for the current year (CY Sales) and the previous year (PY Sales)</p>
<p>The Dashboard should allow users to check historical data by offering them the flexibility to select any desired year</p>

<p>Sales for year 2023:</p>
<p>New created field CY Sales, PY Sales:</p>

<img src="/images/20250114151226.png" alt="CY Sales">

<img src="/images/20250114151330.png" alt="PY Sales">

<p>For dynamic purpose, I can use parameters in Tableau. In order to use it, I needed to have years of order years in a field which I named Order date (Year)</p>
<img src="/images/20250114151138.png" alt="Order Date (Year)">
<p>Created parameter "Select Year"</p>
<img src="/images/20250114152255.png" alt="Select Year Parameter">

<img src="/images/20250114152454.png" alt="Select Year Parameter Configuration">

<p>Now, in order to make it dynamic, I need to change fields CY Sales and PY Sales</p>
<pre>
<code>
IF YEAR([Order Date])= 2023 THEN [Sales]
END
</code>
</pre>
<p>to</p>
<pre>
<code>
IF YEAR([Order Date])= [Select Year] THEN [Sales]
END
</code>
</pre>
<p>And PY Sales to</p>
<pre>
<code>
IF YEAR([Order Date])= [Select Year]-1 THEN [Sales]
END
</code>
</pre>
</details>

<details>
<summary><h4>Build Chart</h4></summary>

<h5>Created BAN</h5>
<img src="/images/20250114153846.png" alt="BAN Chart">
<p>Adjust formatting</p>
<img src="/images/20250114154443.png" alt="BAN Chart Formatting">

<p>In order to create a clear indicator, I used easy custom formatting ▲ 0.00%; ▼ -0.00%; which will show ▲ in a case of positive number and ▼ negative number</p>
<img src="/images/20250114154613.png" alt="Custom Formatting">

<h5>Sparkline</h5>
<p>To be able to compare two graphs on each other, I dragged PY Sales to CY Sales on Y-Axis</p>
<img src="/images/20250114155648.png" alt="Sparkline">

<p>Next, I needed to highlight the lowest and highest value. For that, I needed a new calculated field Min/Max Sales</p>
<pre>
<code>
IF SUM([CY Sales]) = WINDOW_MAX(SUM([CY Sales])) //WINDOW_MAX - max value in current window
THEN SUM([CY Sales])
ELSEIF SUM([CY Sales]) = WINDOW_MIN(SUM([CY Sales]))
THEN SUM([CY Sales])
END
</code>
</pre>

<p>Then I used this new calculated field in a row and to be able to show it in one graph, I had to choose Dual Axis</p>
<img src="/images/20250115095915.png" alt="Dual Axis">

<p>I fixed this range which was caused by continuous graph by changing SUM values to "{}" brackets</p>
<img src="/images/20250115100641.png" alt="Fixed Range">

<img src="/images/20250115100930.png" alt="Fixed Range">

<h5>Format</h5>
<p>I removed all lines and grids and cleaned up Axis and Headers because minimalism is the key. Excessive info on the dashboard can distract users from the important data</p>
<p>I left only X-Axis where instead of the numbers of the month, I made sure it's obvious what values are there even without Axis Title by showing months abbreviation</p>
<img src="/images/20250115101914.png" alt="Minimalist Axis">

<p>Instead of showing all months on Axis</p>
<img src="/images/20250115102208.png" alt="All Months Axis">
<p>I made it minimalist by showing only Jan and Dec so everyone who will look at it can see that it's from Jan to Dec</p>
<img src="/images/20250115103050.png" alt="Minimalist Axis Jan-Dec">
<img src="/images/20250115103208.png" alt="Minimalist Axis Jan-Dec">

<h5>Coloring</h5>
<p>I used colors mentioned above: dark gray for CY Sales and light gray for PY Sales. To change the color of MIN/MAX Sales, I dragged "Min/Max Sales" from Rows by holding Ctrl on Colour</p>
<p>For MAX #1da2d0 and #ff5500 for MIN</p>

<h5>Tooltips</h5>
<p>Info showed while hovering on graph line</p>
<p>I created a new calculated field Current Year and Previous year based on [Select Year]</p>
<img src="/images/20250115112033.png" alt="Calculated Field">
<p>I formatted Tooltip so it shows clearly what I want to show</p>
<img src="/images/20250115112926.png" alt="Formatted Tooltip">

<h5>Create Bar Chart</h5>
<p>**When you merge two charts together, don't forget to synchronize Axis!**</p>
<img src="/images/20250116093006.png" alt="Synchronized Axis">

<p>To be able to easily identify in which subcategory KPI was worse than the previous year, I added an icon</p>
<img src="/images/20250116094056.png" alt="Icon">
<p>For that, I created a calculated field which compares CY Sales KPI with PY Sales result:</p>
<img src="/images/20250116094614.png" alt="Calculated Field">

<p>For better overview, I sorted subcategories based on CY sales</p>
<img src="/images/20250116094857.png" alt="Sorted Subcategories">

<h5>Weekly Trends for Sales & Profit</h5>
<p>Present weekly sales and profit data for the current year.</p>
<p>Display the average weekly values</p>
<p>Highlight weeks that are above and below the average to draw attention to sales & profit performance.</p>

<h5>Line Chart</h5>
<p>Weekly sales and profit data graph:</p>
<img src="/images/20250116100357.png" alt="Weekly Sales and Profit Data">
<p>To display average values, I added a reference line</p>
<img src="/images/20250116100555.png" alt="Reference Line">

<p>For different coloring above and under, I created a calculated field with function WINDOW_AVG instead of AVG for the reason that I only needed to reference to this year, not all of them</p>
<pre>
<code>
IF SUM([CY Sales]) > WINDOW_AVG(SUM([CY Sales])) THEN 'Above'
ELSE 'Below'
END
</code>
</pre>
<img src="/images/20250116101859.png" alt="Calculated Field">
</details>

### STEP 4 - Build Dashboard

My approach and notes:

<details>
<summary><h4>Create Container Structure</h4></summary>
<p>I usually use a fixed size of Dashboard 1200x800 px. I'm starting with floating containers before tiled ones. By holding SHIFT and dragging it inside, I created a floating container.</p>
<img src="/images/20250116104420.png" alt="Floating Container">

<p>Then I created a tiled main vertical container with horizontal containers in it. I used blank fields to see my structure first.</p>
<img src="/images/20250116110938.png" alt="Tiled Container Structure">
</details>

<details>
<summary><h4>Put All Charts Together</h4></summary>
<img src="/images/20250116111357.png" alt="All Charts Together">
</details>

<details>
<summary><h4>Format</h4></summary>
<p>Distribute Object Evenly</p>
<img src="/images/20250116111334.png" alt="Distribute Object Evenly">

<p>Outer padding 10, Inner padding 10</p>
</details>

<details>
<summary><h4>Filter</h4></summary>
<p>Filter Apply to all using this Data Source and then select in each graph which filter you want to be shown.</p>
<img src="/images/20250116121851.png" alt="Filter">

<p>I chose what I will have in filter by clicking on chart and selecting filters</p>
<img src="/images/20250120143719.png" alt="Filter">


<p>Number of Orders per Customer</p>
<pre><code>{FIXED [CY Customers Nr.]: COUNTD([CY Orders])}</code></pre>
<p><code>{FIXED [CY Customers Nr.]:</code> all the customers who ordered this year then the aggregation <code>COUNTD([CY Orders])</code> number of orders</p>
</details>

## **Final Dashboard Design**

[Tableau Public link](https://public.tableau.com/app/profile/miroslav.kopac/viz/PortfolioProject1_17373657626930/SalesDashboard)

![image](/images/20250120124311.png)

![image](/images/20250120124332.png)

![image](/images/20250120124400.png)

  
## **What have I learned**

- Framework which I can apply for next project I will do in Tableau
- Choose Charts and Draw Mockups before even starting with visualization
- Creating parameter 
- Using calculated fields and make it dynamic by using parameter
- Functions Window_max, Window_min, WINDOW_AVG, {FIXED}
- Minimalism of Chart Axis titles 
- Creating Container Structure first and then Put All Charts in so it's easier to modify
- Add/Hide Button for Filter 