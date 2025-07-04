# 🚕 Uber Data Engineering Project

An end-to-end data pipeline built as a part of my data engineering portfolio. The pipeline ingests raw Uber trip data, transforms it into a star schema using Python and Mage, stores it in BigQuery, and visualizes 
business insights through Looker Studio dashboards.

---

## 🧠 Problem Statement

Businesses need real-time insights from raw trip data to understand user trends, optimize pricing, and improve city operations. The raw data is complex, unstructured, and not suitable for direct reporting.

---

## 🔧 Tech Stack

| Layer         | Tool/Service           |
|---------------|------------------------|
| **Orchestration** | Mage (Python-based pipelines) |
| **Storage**        | Google BigQuery             |
| **Transformations** | SQL, Python (Pandas)         |
| **Visualization** | Looker Studio               |
| **Credential Management** | Service Account JSON securely configured in `io_config.yaml` |


---

## 📦 Project Architecture

              ┌──────────────────────────────┐
              │     Raw Uber Trip Data       │
              └────────────┬─────────────────┘
                           │
                  Ingestion with Mage (Python)
                           │
            ┌──────────────▼─────────────┐
            │   Staging in BigQuery      │
            └──────────────┬─────────────┘
                           │
                  Transformations (Star Schema)
                           │
    ┌──────────────────────▼──────────────────────┐
    │       `fact_table` + Dimension Tables       │
    └──────────────────────┬──────────────────────┘
                           │
           Final Reporting Table (tbl_analysis_report)
                           │
                Consumed by Looker Studio



---
## 🧱 Data Pipeline Overview

```text
Raw CSV Data → Mage → Data Cleaning + Star Schema → BigQuery → Looker Studio
```

---

## ✅ Impact & Key Results

| Metric | Value |
|--------|-------|
| ⏱️ ETL Latency | < 2 minutes per pipeline run |
| 🧹 Data Cleanliness | 100% null-handling, data typing, and dimension mapping |
| 📊 Dashboard Metrics | 15+ business KPIs including vendor trends, fare analytics, trip distribution |
| 🧱 Star Schema | 1 Fact Table, 7 Dimension Tables |
| 🧪 Test Coverage | 100% column-level validation in transformation stage |

---







