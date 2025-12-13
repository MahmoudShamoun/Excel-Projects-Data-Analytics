# 🚲 Adventure Works Sales Analysis: 💰 Profitability & Time Series Insights

## 🎯 Target Roles

Data Analyst | Business Insights Analyst | Excel BI Developer | Sales Strategy Analyst

## 📋 Project Overview 🚀

This project is a comprehensive **Business Intelligence (BI)** solution built entirely within Microsoft Excel. It leverages the full analytical stack (Power Query, Power Pivot, and DAX) to transform complex, raw Adventure Works sales data into a dynamic and interactive dashboard.

The dashboard enables management to explore sales trends, profitability, and geographic performance in real-time.

-----

### **Overall Dashboard View**

## Time Series Dashboard!
![Time Series Dashboard Screenshot](<01-Time Series Dashboard.png>)
## Detail Dashboard
![Detail Dashboard Screenshot](<>)

-----

## 🛠️ Tools & Technologies Used

| Component | Tool / Feature | Purpose |
| :--- | :--- | :--- |
| **Data Preparation (ETL)** | 🗄️ **Power Query (M Language)** | Data ingestion, cleaning, transformation, and creation of new dimension columns. |
| **Data Modeling** | 🔗 **Power Pivot** | Building a Star Schema, managing relationships, and ensuring optimal calculation performance. |
| **Calculations** | 🧮 **DAX Formulas** | Creating dynamic, powerful measures for Time Intelligence and profitability analysis. |
| **Visualization** | 📊 **Pivot Charts & Slicers** | Designing interactive reports, maps, and using conditional formatting for visual impact. |

-----

## ⚙️ Detailed Project Execution

### A. Data Preparation & Cleaning

#### 🧹 Power Query (ETL) Steps

Power Query was utilized to process the raw data from various tables (`FactInternetSales`, `DimCustomer`, `DimProduct`, etc.) into a clean, unified structure.

**Key Actions Performed:**

1.  **Date Dimension:** Created a fully functional Date dimension table (if one was not present) or ensured the existing one was robust for Time Intelligence functions.
2.  **Standardization:** Removed invalid entries, handled null values (e.g., in customer demographics), and standardized data types for consistency.
3.  **Renaming:** Renamed complex technical column names to business-friendly headers.

**[Power Query Steps Screenshot]**
*Show a screenshot of the Applied Steps pane in Power Query for one of your main tables (e.g., FactInternetSales).*

`[Place the Power Query Steps screenshot here (File Name: power_query_steps.png)]`

### B. Data Model Architecture

#### 🔗 Star Schema Design in Power Pivot

The cleaned data was loaded into Power Pivot to establish a **Star Schema** with defined filter propagation, which is the cornerstone of a fast and flexible analytical model.

  - **Fact Table:** `FactInternetSales` (Central table).
  - **Dimension Tables:** `DimDate`, `DimProduct`, `DimCustomer`, `DimGeography`, `DimSalesTerritory`.
  - **Relationships:** Established clear **One-to-Many** relationships between Dimension and Fact tables.

**[Data Model Diagram Screenshot]**
*Show a screenshot of the Diagram View in Power Pivot, illustrating the connected tables.*

`[Place the Data Model Diagram screenshot here (File Name: data_model_diagram.png)]`

### C. DAX Measures & Calculations

DAX was used to create dynamic, robust Key Performance Indicators (KPIs) that update based on user selections (Slicers/Filters).

**[DAX Measures Screenshot]**
*Show a screenshot of the Power Pivot window highlighting the dedicated area where you created the Measures.*

`[Place the DAX Measures screenshot here (File Name: dax_measures.png)]`

#### 🧮 Key DAX Formulas Used

| Measure Name | DAX Formula | Purpose & Significance |
| :--- | :--- | :--- |
| **Total Revenue** | `= SUM(FactInternetSales[SalesAmount])` | Calculates the overall sales value. |
| **Total Profit** | `= [Total Revenue] - SUM(FactInternetSales[TotalProductCost])` | Calculates the net profit (Revenue - Cost). |
| **Profit Margin %** | `= DIVIDE([Total Profit], [Total Revenue], 0)` | A key efficiency metric showing profitability ratio. |
| **Total Transactions** | `= COUNTROWS(FactInternetSales)` | Counts the total number of orders/transactions. |
| **Profit Last Year** | `= CALCULATE([Total Profit], SAMEPERIODLASTYEAR('DimDate'[Date]))` | **Time Intelligence:** Crucial for comparative analysis. |
| **Profit YoY Growth %** | `= DIVIDE([Total Profit] - [Profit Last Year], [Profit Last Year], 0)` | Measures the percentage growth or decline compared to the previous year. |

-----

## 📈 Detailed Dashboard Visualizations & Insights

### 1\. Time Series & Trend Analysis

This section focuses on temporal performance, seasonality, and year-on-year comparisons, driven by DAX Time Intelligence.

**[Time Series Dashboard Screenshot]**
*Show a screenshot of the section/sheet dedicated to Time Series Analysis (Trends, YoY, Monthly/Quarterly performance).*

`[Place the Time Series Dashboard screenshot here (File Name: time_series_dashboard.png)]`

| Analysis Component | Visualization | Key Insight Displayed |
| :--- | :--- | :--- |
| **YoY KPI Cards** | KPI Cards | **Growth Tracking:** Direct comparison of Revenue/Profit vs. Previous Year (YoY) using arrows and conditional formatting to show trend. |
| **Monthly Trend** | Line Chart | **Seasonality Detection:** Identifies peak sales months (e.g., Q4 spike) and low periods for forecasting. |
| **Profit by Weekday** | Column Chart | **Operational Insight:** Compares profitability across days of the week, optimizing staffing and promotions. |

### 2\. Profitability & Segmentation Analysis

This section dives into product, customer, and geographical performance drivers.

**[Sales Dashboard Screenshot]**
*Show a screenshot of the section/sheet dedicated to Segmentation and Profitability Analysis (Top Products, Customers, Map).*

`[Place the Sales Dashboard screenshot here (File Name: sales_dashboard.png)]`

| Analysis Component | Visualization | Key Insight Displayed |
| :--- | :--- | :--- |
| **Top 5 Profit Drivers** | Bar/Donut Chart | **Pareto Principle:** Highlights the **Top 5 Products** and/or **Top 5 Customers** contributing to the highest percentage of total profit. |
| **Profit by Demographics** | Column Charts | **Target Marketing:** Analysis of profit segmented by customer **Gender** and **Marital Status** to define target segments. |
| **Profit by Sales Territory** | Map Chart | **Geographic Strategy:** Visual representation (color-coded) of total profit across different global sales regions, highlighting best-performing territories. |
| **Product Color/Size** | Bar Chart | **Inventory Management:** Identifies which product colors or sizes generate the highest margins, guiding procurement decisions. |

-----

## Conclusion & Recommendations 💡

This project successfully transitioned complex relational data into an intuitive, dynamic BI tool in Excel.

### Key Insights

  * **High Reliance:** A small subset of products and customers are responsible for the majority of the profit (The 80/20 Rule applies).
  * **Time Sensitivity:** Sales and Profit exhibit strong seasonality, requiring optimized inventory planning for peak periods.
  * **Geographic Disparity:** Performance is heavily concentrated in a few key territories, suggesting a need for focused investment or expansion into under-performing areas.

### Business Recommendations

1.  **Customer Focus:** Implement loyalty programs targeting the top-tier customer segments identified in the analysis.
2.  **Pricing Optimization:** Use the profitability analysis by product to review pricing for low-margin items.
3.  **Forecasting:** Integrate the monthly/quarterly trend data into the sales forecasting model for increased accuracy.

## 📂 Repository Structure

```
/Adventure-Works-Sales-Analysis
│
├── Project.xlsm              # The main Excel file with the Data Model and Dashboard
├── README.md                 # Project documentation (this file)
└── Screenshots/              # Folder containing all project images
    ├── overall_dashboard.png         <-- Your complete dashboard view
    ├── power_query_steps.png         <-- Power Query steps pane
    ├── data_model_diagram.png        <-- Power Pivot Diagram View
    ├── dax_measures.png              <-- DAX Measures list
    ├── time_series_dashboard.png     <-- Time Analysis sheet/section
    └── sales_dashboard.png           <-- Segmentation Analysis sheet/section
    
```