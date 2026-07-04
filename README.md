# Lab 2: Predictive Analytics with Machine Learning

**Duration:** 2 weeks [18 Jun – 25 Jun, 2026]  
**Due Date:** 25th June, 2026  
**Format:** Jupyter Notebook / Google Colab  
**Grading:** This is a graded lab.

---

## What this lab is about

This lab works through a machine learning workflow on two real datasets. The work covers both supervised and unsupervised learning across three tasks: predicting taxi tips (regression), predicting obesity level (multi-class classification), and grouping people by health profile (K-Means clustering). Along the way I used NumPy, Pandas, and scikit-learn to clean and explore the data, build features, split into train/validation/test sets, train models, and check for overfitting.

---

## Setup

```bash
python -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate
pip install -r requirements.txt
jupyter lab
```

For Google Colab, just open the notebook and run the cells — the datasets load from URLs so no Drive mount is needed.

---

## Files

| File | What it is |
|------|------------|
| `lab_2_predictive_analytics.ipynb` | Main notebook with all the work |
| `yellow_tripdata.csv` | NYC Yellow Taxi dataset (regression) |
| `Obesity_level_prediction_dataset (2).csv` | Obesity dataset (classification + clustering) |
| `requirements.txt` | Python packages needed |
| `lab_2.md` | Original lab instructions and grading rubric |

---

## Datasets

| # | Task | Dataset | Target |
|---|------|---------|--------|
| 1 | Regression | NYC Yellow Taxi trips | `tip_amount` |
| 2 | Classification | Obesity-level prediction | `NObeyesdad` (7 classes) |
| 3 | Clustering | Obesity features (no labels) | find groups |

Dataset URLs (used as fallback in Colab):
- Taxi: `https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/pu9kbeSaAtRZ7RxdJKX9_A/yellow-tripdata.csv`
- Obesity: `https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/GkDzb7bWrtvGXdPOfk6CIg/Obesity-level-prediction-dataset.csv`

---

## Sections

**Section 1 — Regression:** Load and explore the taxi data, clean invalid rows, engineer features (fare per mile, total surcharges), split 60/20/20, train LinearRegression and RandomForest, report RMSE and R² on all three splits.

**Section 2 — Classification:** Load and explore the obesity data, encode all categorical columns, add BMI as a feature, do a stratified 60/20/20 split, train a RandomForestClassifier, report accuracy and macro-F1 plus a confusion matrix.

**Section 3 — Clustering:** Ignore the labels entirely, use the elbow method and silhouette scores to pick k, fit K-Means, visualise clusters with PCA, then compare to the real obesity labels using a crosstab.

**Section 4 — Reflection:** Short written answers on supervised vs unsupervised learning, how regression and classification evaluation differ, and where overfitting showed up across the three tasks.

---

## Grading (100 pts)

| Area | Pts |
|------|-----|
| Section 1 — Regression | 30 |
| Section 2 — Classification | 30 |
| Section 3 — K-Means clustering | 20 |
| Reasoning boxes & reflection | 15 |
| Reproducibility (clean run, random_state, tidy code) | 5 |
