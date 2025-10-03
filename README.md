🩸 Heart Attack Risk Prediction Dashboard 

📌 Project Overview

This project delivers a fully functional Microsoft Excel Dashboard designed to analyze and predict the risk of heart attacks using comprehensive patient health, demographic and lifestyle data. The dashboard's goal is to go beyond simple reporting by leveraging the Excel Data Model and DAX to identify high-risk demographics, pinpoint key causative factors (like stress and lifestyle), and provide a dynamic, interactive tool for public health officials.The final deliverable is an advanced Excel workbook that transforms raw health records into actionable, data-driven insights.

⚙️ Tech Stack

The entire project is built and managed within the Microsoft Excel ecosystem, utilizing its powerful analytical features :

- Dashboard Design & Visualization : Microsoft Excel (Sheets, Pivot Charts, Slicers and interactive controls).
- Data Modeling & Calculation Engine : Excel Data Model / Power Pivot – Used to build relationships between tables, eliminating the need for VLOOKUPs.
- Advanced Logic & Measures: DAX (Data Analysis Expressions) – Used for complex calculated fields, custom Key Performance Indicators (KPIs) and aggregation logic (e.g., weighted risk scores and percentages).
- Data Management: Microsoft Excel / CSV Datasets.

📂 Data Architecture and Source

The analysis is based on ≈10,000 patient records, organized using a Dimensional Modeling approach (Star Schema) within the Excel Data Model for efficient performance and complex query execution.

Core Tables :

- Fact_HeartRisk : Patient ID and the binary outcome (Heart_Attack_Risk: 0 or 1).

- Fact_Health : Health metrics (Cholesterol, Blood Pressure, Conditions) and Lifestyle factors (Stress Level, Diet Score).

- Dim_Demographics : Patient demographics (Age, Gender).

- Dim_Geography : Location details (State).

🛠️ Data Cleaning, Transformation and DAX

The core of the analysis resides in the Data Model, where raw data is transformed into analytical fields :

- Calculated Columns (DAX)
- Age Group Segmentation: Created a calculated column to segment the Age dimension into categorical groups (e.g., 0-20, 21-30, 71+) to enable macro-level risk analysis.
- High/Low Risk Flag : Used to classify patients based on the Heart_Attack_Risk value.
- Calculated Measures (DAX KPIs)
- M_Total Patients : Total count of records (≈10,000).
- PCT_HighRisk Patients : Percentage of the population identified as high risk (Baseline ≈30.07%).
- AVG_HealthRisk Score : A custom weighted score used to measure average risk severity.

🚀 Business Problem – Key Questions

- The dashboard delivers insights directly addressing critical public health and clinical questions:
- What is the relationship between Age Groups and the percentage of high-risk patients?
- How does Stress Level (on a scale of 1-10) directly correlate with the average Health Risk Score?
- What is the risk differential between individuals with a Healthy vs. Unhealthy Lifestyle Score?
- Which Geographical States are identified as high-risk hotspots, requiring immediate resource focus?
- Is there a significant gender disparity in heart attack risk distribution?

📊 Walkthrough of Key Visuals

The interactive Excel dashboard provides dynamic controls (Slicers) to allow drill-down analysis into specific risk factors :

- Visual (Pivot Chart)	Insight Delivered (Leveraging DAX Measures)	Key Finding
- KPI Scorecard	Presents the three core metrics for overall population health.Total Patients=10,000; High-Risk Baseline=30.07%
- Risk by Stress Level	Bar/Line chart demonstrating the incremental impact of stress.	Health Risk Score is highly correlated, rising from ≈8.0 (Stress 1) to ≈17.1 (Stress 10).
- HR By Age Group	Compares the percentage of high-risk patients across segmented age brackets.	Risk increases with age, with the 71+ bracket showing one of the highest risk percentages (≈31.67%).
- HR Score By Lifestyle	A comparison of the custom Health Risk Score based on lifestyle category.	Unhealthy Lifestyle patients have a significantly higher AVG_HealthRisk Score (≈12.87) than Healthy patients (≈11.81).
- High Risk By State	Map or Bar Chart identifying regional variation in risk concentration.	Identifies specific states (e.g., Chhattisgarh, Himachal Pradesh, Maharashtra) as high-risk clusters.

💡 Business Impact and Insights

- This Excel-based analytical solution provides a low-cost, high-impact tool for data-driven decision-making:
- Resource Allocation : Quickly guide the focus of public health spending toward the highest-risk geographical states.
- Preventative Strategy : Quantifiably justify health campaigns focused on stress reduction and lifestyle improvements.
- Targeted Screening : Prioritize clinical interventions and preventative screening for older, high-risk age demographics.

🚀 Future Enhancements

- Automate Data Load: Use VBA or Power Query (Get & Transform) within Excel to automate the loading and cleaning of new CSV data instead of manual refreshes.
- Advanced Statistical Modeling: Integrate Python/R through Excel's capability to run a formal machine learning model (e.g., Logistic Regression) and feed the resulting prediction scores back into the Excel Data Model.
- What-If Analysis: Create simple dynamic cells that allow a user to change key input factors (e.g., Stress Level) and see the immediate impact on the calculated risk scores.

