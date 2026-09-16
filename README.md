# diabetes_readmission_risk_analysis

Business Problem : 

Hospitals face financial penalties when patients are readmitted within 30 days of leaving the hospital. This project looks at 10 years of data from 130 U.S. hospitals to find which patients, diagnoses and care patterns are linked to a higher risk of readmission. The goal is to help care teams identify high-risk patients, focus follow-up resources, and prevent avoidable readmissions

Data & Tools

- Dataset : https://archive.ics.uci.edu/dataset/296/diabetes+130-us+hospitals+for+years+1999-2008 (UCI Machine Learning, CC BY 4.0). ~100,000 patient encounters across 130 hospitals, 1999-2008
- Database: MySQL Workbench
- -Techniques Used: CTEs, Window Functions (RANK, NTILE), CASE-based risk tiering, correlated subqueries, and multi-table joins


Approach/Methodology

-Cleaning: Replaced placeholder missing values with NULLS, removed a column with about 97% missing data, kept only one encounter per patient to avoid duplicate bias, and removed patients who were inactive or discharged to hospice
- Exploratory Analysis: Established baseline readmission rates by age, admission type and diagnosis category.
- Advanced Analysis: Built a reusable high-risk patient group with CTE, applied window function to rank patients by risk, grouped them by medication use and number of diagnoses, and found diagnosis categories with above average readmission rates.
- Findings: Summarized the results into four key findings that connect back to the main business problem
