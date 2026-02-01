# 🌍 **CarbonSense**
## **Revealing the True Carbon Cost of Economic Growth using AI on Databricks**

---

## 🚀 **Project Summary**

**CarbonSense** is an end-to-end **Databricks Lakehouse + AI analytics solution** designed to measure **carbon inefficiency** across emission sources and countries.

Instead of only reporting absolute CO₂ emissions, this project uses **machine learning** to learn the *expected* CO₂ emissions based on economic and energy indicators and compares them with *actual* emissions to identify:

- ❌ Carbon-inefficient sectors and countries  
- ✅ Carbon-efficient best practices  
- 🎯 Priority areas for climate intervention  

The project demonstrates how **Databricks, Delta Lake, ML, and SQL analytics** can be combined to build a **real-world decision support system** for climate intelligence.

---

## 🎯 **Problem Statement**

Traditional climate analysis focuses on **absolute emissions**, which fails to account for economic scale.

### ❓ The Core Question
> *Is a country or sector emitting more CO₂ than it reasonably should, given its economic activity?*

### ✅ Solution Approach
CarbonSense introduces a new metric:


- **Positive Carbon Gap** → Carbon-inefficient (problematic)
- **Negative Carbon Gap** → Carbon-efficient (good performance)

This allows fair, data-driven comparison across sectors and countries.

---

## 🤖 **Why AI is Required**

Rule-based thresholds cannot capture the complex relationship between:
- GDP
- Energy consumption
- Sector-level emissions

AI enables:
- Learning expected emissions dynamically
- Comparing performance beyond raw totals
- Turning predictions into **actionable insights**

---

## 🏗️ **Architecture Overview**
### *(Databricks Lakehouse – Medallion Architecture)*


---

### 🟤 **Bronze Layer – Raw Data**
- Source: OWID CO₂ dataset
- Stored as Delta table


---

### ⚪ **Silver Layer – Cleaned & Structured**
- Sector-level emissions
- Country & year mapping
- Economic and energy indicators


Predictions are **persisted back to Delta**, enabling downstream analytics.

---

## 🤖 **Machine Learning Component**

- **ML Task:** Regression
- **Model Used:** Linear Regression (interpretable & explainable)
- **Features:**
  - GDP
  - Energy per capita
- **Target Variable:** Sector-level CO₂ emissions

### 📊 **Model Evaluation**
- Train/Test Split: 80/20
- Metric Used: **RMSE**
- RMSE Achieved: **17829**

> *Note:* CO₂ values are measured at large absolute scale; the objective is **relative deviation (carbon gap)**, not exact prediction accuracy.

---

## 🔄 **Database ↔ AI Workflow**

1. Raw data ingested into Delta tables
2. Features engineered in Gold layer
3. ML model trained on Gold data
4. Predictions written back to Delta
5. Databricks SQL dashboards consume prediction tables

This creates a **closed-loop Lakehouse + AI system**.

---

## 📊 **Analytics & Dashboards**
*(Built using Databricks SQL)*

### Key Insights Delivered:
- 📌 KPI: Average Global Carbon Inefficiency
- 📌 KPI: % of emissions exceeding AI-expected levels
- 📌 KPI: Most carbon-inefficient sector
- 📌 KPI: Most carbon-efficient sector
- 📈 Line Chart: Actual vs AI-Expected CO₂ emissions
- 📊 Bar Chart: Carbon efficiency by emission source
- 🌍 Bar Chart: Top carbon-inefficient countries
- 🥧 Pie Chart: Sector-wise contribution to global CO₂

All dashboards are powered directly from **Delta tables**, ensuring governance and consistency.

---

## 🌱 **Business Impact & Use Cases**

### 👥 Who Can Use This?
- Government climate policy teams
- ESG & sustainability analysts
- Climate research organizations
- Energy & industrial planners

### 🧠 Decisions Enabled:
- Identify sectors requiring emission controls
- Benchmark efficient industries
- Prioritize countries for climate intervention
- Support data-driven climate policy

---

## 🛠️ **Tech Stack**

- Databricks Lakehouse
- Delta Lake
- PySpark
- Spark MLlib
- Databricks SQL
- MLflow
- GitHub

---

## ▶️ **How to Run the Project (High-Level)**

1. Upload raw dataset to Databricks
2. Execute Bronze → Silver → Gold notebooks
3. Train ML model and generate predictions
4. Build SQL dashboards from Gold tables

---

## 📚 **Key Learnings**

- Designing an end-to-end Lakehouse architecture
- Applying ML for insight generation, not just prediction
- Using Databricks SQL for decision-grade analytics
- Converting data into real-world climate insights

---

## 🧑‍💻 **Author**

**Rohit Ranjan**  
Aspiring Data Analyst | Data & AI Enthusiast  

---

## 🔗 **Project Links**
- GitHub Repository: *(add link here)*
- LinkedIn Submission Post: *(add link after submission)*

---
