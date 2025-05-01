# Loan Default Prediction using Machine Learning

## 📌 Repository Name
**`loan-default-prediction-ml`**

## 📝 Project Description
This project aims to predict the likelihood of a loan applicant defaulting on their loan using advanced machine learning techniques. By analyzing borrower data such as financial background, credit behavior, employment details, and socio-economic attributes, the model accurately classifies applicants into defaulters and non-defaulters. This model can be a valuable asset for financial institutions in making data-driven lending decisions.

---

## 📊 Problem Statement
Loan default prediction is crucial for financial institutions to minimize risk and ensure profitability. Given a dataset of past borrowers with attributes like income, credit score, loan amount, and demographic data, the goal is to develop a robust classification model that can accurately predict whether a borrower is likely to default.

---

## 📂 Dataset Overview
The dataset includes 21 features and a target label `Default`. These features range across:
- Financial indicators (Income, LoanAmount, CreditScore, InterestRate, etc.)
- Socio-demographics (Age, MaritalStatus, Education, etc.)
- Employment and loan behavior details

### Sample Columns:
```
- Age
- Income
- LoanAmount
- CreditScore
- LoanTerm
- EmploymentType
- HasMortgage
- HasDependents
- Default (Target)
```

---

## 🔍 Key Techniques & Methods
- Exploratory Data Analysis (EDA)
- Feature Engineering
  - One-hot encoding
  - Feature binning (e.g., AgeGroup, CreditScoreLevel)
  - WorkLifeRatio derived from Income and Employment Duration
- Feature Importance Analysis using XGBoost
- Handling Imbalance with SMOTE
- Train-test split (67-33)
- Model selection via GridSearchCV (cross-validation)

---

## 🚀 Model Used
**XGBoost Classifier**

### 🔧 Best Hyperparameters (from GridSearchCV):
```
{
  'learning_rate': 0.2,
  'max_depth': 9,
  'n_estimators': 500,
  'subsample': 1.0,
  'colsample_bytree': 0.6,
  'gamma': 0
}
```

---

## 📈 Performance
### ✅ Before Feature Engineering
- Accuracy: **91.06%**
- F1-score: **0.91**
- Balanced performance across both classes

### 🔁 After Feature Engineering (Final Model)
- Accuracy: **91.13%**
- F1-score: **0.91**
- Slightly fewer features used with equally strong results

### 🧾 Classification Report:
```
              precision    recall  f1-score   support

           0       0.88      0.95      0.91     74459
           1       0.95      0.87      0.91     74500

    accuracy                           0.91    148959
   macro avg       0.91      0.91      0.91    148959
weighted avg       0.91      0.91      0.91    148959
```

---

## 📌 Feature Importance (Top 10)
![Feature Importance](images/feature_importance.png)

Features like `LoanTerm`, `HasCoSigner`, `HasDependents`, and `HasMortgage` were highly influential in the model's decisions.

---

## 📦 Folder Structure
> Omitted for simplicity. Code, plots, and README will be directly visible in the root directory.

---

## 💡 Future Enhancements
- Add SHAP values for model explainability
- Deploy model via Flask/Streamlit for UI
- Integrate with real-time scoring APIs
- Try ensemble stacking or deep learning variants

---

## 🧠 Skills Demonstrated
- Machine Learning (XGBoost, GridSearchCV)
- Feature Engineering
- Model Evaluation
- Data Visualization
- Professional Reporting

---

## 🧑‍💻 Author
**Rohit Gomes**
> Bachelor of Computer Science (AI & ML) | AI, Game & Graphics Enthusiast

🔗 [LinkedIn](https://www.linkedin.com/in/rohit-gomes-12209620a)
📧 gomesrohit92@gmail.com

---

## 📌 Acknowledgments
Thanks to open-source platforms and Kaggle for dataset inspiration. This project is a part of Rohit's fundamental ML learning series before progressing to advanced Deep Learning and Research-oriented tasks.

---

## 📜 License
This project is for educational and demonstration purposes. Contact for commercial use or collaboration.

