
# 💼 Excel Salary Dashboard

![Dashboard GIF](D:/Shamoun/COURSES/DATA ANALYSIS/Projects Portfolio/Image/01-Salary_Project_for_Data_Science/1_Salary_Dashboard_Final_Dashboard.gif)

## Introduction

This dashboard is my personal Excel project to showcase insights into data jobs salaries. It allows users to explore salaries by job title, country, and job type, using real-world data collected from 2023.  

It demonstrates my skills in Excel, data analysis, and dashboard creation.

## Dashboard File

- [1_Salary_Dashboard.xlsx](./1_Salary_Dashboard.xlsx)

## Excel Skills Used

- 📉 Charts  
- 🧮 Formulas and Functions  
- ❎ Data Validation  

## Data Jobs Dataset

The dataset includes:

- 👨‍💼 Job titles  
- 💰 Salaries  
- 📍 Locations  
- 🛠️ Skills  

## Dashboard Build

### Charts

#### Data Science Job Salaries - Bar Chart

- Excel Features: Horizontal bar chart, formatted salary values, optimized layout  
- Insights: Quickly identify salary trends; senior roles and engineers are higher-paying  

#### Country Median Salaries - Map Chart

- Excel Features: Map chart, color-coded for salary levels  
- Insights: Highlights global salary disparities and regional differences  

### Formulas and Functions

#### Median Salary by Job Titles

```excel
=MEDIAN(
IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))* 
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
)
)
```

- Purpose: Calculates median salary by job title, country, and type  
- Features: Multi-criteria filtering with an array formula  

#### Count of Job Schedule Type

```excel
=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))
```

- Purpose: Generates a unique list of job schedule types, ignoring zero values and combined entries  

### Data Validation

- Filtered lists applied as data validation rules for Job Title, Country, and Type  
- Ensures consistent data entry and enhances usability  

## Conclusion

This personal Excel project demonstrates my skills in data analysis, dashboard creation, and visualization. The dashboard provides actionable insights into salaries across data-related job titles, considering location and job type.

---

*Project created and maintained by Mahmoud Shamoun.*
