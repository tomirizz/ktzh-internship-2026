# KTZh Passenger Operations — Revenue & Demand Analytics

**Astana IT University** | Big Data Analysis | Internship 2026  
**Student:** Tomiris Alimova, BDA-2408  
**Organization:** JSC "Passenger Transportation" (АО «Пассажирские перевозки»), Department of Information Technology  
**Period:** June 8 – July 4, 2026

---

## Project Overview

End-to-end analytics pipeline applied to one day of operational ticketing data from the KTZh railway network. The goal was to convert a raw transactional export into actionable insights on revenue concentration, demand timing, and sales-channel performance.

## Notebook

[`notebooks/Tomiris_Revenue_Demand_Analysis.ipynb`](notebooks/Tomiris_Revenue_Demand_Analysis.ipynb)

**Contents:**
1. Imports & Configuration
2. Data Loading
3. ETL — Cleaning & Preprocessing (missing values, IQR outlier removal, type casting)
4. Feature Engineering & Load (label encoding, feature matrix assembly)
5. Exploratory & Statistical Analysis
   - Revenue concentration by service class
   - Peak-demand timing (hourly heatmap)
   - Route profitability & channel performance
6. Predictive Modeling
   - Linear Regression (baseline)
   - Random Forest (R² ≈ 0.62)
   - XGBoost (best — R² ≈ 0.64, MAE ≈ 2,824 KZT)
   - K-Means clustering (passenger segmentation, silhouette ≈ 0.47)
   - Logistic Regression (payment type, ROC-AUC ≈ 0.70)
7. Results & Business Recommendations

## Repository Structure

```
ktzh-revenue-demand-analysis/
├── data/
│   └── ktzh_operations_dataset.csv   # Operational ticketing export (17,590 records × 24 fields)
├── notebooks/
│   └── Tomiris_Revenue_Demand_Analysis.ipynb
├── reports/                           # Internship report (DOCX/PDF)
├── requirements.txt
└── README.md
```

## Dataset

File: `data/ktzh_operations_dataset.csv`  
Records: 17,590 rows × 24 columns  
Source: Operational ticketing system, JSC "Passenger Transportation", 2025

Key fields: `operation_type`, `price`, `service_class`, `payment_type`, `sales_channel`, `carrier`, `departure_station`, `arrival_station`, `gender`, `op_hour`, `lead_days`

> The dataset is provided for academic internship purposes only.

## How to Run

```bash
git clone https://github.com/<your-username>/ktzh-revenue-demand-analysis.git
cd ktzh-revenue-demand-analysis
pip install -r requirements.txt
jupyter notebook notebooks/Tomiris_Revenue_Demand_Analysis.ipynb
```

Run all cells in order to reproduce every figure, metric, and table from the internship report.

## Supervisor

**Workplace advisor:** Aziz Kanatuly, System Administrator, Department of Information Technology  
**AITU advisor:** Moldir Toleubek
