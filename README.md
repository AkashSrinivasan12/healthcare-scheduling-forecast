# Healthcare Patient Scheduling Forecast System

> **🔄 Repository Status: Code upload in progress — full implementation being added. Star this repo to get notified when complete.**

---

An end-to-end ML forecasting framework for healthcare operations scheduling — reducing patient exam wait time from **6 weeks to same-day availability** through predictive capacity optimization.

Built from a real production system deployed at a multi-doctor optometry clinic.

---

## What This Project Does

Traditional scheduling systems rely on static templates and manual adjustments. This system uses historical exam data, seasonal patterns, and operational signals to forecast daily demand — enabling same-day appointment availability without overstaffing.

**Production outcome:** Model validated by operations leadership and approved for deployment.

---

## Architecture

```
Raw Operational Data (SQL Server / SharePoint)
        │
        ▼
[ETL & Feature Engineering Pipeline]
  - Historical booking patterns
  - Doctor availability signals
  - Seasonal / day-of-week features
        │
        ▼
[XGBoost Forecasting Model] ←→ [MLflow Experiment Tracking]
  - Demand forecasting                - Run comparison
  - Capacity optimization             - Model registry
  - Anomaly flagging                  - Artifact storage
        │
        ▼
[FastAPI Prediction Endpoint]
  POST /forecast  →  { predicted_demand, recommended_slots }
        │
        ▼
[Streamlit Operations Dashboard]
  - Real-time scheduling view
  - Doctor-level capacity heatmap
  - Alert on demand spikes
```

---

## Tech Stack

| Component | Tool |
|---|---|
| Forecasting Model | XGBoost |
| Experiment Tracking | MLflow |
| Feature Engineering | Pandas, Scikit-learn |
| API | FastAPI |
| Dashboard | Streamlit |
| Containerization | Docker |

---

## Project Structure *(uploading)*

```
healthcare-scheduling-forecast/
├── data/               ← Synthetic healthcare scheduling dataset
├── notebooks/          ← EDA and model development
├── src/
│   ├── features.py     ← Feature engineering pipeline
│   ├── model.py        ← XGBoost training + MLflow tracking
│   └── predict.py      ← Inference utilities
├── api/
│   └── main.py         ← FastAPI endpoints
├── app/
│   └── dashboard.py    ← Streamlit scheduling dashboard
├── Dockerfile
└── requirements.txt
```

---

## Author

**Akash Srinivasan** — [LinkedIn](https://linkedin.com/in/akashsrinivasan12) | [GitHub](https://github.com/akashsrinivasan12)
