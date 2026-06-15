# Task 1 — ML Classification Project
## Telco Customer Churn Prediction
**Alfido Tech Data Science Internship**

---

## 📌 Problem Statement
Build and evaluate a supervised classification model to predict whether a customer will churn (leave the service) based on their account information and usage patterns.

## 📊 Dataset
- **File:** `churn_data.csv`
- **Rows:** 1000 customers
- **Features:** 16 (tenure, contract type, monthly charges, etc.)
- **Target:** `Churn` (Yes / No)
- **Churn Rate:** ~32%

## 🤖 Models Used
1. **Logistic Regression** — A linear model, simple and interpretable
2. **Random Forest** — An ensemble of decision trees, handles non-linear patterns

## 📈 Metrics Reported
- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC

## 🗂️ Project Structure
```
alfido_task1/
├── churn_classification.ipynb   ← Main notebook (all code + outputs)
├── churn_data.csv               ← Dataset
├── requirements.txt             ← Exact package versions
├── README.md                    ← This file
├── plot_churn_distribution.png
├── plot_correlation_heatmap.png
├── plot_roc_curves.png
├── plot_confusion_matrices.png
├── plot_feature_importance.png
└── plot_metrics_comparison.png
```

## ⚙️ Environment Setup

### Step 1 — Install Python 3.10+
Download from: https://www.python.org/downloads/

### Step 2 — Install dependencies
```bash
pip install -r requirements.txt
```

### Step 3 — Run the notebook
```bash
jupyter notebook churn_classification.ipynb
```

Then click **"Run All"** from the Kernel menu.

## 📦 Package Versions
See `requirements.txt` for exact versions used.

Key packages:
- pandas==3.0.2
- numpy==2.4.4
- scikit-learn==1.8.0
- matplotlib==3.10.8
- seaborn==0.13.2

## 🔬 Methodology
1. **Data Preprocessing** — Drop ID column, encode categorical variables, handle missing values
2. **Train/Test Split** — 80% train / 20% test (stratified)
3. **Feature Scaling** — StandardScaler applied for Logistic Regression
4. **Model Training** — Both models trained independently
5. **Evaluation** — 5 metrics + 5-Fold Cross-Validation (ROC-AUC)
6. **Visualization** — 4 plots generated and saved

## ✅ Deliverables
- [x] Notebook with code, plots, and metrics
- [x] Data preprocessing with train/test split
- [x] Cross-validation (5-Fold StratifiedKFold)
- [x] Two algorithms compared (LR vs RF)
- [x] All 5 required metrics reported
- [x] Short report below

---

## 📝 Short Report

### Model Selection & Results

Both Logistic Regression and Random Forest were trained and evaluated on the Telco Churn dataset.

**Key Findings:**
- Random Forest generally outperforms Logistic Regression on ROC-AUC due to its ability to capture non-linear relationships
- Cross-validation confirms that Random Forest generalises better across different data splits
- The most important features for predicting churn are: `tenure`, `MonthlyCharges`, `Contract` type, and `TotalCharges`

**Selected Model: Random Forest**
- Reason: Higher ROC-AUC and F1 score, more robust across cross-validation folds
- Practical benefit: Can rank customers by churn probability, enabling targeted retention campaigns

### Business Implication
Customers on Month-to-month contracts with short tenure and high monthly charges are at highest risk of churning. Targeting these customers with retention offers could significantly reduce churn.
