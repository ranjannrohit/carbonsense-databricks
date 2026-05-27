<div align="center">

# 🌍 CarbonSense

### Revealing the True Carbon Cost of Economic Growth using AI on Databricks

<img src="https://readme-typing-svg.herokuapp.com?font=Poppins&weight=600&size=22&duration=3000&pause=1000&color=2ECC71&center=true&vCenter=true&width=700&lines=Databricks+Lakehouse+%2B+AI+Analytics;Climate+Intelligence+Platform;Carbon+Inefficiency+Detection;Built+using+Delta+Lake+%7C+MLflow+%7C+PySpark" />

<br>

![Databricks](https://img.shields.io/badge/Databricks-Lakehouse-red?style=for-the-badge&logo=databricks)
![PySpark](https://img.shields.io/badge/PySpark-BigData-orange?style=for-the-badge&logo=apachespark)
![MLflow](https://img.shields.io/badge/MLflow-Tracking-blue?style=for-the-badge)
![Delta Lake](https://img.shields.io/badge/Delta-Lake-green?style=for-the-badge)

</div>

---

## 🚀 Project Summary

CarbonSense is an **end-to-end Databricks Lakehouse + AI analytics solution** designed to measure **carbon inefficiency across emission sources and countries.**

Instead of reporting only absolute CO₂ emissions, CarbonSense applies **Machine Learning** to estimate expected emissions using economic and energy indicators and compares them with actual emissions.

### Insights Generated

❌ Carbon-inefficient sectors and countries

✅ Carbon-efficient best practices

🎯 Priority areas for climate intervention

The project demonstrates how **Databricks + Delta Lake + ML + SQL analytics** can build a real-world climate intelligence system.

---

## 🎯 Problem Statement

Traditional climate analysis focuses only on total emissions.

This ignores economic scale.

### ❓ Core Question

**Is a country or sector emitting more CO₂ than expected given its economic activity?**

### ✅ Solution

CarbonSense introduces:

🟥 Positive Carbon Gap → Carbon-inefficient

🟩 Negative Carbon Gap → Carbon-efficient

This enables fair comparison across sectors and countries.

---

## 🤖 Why AI?

Rule-based systems cannot capture complex relationships between:

- GDP
- Energy Consumption
- Sector Emissions

AI enables:

✔ Dynamic emission estimation

✔ Fair benchmarking

✔ Actionable climate intelligence

---

# 🏗 Architecture Overview

## Databricks Lakehouse (Medallion Architecture)

<div align="center">

```text
OWID Dataset
      ↓
🟤 Bronze Layer
(Raw Delta Tables)

      ↓

⚪ Silver Layer
(Cleaning + Structuring)

      ↓

🟡 Gold Layer
(Feature Engineering)

      ↓

🤖 ML Regression

      ↓

Predictions → Delta Tables

      ↓

📊 Databricks SQL Dashboard
```

</div>

---

## 📸 Architecture Diagram

<p align="center">
<img width="900" src="architecture/lakehouse_architecture.png">
</p>

---

## 🤖 Machine Learning Component

| Component | Details |
|-----------|----------|
| Task | Regression |
| Model | Linear Regression |
| Features | GDP, Energy per capita |
| Target | Sector-level CO₂ emissions |
| Metric | RMSE |
| Score | 17829 |

> CO₂ values exist at very large scale.  
> Goal = relative carbon gap analysis rather than exact prediction.

---

## 🔄 Database ↔ AI Workflow

```text
Raw Data

↓

Delta Bronze

↓

Silver Cleaning

↓

Gold Features

↓

ML Training

↓

Prediction Storage

↓

SQL Dashboard
```

Predictions persist back into Delta tables enabling downstream analytics.

---

# 📊 Analytics Dashboard

(Built using Databricks SQL)

### KPI Insights

📌 Average Global Carbon Inefficiency

📌 % Emissions exceeding AI expectation

📌 Most carbon inefficient sector

📌 Most carbon efficient sector

---

### Visual Analytics

📈 Actual vs Expected CO₂

📊 Carbon efficiency by source

🌍 Carbon inefficient countries

🥧 Sector contribution analysis

---

## Dashboard Preview

<p align="center">
<img width="1000" src="architecture/dashboard_preview.png">
</p>

---

# 🌱 Business Impact

## 👥 Users

🏛 Government policy teams

🌿 ESG analysts

🔬 Climate researchers

⚡ Energy planners

---

## 🧠 Decisions Enabled

✔ Identify sectors needing intervention

✔ Benchmark efficient industries

✔ Prioritize climate action

✔ Support policy decisions

---

# 🛠 Tech Stack

<div align="center">

| Technology | Usage |
|------------|-------|
| Databricks | Lakehouse Platform |
| Delta Lake | Storage |
| PySpark | Data Engineering |
| Spark MLlib | ML |
| Databricks SQL | Dashboards |
| MLflow | Tracking |
| GitHub | Version Control |

</div>

---

# ▶ Project Workflow

| Notebook | Purpose |
|----------|----------|
| 01_bronze_ingestion | Raw ingestion |
| 02_silver_cleaning | Cleaning |
| 03_gold_feature_engineering | Features |
| 04_model_training | ML |
| 05_predictions | Carbon Gap |
| 06_dashboard_queries | SQL |

---

# 📚 Key Learnings

✅ End-to-end Lakehouse architecture

✅ Climate intelligence using AI

✅ Databricks SQL analytics

✅ ML-powered insight generation

✅ Real-world sustainability use case

---

# 🧑‍💻 Author

## Rohit Ranjan

Aspiring Data Analyst | Data & AI Enthusiast

---

# 🔗 Links

GitHub Repository: 

LinkedIn Post: https://www.linkedin.com/posts/rohitranjann_databricks-codebasics-indiandataclub-activity-7423925075030126592-gaQN?utm_source=social_share_send&utm_medium=member_desktop_web&rcm=ACoAAFcIbbkByZzSFMtHqHWq4_uKsPKjB6m6be4

---

<div align="center">

### 🌍 CarbonSense — Turning Data into Climate Intelligence

</div>
