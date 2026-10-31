# Churn_Analysis-and-Customer_Intelligence
# 📊 Customer Churn Analysis – Complete Data Analytics Project

![Project](https://img.shields.io/badge/Project-Customer%20Churn%20Analysis-blue)
![Python](https://img.shields.io/badge/Python-Data%20Analysis-yellow)
![SQL](https://img.shields.io/badge/SQL-Database-orange)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Cleaning-purple)
![Status](https://img.shields.io/badge/Status-Portfolio%20Project-success)

# 1. Project Overview

Customer Churn Analysis is a data analytics project focused on understanding why customers stop using a company's products or services.

In the highly competitive OTT industry (Netflix, Hotstar, Prime Video), customer retention is essential for business survival.

In this project, the role of a Data Analyst is to identify high-risk subscribers using a multidimensional dataset containing:

- Customer Demographics
- Subscription Information
- Customer Support and Escalations

The project analyzes customer behavior, subscription patterns, churn risk, customer complaints, and revenue impact to generate actionable business insights.

This is not just a coding exercise; it is a business solution applicable to E-commerce, SaaS, Fintech, and Adtech industries.

# 2. Business Challenge

The main business challenge is to identify customers who are likely to leave the subscription platform and understand the reasons behind their decisions.

The analysis focuses on three important questions:

- **Who:** Identifying which customers have left or may leave in the future.
- **Why:** Analyzing customer behavior before they leave.
- **When:** Identifying the danger zone or point at which a customer is likely to leave.

# 3. Churn Definition by Business

Churn analysis is the process of identifying why customers stop doing business with a company.

Churn definitions vary depending on the business industry.

| Business Type | Churn Definition |
|---|---|
| SaaS | Subscription canceled |
| E-commerce | No purchase in 90 days |
| Adtech | Using service/app in 90–120 days |
| Streaming | Membership inactive |
| Telecom | Account terminated |
| Banking | No transactions for X months |

# 4. Core Technology Stack

The project uses the following technologies and analytical techniques:

### Programming and Database
- SQL
- Python
- SQLite3

### Python Libraries
- NumPy
- Pandas
- Matplotlib
- Seaborn

### Analytical Techniques
- Data Cleaning
- Feature Engineering
- Exploratory Data Analysis (EDA)
- Data Aggregation
- Customer Segmentation
- Behavioral Visualization
- Performance Engineering
- Actionable Business Insights

# 5. Project Milestones

The project consists of three major milestones.

### 5.1 Relational Data Extraction

- Connecting Python to SQL databases.
- Extracting data from multiple relational tables.
- Combining customer, subscription, and support information.

### 5.2 Advanced Feature Engineering

- Importing and processing datasets.
- Calculating customer tenure.
- Calculating churn rates.
- Calculating customer age.
- Creating new analytical features.

### 5.3 Executive Reporting

- Translating technical findings into business insights.
- Identifying revenue risks.
- Presenting actionable recommendations.
- Preparing executive-level reports.

# 6. Database Structure

**Database Name:** `customer_churn`

The project database contains three major relational tables.

## 6.1 Customer Table – db_customer

| Column Name |
|---|
| customerid |
| name |
| country |
| State |
| gender |
| dob |
| interests |
| pincode |

This table contains customer demographic and personal information.

## 6.2 Subscription Table – db_subscription

| Column Name |
|---|
| customerid |
| subscription_start_date |
| subscription_type |
| Plan_type |
| contract_type |
| renewal_date |
| cancellation_date |
| cancellation_reason |
| monthly_charges |
| cltv |
| churn_score |

This table contains customer subscription details, contract information, charges, cancellation details, and churn-related metrics.

## 6.3 Support Table – db_support

| Column Name |
|---|
| customerid |
| complaint_date |
| Escalations |
| csat_score |
| col_1 |
| comment |

This table contains customer complaints, support escalations, customer satisfaction scores, and comments.

# 7. Churn Analysis Roadmap

The complete analytical workflow consists of the following steps.

## Step 1: Connect SQL Database to Python

- Connect the SQL database with Python.
- Use Pandas and SQLite3.
- Establish database connectivity.

## Step 2: Data Import

- Import data using SQL queries in Python.
- Use Pandas and SQLite3 for data extraction.

## Step 3: Data Cleaning

Libraries: NumPy and Pandas.

Tasks:
- Check and correct data types.
- Rename columns.
- Select specific columns.
- Perform quality checks (QCs).
- Handle missing and NULL values.

## Step 4: Feature Engineering

Libraries: NumPy and Pandas.

Tasks:
- Create new calculated columns.
- Perform data transformations.
- Apply filters.
- Calculate customer age.
- Calculate customer tenure.
- Create churn-related metrics.

## Step 5: Data Analysis

Libraries: NumPy and Pandas.

Techniques:
- Exploratory Data Analysis (EDA).
- Aggregation.
- Group By.
- Pivot Tables.
- Customer behavior analysis.

## Step 6: Data Visualization

Libraries:
- Matplotlib
- Seaborn

Create visualizations to identify churn patterns, customer segments, and revenue impact.

## Step 7: Insights and Presentation

Prepare a PowerPoint presentation containing:

- Key Business Insights.
- Important Findings.
- Recommended Next Steps.
- Business Impact.
- Results suitable for showcasing in a professional resume.

# 8. Calculated Metrics and KPI Formulas

The following KPIs are used to measure customer churn, retention, revenue, and support performance.

| KPI | Formula |
|---|---|
| Churn Rate | Churned Customers / Total Customers |
| Churn by Plan Type | Churn Rate GROUP BY plan_type (Basic/Standard/Premium) |
| Churn by State | Churn Rate GROUP BY country, state |
| Retention Rate | 1 - Churn Rate |
| ARPU | SUM(monthly_charges) / COUNT(active customerid) |
| Average Customer Tenure | AVG(DATEDIFF(cancellation_date OR NOW(), subscription_start_date)) |
| Revenue at Risk | SUM(monthly_charges) WHERE churn_score > 70 |
| Escalation Rate | SUM(escalations) / COUNT(complaints) × 100 |
| Average Complaints per Customer | COUNT(complaints) / COUNT(DISTINCT customerid) |
| Correlation: Escalations → Churn | Churn Rate WHERE escalations ≥ 1 vs 0 |

# 9. Key Business Insights

The following results are reported in the project analysis.

## 9.1 Overall Churn Performance

| Metric | Result |
|---|---:|
| Churn Rate | 28.6% |
| Retention Rate | 71.4% |

The overall customer churn rate is 28.6%, while 71.4% of customers are retained.

## 9.2 Subscription Plan Analysis

- Most of the churn comes from the Basic subscription plan.
- The report indicates that this does not create a major revenue impact.

## 9.3 Geographical and Monthly Analysis

- Most customer churn occurred in September 2024.
- Karnataka was identified as the most affected state.

## 9.4 Customer and Revenue Metrics

| Metric | Result |
|---|---:|
| Average Tenure | 1,451 Days |
| ARPU | Rs 18.8 |
| Total Revenue | 395 |
| Revenue Loss Due to Churn | 74 |
| CLTV Lost | 2,047 |
| Percentage of Revenue Loss | 18% |

## 9.5 Contract Type Analysis

| Contract Type | Churn Rate |
|---|---:|
| Monthly | 55.6% |
| Annual | 8.3% |

Monthly subscription customers have a significantly higher churn rate compared to annual subscription customers.

# 10. Business Recommendations and Action Items

Based on the findings, the following business actions are recommended.

### 10.1 Investigate Karnataka Churn

Investigate what happened in Karnataka:

- Was there any increase in subscription prices?
- Were there more customer complaints?
- Were there technical issues?
- Did any other operational problems affect customers?

### 10.2 Review Basic Subscription Plan

- Check whether the subscription price of the Basic plan was increased.
- Investigate whether any recent changes were made.
- Pay special attention to changes made during September.

### 10.3 Competitor Analysis

- Analyze competitor activities.
- Understand why customers are moving to competitors.
- Identify competitive pricing and service differences.

### 10.4 High-Risk Customer Retention

Focus on customers with High and Medium churn risk.

- Check their Lifetime Value (LTV).
- Prepare a priority list.
- Analyze their complaint history.
- Contact them through email, SMS, and phone calls.
- Resolve their issues to prevent customer loss.

# 11. Portfolio Project Summary

## 11.1 Churn and Revenue Impact – General Summary

Engineered an end-to-end churn analytics pipeline for an OTT subscription platform by integrating multi-table subscriber data across acquisition type, contract structure, and plan tier (20+ KPIs).

Uncovered a significant churn disparity between monthly and annual contract segments, quantified MRR leakage and CLTV erosion attributed to high-risk cohorts, and delivered a data-backed contract-migration retention strategy to reduce involuntary subscriber loss.

## 11.2 Risk Scoring and Segmentation

Developed a multi-dimensional churn risk scoring model by synthesizing subscription tenure, plan type, and support escalation signals across three relational tables (20+ KPIs).

Segmented the customer base into risk tiers using composite churn scores, exposed a significant lifetime value gap between churned and retained cohorts, and recommended prioritizing Premium annual-plan retention over Basic monthly acquisition to maximize long-term revenue yield.

## 11.3 Support Intelligence and Cancellation Analysis

**Status: Working on live data**

Performed cross-functional support-churn correlation analysis by joining complaint, escalation, and CSAT data with subscription records.

Identified that escalated support interactions were disproportionately concentrated among churned customers.

Decomposed cancellation drivers into:

- Competitor Switching
- Pricing Sensitivity
- Content Dissatisfaction

Translated findings into a prioritized product and pricing roadmap presented to the platform's growth team.

# 12. Portfolio Project Summary – Dataset-Based Results

## Churn and Revenue Impact (General Summary + Numbers from Dataset)

Engineered an end-to-end churn analytics pipeline for an OTT subscription dataset (20+ KPIs), identifying a 28.6% overall churn rate and surfacing that monthly-contract subscribers churned at 55.6%, which is 6.7 times the 8.3% annual-contract rate.

Directly attributed $73.94/mo in MRR leakage and $2,047 in CLTV erosion to six at-risk customers, enabling a targeted contract-migration retention strategy.

# 13. Project Skills and Learning Outcomes

Through this project, the following data analytics concepts and skills are covered:

- SQL Database Connectivity
- Multi-Table Data Extraction
- Python Programming
- Pandas Data Manipulation
- NumPy Numerical Analysis
- SQLite3 Database Integration
- Data Cleaning
- Data Quality Checks
- Missing Value Handling
- Data Type Conversion
- Feature Engineering
- Customer Age Calculation
- Customer Tenure Calculation
- Churn Rate Calculation
- Exploratory Data Analysis
- Group By and Aggregation
- Pivot Table Analysis
- Customer Segmentation
- Churn Risk Scoring
- Revenue Impact Analysis
- Customer Lifetime Value Analysis
- Customer Support Analysis
- Data Visualization
- Matplotlib and Seaborn
- Business Intelligence
- Actionable Business Recommendations
- Executive Reporting

# 14. Project Conclusion

Customer Churn Analysis demonstrates how data analytics can help subscription-based businesses understand customer behavior, identify churn risks, and measure the financial impact of customer loss.

By integrating customer demographics, subscription records, and support information, this project provides a comprehensive approach to customer churn analysis.

The analysis highlights the difference between monthly and annual subscription churn rates, identifies geographical and subscription-related churn patterns, and measures revenue loss and customer lifetime value erosion.

The project also demonstrates how SQL, Python, Pandas, NumPy, Matplotlib, and Seaborn can be used together to transform raw data into meaningful business insights.

The ultimate goal is to help businesses improve customer retention, reduce revenue loss, and make better data-driven decisions.

# 15. Final Project Roadmap – Original Checklist

The following is the complete roadmap checklist included in the project report:

- [x] Connect SQL database to Python using Pandas and SQLite3.
- [x] Import data using SQL queries in Python.
- [x] Perform data cleaning using NumPy and Pandas.
- [x] Check data types.
- [x] Rename columns.
- [x] Select specific columns.
- [x] Perform quality checks.
- [x] Handle missing and NULL values.
- [x] Perform feature engineering.
- [x] Create new calculated columns.
- [x] Perform data transformations.
- [x] Apply filters.
- [x] Perform data analysis.
- [x] Conduct EDA.
- [x] Perform aggregation and Group By operations.
- [x] Create Pivot Tables.
- [x] Perform data visualization using Matplotlib and Seaborn.
- [x] Prepare PowerPoint insights.
- [x] Identify key insights, next steps, and business impact.

---

## 👨‍💻 Author

**MD Subhan Khan**

**Project:** Customer Churn Analysis

**Domain:** OTT Subscription Analytics | Customer Intelligence | Data Analytics
