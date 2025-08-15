# Customer Churn Analysis – Logistic Regression (Baseline vs Improved Model)

## 📌 Project Overview
This project predicts whether a customer will churn (leave a service) based on their account information and usage patterns.  
The main goal is to help businesses identify customers at risk and take action to retain them.

The project is divided into **two phases**:
1. **Baseline Model** – Logistic Regression without any balancing techniques.
2. **Improved Model** – Logistic Regression with SMOTE oversampling to handle class imbalance.

---

## 🗂 Dataset
**Source:** Telco Customer Churn Dataset (Kaggle)  
**Target Variable:** `Churn` (Yes/No)  
**Number of Rows:** ~7043  
**Number of Features:** 21 (after encoding)

---

## 🛠 Tools & Libraries
- **Python**
- **Pandas & NumPy** – Data handling and preprocessing
- **Matplotlib & Seaborn** – Visualization
- **scikit-learn** – Model building & evaluation
- **imblearn (SMOTE)** – Handling imbalanced data

---

## 📊 Data Preprocessing
- Removed unnecessary columns (`customerID`)
- Converted `TotalCharges` to numeric and handled missing values
- One-hot encoded categorical variables
- Standardized numerical features

---

## 📉 Churn Distribution
![Churn Distribution](images/churn_distribution.png)

The dataset was **imbalanced**, with more customers staying than churning, which can affect model performance.

---

## ⚙ Baseline Model – Logistic Regression
**Model:** Logistic Regression (max_iter=1000)  
**Balancing:** None

**Results:**
- **Precision, Recall, F1-score** showed poor recall for churned customers.
- **ROC-AUC Score:** *[Insert your baseline score here]*

---

## 🔄 Improved Model – Logistic Regression with SMOTE
To improve churn prediction, **SMOTE (Synthetic Minority Oversampling Technique)** was applied to balance the dataset.

**Results:**
- Improved recall for churned customers
- **ROC-AUC Score:** *[Insert your improved score here]*

**Confusion Matrix:**
![Confusion Matrix](images/confusion_matrix.png)

---

## 📌 Key Insights
- The baseline model struggled to identify churned customers due to data imbalance.
- Applying SMOTE improved the recall score significantly, making the model better at detecting churn.
- ROC-AUC score increased, showing better overall classification performance.

---

## 🚀 How to Run the Project
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/customer-churn-analysis.git
   pip install -r requirements.txt
python customer_churn_analysis.py

