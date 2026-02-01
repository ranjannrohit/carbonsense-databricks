🌍 CarbonSense
Revealing the True Carbon Cost of Economic Growth using AI on Databricks
📌 Project Overview

CarbonSense is an end-to-end Databricks Lakehouse + AI analytics project that measures carbon inefficiency across emission sources and countries.

Instead of only reporting CO₂ emissions, this project uses machine learning to learn the expected CO₂ emissions based on economic activity (GDP, energy usage) and compares them with actual emissions to identify:

Carbon-inefficient sectors

Carbon-efficient best practices

Countries requiring urgent climate intervention

The solution is designed as a decision-support system for policymakers, sustainability teams, and climate researchers.

🎯 Problem Statement

Traditional carbon analysis focuses on absolute emissions, which does not account for economic scale.

Problem:
How can we identify whether a sector or country is emitting more CO₂ than it reasonably should, given its economic and energy activity?

Solution:
Train an AI model to learn expected CO₂ emissions and compute a Carbon Gap:

Carbon Gap = Actual CO₂ − AI-Expected CO₂


Positive Gap → Carbon-inefficient (problem)

Negative Gap → Carbon-efficient (good performance)

🧠 Why AI is Required

Rule-based thresholds cannot capture complex, non-linear relationships between:

GDP

Energy consumption

Sectoral emissions

AI enables:

Learning expected emissions dynamically

Comparing performance across countries and sectors

Turning predictions into actionable insights

🏗️ Architecture (Databricks Lakehouse)

Medallion Architecture used:

🟤 Bronze Layer

Raw OWID CO₂ dataset

Stored as Delta table

carbon_sense.bronze.co2_raw

⚪ Silver Layer

Cleaned & structured sector-level data

Key columns: country, year, sector, CO₂, GDP, energy

carbon_sense.silver.sector_metrics

🟡 Gold Layer

ML-ready features

carbon_sense.gold.ml_features


AI predictions written back to Delta

carbon_sense.gold.predictions

🤖 Machine Learning Component

Task: Regression (predict expected CO₂ emissions)

Model: Linear Regression (interpretable & explainable)

Features used:

GDP

Energy per capita

Label: Sector CO₂ emissions

🔍 Evaluation

Train/Test split: 80/20

Metric used: RMSE

RMSE achieved: 17829

Note: CO₂ values are measured at large absolute scale; the goal is relative deviation (carbon gap), not exact prediction.

🔄 Database ↔ AI Workflow

Data ingested into Delta tables

ML model trained on Gold features

Predictions written back to Delta

Databricks SQL dashboards consume prediction tables

Insights visualized for decision-making

📊 Analytics & Dashboard

Built using Databricks SQL Dashboards.

Key Visualizations:

KPI: Average Global Carbon Inefficiency

KPI: % of emissions exceeding AI-expected levels

KPI: Most carbon-inefficient sector

KPI: Most carbon-efficient sector

Line Chart: Actual vs AI-Expected CO₂ emissions

Bar Chart: Carbon efficiency by sector

Bar Chart: Top carbon-inefficient countries

Pie Chart: Sector-wise CO₂ contribution

Dashboards are powered directly from Delta tables, ensuring consistency and governance.

🌱 Business Impact & Use Cases
Who can use this?

Government climate policy teams

ESG & sustainability analysts

Climate research organizations

Energy & industrial planners

Decisions enabled:

Identify sectors requiring emission controls

Benchmark efficient industries

Prioritize countries for climate intervention

Support data-driven climate policy

🛠️ Tech Stack

Databricks Lakehouse

Delta Lake

PySpark

Spark MLlib

Databricks SQL

MLflow (experiment tracking)

GitHub

🚀 How to Run (High-Level)

Upload raw dataset to Databricks

Run Bronze → Silver → Gold notebooks

Train ML model and generate predictions

Build SQL dashboards from Gold tables

📌 Key Learnings

End-to-end AI + data engineering pipeline

Practical use of ML for insight generation

Databricks Lakehouse best practices

Turning predictions into decisions

🧑‍💻 Author

Rohit Ranjan
Aspiring Data Analyst | Data & AI Enthusiast

🔗 Links

GitHub Repository: (add link)

LinkedIn Post: (add after submission)
