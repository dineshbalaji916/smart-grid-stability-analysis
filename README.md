---

# Smart Grid Stability Prediction

##  Abstract

The transition from conventional power grids to smart grids has significantly improved sustainability and energy efficiency. However, integrating renewable energy sources alongside a complex web of interconnected devices poses challenges for maintaining grid stability.

This project applies machine learning techniques to tackle these stability challenges in two scenarios:

* Regression task: predicting continuous stability measures.
* Binary classification task: distinguishing between stable and unstable grid conditions.

To address class imbalance, the **SMOTE** method is applied. Various models—including tree-based classifiers, boosting algorithms, and ensemble learners—are evaluated.
Key findings:

* **XGBoost with SMOTE** achieved **99.97%** accuracy for instability detection.
* **Stacking ensemble** achieved **99.99%** accuracy for the regression task.
* Explainable AI (XAI) techniques (e.g., SHAP) were used to interpret the models and reveal the most influential features.

This project proposes robust approaches to improve grid stability, contributing to reliable and sustainable energy supply.

---

##  Dataset

The dataset is publicly available from the UCI Machine Learning Repository:
[Electrical Grid Stability Simulated Data](https://archive.ics.uci.edu/dataset/471/electrical+grid+stability+simulated+data)

* **Instances:** 10,000
* **Features:** 14
* **Target:** Binary (0 = stable, 1 = unstable)

---

##  Methodology

### 1️ Data Preprocessing

* Cleaned missing values, noise, and outliers.

### 2️ Data Balancing

* Applied **SMOTE** to improve minority class representation.

### 3️ Exploratory Data Analysis (EDA)

* Visualized feature distributions and correlations.

### 4️ Classification Models

* Trained multiple classifiers:

  * XGBoost, Logistic Regression, Bagging SVC, Naïve Bayes, KNN, QDA, LDA
* Best result: **XGBoost + SMOTE → 99.97% accuracy**

### 5️ Regression Models

* Trained regression models to predict stability scores:

  * Stacking, Voting, XGBoost
* Best result: **Stacking ensemble → 99.99% accuracy**

### 6️ Model Explainability

* Applied **SHAP (SHapley Additive exPlanations)** to interpret predictions.
* Most impactful features: `tau4` and `tau2` with SHAP values of 7.652 and 4.616 respectively.

---

##  Performance Metrics

For evaluation:

* Accuracy
* Precision
* Recall (Sensitivity)
* F1 Score
* R² Score
* RMSE
* MAE

---

##  Merits

* Addresses a critical and timely problem.
* Rigorous evaluation with multiple ML models and metrics.
* Transparent methodology and reproducible results.
* Demonstrates the benefits of XAI for model interpretability.
* Provides actionable insights for real-world grid operators.

##  Limitations

* Scalability concerns for larger, more complex grids.
* Limited handling of cyber-physical security threats.
* Dependence on historical data and its potential limitations.
* External factors (e.g., weather, economy) not fully captured.
* Continuous model maintenance not addressed in depth.

---

##  Conclusion & Future Work

This study demonstrates the potential of advanced machine learning models, achieving high accuracy in predicting smart grid stability. Future research directions include:

* Incorporating deep learning models.
* Improving model security against adversarial attacks.
* Enhancing resilience, reducing maintenance costs, and enabling early fault detection.

---

##  How to Run

1️ Clone this repository:

```bash
git clone https://github.com/<your-username>/smart-grid-analysis.git
cd smart-grid-analysis
```

2️ Open the notebook:
You can launch the notebook with:

```bash
jupyter notebook Smart_Grid.ipynb
```

or use [Google Colab](https://colab.research.google.com/) and upload the notebook.


---
