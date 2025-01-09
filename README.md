# Optimizing Bin Shuaibu Coffee Oasis(BSCo) Sales and Operations with a Dynamic Dashboard

![](https://github.com/anuhimustee/BSCo-Excel-Data-Analysis-Project/blob/main/BSCO%20Front%20Image%201.jpg)

## Introduction
This is project is a Full Excel Data Analysis Project of a figurative store called **“Bin Shuaibu Coffee Oasis (BSCo)”**. 
The project aims to analyze and derive insights by answering crucial questions and gain insights that will help franchise owner _“Mustafah Bin Shuaibu”_  make data-driven decisions.

**_Disclaimer:_** _All datasets and reports do not represent any company, institution or country, the datasets are from the Maven Coffee Shop Sales Dashboard project which can be accessed [here](https://maven-datasets.s3.amazonaws.com/Coffee+Shop+Sales/Coffee+Shop+Sales.zip). 
 For this project, I did some in-depth analysis and provided deeper insights and recommendations for BSCo._

### Project Overview
BSCo is a franchise coffee shop chain with three locations in New York City. Between January and June 2023, the shop recorded transactional data to better understand **customer behavior**, **optimize operations**, and **identify growth opportunities**. Each location serves a mix of beverages, & bakery items during morning rush hours, lunch breaks, and evening downtime.
The franchise owners Mustafah Bin Shuaibu aim to stay competitive in a growing coffee market by leveraging data-driven decisions. They are particularly interested in gaining insights into **purchase patterns**, **identifying opportunities** for cross-selling, and improving **sales trends**.

### Objective
The aim of this data analysis project is to consolidate my Excel skills in helping businesses solve problems. Gain insights in order to make data-driven decisions. For this project, my goal is to create a comprehensive and interactive dashboard that provides actionable insights into customer behavior, sales performance, and operational efficiency across all locations. The dashboard will help __Bin Shuaib 8Coffee Oasis__ identify **patterns**, **trends**, and **opportunities** to improve **revenue** and __streamline operations.__

### About Dataset:  
The dataset used for this project was of a single table data structure that contains 149,116 records and 11 fields. Understanding the contents of the dataset is key and knowing what each field represents gives a holistic idea of what I am working with. See the image 

## Problem Statement
BSCo are struggling to understand the granular details of their sales performance across three NYC locations, which was hindering its ability to make data-driven decisions. They ask key questions to get insights which are:
- What is the total revenue by location?
- How do sales vary across days of the week and hours of operation?
- What are the peak sales hours?
- Are there specific purchase patterns or trends by time (morning vs. afternoon)?
- What are the most popular menu items?
- What is the average transaction size?
- Are there any noticeable monthly or weekly trends?

## Concepts/Skills Demonstrated
The following Excel features were incorporated during the run of this project
-	Data Cleaning/Transformation (Using Power Query)
-	Data Modelling (Power Query for ata normalization applying the 1NF,2NF, and 3NF Methods, and Use of Power Pivot to build, and manage table relationships)
-	Excel Pivot Table Analysis
-	Excel Interactive Dashboard Design

## Data Transformation/Cleaning
The raw dataset that was used for this analysis project was already cleaned with fewer or no issues. But as a data analyst, the idea of cleaning data is to ensure that the data is good to go for analysis in order to ensure and maintain data integrity and accuracy. As much as the dataset was already cleaned, it won’t hurt again to carefully check it out to ensure it meets the standard. As I checked the datasets for any form of nitty-gritty dirtiness, I found out the following:
- No Missing Values
-	No Duplicate Values-
-	Issue of Data Types and Standardization. ( i.e. some columns like the Transaction date, Unit price were not in the correct datatype so had to change and standardization them)

## Modelling:  
As a data analyst, I soon came to realize that this single table has data redundancy (repeated data) and can therefore  be normalized in order to reduce data redundancy and ensure data integrity. 
Loading the data into power query, I was able to achieve the 1NF,2NF & 3NF of normalization which at the end of the day provided me with 3 separate and thus creating and building a model using Power Pivot in Excel. _**See image below.**_

The model is a star schema and thus there are 2-dimension tables and 1 fact table. The dimension tables are all joined to the fact table with a one-many relationships.
For easy access and reference, I also created a calender table from the Power Pivot which automatically gives all dates drill down hierarchy such as Day,Year,Month, Day of the Week Num, Day of the week name etc. _**See image below.**_

|                                              Original Model                                        |                                 After Normalizaation & Modelling                                     |
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------- |
| ![](https://github.com/anuhimustee/BSCo-Excel-Data-Analysis-Project/blob/main/Initial%20Model.png) | ![](https://github.com/anuhimustee/BSCo-Excel-Data-Analysis-Project/blob/main/ModellingComplete.png) |

### Data Analysis & Visuals
Given the problem statement above as well as the business analysis question,  there are couple of additions to be made to the dataset that will help in answering and analyzing the question and problem(s).

**Firstly,** I added a new column called Revenue by multiplying the Unit_Price Column with the Transation_Qty.
```
Revenue =H2*D2
```
Check the image below:
![](https://github.com/anuhimustee/BSCo-Excel-Data-Analysis-Project/blob/main/RevenueCal.png)

**Secondly,** I added a new column called Transaction_Month to extract the month names from the Transaction_Date.
Check the image below:
![](https://github.com/anuhimustee/BSCo-Excel-Data-Analysis-Project/blob/main/MonthExtract.png)

**Thirdly,** I also added a new column called Transaction_Hour whose value is an extract hour from the Transactions_Time column.
![](https://github.com/anuhimustee/BSCo-Excel-Data-Analysis-Project/blob/main/HourExtract.png)

### Now, it was ready for the actual analysis while answering the business question and problem.

