


##IBM HR Attrition & Sentiment Intelligence Dashboard

> **An end-to-end People Analytics solution identifying high-risk turnover drivers using Power BI, DAX, and automated ETL.**

![Dashboard Overview](./IBM%20HR%20DASHBOARD%20Screenshot.png)

##Project Overview
This project transforms raw HR data (1,470 records) into actionable intelligence. By correlating compensation, overtime, and role-based satisfaction, this dashboard isolates **why** employees leave and quantifies the **financial impact** of that turnover.

## Key Insights
* **Turnover Hotspot:** Sales Representatives exhibit the highest attrition intensity, specifically correlated with high overtime frequency.
* **Financial Impact:** Identified an average monthly salary loss of **$4.9K per departed employee**, providing a clear target for retention ROI.
* **Predictive Drivers:** Analysis reveals that "Overtime" is the single strongest predictor of attrition across high-volume roles (Sales and Lab Technicians).

## Technical Implementation
* **Data Modeling:** Cleaned and transformed the `HREmployee.csv` dataset using **Power Query**, ensuring 100% data integrity and correct data types for time-series analysis.
* **DAX Engineering:** Developed custom DAX measures for complex KPIs, including:
  * `Attrition Rate %` (Total Attrition / Total Employees)
  * `Average Monthly Attrition Income` (Calculating revenue/salary leak)
* **Interactive UX:** Implemented a standardized vertical filter pane (Slicers) for real-time drill-down into Department, Education, and Gender demographics.
* **Visual Storytelling:** Utilized a **Correlation Heatmap** and dual-axis combo charts to highlight the gap between staff volume and attrition spikes.

## Repository Structure
* `IBM HR Dashboard.pbix`: The complete Power BI source file.
* `HREmployee.csv`: The underlying IBM HR dataset used for the analysis.
* `Untitled.png`: A high-resolution preview of the final dashboard.

## Video Walkthrough
*If you recorded a narrated video, add the link here!*
[Watch the 90-second technical demo](LINK_TO_YOUR_VIDEO)

---
### Contact
**Ryan Gillespie** [LinkedIn](YOUR_LINKEDIN_URL) | [Portfolio](YOUR_PORTFOLIO_URL)


Data obtained from Kaggle: https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset/data


Dax Measured used: 

Attrition Rate = DIVIDE([Total Attrition],[Total Employees])

Avg Job Satis. = AVERAGE(HREmployee[JobSatisfaction])

Avg Monthly Attrition Income = CALCULATE(AVERAGE(HREmployee[MonthlyIncome]),HREmployee[Attrition] = "Yes")

Avg Monthly Income = AVERAGE(HREmployee[MonthlyIncome])

Total Attrition = SUM(HREmployee[Attrition Count])

Total Employees = COUNTROWS('HREmployee')





