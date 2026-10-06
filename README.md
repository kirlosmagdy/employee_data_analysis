<div align="center">

# 👥 Employee Attrition & Compensation Analysis

**Why do employees leave, who is most at risk, and does pay follow performance? An end-to-end HR analytics project with Python and Power BI**

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-4C72B0)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?logo=powerbi&logoColor=black)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

</div>

---

## 📌 Table of Contents
- [Project Overview](#-project-overview)
- [Business Questions & Answers](#-business-questions--answers)
- [Dataset](#-dataset)
- [Tech Stack](#-tech-stack)
- [Workflow](#-workflow)
- [Data Cleaning & Preparation](#-data-cleaning--preparation)
- [Dashboard](#-dashboard)
- [Key Insights](#-key-insights)
- [Recommendations](#-recommendations)
- [Repository Structure](#-repository-structure)
- [How to Run](#-how-to-run)
- [Author](#-author)

---

## 🎯 Project Overview

Employee turnover is expensive: lost knowledge, recruiting costs, and lower team morale. This project analyzes an HR dataset of **1,470 employees** to find **where attrition is concentrated**, **how pay relates to experience and performance**, and **which roles need attention**.

The work has two parts:
1. **Python (Jupyter Notebook):** cleaning, feature preparation, and analysis of departments, job roles, compensation, and salary hikes
2. **Power BI:** an interactive dashboard that lets HR explore the workforce by department, role, and more

## ❓ Business Questions & Answers

| # | Question | Answer |
|---|---|---|
| 1 | **What is the overall attrition rate?** | **16.1%**: 237 of 1,470 employees left |
| 2 | **Which department loses the most people?** | **Sales (20.6%)**, followed by Human Resources (19.1%). R&D is lowest at 13.8%, though it loses the most people in absolute terms (133 vs 92 in Sales) because it is the largest department |
| 3 | **Which job roles are most at risk?** | **Sales Representatives: 39.8%** (about 2.5× the company average). Next are Laboratory Technicians (23.9%) and Human Resources staff (23.1%) |
| 4 | **Which roles are the most stable?** | Managers (5.4% to 5.6%), Research Directors (2.5%), and HR Managers (0%) |
| 5 | **How does pay differ by department and role?** | Average monthly income is **$6,959 in Sales**, $6,654 in HR, and $6,281 in R&D. By role, it ranges from **$2,626 (Sales Representative)** to **$18,089 (HR Manager)** |
| 6 | **What drives monthly income?** | **Job level (correlation 0.95)** and **total working years (0.77)**. Performance rating has essentially no link to income (−0.02) |
| 7 | **Do high performers get bigger raises?** | Yes. Performance rating and salary hike are strongly correlated (**0.77**). But salary hike is unrelated to income level (−0.03), so raises are percentage-based and don't close pay gaps |
| 8 | **How is performance distributed?** | Only two tiers are used: **rating 3 (1,244 employees, 84.6%)** and **rating 4 (226 employees, 15.4%)**, so ratings offer little differentiation |
| 9 | **Do salary hikes differ across departments?** | Barely. Average hike is **14.8% to 15.3%** with a median of 14% in every department, and a range of 11% to 25% |
| 10 | **How long do employees stay?** | Average tenure is **6.9 to 7.3 years** across departments. Sales Representatives have by far the shortest tenure at **2.9 years**, while managers average **13.5 to 16.3 years** |

## 🗂 Dataset

| Property | Details |
|---|---|
| **Source file** | `WA_Fn-UseC_-HR-Employee-Attrition.csv` (IBM HR Analytics Employee Attrition & Performance dataset) |
| **Rows** | 1,470 employees |
| **Columns** | 35 raw, 32 after cleaning, 34 with engineered flags |
| **Missing values** | None |

**Main fields:** `Age`, `Attrition`, `BusinessTravel`, `Department`, `JobRole`, `JobLevel`, `MonthlyIncome`, `PercentSalaryHike`, `PerformanceRating`, `OverTime`, `TotalWorkingYears`, `YearsAtCompany`, `YearsSinceLastPromotion`, `DistanceFromHome`, plus satisfaction scores (job, environment, relationship, work-life balance)

## 🛠 Tech Stack

| Purpose | Tools |
|---|---|
| Data cleaning & analysis | Python, Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Environment | Jupyter Notebook |
| Dashboard & reporting | Power BI |

## 🔄 Workflow

```
Raw Data → Cleaning → Feature Prep → Department & Role Analysis → Compensation Analysis → Dashboard → Insights
```

1. **Data Understanding:** reviewed all 35 columns, types, and null counts
2. **Cleaning:** removed columns with no information and fixed data types
3. **Feature Preparation:** created numeric flags for modeling and aggregation
4. **Department & Job Role Analysis:** headcount, income, tenure, and attrition rate per group
5. **Compensation Analysis:** correlations, performance distribution, and salary-hike breakdowns
6. **Dashboard:** interactive Power BI report built on the cleaned data
7. **Insights:** summarized findings into HR recommendations

## 🧹 Data Cleaning & Preparation

| Step | What Was Done | Why |
|---|---|---|
| **Missing values** | Checked with `df.info()`: all 1,470 rows are complete | No imputation required |
| **Dead columns dropped** | `EmployeeCount` (always 1), `Over18` (always "Y"), `StandardHours` (always 80) | Constant values carry no analytical information |
| **Binary flags created** | `AttritionFlag` and `OverTimeFlag` (Yes/No converted to 1/0) | Makes it easy to calculate attrition rates and averages |
| **Categorical typing** | `Department`, `JobRole`, `EducationField`, `MaritalStatus`, `BusinessTravel`, and `Gender` cast to `category` | Cleaner grouping and lower memory use |
| **Outlier check** | Boxplots for `MonthlyIncome`, `DistanceFromHome`, and `Age` | Visual sanity check before analysis |
| **Export** | Saved as `HR_Cleaned.csv` | Clean input for the Power BI dashboard |

## 📈 Dashboard

> 📸 **Add your Power BI screenshot here** (export it from Power BI and save it as `images/dashboard.png`):
>
> `![HR Dashboard](images/dashboard.png)`

The `.pbix` file cannot be previewed on GitHub, so a screenshot is the best way to show recruiters what you built.

**Metrics analyzed (in the notebook and available for the dashboard):**
- 👥 Headcount by department and job role
- 📉 Attrition count and attrition rate
- 💰 Average monthly income
- ⏳ Average tenure (years at company)
- 📈 Salary hike by department, role, and performance rating

## 💡 Key Insights

1. **📉 Overall attrition is 16.1%** (237 of 1,470 employees), with Sales (20.6%) and HR (19.1%) above average and R&D (13.8%) below.

2. **🚨 Sales Representatives are the biggest retention risk.** Their attrition rate is **39.8%**, roughly 2.5× the company average, and they combine the **lowest average income ($2,626)** with the **shortest tenure (2.9 years)**.

3. **🔬 Entry-level technical roles also leak talent.** Laboratory Technicians (23.9%) and HR staff (23.1%) have above-average attrition and mid-to-low pay (about $3,200 to $4,200 per month).

4. **🏆 Senior roles stay.** Managers and directors earn **$16K to $18K per month**, average **11 to 16 years** of tenure, and have attrition between **0% and 5.6%**.

5. **💵 Pay follows seniority, not performance.** Monthly income correlates strongly with job level (**0.95**) and working years (**0.77**), but not with performance rating (**−0.02**).

6. **🎯 Raises reward performance, but the rating scale is blunt.** Salary hike correlates with performance rating (**0.77**), yet **84.6% of employees sit in rating tier 3** and only 15.4% in tier 4, so most people receive similar raises.

7. **⚖️ Raises are uniform across departments.** Average hikes are nearly identical (14.8% to 15.3%), and since hikes are unrelated to income (−0.03), they do little to close the gap between low-paid and high-paid roles.

## ✅ Recommendations

- **Prioritize Sales Representative retention:** review pay, career path, and workload for this role, since it has the highest attrition and lowest pay
- **Create early-career pay progression:** the data shows attrition is concentrated in low-income, short-tenure roles
- **Refine the performance rating scale:** adding more tiers would let HR recognize and reward top performers more clearly
- **Link raises to pay position as well as performance:** this would help narrow gaps for the lowest-paid roles
- **Learn from stable roles:** study what keeps managers and directors engaged (tenure, pay, autonomy) and apply it to junior roles
- **Next step:** extend the analysis with overtime, business travel, and satisfaction scores to find the underlying drivers of attrition

## 📁 Repository Structure

```
employee_data_analysis/
│
├── Data_Files/
│   ├── Raw_Files/
│   │   └── WA_Fn-UseC_-HR-Employee-Attrition.csv   # Raw dataset
│   └── Cleaned_Files/
│       └── HR_Cleaned.csv                          # Cleaned dataset
│
├── employee_data_analysis.ipynb                    # Cleaning & analysis
├── Employee Data Analysis Dashboard.pbix           # Power BI dashboard
├── images/
│   └── dashboard.png                               # Dashboard screenshot
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
> ⚠️ Update the file paths in the notebook (`pd.read_csv(...)` and `df.to_csv(...)`) to match your local folders.

**Power BI dashboard**
1. Install [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (Windows)
2. Open `Employee Data Analysis Dashboard.pbix`
3. If prompted, point the data source to `Data_Files/Cleaned_Files/HR_Cleaned.csv` and click **Refresh**

## 👤 Author

**Kirolos Magdy**: Data Engineer | Analytics Engineer
Faculty of Computers and Data Science, Alexandria University

[![GitHub](https://img.shields.io/badge/GitHub-kirlosmagdy-181717?logo=github)](https://github.com/kirlosmagdy)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Kirolos%20Magdy-0A66C2?logo=linkedin)](https://linkedin.com/in/kirolos-magdy1/)

---

<div align="center">

⭐ If you found this project useful, consider giving it a star!

</div>
