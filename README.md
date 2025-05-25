# 🎓 Student Performance Prediction Using Machine Learning

This project aims to predict whether a student will pass or fail a course using a combination of academic, demographic, and behavioral features. Built using the UCI Student Performance Dataset, the model helps in early identification of at-risk students, allowing educators to provide timely support.

---

## 📌 Project Overview

- **Goal:** Binary classification (Pass = 1, Fail = 0)
- **Dataset Source:** UCI Machine Learning Repository – Student Performance Data
- **Total Records:** 395 students (merged from Math and Portuguese classes)
- **Grade Leakage Prevention:** G1 and G2 scores excluded from training

---

## 📊 Features Used

- Demographics: Age, gender, family size, parental education
- Academic behavior: Study time, past failures, absences
- Lifestyle: Alcohol use (weekday & weekend), internet access, free time
- Derived features: Study time × Failures, Absences per Age

---

## 🧠 Machine Learning Approach

| Step                     | Description                                                             |
|--------------------------|-------------------------------------------------------------------------|
| Data Integration         | Merged Math and Portuguese student datasets                             |
| Preprocessing            | Label encoding, outlier removal, SMOTE for class imbalance              |
| Model Training           | Logistic Regression, Decision Tree, Random Forest                       |
| Threshold Tuning         | Custom probability threshold (0.60) to improve recall for "fail" class  |
| Explainability           | SHAP and LIME used to identify most influential features                |

---

## ✅ Model Performance (Best: Random Forest, Threshold = 0.60)

- **Accuracy:** 71.4%
- **Recall (Fail):** 60%
- **F1 Score (Fail):** 0.52
- **Top Predictors:** Past failures, absences, study time, weekend alcohol use

---

## 📈 Key Insights

- Over 60% of students predicted to fail had low study time and frequent absences.
- Students with higher parental education and internet access had better outcomes.
- Alcohol consumption on weekends showed negative correlation with performance.

---

## 🛠️ Tech Stack

- **Languages:** Python
- **Libraries:** pandas, scikit-learn, imbalanced-learn, matplotlib, seaborn, SHAP, LIME
- **Tools:** Jupyter Notebook, Google Colab

---

## 📂 Repository Structure

```
student-performance-prediction/
├── data/
│   ├── student-mat.csv
│   └── student-por.csv
├── notebooks/
│   └── student_performance_model.ipynb
├── images/
│   ├── shap_summary_plot.png
│   ├── lime_explanation.png
│   └── threshold_metrics_plot.png
├── Student_Performance_Prediction_PPT.pptx
├── README.md
└── requirements.txt
```

