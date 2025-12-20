# Adventure Works Sales Analysis

## Profitability, Time Series & Business Insights Dashboard (Excel BI Project)
## Dashboards Overview
![Dashboards Overview](https://github.com/user-attachments/assets/b05fec9a-7f9c-4451-a4a3-5057e8d5a148)

## Detail Dashboard
![Detail Dashboard](https://github.com/user-attachments/assets/66c3c627-607f-43db-90bc-6e193d823847)

---

## Project Overview

This project is a complete Business Intelligence (BI) solution built entirely using Microsoft Excel. It analyzes sales performance, profitability, and time-based trends using the Adventure Works dataset.

The project simulates a real-world business analytics scenario where raw transactional data is transformed into clean, structured, and insightful dashboards to support data-driven decision making.

The solution is implemented using Excel BI components only:

* Power Query for data preparation (ETL)
* Power Pivot for data modeling and DAX calculations
* Pivot Tables and Pivot Charts for analysis and visualization

---

## Target Roles

* Data Analyst
* Business Intelligence Analyst
* Excel BI Developer
* Sales & Performance Analyst

---

## Business Objectives

The project answers key business questions:

* How are revenue, profit, and transactions changing over time?
* How does current-year performance compare to the previous year?
* Which time periods generate the highest profitability?
* Which products, customers, and segments contribute most to profit?
* How is profit distributed across geography and demographics?

---

## Dataset Description

* Source: Adventure Works Sales Dataset
* Data Type: Transactional sales data
* Main Tables:

  * Sales (Fact table)
  * Products
  * Customers
  * Date

---

## Tools & Technologies Used

| Tool            | Purpose                          |
| --------------- | -------------------------------- |
| Microsoft Excel | Main BI platform                 |
| Power Query     | Data cleaning and transformation |
| Power Pivot     | Data modeling and DAX measures   |
| Pivot Tables    | Aggregation and analysis         |
| Pivot Charts    | Visualization and dashboards     |

---

## Data Preparation (ETL Process)

### Data Cleaning (Power Query)

* Removed blank and irrelevant records
* Handled missing values
* Standardized data types (dates, numeric fields, text)
* Ensured consistent column naming

### Data Transformation

* Created derived columns where required
* Extracted Year, Month, Quarter attributes
* Prepared fact and dimension tables for modeling

Screenshot suggestion:

* Power Query Editor showing cleaned tables and applied steps

---

## Data Modeling

A star schema model was implemented in Power Pivot to ensure performance and accuracy.

Relationships:

* Sales (Fact) to Products
* Sales (Fact) to Customers
* Sales (Fact) to Date

Screenshot suggestion:

* Power Pivot diagram view showing table relationships

---

## Key DAX Measures

The project uses professional DAX measures to calculate KPIs and time-based insights.

### Core Measures

Total Revenue:

```
Total Revenue = SUM(Sales[SalesAmount])
```

Total Profit:

```
Total Profit = SUM(Sales[Profit])
```

Total COGS:

```
Total COGS = SUM(Sales[COGS])
```

Total Quantity:

```
Total Quantity = SUM(Sales[OrderQuantity])
```

Total Transactions:

```
Total Transactions = DISTINCTCOUNT(Sales[OrderNumber])
```

Profit Margin:

```
Profit Margin % = DIVIDE([Total Profit], [Total Revenue])
```

---

### Time Intelligence Measures

Previous Year Revenue:

```
Revenue PY = CALCULATE([Total Revenue], SAMEPERIODLASTYEAR(Date[Date]))
```

Year-over-Year Revenue Change:

```
Revenue YoY % = DIVIDE([Total Revenue] - [Revenue PY], [Revenue PY])
```

Running Total Revenue:

```
Running Revenue = CALCULATE([Total Revenue], FILTER(ALL(Date), Date[Date] <= MAX(Date[Date])))
```

Screenshot suggestion:

* Power Pivot measures list

---

## Dashboards Overview

The project contains two main dashboards:

1. Time Series Dashboard
2. Detail Dashboard (Profitability Drivers)

---

## Time Series Dashboard

Sheet Name: Time Series Dashboard

This dashboard focuses on performance analysis over time.

### Analyses Included

1. KPI Comparison to Previous Year

   * Revenue, Profit, COGS, Quantity, Profit Margin, Transactions

2. Yearly Performance Metrics (Above-Average Years)

   * Revenue, Profit, and Transactions for years exceeding the average

3. Monthly Profit Trends

   * Identification of seasonality and monthly behavior

4. Profit by Week Type

   * Weekday versus Weekend profitability

5. Quarterly Profit Analysis

   * Q1 to Q4 profit contribution

6. Profit by Weekday

   * Profit distribution across individual days


---

## Detail Dashboard (Profitability Analysis)

Sheet Name: Dashboard

This dashboard focuses on identifying the main contributors to profitability.

### Analyses Included

1. Top 5 Profitable Products

   * Profit contribution percentage versus all other products

2. Top 5 Profitable Customers

   * Profit contribution percentage versus all other customers

3. Profit by Gender

   * Male versus Female profit distribution

4. Profit by Product Color

   * Highlighting best-selling and most profitable colors

5. Profit by Pricing Types

   * Comparison between higher-priced and lower-priced products

6. Country-wise Profit Contribution

   * Custom map visualization by country

7. Profit by Age Groups

   * Profit segmentation by customer age ranges


---

## Usage Policy

This project is published for viewing and evaluation purposes only.

* Redistribution is not allowed
* Commercial use is not permitted
* Modification or reuse is prohibited

All rights reserved.

---

## Final Notes

This project demonstrates advanced skills in:

* Excel-based BI solutions
* Data modeling with Power Pivot
* DAX calculations and time intelligence
* Business-focused dashboard design
