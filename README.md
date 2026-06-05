# Explaining Spatio-Temporal Clustering with ClAMP

**Master's Thesis — Hochschule Hof, University of Applied Sciences, 2025**  
**Author:** Shruti Patil · [LinkedIn](https://linkedin.com/in/shrutipatil1008) · [Email](mailto:shrutipatil10898@gmail.com)

---

## Overview

This project applies the **ClAMP (Cluster Analysis with Multidimensional Prototypes)** framework
to real-world mobility data to make spatio-temporal clustering results explainable through
human-readable if-then rules.

The core question: *can we explain why a trip belongs to a given mobility cluster — in terms
a transport planner can actually understand?*

---

## Methodology

The project follows the four-phase ClAMP pipeline:

```
Raw Mobility Data
        │
        ▼
Phase 1 ── Data Preprocessing ──────── Feature engineering, time scaling
        │
        ▼
Phase 2 ── Clustering Analysis ─────── ST-DBSCAN (final), vs OPTICS & HDBSCAN
        │
        ▼
Phase 3 ── Classification & Prototypes  Random Forest, prototype selection strategies
        │
        ▼
Phase 4 ── Rule Generation & Evaluation Anchor Explainer + HeaRTDroid validation
```

---

## Dataset

**Hofer LandBus** regional transport data — ~63,000 trips, Landkreis Hof, Germany.

> ⚠️ Raw data is confidential. See [`data/README.md`](data/README.md) for schema  
> and instructions to substitute your own dataset.

---

## Key Results

| Metric | Value |
|---|---|
| Final clustering algorithm | ST-DBSCAN (eps1=500m, eps2=3600s) |
| Outlier rate | 5.5% (start points) |
| Classifier accuracy (Random Forest) | 99.42% |
| Max rule F1 score | **0.88** |
| Best prototype strategy | Random + KD-Tree combination |

---

## Notebooks

Run in order:

| # | Notebook | Description |
|---|---|---|
| 01 | [`01_data_preprocessing.ipynb`](notebooks/01_data_preprocessing.ipynb) | Data loading, time feature engineering, EDA |
| 02 | [`02_clustering_analysis.ipynb`](notebooks/02_clustering_analysis.ipynb) | ST-DBSCAN parameter sweep, OPTICS/HDBSCAN comparison, evaluation |
| 03 | [`03_classification_prototypes.ipynb`](notebooks/03_classification_prototypes.ipynb) | Random Forest classifier, prototype selection (Random, KD-Tree, IsoForest) |
| 04 | [`04_rule_generation_evaluation.ipynb`](notebooks/04_rule_generation_evaluation.ipynb) | Anchor Explainer rules, filtering, quality evaluation, visualisation |

---

## Installation

```bash
git clone https://github.com/shrutipatil1008/Explaining-Spatio-Temporal-Clustering-with-ClAMP.git
cd Explaining-Spatio-Temporal-Clustering-with-ClAMP

pip install -r requirements.txt
```

---

## Technologies

| Category | Tools |
|---|---|
| Data processing | Python, pandas, NumPy, GeoPandas |
| Clustering | ST-DBSCAN, HDBSCAN, OPTICS (scikit-learn) |
| Classification | XGBoost, Random Forest (scikit-learn) |
| Explainability | Alibi AnchorTabular |
| Rule inference | HeaRTDroid + HMR+ |
| Visualisation | Matplotlib, Seaborn, OpenStreetMap |
| Database | PostgreSQL (pgAdmin) |

---

## Project Structure

```
├── notebooks/
│   ├── 01_data_preprocessing.ipynb
│   ├── 02_clustering_analysis.ipynb
│   ├── 03_classification_prototypes.ipynb
│   └── 04_rule_generation_evaluation.ipynb
├── data/
│   └── README.md               ← Data schema & access info
├── results/
│   └── README.md               ← Output file index
├── requirements.txt
├── .gitignore
└── README.md
```

---

## Citation

If you use this work, please cite:

> Patil, S. (2025). *Explaining Spatio-Temporal Clustering for Mobility Data with ClAMP.*  
> Master's Thesis, Hochschule Hof — University of Applied Sciences, Germany.
