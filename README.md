<div align="center">

# 👥 Employee Data Analysis & Power BI Dashboard

**Turning raw HR data into workforce insights: Python for cleaning & analysis, Power BI for interactive reporting**

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?logo=powerbi&logoColor=black)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

</div>

---

## 📌 Table of Contents
- [Project Overview](#-project-overview)
- [Business Questions](#-business-questions)
- [Dataset](#-dataset)
- [Tech Stack](#-tech-stack)
- [Workflow](#-workflow)
- [Data Quality Report](#-data-quality-report)
- [Dashboard](#-dashboard)
- [Key Insights](#-key-insights)
- [Repository Structure](#-repository-structure)
- [How to Run](#-how-to-run)
- [Author](#-author)

---

## 🎯 Project Overview

People are a company's biggest asset and biggest cost, yet HR data is often messy and underused. This project analyzes an **employee dataset** end to end:

1. **Python (Jupyter Notebook):** data cleaning, validation, and exploratory analysis
2. **Power BI:** an interactive dashboard that lets HR and management explore the workforce by department, role, demographics, and more

The result is a clear, decision-ready view of the workforce.

## ❓ Business Questions

- What does the **workforce composition** look like (headcount, departments, roles, gender, age)?
- How are **salaries and compensation** distributed across departments and job levels?
- Where is **attrition** concentrated, and what factors are linked to it?
- How do **tenure and experience** vary across the organization?
- Which areas need **HR attention or action**?

> Adjust this list to match the exact questions your dashboard answers.

## 🗂 Dataset

| Property | Details |
|---|---|
| **Location** | `Data_Files/` |
| **Type** | Employee / HR records |
| **Rows × Columns** | `[add number of rows]` × `[add number of columns]` |

**Main fields:** `[e.g. EmployeeID, Department, Job Role, Gender, Age, Hire Date, Salary, Attrition, ...]`

## 🛠 Tech Stack

| Purpose | Tools |
|---|---|
| Data cleaning & EDA | Python, Pandas, NumPy |
| Visualization (EDA) | Matplotlib, Seaborn |
| Environment | Jupyter Notebook |
| Dashboard & reporting | Power BI Desktop (DAX, Power Query) |

## 🔄 Workflow

```
Raw Data  →  Cleaning (Python)  →  EDA  →  Data Model (Power BI)  →  DAX KPIs  →  Dashboard  →  Insights
```

1. **Data Understanding:** reviewed structure, data types, and distributions
2. **Cleaning & Validation:** handled missing values, duplicates, inconsistent formats, and outliers
3. **Exploratory Analysis:** explored patterns across departments, demographics, pay, and tenure
4. **Dashboard Design:** loaded the cleaned data into Power BI and defined KPIs with DAX
5. **Interactivity:** added slicers and filters so users can drill into any segment
6. **Insights:** summarized findings into business-focused takeaways

## 🧹 Data Quality Report

| Issue Found | How It Was Handled |
|---|---|
| Missing values | `[e.g. median for numeric, mode for categorical]` |
| Duplicate records | `[e.g. removed exact duplicates]` |
| Inconsistent formats | `[e.g. standardized dates and text casing]` |
| Outliers / invalid values | `[e.g. flagged and treated]` |

> Replace with the real issues and counts from your notebook.

## 📈 Dashboard

> 📸 *Add dashboard screenshots here:*
>
> `![Dashboard Overview](images/dashboard_overview.png)`

**Key KPIs:**
- 👥 Total Headcount
- 💰 Average Salary
- 📉 Attrition Rate
- ⏳ Average Tenure
- 🏢 Headcount by Department

**Interactive features:** slicers (department, job role, gender, etc.), cross-filtering between visuals, and drill-down views.

## 💡 Key Insights

1. **`[Insight 1]`**: e.g. Department `[X]` has the highest attrition at `[Y]%`
2. **`[Insight 2]`**: e.g. Average salary differs by `[Z]%` between `[groups/levels]`
3. **`[Insight 3]`**: e.g. Employees with `[tenure range]` are most likely to leave
4. **Recommendation:** `[one clear HR action based on the findings]`

## 📁 Repository Structure

```
employee_data_analysis/
│
├── Data_Files/                              # Raw and cleaned datasets
├── employee_data_analysis.ipynb             # Python cleaning & exploratory analysis
├── Employee Data Analysis Dashboard.pbix    # Power BI dashboard
├── images/                                  # Dashboard screenshots
└── README.md
```

## 🚀 How to Run

**Python analysis**
```bash
git clone https://github.com/kirlosmagdy/employee_data_analysis.git
cd employee_data_analysis
pip install pandas numpy matplotlib seaborn jupyter
jupyter notebook employee_data_analysis.ipynb
```

**Power BI dashboard**
1. Install [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (Windows)
2. Open `Employee Data Analysis Dashboard.pbix`
3. If prompted, update the data source path to the `Data_Files/` folder, then click **Refresh**

## 👤 Author

**Kirolos Magdy**: Data Engineer | Analytics Engineer
Faculty of Computers and Data Science, Alexandria University

[![GitHub](https://img.shields.io/badge/GitHub-kirlosmagdy-181717?logo=github)](https://github.com/kirlosmagdy)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Kirolos%20Magdy-0A66C2?logo=linkedin)](https://linkedin.com/in/kirolos-magdy1/)

---

<div align="center">

⭐ If you found this project useful, consider giving it a star!

</div>
