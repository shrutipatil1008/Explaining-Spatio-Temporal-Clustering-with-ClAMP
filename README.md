🧠 Explaining Spatio-Temporal Clustering with ClAMP

Master’s Thesis Project — Hof University of Applied Sciences, 2025

Overview
This research explores how Explainable Artificial Intelligence (XAI) can enhance the interpretability of clustering algorithms, focusing on spatio-temporal data. The project adapts the Cluster Analysis with Multidimensional Prototypes (ClAMP) framework to a real-world mobility dataset (Hofer LandBus) to make clustering results explainable through human-readable rules.

🚀 Objectives
- Apply the ClAMP framework to real-world spatio-temporal data.
- Adapt clustering and rule-generation phases for noisy, irregular datasets.
- Generate interpretable, rule-based explanations for clusters.
- Evaluate rule quality using F1-score, precision, recall, and accuracy.

🧩 Methodology
The project follows the four-phase ClAMP process:
1. Clustering: Using ST-DBSCAN to identify spatial-temporal clusters.
2. Classification: Reformulating clusters as a classification problem via XGBoost.
3. Prototype Generation: Selecting representative points using Random, KD-Tree, and Isolation Forest methods.
4. Rule Generation: Creating interpretable if-then rules with the Anchor Explainer and validating them using HeaRTDroid.

📊 Dataset
1. Source: Hofer LandBus (Germany)
2. Records: ~63,000 rides
3. Features: Start & end locations, timestamps, derived temporal variables (duration, frequency)
4. Spatial Reference: EPSG:3035 (ETRS-LAEA Europe)

🧮 Results Summary
- High-quality rule generation for top-performing clusters (F1 up to 0.88).
- Strong interpretability for dense, well-defined clusters.
- Challenges remain for small or overlapping clusters — addressed with hybrid prototype strategies.

🛠️ Technologies
- Python (pandas, scikit-learn, alibi, matplotlib)
- PostgreSQL (pgAdmin) for data retrieval
- XGBoost for classification

📈 Key Insights
- ClAMP’s modular design enables explainable clustering across domains.
- Combining Random + KD-Tree prototypes offers the best balance of interpretability and accuracy.
- Rule-based explanations bridge the gap between AI outputs and human understanding — especially useful for decision-support systems in transport analytics.

🧩 Future Work
- Extend ClAMP to trajectory-level clustering.
- Integrate visual dashboards for interactive rule inspection.
- Apply the approach to other domains like urban planning or environmental monitoring.

HeaRTDroid & HMR+ for rule inference

OpenStreetMap for visualizations
