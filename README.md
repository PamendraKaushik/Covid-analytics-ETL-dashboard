# Covid-analytics-ETL-dashboard
# 🦠 AI-Powered COVID-19 Crisis Intelligence & Monitoring System

## 📌 Project Overview

This project builds an **end-to-end data analytics pipeline** that transforms raw COVID-19 datasets into **interactive dashboards, automated risk alerts, and AI-generated daily situation reports**.

The system integrates multiple pandemic datasets, performs data cleaning and feature engineering using SQL, visualizes insights using Power BI, and automates monitoring and reporting using **n8n and Generative AI**.

The objective of this project is to demonstrate how **data analytics and automation can support real-time monitoring of public health crises**.

---

# 📊 Dataset

The datasets used in this project were downloaded from **Kaggle** and include:

- COVID-19 confirmed cases
- State-wise testing data
- Vaccination statistics

These datasets contain information such as:

```
Date
State
Confirmed Cases
Deaths
Recovered
Testing Data
Vaccination Data
Population
```

---

# ⚙️ Tools & Technologies

| Category | Tools Used |
|--------|-------------|
| Data Engineering | PostgreSQL, SQL |
| Data Analysis | Excel |
| Visualization | Power BI |
| Automation | n8n |
| Programming | JavaScript |
| AI Integration | Google Gemini |
| Notification | Gmail SMTP |

---

# 🏗 Project Architecture

```
Raw COVID Data (CSV)
        ↓
Data Ingestion (PostgreSQL Staging Tables)
        ↓
SQL ETL Pipeline
        ↓
Clean Analytical Dataset
        ↓
Excel Exploratory Analysis
        ↓
Power BI Interactive Dashboard
        ↓
Automation Workflows (n8n)
        ↓
AI Generated Reports & Alerts
```

---

# 🔄 Data Pipeline

## 1️⃣ Data Ingestion

Raw datasets downloaded from Kaggle were imported into **PostgreSQL staging tables**.

Example staging tables:

```
covid_19_india_staging
covid_vaccine_statewise_staging
statewisetestingdetails_staging
```

These tables store raw data before transformation.

---

## 2️⃣ Data Cleaning & Transformation

The SQL ETL pipeline performs:

- data cleaning
- standardization of state names
- handling missing values
- data type conversions

Example transformations:

```
TEXT → INTEGER
TEXT → DATE
```

---

## 3️⃣ Feature Engineering

Important metrics were calculated:

### Daily New Cases

```
Daily Cases = Today Confirmed − Yesterday Confirmed
```

Using SQL window function:

```
LAG()
```

### Positivity Rate

```
Positive Tests / Total Tests
```

### Vaccination Rate

```
Total Vaccinated Population / Total Population
```

### Case Fatality Rate (CFR)

```
Deaths / Confirmed Cases
```

---

# 📈 Exploratory Data Analysis (Excel)

Excel was used for:

- pivot tables
- trend analysis
- metric validation
- exploratory data analysis

Key metrics analyzed:

```
Active Cases
Recovery Rate
Daily Growth Rate
```

---

# 📊 Power BI Dashboard

An interactive Power BI dashboard was built to visualize pandemic trends.

## Key KPIs

- Confirmed Cases
- Deaths
- Recovery Rate
- Vaccination Rate
- Positivity Rate

## Dashboard Features

- time-series analysis of infection trends
- state-wise comparisons
- vaccination progress monitoring
- dynamic filtering by state and time

---

# 🤖 Automation Workflows (n8n)

To enable real-time monitoring, automation workflows were implemented using **n8n**.

## Workflow 1 – Risk Detection System

This workflow detects high-risk states using SQL queries based on conditions such as:

- consecutive rise in daily cases
- high positivity rate
- vaccination stagnation

When a risk is detected, the workflow generates an alert.

---

## Workflow 2 – Daily Situation Report

This workflow generates an automated **daily COVID situation report**.

Steps:

1. read national and state datasets  
2. identify top affected states  
3. merge national and state statistics  
4. generate a natural-language report using AI  
5. send the report via email  

---

# 🧠 AI Integration

The project uses **Google Gemini (Generative AI)** to convert structured data into natural-language reports.

Example output:

```
India reported 38,353 new COVID-19 cases in the last 24 hours.
Kerala and Maharashtra remain the most affected states.
Vaccination progress continues steadily across the country.
```

---

# 📧 Automated Reports

The automation pipeline sends reports to stakeholders via email.

Reports include:

- national COVID statistics
- top affected states
- infection trends
- AI-generated insights

---

# 📊 Key Insights

Some observations from the analysis:

- Pandemic waves are clearly visible in time-series data.
- A small number of states contribute to the majority of cases.
- Higher vaccination rates are associated with improved recovery trends.

---

# 🚀 Business Impact

This project demonstrates how a **data-driven monitoring system** can support crisis management by:

- integrating multiple datasets
- providing real-time dashboards
- detecting outbreak signals automatically
- generating AI-powered health intelligence reports

Such systems can help decision-makers respond faster to emerging public health threats.



# 📌 Future Improvements

Potential enhancements include:

- integrating real-time data APIs
- implementing predictive models for case forecasting
- deploying dashboards on cloud platforms

---

# 👨‍💻 Author

**Pamendra Kaushik**

Data Analytics Project
