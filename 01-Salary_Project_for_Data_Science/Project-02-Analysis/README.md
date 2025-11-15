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
    
    <img width="244" height="312" alt="data_jobs_all" src="https://github.com/user-attachments/assets/9b285390-dce9-45e1-a655-07e4fe2999dc" />

- `data_job_skills`

    <img width="243" height="328" alt="data_job_skills" src="https://github.com/user-attachments/assets/9d297169-eaa2-4ecf-9e10-1732bf57a8de" />

#### 🔗 Load

Loaded both transformed queries into the workbook for analysis.

- `data_jobs_all`

    <img width="1916" height="649" alt="power_query_data_jobs_all" src="https://github.com/user-attachments/assets/a05bad3f-4a21-4102-a8d3-67ff46563b6a" />

- `data_job_skills`

    <img width="1914" height="702" alt="power_query_data_job_skills" src="https://github.com/user-attachments/assets/8abbd75c-ab79-4242-8171-f27c2821fb2c" />

### 📊 Analysis

- Positive correlation between number of skills and median salary.
- Senior roles and specialized skills lead to higher pay.

    <img width="874" height="537" alt="do_more_skills_get_you_better_pay" src="https://github.com/user-attachments/assets/53f02221-39e6-4c6a-a701-eba231866b1a" />

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

    <img width="1776" height="738" alt="US_vs_Non-US_salary" src="https://github.com/user-attachments/assets/cf7ec649-27c3-45ae-9aa2-8f682ac48764" />

---

## 3️⃣ Top skills of data professionals

### 🔧 Skill: Power Pivot

- Integrated `data_jobs_all` and `data_jobs_skills` into one model.
- Created relationship between tables via `job_id`.

    <img width="1788" height="1264" alt="relationship" src="https://github.com/user-attachments/assets/80c5ed03-4a51-4482-bb54-7c052b499ecf" />

📃 Power Pivot Menu
- The Power Pivot menu was used to refine my data model and makes it easy to create measures.

    <img width="1918" height="742" alt="power_pivot_menu" src="https://github.com/user-attachments/assets/8827643d-67d2-454a-9be7-b25dc4ddd32e" />

### 📊 Insights

- SQL, Python dominate as top skills.
- Cloud skills like AWS, Azure increasing in demand.

    <img width="759" height="513" alt="what_are_the_top_skills_of_Data_Nerds" src="https://github.com/user-attachments/assets/6b16ebf4-4be3-4fcc-802c-701981fb778e" />

---

## 4️⃣ Pay of the top 10 skills

### 📊 Skill: Advanced Charts (Pivot Chart)

- Created combo PivotChart: Clustered Column for median salary, Line with markers for skill likelihood.
- Customized chart for clarity.

    <img width="862" height="452" alt="what&#39;s_the_pay_of_the_10_skills" src="https://github.com/user-attachments/assets/b360cbc9-e9f8-476d-a244-9c534a0d4019" />


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
