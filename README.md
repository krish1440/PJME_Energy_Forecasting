# ⚡ PJME Energy Consumption Forecasting

![Python](https://img.shields.io/badge/Python-3.12-blue?style=for-the-badge&logo=python)
![XGBoost](https://img.shields.io/badge/XGBoost-Models-orange?style=for-the-badge)
![MLflow](https://img.shields.io/badge/MLflow-Tracking-blueviolet?style=for-the-badge)

An advanced end-to-end time series forecasting project focused on predicting hourly energy consumption for the PJM East region. This project leverages state-of-the-art machine learning algorithms and robust MLOps practices using MLflow.

---

## 🚀 Solution Overview

Predicting energy demand is critical for grid stability and resource allocation. This solution provides a comprehensive pipeline:
1.  **Data Ingestion**: Automated downloading of the PJM Hourly dataset.
2.  **Exploratory Data Analysis (EDA)**: Visualizing seasonality, trends, and outliers in electricity usage.
3.  **Feature Engineering**: Creation of time-based features (hour, day, month, quarter, lag features) to capture cyclical patterns.
4.  **Modeling**: Comparison between baseline Linear Regression and advanced ensemble methods (XGBoost, Random Forest).
5.  **Experiment Tracking**: Utilizing **MLflow** to log parameters, metrics (RMSE, MAE), and model artifacts for reproducibility.

---

## 📂 Repository Structure

| File | Description |
| :--- | :--- |
| `TimeSeriesForecastingProject_XGBoost_RandomForest.ipynb` | **Core Notebook**: Implementation of high-performance models (XGBoost & Random Forest) with MLflow instrumentation. |
| `TimeSeriesForecastingProject_preprocessing+linearregression.ipynb` | **Baseline Notebook**: Focuses on data cleaning, feature engineering, and Linear Regression benchmarks. |
| `PJME_hourly.csv` | **Dataset**: Hourly energy consumption data (MW) from 2002 to 2018. |
| `featured_data_sample.csv` | **Sample Data**: A snapshot of the dataset after feature engineering (used for quick validation). |
| `.gitignore` | Standard exclusion list for virtual environments, Python cache, and MLflow local storage. |

---

## 🛠️ Technology Stack

-   **Language**: Python 3.12
-   **Machine Learning**: XGBoost, Scikit-Learn (Random Forest, Linear Regression)
-   **Data Manipulation**: Pandas, NumPy
-   **Visualization**: Matplotlib, Seaborn, Plotly
-   **MLOps**: MLflow (Tracking UI, Model Logging)

---

## ⚙️ Setup & Installation

1.  **Clone the repository**:
    ```bash
    git clone https://github.com/krish1440/PJME_Energy_Forecasting.git
    cd PJME_Energy_Forecasting
    ```

2.  **Create a Virtual Environment**:
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use: venv\Scripts\activate
    ```

3.  **Install Dependencies**:
    ```bash
    pip install pandas numpy matplotlib seaborn xgboost scikit-learn mlflow
    ```

4.  **Run MLflow UI**:
    To view experiment logs, run:
    ```bash
    mlflow ui
    ```

---

## 📊 Results Summary
The project achieves low MAE/RMSE by capturing peak load times and seasonal variances. Detailed metrics for each model run can be found in the local `mlruns` directory after execution.

---
Developed by [krish1440](https://github.com/krish1440)
