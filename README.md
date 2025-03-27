# 📈 How to Maximize Revenue: Predicting Telecom Customer Loyalty

A machine learning project that tackles customer churn prediction in the telecom sector by identifying the key factors driving churn and offering actionable business insights.

---

## 📌 1. Project Motivation

Acquiring new customers is costly. In contrast, retaining current customers is more cost-effective and profitable. This project analyzes **customer churn**, a major challenge for telecom companies, using the Telco Customer Churn dataset from Kaggle.

- **Business Question**: _How can telecommunication companies reduce customer churn?_

---

## 🧠 2. Problem Formulation

- **Type**: Classification
- **Target Variable**: `Churn` (Yes or No)
- **Baseline**: Predicting the mode (`No churn`)
- **Key Evaluation Metrics**: Recall, F1 Score (Accuracy avoided due to class imbalance)

---

## 📊 3. Dataset Details

- 📁 **Source**: [Telco Customer Churn – Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
- 📌 **Features include**:
  - Demographics (gender, age, seniority, dependents)
  - Services (phone, internet, security, tech support, streaming)
  - Account information (contract type, billing, charges, tenure)
- ⚠️ The dataset is imbalanced: **Churn rate = 26.5%**

---

## 🧪 4. Hypotheses Tested

- ❓ Does gender affect customer churn? → **No significant difference**
- ❓ Does tenure affect churn? → **Yes. <10 months tenure = higher churn**
- ❓ Is `TotalCharges` related to `tenure` and `MonthlyCharges`? → **Strong correlation confirmed**

---

## 🧹 5. Data Preprocessing

- Handled missing values
- One-hot encoded categorical variables
- Used **SMOTE** to balance classes
- Scaled numeric features
- Train-test split: 80/20

---

## 🤖 6. Model Training & Results

| Model                  | Accuracy | Recall  | F1 Score |
|-----------------------|----------|---------|----------|
| Logistic Regression   | 0.7935   | 0.5156  | 0.5764   |
| Random Forest         | 0.8105   | 0.8385  | 0.7069   |
| SMOTE + Random Forest | 0.8269   | 0.8885  | 0.8381   |
| **Baseline**          | 0.7424   | –       | –        |

> ⚠️ SMOTE-Random Forest performed best, but in consideration of time and cost in practical settings, standard Random Forest was selected as the final model.

---

## 📌 7. Key Findings

- Customers with **Month-to-Month contracts** churn more frequently.
- Churn is higher among those paying **>$60/month**.
- **Senior citizens** and those **without dependents** are more likely to churn.
- **Fiber optic internet** users churn more frequently – a potential quality issue?

---

## 📉 8. Interpretability

- Used **Feature Importance**, **SHAP**, and **Permutation Importance** to understand model decisions.
- Most important features:
  - `TotalCharges`, `MonthlyCharges`, `Tenure`, `Contract Type`, `InternetService`

---

## 💡 9. Business Recommendations

1. **Promote long-term contracts** with attractive offers.
2. **Reduce monthly charges** for high-risk churners (e.g., those on month-to-month contracts).
3. **Survey Fiber Optic users** to improve quality and reduce dissatisfaction.
4. **Enhance support services** like OnlineSecurity and TechSupport.

---

## ⚠️ 10. Limitations

- No time or quarterly data; difficult to identify seasonal trends or recent customer behavior patterns.
- All features were used in the model — future work could explore feature selection and engineering.

---

## 📚 References

- Kaggle Dataset: https://www.kaggle.com/datasets/blastchar/telco-customer-churn
- SMOTE (Synthetic Minority Over-sampling Technique)
- Scikit-learn, SHAP, XGBoost

---

## 👩‍💻 Author

**Minju Kim**  
M.S. in Data Science, Indiana University Bloomington  
📧 minjukim023@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/minjukim023/)  
💻 [GitHub](https://github.com/MinjuKim023)

s
