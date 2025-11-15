
# 💼 Excel Salary Dashboard

![Dashboard GIF](https://github.com/user-attachments/assets/007b96e5-cabc-4a8b-aff8-9197a532aedf)

## Introduction

This dashboard is my personal Excel project to showcase insights into data jobs salaries. It allows users to explore salaries by job title, country, and job type, using real-world data collected from 2023.  

It demonstrates my skills in Excel, data analysis, and dashboard creation.

## Dashboard File

- [1_Project_Dashboard.xlsx](https://github.com/user-attachments/files/23564243/1_Project_Dashboard.xlsx)


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

### 📉 Charts

#### 📊 Data Science Job Salaries - Bar Chart

<img width="393" height="299" alt="data_science_job_salaries-bar_chart" src="https://github.com/user-attachments/assets/f29f86f8-6a6c-4696-98b4-433790bb7d39" />

- Excel Features: Horizontal bar chart, formatted salary values, optimized layout  
- Insights: Quickly identify salary trends; senior roles and engineers are higher-paying  

#### Country Median Salaries - Map Chart

![Country Median Salaries - Map Chart](https://github.com/user-attachments/assets/89f79fd4-6bff-46ae-94cd-9abf8d1fb1da)

- 🛠️ **Excel Features:** Utilized Excel's map chart feature to plot median salaries globally.
- 🎨 **Design Choice:** Color-coded map to visually differentiate salary levels across regions.
- 📊 **Data Representation:** Plotted median salary for each country with available data.
- 👁️ **Visual Enhancement:** Improved readability and immediate understanding of geographic salary trends.
- 💡 **Insights Gained:** Enables quick grasp of global salary disparities and highlights high/low salary regions.

###  Formulas and Functions
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

![Data_Validation](https://github.com/user-attachments/assets/d87f9ab8-4e6c-4033-a197-35c4c6d19b14)

- Filtered lists applied as data validation rules for Job Title, Country, and Type  
- Ensures consistent data entry and enhances usability  

## Conclusion

This personal Excel project demonstrates my skills in data analysis, dashboard creation, and visualization. The dashboard provides actionable insights into salaries across data-related job titles, considering location and job type.
