# Combined Cycle Power Plant Energy Prediction

## 📌 Project Overview
This project focuses on predicting the net hourly electrical energy output (PE) of a Combined Cycle Power Plant (CCPP) using a **Random Forest Regressor**. The model analyzes ambient environmental parameters—Temperature, Ambient Pressure, Relative Humidity, and Exhaust Vacuum—to estimate power generation efficiency.

The goal is to demonstrate how machine learning techniques can be applied to industrial thermodynamic processes to optimize performance monitoring.

## 🚀 Key Findings & Performance
The final model was evaluated on an independent test set, yielding the following performance metrics:

- **R² Score:** 0.96 (The model explains 96% of the variance in energy output).
- **RMSE:** 3.28 MW.
- **NRMSE:** 0.72% (Error relative to the average energy output).

### Visual Analysis
1. **Actual vs. Predicted:** The predictions are tightly clustered around the identity line, confirming high accuracy.
2. **Residual Analysis:** The errors follow a Gaussian distribution centered at zero, indicating the **absence of systematic bias**.

![Model Performance Results](images/CCPP_Results_Panel.png)

> *"The Random Forest Regressor model achieved a Coefficient of Determination (R^2) of 0.96 on the test set, demonstrating a robust predictive capacity. Feature importance analysis identified Ambient Temperature as the dominant predictor, consistent with thermodynamic principles."*

![Feature Importance Graph](images/CCPP_Feature_Importance.png)

## 🛠️ Methodology
1. **Exploratory Data Analysis (EDA):** Analyzed variable distributions and correlations. Identified non-linear relationships between environmental parameters and energy output.
2. **Data Cleaning:** Handled physical inconsistencies in the data, specifically capping Relative Humidity ($RH$) values at 100% to reflect realistic sensor saturation limits.
3. **Preprocessing:** Split the dataset into Training and Test sets to prevent data leakage.
4. **Model Selection:** Selected **Random Forest Regressor** for its robustness against overfitting and ability to capture non-linear interactions without complex feature engineering.
5. **Hyperparameter Tuning:** Optimized the number of trees (`n_estimators`) using **Out-of-Bag (OOB) error** estimation on the training set. A value of 40 was selected to balance accuracy with computational efficiency.
6. **Final Evaluation:** The optimized model was validated using the unseen Test Set to report final performance metrics.

## 💻 Technologies Used
- **Language:** Python 3.x
- **Libraries:**
  - `scikit-learn` (Modeling & Metrics)
  - `pandas` & `numpy` (Data Manipulation)
  - `seaborn` & `matplotlib` (Data Visualization)

## 📂 Repository Structure
- `CCPP_Energy_Prediction.ipynb`: The complete analysis, from EDA to Model Evaluation.
- `images/`: Contains the generated plots used in this README (Actual vs Predicted, Residue Plot, Feature Importance).

---
*Author: Natalia L. Courtalón - Chemical Engineer & Data Analyst*
*Connect with me on https://www.linkedin.com/in/natalia-courtalon*
