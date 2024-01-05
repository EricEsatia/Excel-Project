# Hospital Wait Time Analysis

## Table of Content
  - [Project Overview](#project-overview)
  - [Data Source](#data-source)
  - [Tools](#tools)
  - [Data Cleaning and Preparation](#data-cleaning-and-preparation)
  - [Exploratory Data Analysis(EDA)](#exploratory-data-analysis(eda))
  - [Data Analysis](#data-analysis)
  - [Results and Findings](#results-and-findings)
  - [Recommendations](#recommendations)


## Project Overview

The aim of this Data Analysis Project is to analyze hospital data to identify positive and negative trends in the wait time, how wait times affect service delivery within the hospital, recommend how to reslove the issues identified and to limit long wait times for the patients while maximizing profits for the hospital.

## Data Source

The primary dataset used for this analysis is "hospital_data.xlsx" which contains data on patient entry times, consultation times and different days of the week. This dataset contains a total of 29999 rows of data.

## Tools

- Excel

Excel is the only tool of choice used for this analysis for Data Cleaning, Data Analysis and Data Visiualization. [Download Excel Here](https://www.microsoft.com/en-us/microsoft-365/excel)

## Data Cleaning and Preparation

In the intitial data preparation phase, the following tasks were conducted;
1. Overal inspection for better understanding of the data.
2. Data cleaning and formatting - Date and Time formats were standardized to the same format for easy analysis.

## Exploratory Data Analysis(EDA)

EDA for this analysis involved looking into the data to answer the following key questions;
1. Who is waiting the longest?
2. What days of the week are affected?
3. Are long wait times associated with busy periods within the day?
4. Do we need more staff and Where?

## Data Analysis

Wrote excel formulas to determine our metric for success which in this case is WAIT TIME.

``` Excel
=J2-H2
```
This was then converted to minutes and standardized to follow the format set for time.

```Excel
=1440*L2
```
The next step was to create a day of week column using the =WEEKDAY function and the date column. This was then wrapped in a TEXT function with the format "dddd" to convert it to an actualy day of week instead of number as prescribed by the formula.
``` Excel
=TEXT(WEEKDAY(A2),"dddd")
```
 Also, another column for the patient entry hour was created using the =HOUR function and the entry time column
```Excel
=HOUR(H2)
```
Created columns for Consultation Time	Processing Time	Consultation %	Processing %
![image](https://github.com/EricEsatia/Excel-Project/assets/145187562/80d5293d-f2dc-4141-b617-0511a5da2483)

Created Pivot Tables for summarizing and aggregating data points in a flexible and interactive way.

## Results and Findings
1. Under the financial classes (Insuarance Type) listed, MEDICARE seems to be taking the longest to process their patients. This is however not representative of the true picture as Medicare only represents 1% of the patients hence not enough to conclude that this is a major factor.
![image](https://github.com/EricEsatia/Excel-Project/assets/145187562/d17f382f-24fb-4250-919a-eb04785de00c)

2. The days of the week that appear to be more affected are Monday with an average of 49 Mins wait time and Wednesday with an average of 47 Mins wait time. The overall average wait time is 44 Minutes.
![image](https://github.com/EricEsatia/Excel-Project/assets/145187562/3d5637c1-3e13-403e-a5a6-4d4c6641676a)

3. Morning hours appear to be busier than the rest of the times and with longer wait times. This could be an indication of increased work-load and under-staffing during the morning rush.
![image](https://github.com/EricEsatia/Excel-Project/assets/145187562/6e5d7088-ebe7-45be-9c78-4f0ccda53cc8)
<img width="500" alt="image" src="https://github.com/EricEsatia/Excel-Project/assets/145187562/d0715cc9-9086-4004-ae5f-a357c982e2ff">

4. Average consultation times are much higher and focus should therefore be to reduce the time by increasing medical staff assuming the wait time to see a doctor is limited by the number of medical staff available during the required time.
![image](https://github.com/EricEsatia/Excel-Project/assets/145187562/c8e94194-bdba-4dc1-9495-578ced517a8f)

## Recommendations

Based on the analysis, the following are recommended to the management for consideration;

- Consider the possibilty of adding more staff during the morning rush hour.
- Focus should be on reducing the average consultation time.
- The management to determine whether it makes financial sense to hire more staff to cover for the morning and a lunch time demand.







