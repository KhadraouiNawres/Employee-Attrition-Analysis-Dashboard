# Employee Attrition Analysis Dashboard
A dashboard that analyzes employee attrition patterns, explores key factors influencing employee turnover and supports data-driven HR decisions using Power BI and Power Query.

## 📌 Table of Contents

- [Overview](#-overview)
- [Business Problem](#-business-problem)
- [Dataset](#-dataset)
- [Tools & Technologies](#-tools--technologies)
- [Project Structure](#-project-structure)
- [Data Cleaning & Transformation](#-data-cleaning--transformation)
- [Dashboard Overview](#-dashboard-overview)
- [Dashboard Analysis](#-dashboard-analysis)
- [Key Insights](#-key-insights)
- [Final Recommendations](#-final-recommendations)
- [How to Use This Project](#-how-to-use-this-project)
- [Author & Contact](#-author--contact)

## 📖 Overview
This project analyzes employee attrition to identify the key factors driving employees to leave the organization and to uncover opportunities for improving retention.

An interactive **Power BI** dashboard was created using **Power Query** for data cleaning and transformation and **DAX (Data Analysis Expressions)** for building measures.

The dashboard provides insights into employee attrition based on department, job roles, salary, satisfaction levels, and other workplace factors.

## ❓ Business Problem
High employee attrition increases replacement costs through recruitment, onboarding, and training while creating productivity gaps and additional workload pressure on remaining employees. Over time, continued turnover impacts workforce stability by reducing knowledge, weakening team cohesion and morale which can further accelerate future attrition.

This project aims to:

- Analyze the overall employee attrition rate to understand the proportion of employees who have left the organization.

- Identify the key drivers of employee attrition and the factors contributing most to employee exits.

- Identify the departments and job roles with the highest turnover to pinpoint where employee loss is concentrated.

- Compare attrition across employee demographics to understand how turnover varies among different groups.

- Assess the impact of salary, experience, and job satisfaction on retention.

- Provide actionable recommendations to improve employee retention based on the insights gained.

## 📂 Dataset
**CSV** file that contains 1,481 rows and 37 columns of structured employee data.

The dataset includes important employee-related columns such as:

- **Age & AgeGroup** ⟹ used to analyze workforce demographics.

- **Department & JobRole** ⟹ used to understand the organizational workforce structure.

- **MonthlyIncome and SalarySlab** ⟹ used to analyze salary distribution.

- **Attrition** ⟹ indicates whether an employee has left the company or is still working.

- **JobSatisfaction** ⟹ helps measure employee engagement levels.

- **TotalExperience & YearsatCompany** ⟹ used to analyze employee career progression.

<a name="-tools--technologies"></a>
## 🛠️ Tools & Technologies
- **Power Query Editor** for data cleaning.

- **DAX** for building measures.

- **Power BI** for interactive visualization.

<a name="-project-structure"></a>
## 🗂️ Project Structure

Employee-Attrition-Analysis-Dashboard/

├── README.md

├── Dataset/

│   └── Employee_Attrition_Data.csv

├── Dashboard/

│   └── Employee_Attrition_Analysis_Dashboard.pbix

|   └── Employee_Attrition_Analysis_Dashboard.png

## 🧹 Data Cleaning & Transformation

Data cleaning was performed using **Power Query Editor**.

**Steps included**:

- I removed **null values** by dropping the 61 rows in the **YearsWithCurrManager** column. I used the **Column Quality view** to identify null values and data errors.

- I **removed duplicate** rows to maintain data integrity, eliminating 2 duplicate records.
 
- I fixed spelling inconsistencies by standardizing category values using **Find and Replace**. I unified **TravelRarely** and **Travel_Rarely** into a single consistent value: **Travel-Rarely**.
 
- I used the **Detect Data Type** option in the **Transform tab** to adjust incorrectly classified data types.

- I created **a conditional column** called **Attrition Count** to convert the Attrition values from text (Yes/No) into numeric values (1/0), which were then used to calculate the Attrition Rate % measure.

- I created **a DAX measure** for **Attrition Rate %** to calculate the percentage of employees who left compared to the total workforce.

## 📊 Dashboard Overview

<img width="1127" height="647" alt="Employee Attrition Analysis Dashboard" src="https://github.com/user-attachments/assets/06940afa-4193-436b-94c4-fcbe02582426" />

## 🔍 Dashboard Analysis
- Attrition by Department: Administration leads with 84 exits (36%), followed by Sales (52, 23%) and Operations (43, 19%). IT (30, 13%), Marketing (10, 4%), HR (9, 4%), and Finance (3, 1%) trail behind.

- Attrition by Salary Slab: The 6–10 LPA bracket has the most leavers (73), ahead of 0–3 LPA (61), 3–6 LPA (49), and 10+ LPA (48). Attrition is fairly spread across all pay bands rather than concentrated at the bottom.

- Attrition by Job Role and Job Satisfaction: Laboratory Technician has the highest attrition (59), then Sales Executive (56) and Research Scientist (45). By satisfaction score, "3" (moderately satisfied) has the most leavers (72), narrowly ahead of "1" (lowest satisfaction, 64), showing dissatisfaction alone doesn't explain most exits.

- Age Group Distribution: Workforce is concentrated in 26–35 (588) and 36–45 (446), with much smaller 46–55 (222), 18–25 (117), and 55+ (44) groups.

- Attrition by Gender: Male employees represent 63.2% of attrition (146) vs. 36.8% female (85), nearly double.

- Attrition by Experience: A sharp spike at 0–2 years (40 exits), a secondary bump around 5–10 years (21–22), then a steep decline after 10 years, tapering to near-zero past 20 years.

- Department-wise employee count: Operations (512) and Administration (406) dominate headcount; Sales (207) and IT (166) are mid-sized; Marketing (64), HR (39), and Finance (23) are the smallest.

## 💡 Key Insights
 - **Early-career, early-tenure risk cluster**: Most attrition is concentrated among employees with 0–2 years of experience. This aligns with the dominant 26–35 age group, suggesting onboarding, early engagement, or unmet expectations are the main churn drivers, not long-term burnout.

- **Attrition rate vs. volume gap**: Administration and Operations show the highest attrition counts, but that's largely a function of headcount size. Relative to department size, IT (≈ 18%) and Sales (≈ 25%) actually have proportionally higher attrition rates than Operations (≈ 8%) — meaning the real "hot spots" are masked when only looking at raw counts.

- **Mid-salary band is a blind spot**: The 6–10 LPA group loses the most employees in absolute terms. Often overlooked because attention typically goes to the lowest-paid tier. This band likely represents employees who feel "stuck" between entry pay and senior compensation.

- **Role-specific concentration**: Laboratory Technician and Sales Executive alone account for ~50% of total attrition (115 of 231) despite representing a fraction of total headcount. These two roles deserve the most focused retention effort. 

- **Satisfaction isn't the sole driver**: The concentration of leavers at satisfaction level "3" rather than "1" indicates attrition is being pulled by external factors (competing offers, compensation, growth ceiling) as much as internal dissatisfaction. A pure engagement-survey fix won't solve this alone.

- **Gender Attrition Distribution**: Male employees account for the majority of attrition cases (63.2%) versus female employees (36.8%). This gap warrants further investigation into whether it reflects role/department concentration rather than a broad gender-based retention issue.

## ✅ Final Recommendations

Based on the dashboard insights:

- **Strengthen early-tenure onboarding (0–2 years)**: Introduce structured 30/60/90-day check-ins, role-specific training, mentorship, and clear job expectation discussions to help employees adapt to role demands and reduce first-year attrition.

- **Targeted retention for Lab Technician & Sales Executive roles**: Conduct exit/stay interviews specific to these two roles to identify whether it's workload, compensation, or growth-path issues driving the disproportionate attrition.

- **Review compensation structure at 6–10 LPA**: Benchmark this band against market rates, review internal pay progression, and ensure clear salary growth opportunities to reduce attrition in this pay band.

- **Investigate rate-based attrition, not just volume**: Track attrition rate (not just count) by department going forward. IT and Sales need closer monitoring despite lower absolute numbers than Operations/Administration.

- **Broaden retention levers beyond satisfaction scores**: Since moderate-satisfaction employees are leaving at similar rates to dissatisfied ones, pair engagement surveys with competitive benchmarking (market pay, role mobility, career ladders) to catch flight risks satisfaction scores miss.

- **Investigate gender attrition gap**: Cross-check male/female attrition rates against departmental gender composition to confirm whether the split is role-driven or requires targeted retention strategies.

## 🚀 How to Use This Project
- Download the .pbix file from my repository.

- Open the dashboard using Microsoft Power BI Desktop.

- Use slicers and filters to explore: employee demographics, attrition drivers, and workforce distribution.

## 👤 Author & Contact

**Khadraoui Nawres - Junior Data Analyst**

📧 Email: khadraouinawres21@gmail.com

🔗 LinkedIn: www.linkedin.com/in/khadraoui-nawres-8339bb278

### Acknowledgments
> This dashboard's design and structure were built, and the dataset was sourced, by following a Power BI tutorial by [Vedakarna](https://www.youtube.com/watch?v=QcTeeBrL6EY).

> All data analysis, insights, and business recommendations included in this project are my own work.
