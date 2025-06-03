# Business Insights 360

## Project Overview

AtliQ Hardware is growing rapidly in the recent years, and they have decided to implement the data analytics using PowerBi in their company for the first time to surpass their competitors in the market and to make data driven decisions. This project is hoped to give answers to the questions of stakeholder in terms all the aspects like finance, sales, marketing and supply chain.

Link to [Interactive Dashboard](https://app.powerbi.com/view?r=eyJrIjoiMzczYzI3NzgtNGQwNy00OTcxLTg5MTAtZjkxNTczNDk5YTVjIiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9)

## Tech stacks

- SQL
- PowerBi Desktop
- Excel
- DAX language
- DAX studio (for optimizing the report)
- Project charter file

## PowerBI techniques Learnt

- What are all the questions should be asked before staring the project
- Creating calculated columns
- creating measure using DAX language
- Data modeling
- Using Bookmarks to switch between two visuals
- Page navigation with buttons
- Using divide function to prevent zero division errors
- creating date table using m language
- Dynamic titles based on the applied filters
- Using KPI indicators
- Conditional formatting the values in visuals using icons or background color
- Data validation techniques
- PowerBi services
- Publishing reports to PowerBi services
- Setting up personal gateway to set up the auto refresh of data
- PowerBi App creation
- Collaboration, workspace, access permissions in PowerBi services

## Business related terms

- Gross price
- Pre-invoice deductions
- Post-Invoice deductions
- Net Invoice sale
- Gross Margin
- Net sales
- Net profit
- COGS - cost of goods sold
- YTD - Year to Date
- YTG - Year to Go
- Direct
- Retailer
- Distributors
- Consumer

## Company’s back ground

AltiQ hardware is a company which has grown vastly in the recent years, and opened business all over the globe. It is a company which sells, computer and computer accessories through three mediums/channel

- Retailers
- Direct
- Distributors

Recently the company has faced a unforeseen loss by opening store in America based on the surveys, intuition and some excel analysis and also the company’s competitors has handful of analytics team to perform analysis and make data driven decision. So, the AltiQ hardware has no other option other than building their analytics team for data driven insights and decisions in the future to survive better in the industry. 

Project kick off session, where you should get clear of for what and why this project and all other questions you have with regards to the project

### Questions to ask before starting with dashboard

- What is the objective of building this PowerBi dashboard?
- In what terms the success of this project will be measured?
- What will be the deadline for the project?
- Do the stakeholders expecting preview before the actual release?
- What are all the hopes stakeholders have out of this project?
- What are all fears the stakeholder have in terms of building this dashboard?
- Who are all will be using this dashboard and for what purpose?
- What are all expectation the stakeholders have, by the completion of this project?
- What can go wrong while building this project?
- What are all the resources/ data needed to build this dashboard?
- Is there any inputs from stakeholders in terms of design and views of the dashboard?

After the project kick off meetings, the data engineering team has given the data as per the request of data analytics team, let’s explore them.

### Dataset **Understanding.**

Understanding what data is available will be more helpful while doing analysis. before jumping on to the analysis get good understanding of what are data available.

Dimension table : It will have the static data like details of customer and products

Fact table : It will have the data about the transactions

- gdb041:
    - dim_customer
        - **27** distinct markets (ex India, USA, Spain)
        - **75** distinct customers thorough out the market
        - **2** types of platforms
            - Brick & Mortar - Physical/offline store
            - E-commerce - Online Store (Amazon, Flipkart)
        - Three channels
            - Retailer
            - Direct
            - Distributors
    - dim_market
        - **27** distinct markets (ex India, USA, Spain)
        - 7 sub-zones
        - 4 regions
            - APAC
            - EU
            - NA
            - LATAM
    - dim_product
        - Divisions
            - P & A
                - Peripherals
                - Accessories
            - PC
                - Notebook
                - Desktop
            - N & S
                - Networking
                - Storage
        - There are 14 different categories like Internal HDD, Keyboard etc.
        - There are different variants available for the same product.
    - fact_forecast_monthly
        - This table is used to forecast the customer’s need in advance, which can help in
            - Ensuring Order Fullfiment
            - Reduced cost in warehouses for storage purpose
        - The table is denormalized by data engineering team, as it is a data warehouse which is aimed to be used for analytical work.
        - All the date of the month will be replaced by the start date of the month
        - It will have all the column names and in the end it will have the forecast quantity need of the customer
    - fact_sales_monthly
        - This table is more or less is same as fact_forecase_monthly table, but the last column has the value of sold quantity instead of forecast value.
- gdb056
    - freight_cost
        - Freight cost and other cost for each market with fiscal year
    - gross_price
        - Gross prices with product code
    - manufacturing_cost
        - Manufacturing cost with product code with year
    - Pre_invoice_dedutions
        - Pre invoice deductions percentage for each cutomer with year
    - Post_invoice_deductions
        - Post invoice deductions and other deductions details

## Importing data into PowerBi

- As the database is MySQL in this project, we need to import the datasets from Mysql database to PowerBi by providing the Database access credential

## Data Model

- Data modeling plays a vital role and is considered as the basement of report. All the visuals will be build upon this data model.
- Poor data modeling affects the over all performance of the report.
- In this project, we have followed Snowflake data modeling method.

[Data Model](https://github.com/SatyapriyaDasgupta/Business-Insight-360/blob/db918cbf43f361cc487bc5a3217e63bd8f2fc4ec/Resources/BI%20360%20Data%20Model.png)

### Dashboard designing

Based on the mock ups received as per the requirement, I have designed the visuals and created measures as per reqirements.

## Home Page

In Home Page, all the views button will be available. Users can access any specific view page by clicking the buttons. 

- Home Page
- Finance View
- Sales View
- Marketing View
- Supply chain View
- Executive View

## Home Page

<p align="center">
    <img scr='https://github.com/SatyapriyaDasgupta/Business-Insight-360/blob/7995319b1beac225a2559e6fdba7ddedf68d8e39/Resources/Homepage.png'>
</p>

## Finance View

![Finance View.gif](https://github.com/SatyapriyaDasgupta/Business-Insight-360/blob/7995319b1beac225a2559e6fdba7ddedf68d8e39/Resources/Finance%20View.gif)

## Sales View

![Sales View.gif](https://github.com/SatyapriyaDasgupta/Business-Insight-360/blob/ddaba7d900168348aece82abacdc8c538510cf5c/Resources/Sales%20View.gif)

## Marketing View

![Marketing View.gif](https://github.com/SatyapriyaDasgupta/Business-Insight-360/blob/ddaba7d900168348aece82abacdc8c538510cf5c/Resources/Marketing%20View.gif)

## Supply chain View

<p align="center">
    <img src='https://github.com/SatyapriyaDasgupta/Business-Insight-360/blob/ddaba7d900168348aece82abacdc8c538510cf5c/Resources/Supply%20Chain%20View.png'>
</p>

## Executive View

<p align='center'>
    <img src='https://github.com/SatyapriyaDasgupta/Business-Insight-360/blob/ddaba7d900168348aece82abacdc8c538510cf5c/Resources/Executive%20View.png'>
</p>

You can find the full report file here : [Report]

## Project Outcome

By using this report, decisions can be taken based on the data. Further it will help in answering n number of why questions based on the situations.
