# Credit Risk Prediction

An end-to-end Machine Learning project focused on predicting credit risk by identifying borrowers with a higher probability of loan default. This project covers the complete machine learning workflow, from data exploration and preprocessing to model development, evaluation, explainability, and interactive dashboard visualization.

## Project Overview

Credit risk prediction is an important part of financial risk management. By analyzing historical loan data, financial institutions can identify borrowers who may have difficulties repaying their loans.

This project aims to develop a classification model that distinguishes between:

- **Good Loan (0):** Borrowers categorized as lower credit risk.
- **Bad Loan (1):** Borrowers categorized as higher credit risk.

The goal is to support more informed credit risk assessment and lending decisions through data-driven analysis.

## Dataset

The project uses the `loan_data_2007_2014.csv` dataset.

| Description | Value |
|---|---:|
| Total Observations | 466,285 |
| Total Features | 75 |
| Duplicate Rows | 0 |

The dataset contains historical loan information, including borrower characteristics, loan details, and repayment status.

The target variable is constructed from loan status to represent binary credit risk classification.

*Note: The dataset is not included in this repository and must be obtained separately.*

## Project Workflow

The project follows an end-to-end machine learning workflow:

1. **Business Understanding** – Define the credit risk problem and prediction objectives.
2. **Exploratory Data Analysis (EDA)** – Explore data distributions, loan characteristics, and repayment patterns.
3. **Data Preprocessing** – Handle missing values, encode categorical variables, and prepare numerical features.
4. **Feature Engineering** – Construct the target variable and select relevant predictive features while considering potential data leakage.
5. **Model Development** – Build and compare multiple classification algorithms.
6. **Model Evaluation** – Evaluate model performance using various classification metrics.
7. **Threshold Optimization** – Optimize the classification threshold to balance precision and recall.
8. **Model Explainability** – Apply SHAP to understand feature contributions and model predictions.
9. **Dashboard Development** – Present analytical insights and model information through an interactive dashboard.

## Machine Learning Models

Three classification algorithms are implemented and compared:

| Algorithm | Description |
|---|---|
| Logistic Regression | Baseline classification model |
| XGBoost | Gradient boosting algorithm |
| LightGBM | Efficient gradient boosting framework |

XGBoost is selected as the main model candidate based on the benchmarking results discussed in the project.

## Model Evaluation

To evaluate model performance, several metrics are used:

- **ROC-AUC:** Measures the model's ability to distinguish between good and bad loans.
- **PR-AUC:** Evaluates the trade-off between precision and recall, particularly useful for imbalanced datasets.
- **Precision:** Measures the proportion of correctly predicted bad loans among all loans predicted as bad.
- **Recall:** Measures the proportion of actual bad loans successfully identified by the model.
- **F1-Score:** Provides a balance between precision and recall.
- **Confusion Matrix:** Shows the distribution of correct and incorrect predictions.

### XGBoost Performance

The selected XGBoost model reports the following performance:

| Metric | Score |
|---|---:|
| ROC-AUC | 0.7145 |
| PR-AUC | 0.4058 |

These metrics provide an overview of the model's ability to distinguish borrowers based on credit risk.

## Model Explainability (SHAP)

SHAP (SHapley Additive exPlanations) is used to interpret the model's predictions.

This approach helps identify:

- Features that have the greatest influence on credit risk predictions.
- How individual features contribute to increasing or decreasing predicted risk.
- The relationship between borrower characteristics and model outputs.

SHAP improves model transparency and helps make machine learning results more interpretable.

## Interactive Dashboard — Quantro Risk

This project also includes an interactive dashboard called **Quantro Risk**, designed to present credit risk analysis and model insights.

The dashboard provides several main features:

- **Overview & Dashboard:** Displays key information and summaries of the lending dataset.
- **Exploratory Data Analysis:** Visualizes borrower characteristics and loan patterns.
- **Risk Policy Simulator:** Allows exploration of different risk policy scenarios.
- **Applicant Risk Calculator:** Provides an interface for applicant risk assessment.
- **Model Benchmark & SHAP:** Presents model comparison and explainability insights.

## Repository Structure

```text
credit-risk-prediction/
│
├── Credit_Risk_Prediction_End_to_End.ipynb
├── dashboard.html
├── index.html
├── vercel.json
├── .gitignore
└── .vercelignore
```

| File | Description |
|---|---|
| `Credit_Risk_Prediction_End_to_End.ipynb` | Main notebook containing the complete data analysis and machine learning workflow. |
| `dashboard.html` | Interactive dashboard interface. |
| `index.html` | Main web application entry point. |
| `vercel.json` | Vercel deployment configuration. |

## Tools & Technologies

**Programming & Data Analysis**
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn

**Machine Learning**
- Scikit-learn
- XGBoost
- LightGBM

**Model Explainability**
- SHAP

**Dashboard & Deployment**
- HTML
- Tailwind CSS
- ApexCharts
- Lucide Icons
- Vercel

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/Kartika-Nur-Savira/credit-risk-prediction.git

cd credit-risk-prediction
```

### 2. Prepare the Dataset

Download the `loan_data_2007_2014.csv` dataset separately and place it in the appropriate working directory.

### 3. Install Dependencies

```bash
pip install numpy pandas matplotlib seaborn scikit-learn xgboost lightgbm shap
```

### 4. Run the Notebook

Open `Credit_Risk_Prediction_End_to_End.ipynb` using Jupyter Notebook, JupyterLab, or Google Colab.

Make sure the dataset path is correctly configured before executing the notebook.

### 5. Run the Dashboard

Open `index.html` in your web browser to explore the Quantro Risk dashboard.

An internet connection is required to load external front-end libraries through their CDNs.

## Project Purpose

This project demonstrates the application of machine learning in financial risk analytics, particularly in identifying potential loan defaults.

By combining predictive modeling, model evaluation, and explainable AI, this project aims to provide a more transparent and data-driven approach to credit risk assessment.

## Author

**Kartika Nur Savira**

GitHub: [Kartika-Nur-Savira](https://github.com/Kartika-Nur-Savira)
