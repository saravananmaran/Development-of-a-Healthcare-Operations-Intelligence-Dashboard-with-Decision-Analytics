# Development of a Healthcare Operations Intelligence Dashboard with Decision Analytics

A data analytics and business intelligence project that converts raw hospital operational data — admissions, discharges, bed occupancy, staffing, and treatment demand — into a centralized, interactive decision-support dashboard for healthcare administrators.

The platform combines SQL-based data analysis, Python/Scikit-learn machine learning models, and a Power BI dashboard to move from descriptive reporting ("what happened") to predictive and decision analytics ("what will happen" and "what should we do about it").

## Project Overview

Hospitals generate operational data across admissions, discharges, treatments, departments, beds, and staff activities. When this data sits in disconnected spreadsheets or tables, spotting trends and operational problems quickly becomes difficult. This project builds a centralized analytics pipeline that cleans and analyzes hospital operations data and presents the results through an interactive dashboard, supported by machine learning models for forecasting, risk classification, segmentation, and anomaly detection.

## Repository Contents

| File | Description |
|---|---|
| `Model_Research_and_Selection_Saravanan.docx` | Research document comparing candidate ML models (time-series forecasting, Random Forest, XGBoost, K-Means, Isolation Forest, SHAP, etc.) against project requirements, with the final selected model stack and justification. |
| `TeamB_Feature_Document_MongoDB.docx` | Team B's feature and module document, covering the full dashboard scope (patient operations, billing, claims, AI/predictive intelligence, security, integrations) and the MongoDB-based data architecture decision. |
| `SQL_TASK.ipynb` | SQL-based analysis notebook — KPI calculations and operational queries (e.g., admissions by month, bed occupancy by department, length-of-stay analysis). |
| `Python_Task.ipynb` | Python notebook for data cleaning, exploratory data analysis, and model implementation. |

## Selected Machine Learning Models

Based on the research in `Model_Research_and_Selection_Saravanan.docx`, six models form the core analytics pipeline:

1. **Time-Series Forecasting** — forecasts future patient admissions and treatment demand
2. **Random Forest Regression** — predicts continuous operational metrics (bed occupancy, length of stay)
3. **Random Forest Classification** — classifies operational risk as Low / Medium / High
4. **K-Means Clustering** — groups hospitals/departments into operational segments
5. **Isolation Forest** — detects anomalous operational patterns and bottlenecks
6. **SHAP Explainability** — explains the factors driving each prediction

## Technology Stack

- **Languages & Libraries:** Python, Pandas, NumPy, Scikit-learn, SHAP
- **Database:** MongoDB (Team B) — see `TeamB_Feature_Document_MongoDB.docx` for data model and architecture details
- **Query & Analysis:** SQL (see `SQL_TASK.ipynb`)
- **Visualization:** Power BI

## Analytics Pipeline

```
Healthcare Operational Data
        │
        ▼
Data Cleaning & Preprocessing
        │
        ▼
Exploratory Data Analysis
        │
        ▼
Feature Engineering
        │
        ▼
Time-Series Forecasting → Random Forest Regression → Random Forest Classification
        │
        ▼
K-Means Clustering → Isolation Forest → SHAP Explainability
        │
        ▼
Decision Analytics
        │
        ▼
Power BI Dashboard
```

## Project Scope

This is an academic/prototype implementation. Synthetic or anonymized data is used throughout — no real patient identifiers are stored — and predictions are treated as operational planning indicators rather than clinical or medical recommendations.

## Status

🚧 In development — research and modeling phase complete; dashboard and full pipeline implementation in progress.
