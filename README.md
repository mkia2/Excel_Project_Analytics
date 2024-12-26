# Excel_Project_Analytics
 
# Excel Salary Dashboard

![Excel Skills](https://img.shields.io/badge/Excel-Skills-blue)  
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

## 📊 Overview

The **Data Jobs Salary Dashboard** is designed to assist job seekers in evaluating salaries for various roles, helping them determine fair compensation. 

The dataset originates from my **Excel course**, which emphasizes mastering Excel for data analysis. It includes job titles, salaries, locations, and required skills, all presented through insightful visualizations.

---

## 📁 Dashboard File

- Download the dashboard: **[1_Salary_Dashboard.xlsx](1_Salary_Dashboard.xlsx)**  
- Screenshot preview:  
  ![Salary Dashboard](1_Salary_Dashboard.png)

---

## 🛠️ Excel Skills Demonstrated

This project highlights the following Excel functionalities:

- 📉 **Charts**  
- 🧮 **Formulas and Functions**  
- ❎ **Data Validation**  

---

## 📁 Dataset Details

The project leverages a dataset featuring real-world data science job statistics from **2023**.  
Key attributes include:

- 👨‍💼 **Job Titles**  
- 💰 **Salaries**  
- 📍 **Locations**  
- 🛠️ **Required Skills**

---

## 🛠️ Dashboard Components

### 📉 Visualizations

#### **Bar Chart: Data Science Job Salaries**

- **Features**: Used Excel’s bar chart to visually compare median salaries.  
- **Design**: Horizontal layout for improved clarity.  
- **Organization**: Sorted job titles in descending order of salary.  
- **Takeaway**: Senior positions and engineering roles tend to offer higher salaries than analyst roles.

#### **Map Chart: Country Median Salaries**

- **Features**: Utilized Excel’s map chart to display median salaries geographically.  
- **Design**: Color-coded regions to highlight salary differences across countries.  
- **Takeaway**: Easily identifies regions with higher or lower salary ranges.

---

### 🧮 Formulas and Functions

#### **Median Salary Calculation**

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
- **Purpose**: Computes median salary for selected job titles, locations, and work types.
Key Features: Multi-condition filtering and array-based formula for tailored results.
