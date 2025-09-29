# Financial Risk Assessment – Explainable AI Techniques II

This project explores **explainable machine learning techniques** applied to the **Financial-Risk-Assessment dataset** from OpenML. The main goal is to predict borrowers’ **credit risk rating** (low, medium, high) and interpret model behavior using **PDP, ICE, and ALE plots**.

## 📊 Dataset

* **Source:** OpenML – [Financial-Risk-Assessment](https://www.openml.org/search?type=data&status=active&id=46481)
* **Size:** 15,000 records, 20 features
* **Features:** demographic (age, gender, education), financial (income, assets, debt-to-income ratio, credit score), loan details, and behavioral attributes.
* **Target:** `risk_rating` (0 = low risk, 1 = medium risk, 2 = high risk).

## ⚙️ Workflow

1. **Exploratory Data Analysis (EDA)**

   * Numeric and categorical distributions
   * Correlation heatmap

2. **Model Training**

   * Random Forest Classifier
   * Gradient Boosting Classifier
   * Evaluation using accuracy, precision, recall, F1-score

3. **Feature Importance**

   * Ranked predictors from the Random Forest model

4. **Model Interpretability**

   * **Partial Dependence Plots (PDP)**
   * **Individual Conditional Expectation (ICE)**
   * **Accumulated Local Effects (ALE)**
  

## 🧾 Results

* **Random Forest outperformed Gradient Boosting** with ~60% accuracy.
* Both models predicted **low risk well**, but struggled with **medium/high risk classes** due to class imbalance.
* Top predictive features:

  * `assets_value`
  * `loan_amount`
  * `debt-to-income_ratio`
    
* **Interpretability findings:**

  * PDP showed general average effects but sometimes smoothed over real patterns.
  * ICE revealed heterogeneous responses and feature interactions.
  * ALE provided the most reliable local explanations, avoiding unrealistic feature combinations.


