# Power-BI-Project---Analyzing-Customer-Churn
**Overview**

A Power BI analysis examining customer churn patterns, with a focus on contract types, demographic segmentation, and the relationship between customer service interactions and churn behaviour. This project demonstrates foundational Power BI competencies: DAX measure creation, data transformation, and insight visualization.

**Skills Demonstrated**

DAX Measures & Calculations


Contract Type Categorization: Used SWITCH logic to group contract types into billing frequency categories


dax  SWITCH('Databel - Data'[Contract Type], 
    "One Year", "Yearly", 
    "Two Year", "Yearly", 
    "Monthly")

This measure simplifies granular contract types into meaningful billing cycles for trend analysis.


Demographic Segmentation: Built nested IF logic to categorize customers by age profile


dax  IF('Databel - Data'[Senior]="Yes", "Senior",
    IF('Databel - Data'[Under 30]="Yes", "Under 30", "Other"))

Enables comparison of churn behaviour across age cohorts without cluttering visuals with raw values.


Churn Rate %: Calculated churned customer ratio as a percentage metric for key performance monitoring


**Data Transformation**


Created new columns for customer insights, enabling segmentation without modifying source data
Structured categorical logic (contract types, age groups) to support pivot and filtering operations
Organized measures to isolate calculated fields from dimension tables


**Visualizations & Insights**


Churn Trend Line: Tracked churn rate over time to identify seasonal or cumulative patterns
Churn by Region: Compared regional performance to pinpoint geographic risk areas
Customer Service Calls vs. Churn Rate: Explored the correlation between support interaction frequency and customer retention


**Key Insights**


Churn patterns vary significantly by contract type and customer demographic
Regional disparities suggest localized retention challenges
Service call volume shows meaningful relationship with churn outcomes



**How to Use This Project**


Open Customer_Churn_Rate_Report.pbix in Power BI Desktop
Navigate through report pages to explore churn trends by dimension
Use slicers to filter by contract type, region, or demographic group
Examine measure calculations in the Data Model to understand DAX logic


**What This Demonstrates for Procurement Roles**

While this analysis focuses on customer retention, the underlying Power BI techniques directly transfer to procurement use cases:


Segmentation logic (SWITCH, nested IF) applies to supplier categorization by performance tier, contract type, or risk level
Trend visualization supports cost variance tracking, lead time performance, and on-time delivery monitoring
Correlation analysis can reveal relationships between vendor metrics and business outcomes (e.g., quality issues vs. order delays)



