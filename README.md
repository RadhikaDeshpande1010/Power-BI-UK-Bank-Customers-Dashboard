# Power-BI-UK-Bank-Customers-Dashboard

<img src="https://github.com/RadhikaDeshpande1010/Power-BI-UK-Bank-Customers-Dashboard/blob/main/UK_Bank_Customers_Banner.png" height="270" width="1200">

## Table of Contents
* [Introduction](#Introduction)
* [Dataset](#Dataset)
* [Data Analysis](#Data-Analysis)
* [Data Preparation and Processing](#UK-Customers-Data-Preparation-and-Processing)
* [Technology Stack](#Technology-Stack)
* [How to Use](#How-to-Use)
* [DAX Formulas Used in Measures](#DAX-Formulas-Used-in-Measures)
* [Dashboard](#Dashboard)
* [Future Enhancements](#Future-Enhancements)
* [Conclusion](#Conclusion)
  
## Introduction
* This project showcases a <strong>Power BI dashboard</strong> designed to provide actionable insights into UK bank customers' financial activities. By leveraging data visualization techniques, the dashboard enables users to explore key banking metrics, customer demographics, and transaction behaviors in an intuitive and efficient manner. With a user-friendly interface, it simplifies navigation and enhances data-driven decision-making for banking professionals and analysts.
* The Power BI dashboard for analyzing UK Bank Customers data can be accessed through the following link: [UK Bank Customers Dashboard](https://github.com/RadhikaDeshpande1010/Power-BI-UK-Bank-Customers-Dashboard/blob/main/SRC/UK%20Bank%20Customer%20Report.pbix)

## Dataset
The dataset provides a comprehensive view of UK bank customers, containing key attributes such as <strong>Region, Gender, Customer ID, Name Classification, Age Distribution, Balance, and Job Classification</strong>. These attributes serve as the foundation for various analytical perspectives, including:
- <strong>Region-wise classification</strong> – Understanding customer distribution across different geographic areas.
- <strong>Gender-wise classification</strong> – Identifying trends in banking behaviors based on gender demographics.
- <strong>Age classification</strong> – Segmenting customers into age groups to analyze financial preferences and spending habits.
- <strong>Balance distribution</strong> – Exploring financial patterns, savings trends, and account activity levels.
- <strong>Job classification</strong> – Assessing how occupational backgrounds correlate with banking choices and financial behavior.

The dataset enables rich insights into customer profiles and trends, helping analysts make data-driven decisions. The data for this dashboard is sourced from <strong>Kaggle</strong>, a widely recognized platform for hosting datasets.


## Data Analysis

## UK Customers Data Preparation and Processing 
Before building the interactive dashboard, the raw dataset underwent a structured transformation and cleaning process using <strong>Power Query</strong> to ensure accuracy and consistency.

**1. Data Transformation**
The dataset was reshaped from <strong>wide to long format</strong> by unpivoting date columns, allowing for more flexible analysis

**2. Data Cleaning**
- Removed <strong>unnecessary columns</strong> to retain only relevant attributes.
- Eliminated <strong>duplicate entries</strong> to maintain data integrity.
- Standardized formatting and corrected <strong>spelling errors</strong> for consistency.
- Addressed <strong>missing values</strong> to enhance completeness and reliability.
- Resolved <strong>conflicting information</strong>, ensuring data accuracy across all attributes.

**3. Final Preparation**
With data transformation and cleaning complete, the dataset was <strong>optimized and structured</strong> for dashboard development, enabling seamless interaction and insightful visualizations in <strong>Power BI</strong>.

## Technology Stack
| Tool       | Purpose                             |
|------------|-------------------------------------|
| Power BI   | Data visualization and dashboard creation |
| Excel/CSV  | Source data management              |

## How to Use
1. Load the dataset into Power BI.
2. Explore different dashboard tabs for various banking insights.
3. Use filters to analyze specific customer segments.
4. Interpret key findings for strategic decision-making.

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

<img width="1800" alt="UK Bank Customer Dasboard" src="https://github.com/RadhikaDeshpande1010/Power-BI-UK-Bank-Customers-Dashboard/blob/main/SRC/UK%20Bank%20Customer%20Report.jpg">

## Future Enhancements
- Integration with live data sources.
- Advanced predictive analytics for customer behavior.
- Customizable reporting features.

## Conclusion
The analysis highlights key customer demographics and financial trends, providing valuable insights for strategic banking decisions.
* <b>Customer Demographics:</b> The majority of customers fall within the <b>30-55 age range</b>, with a balanced gender distribution. The highest concentration is observed in <b>England and Scotland</b>, reflecting regional banking preferences.
* <b>Financial Insights:</b> A significant proportion of customers maintain <b>moderate account balances</b>, offering opportunities for banks to personalize financial products and services based on customer profiles.
* <b>Customer Acquisition Trends:</b> The distribution of customers based on their <b>joining month</b> reveals notable patterns, aiding in the formulation of effective <b>marketing strategies and retention initiatives</b> to enhance long-term engagement.

By leveraging these insights, banks can optimize their offerings, improve customer satisfaction, and drive strategic growth.
