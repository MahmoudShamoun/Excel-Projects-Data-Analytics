# Project 2 Analysis

## Overview

This project explores the data science job market to identify high-demand skills and how they affect compensation. The goal is to provide actionable insights for professionals aiming for higher-paying roles.

### Key Questions

1. Does having more skills lead to higher salaries?
2. How do salaries vary across different regions?
3. Which skills are most in demand?
4. What is the salary impact of the top 10 skills?

### Excel Techniques Applied

The following Excel skills were utilized for analysis:

- **📊 Pivot Tables**
- **📈 Pivot Charts**
- **🧮 DAX (Data Analysis Expressions)**
- **🔍 Power Query**
- **💪 Power Pivot**

### Data Jobs Dataset

The dataset used for this project contains real-world data science job information from 2023. It includes detailed information on:

- **👨‍💼 Job titles**
- **💰 Salaries**
- **📍 Locations**
- **🛠️ Skills**

---

## 1️⃣ Do more skills get you better pay?

### 🔍 Skill: Power Query (ETL)

#### 📥 Extract

Used Power Query to extract the original data (`data_salary_all.xlsx`) and created two queries:

- All job information.
- Skills per job ID.

#### 🔄 Transform

Transformed each query by changing column types, removing unnecessary columns, cleaning text, and trimming whitespace.

- `data_jobs_all`

    ![data_jobs_all](2_Project_Analysis_Screenshot1.png)

- `data_job_skills`

    ![data_job_skills](data_job_skills.png)

#### 🔗 Load

Loaded both transformed queries into the workbook for analysis.

- `data_jobs_all`

    ![power_query_data_jobs_all](power_query_data_jobs_all.png)

- `data_job_skills`

    ![power_query_data_job_skills](power_query_data_job_skills.png)

### 📊 Analysis

- Positive correlation between number of skills and median salary.
- Senior roles and specialized skills lead to higher pay.

    ![do_more_skills_get_you_better_pay](do_more_skills_get_you_better_pay.png)

---

## 2️⃣ Salary for data jobs in different regions

### 🧮 Skills: PivotTables & DAX

Calculated median salary using PivotTables and DAX formulas.

```DAX
Median Salary := MEDIAN(data_jobs_all[salary_year_avg])
```

### 📊 Analysis

- High-level roles have higher salaries globally.
- US vs Non-US salary differences notable in tech jobs.

    ![alt text](US_vs_Non-US_salary.png)

---

## 3️⃣ Top skills of data professionals

### 🔧 Skill: Power Pivot

- Integrated `data_jobs_all` and `data_jobs_skills` into one model.
- Created relationship between tables via `job_id`.

    ![relationship t](relationship.png)

📃 Power Pivot Menu
- The Power Pivot menu was used to refine my data model and makes it easy to create measures.

    ![power_pivot_menu](power_pivot_menu.png)

### 📊 Insights

- SQL, Python dominate as top skills.
- Cloud skills like AWS, Azure increasing in demand.

    ![what_are_the_top_skills_of_Data_Nerds](what_are_the_top_skills_of_Data_Nerds.png)
---

## 4️⃣ Pay of the top 10 skills

### 📊 Skill: Advanced Charts (Pivot Chart)

- Created combo PivotChart: Clustered Column for median salary, Line with markers for skill likelihood.
- Customized chart for clarity.

    ![what's_the_pay_of_the_10_skills](what's_the_pay_of_the_10_skills.png)

### 📊 Insights

- Skills like Python, Oracle, SQL linked to higher salaries.
- Office skills (Word, PowerPoint) linked to lower pay.

---

## Conclusion

This Excel-based project uncovers key insights about the data science job market:

- Multiple skills → higher salaries.
- Certain regions pay more for tech roles.
- SQL, Python, Cloud are top-value skills.

It demonstrates my ability to clean, analyze, and visualize data using Excel's Power Query, PivotTables, DAX, and charts.