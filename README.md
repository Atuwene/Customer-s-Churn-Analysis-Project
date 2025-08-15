# Telco Customer Churn Prediction

## 📌 Project Overview
This project predicts **customer churn** (whether a customer will leave the service) using the **Telco Customer Churn dataset**.  
The main goal is to help businesses **identify customers at risk** so they can take proactive steps to retain them.

We built multiple Logistic Regression models — starting with a baseline model and then improving it using **SMOTE** oversampling and class balancing techniques.

---

## 📂 Dataset
- **Source:** IBM Telco Customer Churn dataset
- **Size:** 7,043 rows × 21 columns
- **Target variable:** `Churn` (Yes = customer left, No = customer stayed)

Key features include:
- **Demographics:** gender, senior citizen, partner, dependents
- **Account info:** tenure, contract type, payment method
- **Service usage:** internet service, phone service, streaming, etc.
- **Billing details:** monthly charges, total charges

---

## 🛠️ Technologies Used
- **Python** (Pandas, NumPy)
- **Scikit-learn** (Logistic Regression, train-test split, metrics)
- **Imbalanced-learn** (SMOTE)
- **Matplotlib & Seaborn** (visualizations)
- **Google Colab** (development environment)

---

## 📊 Approach & Steps

### 1. **Data Cleaning**
- Converted `TotalCharges` to numeric and handled missing values.
- Encoded `Churn` into binary values (`Yes` → 1, `No` → 0).
- Applied **One-Hot Encoding** to categorical features.

### 2. **Baseline Model**
- Model: Logistic Regression (`class_weight='balanced'`)
- Train-test split: 80% training, 20% testing
- **Results:**
- **Observation:** Recall was decent, but precision for churned customers could be improved.

### 3. **Model Improvement**
- Applied **SMOTE** oversampling to handle class imbalance.
- Re-trained Logistic Regression without explicit class weights.
- **Results after improvement:**

- **Outcome:** More balanced results and slightly improved accuracy.

---

## 📈 Evaluation Metrics
- **Confusion Matrix**
- **Classification Report** (Precision, Recall, F1-score)
- **ROC-AUC Score**

The final model achieved:
- **Accuracy:** 76%
- **ROC-AUC:** 0.84
- **Better balance** between predicting churn and non-churn customers.

---

## 🚀 How to Run
1. Clone the repository:
 ```bash
 git clone https://github.com/yourusername/telco-customer-churn.git

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Atuwene/telco-customer-churn/blob/main/customer_churn_analysis.ipynb)

