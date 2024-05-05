# Power-BI-UK-Bank-Customers-Dashboard

<img src="https://github.com/RadhikaDeshpande1010/Power-BI-UK-Bank-Customers-Dashboard/blob/main/Snap/Background.png" height="230" width="1200">

## Table of Contents
* [Introduction](#Introduction)
* [Dataset](#Dataset)
* [Data Analysis](#Data-Analysis)
* [Data Preparation and Processing](#Q2-Employee-Attendance-Data-Preparation-and-Processing)
* [DAX Formulas Used in Measures](#DAX-Formulas-Used-in-Measures)
* [Dashboard](#Dashboard)
* [Conclusion](#Conclusion)
  
## Introduction
* This project aims to develop a Power BI Dashboard to provide insights into UK Bank Customers which providesa concise overview of key metrics and insights relevant to customers' banking activities, offering a simplified interface for easy navigation and quick access to important information.
* The Power BI dashboard for analyzing UK Bank Customers data can be accessed through the following link: [UK Bank Customers Dashboard](https://github.com/RadhikaDeshpande1010/Power-BI-UK-Bank-Customers-Dashboard/blob/main/UK%20Bank%20Customer%20Report.pbix)

## Dataset
The dataset comprises attributes information such as Region, Gender, Customers id and Name Classification, Age Distribution, Distribution by Balance, Job Classification etc. Various analyses like the Region-wise classification, Gender-wise classification, Customer Id and Name classification, Age classification, Distribution by Balance and many other analysis are performed on the dataset.
The data for this UK Bank Customer Dashboard is sourced from Kaggle, a renowned platform for hosting datasets.

## Data Analysis

## UK Customers Data Preparation and Processing 
* Load the Raw Data.
* To conduct the analysis, I needed to convert the dataset from wide to long format. To do so, I used Power Query to unpivot the date columns.
* Data cleaning is performed on Power Query.
* In Power Query, I ensured data quality by removing unnecessary columns, eliminating duplicate rows, and meticulously cleaning individual rows such as correcting spelling mistakes, standardizing formatting, filling in missing values, or resolving conflicting information to ensure to data accuracy and consistency.
* After Data Preparation and Processing activity, it is ready for developing the Interactive Dashboard.

## DAX Formulas Used in Measures

**1. Total Customers:** This DAX expression counts the total number of customers in the dataset.
* ```
  Total Customers = COUNT('UK Bank Customers Template'[Customer ID])
  ```
  
**2. Male Count and Female:** This DAX expression calculate the count of male and female customers respectively based on your dataset.
* ```
  Male Count = COUNTROWS(FILTER('UK Bank Customers Template','UK Bank Customers Template'[Gender] = "Male"))
  Female Count = COUNTROWS(FILTER('UK Bank Customers Template','UK Bank Customers Template'[Gender] = "Female"))
  ```

**3. Region:** This DAX expression gives a distinct count of the regions in the dataset.
* ```
  Region = DISTINCTCOUNT('UK Bank Customers Template'[Region])
  ```

**4. Average Balance Per Customers:** This DAX expression provides average balance per customer..
* ```
  Average Balance Per Customers = DIVIDE(
  SUM('UK Bank Customers Template'[Balance]),
  COUNT('UK Bank Customers Template'[Customer ID]))
  ```

## Dashboard

<img width="1800" alt="UK Bank Customer Image1" src="https://github.com/RadhikaDeshpande1010/Power-BI-UK-Bank-Customers-Dashboard/blob/main/UK%20Bank%20Customer%20Image1.png">

<img width="1800" alt="UK Bank Customer Image2" src="https://github.com/RadhikaDeshpande1010/Power-BI-UK-Bank-Customers-Dashboard/blob/main/UK%20Bank%20Customer%20Image2.png">

## Conclusion
* The majority of customers fall within the 30-55 age range, with a fairly even split between genders. The highest concentration of customers is in the England and Scotland regions.
* A significant proportion of customers maintain a moderate balances. This understanding enables the bank to personalize services and financial products according to customers' financial profiles.
* The distribution of customers by the month they joined the bank describes the notable trends. Understanding customer acquisition patterns over time facilitates strategic planning for marketing campaigns and customer retention initiatives.
