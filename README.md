# 🏦 Bank Customer Churn Prediction  
Supervised Classification – F1 Optimization & AUC-ROC Evaluation

---

## 📖 Project Overview

This project builds a supervised learning model to predict whether a bank customer is likely to churn (leave the bank). Since retaining existing customers is typically more cost-effective than acquiring new ones, the goal is to support proactive retention strategies through data-driven churn prediction.

The dataset includes historical customer behavior and contract termination outcomes.

---

## 🎯 Business Objective

- Predict customer churn (**Exited = 1**) using customer demographic and account features  
- Optimize model performance for **F1-score** (minimum target: **0.59** on the test set)  
- Evaluate model discrimination using **AUC-ROC** and compare it with F1 results  
- Address **class imbalance** using multiple techniques and select the best-performing approach  

---

## 🗂 Data

Target:
- **Exited** – churn label (1 = churn, 0 = stay)

Key features include:
- CreditScore, Geography, Gender, Age, Tenure  
- Balance, NumOfProducts, HasCrCard, IsActiveMember, EstimatedSalary  

---

## 🛠️ Methodology

### 1️⃣ Data Preparation
- Data loading and basic preprocessing  
- Feature encoding for categorical variables (e.g., Geography, Gender)  
- Train/validation/test split to support model selection and unbiased testing  

### 2️⃣ Baseline Modeling
- Model training without imbalance correction  
- Class balance analysis and baseline metric tracking  

### 3️⃣ Class Imbalance Handling (Multiple Approaches)
At least two methods are applied, for example:
- Class weight adjustment  
- Oversampling / undersampling techniques  

Models and hyperparameters are tuned using training and validation sets to maximize F1-score.

### 4️⃣ Final Evaluation
- Test set evaluation using **F1-score**  
- **AUC-ROC** calculation and comparison with F1  
- Summary of the final model performance

---

## 📊 Results

After addressing class imbalance and tuning hyperparameters, the final selected model achieved:

- **F1-score (test set): ~0.62**
- **AUC-ROC (test set): ~0.85**

The model exceeded the required F1 threshold (0.59) while maintaining strong class discrimination performance as measured by AUC-ROC.

The results demonstrate that correcting class imbalance significantly improves recall and overall model effectiveness in churn prediction.

---

## 📈 Evaluation Metrics

- **F1-score** – balances precision and recall, suitable for imbalanced classification  
- **AUC-ROC** – measures overall class separation and ranking ability  

---

## 🧰 Tools & Technologies

- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- Matplotlib  
