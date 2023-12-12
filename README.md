# Data Analysis Using Python, SQL and Power BI
 
## Overview

This project involves analyzing the Production and Inventory sections of the Microsoft AdventureWorks Database, which represents a fictitious bicycle manufacturing company. The database comprises typical transactional 
data gathered from an Enterprise Resource Planning System. It encompasses various facets of the company, including Human Resources, Product Management, Manufacturing, Purchasing, Inventory, Sales, and Admin. The analysis 
primarily concentrates on the Manufacturing and Inventory aspects of this dataset. To visualize and analyze this data, Microsoft Power BI was utilized to develop an interactive dashboard, sourcing information directly 
from SQL Server.
## Model


[Data Source](https://docs.microsoft.com/en-us/sql/samples/adventureworks-install-configure?view=sql-server-ver15&tabs=ssms)

Below we have defined the data model in star structure view:

<img width="1024" alt="DataModel" src="https://raw.githubusercontent.com/ritik8801/Data-Analysis-of-Bicycle-Manufacturing-Company-Using-Python-SQL-and-PowerBI/main/Dashboard%20Screenshots%20and%20Features/DataModel.png">

### Tables made:

Production Location: Holds assembly data, specifying the parts assigned to manufacture each product along with their assembly location categories.

Production Product: Contains information regarding products, encompassing their physical attributes, pricing, and related details.

Production ProductCategory: Organizes products into distinct categories, providing a structured classification system.

Production ProductSubcategory: Further categorizes products into subgroups, refining the classification of products.

Production ProductInventory: Manages and maintains inventory data specifically for the produced products.

Production ScrapReason: Stores data concerning waste generated during the manufacturing process, detailing reasons for waste occurrence.

Production WorkOrder: Records production transactions and associated data, tracking the progression of production activities.

Production WorkOrderRouting: Contains scheduling details and data related to the routing of production work orders, facilitating the organization of production processes.

Sales SalesOrderDetail: Captures transactional sales data, providing detailed information about sales transactions.

## Analysis

### Main Page

This dashboard analyses manufacturing and inventory operations, the dashboard is made to have an app-like navigational interface. The main page includes leads to two areas namely Production Overview and Inventory Overview. Each then breakdown details and KPIs on their own page afterward.

<img width="1024" alt="Main Page" src="https://raw.githubusercontent.com/ritik8801/Data-Analysis-of-Bicycle-Manufacturing-Company-Using-Python-SQL-and-PowerBI/main/Dashboard%20Screenshots%20and%20Features/Main%20Page.png">

### Production Overview

<img width="1024" alt="Production Overview Page" src="https://raw.githubusercontent.com/ritik8801/Data-Analysis-of-Bicycle-Manufacturing-Company-Using-Python-SQL-and-PowerBI/main/Dashboard%20Screenshots%20and%20Features/Production%20Overview%20Page.png">

The dashboard is made according to the fiscal year terms, a custom date table was created using DAX, to automatically generate Fiscal year segregations. An assumption is made that the fiscal year starts on October 1st and ends on September 30th.  

This page gives information about the manufacturing overview of the company, Measures were created in Power BI in order to have custom KPIs. All the charts and KPIs are described below: -

<img width="1024" alt="Production Overview KPI" src="https://raw.githubusercontent.com/ritik8801/Data-Analysis-of-Bicycle-Manufacturing-Company-Using-Python-SQL-and-PowerBI/main/Dashboard%20Screenshots%20and%20Features/Production%20Overview%20KPI.png">

### Charts on the page

* Cumulative Multiline chart showing Production totals helps compare the fiscal year production trends and helps remove bottlenecks in manufacturing. *

<img width="1024" alt="Cumulative Multiline chart" src="https://raw.githubusercontent.com/ritik8801/Data-Analysis-of-Bicycle-Manufacturing-Company-Using-Python-SQL-and-PowerBI/main/Dashboard%20Screenshots%20and%20Features/Cumulative_Monthly_totals_by_fiscal_year.jpg">

* Donut Chart showing Actual cost distribution over different parts of the assembly line. Helps determine which parts cost more and where improvement is needed so that production costs are reduced. *

<img width="1024" alt="Donut Chart" src="https://raw.githubusercontent.com/ritik8801/Data-Analysis-of-Bicycle-Manufacturing-Company-Using-Python-SQL-and-PowerBI/main/Dashboard%20Screenshots%20and%20Features/Actual%20Cost%20of%20production%20by%20Assembly%20location.jpg">

* Waste cost by year line chart. A simple chart showing how much money is the company wasting on discarded products and what is the trend. *

<img width="1024" alt="Donut Chart" src="https://raw.githubusercontent.com/ritik8801/Data-Analysis-of-Bicycle-Manufacturing-Company-Using-Python-SQL-and-PowerBI/main/Dashboard%20Screenshots%20and%20Features/Waste%20cost%20by%20the%20Year.jpg">

### Category Analysis

After looking at the overview of the manufacturing department, one can navigate to the Product Category Page for a more detailed analysis. Which will help identify specific issues in the manufacturing system. 

This section consists of 4 charts that show an in-depth analysis of the Production components and help determine specific issues.

<img width="1024" alt="Production Category Analysis" src="https://raw.githubusercontent.com/ritik8801/Data-Analysis-of-Bicycle-Manufacturing-Company-Using-Python-SQL-and-PowerBI/main/Dashboard%20Screenshots%20and%20Features/Production%20Category%20Analysis.png">

**Pareto Charts**

A Pareto chart is a Bar graph, the length of the chart represents frequency or cost, the longest bars are arranged on the left and the shortest to the right which amplifies the importance of the category with the highest bar. A line overlaps over the bar graph showing the percent contribution of the specific bar chart towards the total and the line accumulates the percent showing how many categories are important and consume most of the process. There are 2 Pareto Charts on this page, first is for the components required to manufacture a bike showing where most of the production is occupied and the other one is for the finished bike products showing categories of bikes produced.

<img width="1024" alt="Pareto Charts" src="https://raw.githubusercontent.com/ritik8801/Data-Analysis-of-Bicycle-Manufacturing-Company-Using-Python-SQL-and-PowerBI/main/Dashboard%20Screenshots%20and%20Features/Pareto_Charts.jpg">

**Waste Cost - Product Matrix Visual**

The Matrix visual shows the reason where exactly the waste is costing money to the company and due to which reasons. The first column provides the reason for waste, while the other two columns are divided into two categories Bikes (Actual bikes wasted in production) and Components (Components of bikes wasted in production). The Cost is conditionally formatted showing which portion is costing more and the reason for it. There are subtotals on rows and columns and grand total for total waste money.

<img width="1024" alt="Waste Cost" src="https://raw.githubusercontent.com/ritik8801/Data-Analysis-of-Bicycle-Manufacturing-Company-Using-Python-SQL-and-PowerBI/main/Dashboard%20Screenshots%20and%20Features/Waste_Cost_Matrix.jpg">

**Bar chart**

A simple bar chart showing how many Product categories are produced on time.

<img width="1024" alt="Bar chart" src="https://raw.githubusercontent.com/ritik8801/Data-Analysis-of-Bicycle-Manufacturing-Company-Using-Python-SQL-and-PowerBI/main/Dashboard%20Screenshots%20and%20Features/On_time_production_by_category.jpg">

### Inventory Overview

Another major component of the dashboard is the Inventory overview, although there is no data regarding the distribution supply chain in the database this analysis is done assuming the is one location.

Main Page

The overview includes 3 KPI's, 3 Filters to slice the data, and 2 charts.

<img width="1024" alt="Inventory data overview" src="https://raw.githubusercontent.com/ritik8801/Data-Analysis-of-Bicycle-Manufacturing-Company-Using-Python-SQL-and-PowerBI/main/Dashboard%20Screenshots%20and%20Features/Inventory%20data%20overview.png">

**KPIs**

<img width="1024" alt="Inventory data overview KPI" src="https://raw.githubusercontent.com/ritik8801/Data-Analysis-of-Bicycle-Manufacturing-Company-Using-Python-SQL-and-PowerBI/main/Dashboard%20Screenshots%20and%20Features/Inventory%20Overview%20KPI.png">

**Area Charts**

Area charts showing how much Inventory quantity and Inventory value does the company hold by the Assembly location category are shown in the area chart. This shows which part of the manufacturing is holding most of the money and if the company is making the right choices of investing in those parts. There is a button on top of the chart so the end-user can choose if he wants to view the quantity or value on the chart.

**Inventory Turnover Multiline chart**

Comparing inventory turnover on different fiscal years can show important data. It can help show the trends in previous years of how the inventory has been used and can help plan the production process in a better way.

<img width="1024" alt="Inventory Turnover Multiline chart" src="https://raw.githubusercontent.com/ritik8801/Data-Analysis-of-Bicycle-Manufacturing-Company-Using-Python-SQL-and-PowerBI/main/Dashboard%20Screenshots%20and%20Features/Inventory_tunrover_chart.jpg">

