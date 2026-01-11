# VishwaOps MLOps Project Files Structure

This is a **sample project folder structure** for the VishwaOps MLOps lifecycle projects. You can use this for both the **layman cake project** and the **professional student intelligence project**.

```
VishwaOps_MLOps_Project/
│
├── README.md  # Complete lifecycle, diagrams, project explanation
├── data/
│   ├── raw/             # Raw collected data
│   ├── processed/       # Cleaned & preprocessed data
│   └── features/        # Feature engineered datasets
│
├── notebooks/
│   ├── 01_data_ingestion.ipynb
│   ├── 02_data_validation.ipynb
│   ├── 03_feature_engineering.ipynb
│   └── 04_model_training.ipynb
│
├── src/
│   ├── data_collection.py
│   ├── data_validation.py
│   ├── feature_engineering.py
│   ├── model_training.py
│   └── model_evaluation.py
│
├── models/
│   └── trained_model.pkl  # Serialized model
│
├── docker/
│   ├── Dockerfile
│   └── requirements.txt
│
├── kubernetes/
│   └── deployment.yaml
│
├── ci_cd/
│   └── github_actions.yml
│
├── monitoring/
│   └── prometheus_config.yml
│
└── docs/
    └── diagrams/  # ASCII or image diagrams
```

### **Notes:**

1. `data/` – store raw, cleaned, and feature datasets separately.
2. `notebooks/` – Jupyter notebooks for step-by-step learning.
3. `src/` – Python scripts for automation and modularity.
4. `models/` – save trained ML models.
5. `docker/` – Dockerfile and dependencies for containerization.
6. `kubernetes/` – YAML files for deployment.
7. `ci_cd/` – GitHub Actions or Jenkins pipelines for automation.
8. `monitoring/` – configuration for Prometheus / Grafana.
9. `docs/` – diagrams and project documentation.

---

This structure is flexible and **covers full MLOps lifecycle** so students/professionals can follow end-to-end workflow from **data ingestion → training → deployment → monitoring → retraining**.

