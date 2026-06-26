# Employee Attrition Prediction using Machine Learning

## Project Overview

Employee attrition is one of the biggest challenges faced by organizations. High employee turnover increases recruitment costs, decreases productivity, and impacts overall organizational performance.

This project predicts whether an employee is likely to leave the organization using Machine Learning techniques. Multiple classification algorithms were trained, evaluated, and compared to identify the best-performing model.

---

# Project Objective

The objective of this project is to:

- Analyze employee attrition data.
- Perform data cleaning and preprocessing.
- Conduct Exploratory Data Analysis (EDA).
- Train multiple machine learning models.
- Compare model performance.
- Select the best-performing model.
- Analyze feature importance.
- Save the trained model for future predictions.

---

# Dataset

## Source

IBM HR Analytics Employee Attrition Dataset

## Target Variable

**Attrition**

- No → Employee stays
- Yes → Employee leaves

## Dataset Size

- Rows: **1470**
- Columns: **35**

---

# Project Workflow

## Day 1 – Data Loading & Understanding

### Objective

Understand the dataset structure and inspect the quality of data.

### Tasks Performed

- Imported the dataset
- Explored dataset dimensions
- Inspected data types
- Checked missing values
- Checked duplicate records
- Identified numerical and categorical features
- Generated descriptive statistics

### Outcome

Developed a clear understanding of the dataset before preprocessing.

---

## Day 2 – Data Cleaning & Preprocessing

### Objective

Prepare the dataset for machine learning.

### Data Cleaning Steps

- Removed constant columns:
  - EmployeeCount
  - Over18
  - StandardHours

- Encoded the target variable:
  - No → 0
  - Yes → 1

- Applied Label Encoding to categorical features.

- Split the dataset into:
  - Features (X)
  - Target Variable (y)

- Performed Train-Test Split:
  - Training Set: 80%
  - Testing Set: 20%

### Outcome

Created a clean, encoded, and machine-learning-ready dataset.

---

## Day 3 – Exploratory Data Analysis (EDA)

### Objective

Analyze employee behavior and identify important patterns.

### Visualizations Created

- Age Distribution
- Attrition Distribution
- Gender vs Attrition
- Department vs Attrition
- Job Satisfaction Distribution
- Monthly Income Distribution
- Overtime vs Attrition
- Correlation Heatmap

### Key Insights

- Employees working overtime were more likely to leave.
- Monthly income showed significant variation across employees.
- Employee attrition is an imbalanced classification problem.
- Multiple demographic and work-related factors influence attrition.

### Outcome

Generated business insights that helped understand employee turnover.

---

## Day 4 – Machine Learning Model Training & Evaluation

### Objective

Train multiple machine learning models for predicting employee attrition and compare their performance using standard evaluation metrics.

### Models Trained

- Logistic Regression
- Decision Tree Classifier
- Random Forest Classifier
- K-Nearest Neighbors (KNN)
- Support Vector Machine (SVM)

### Model Evaluation Metrics

Each model was evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC Score

The evaluation results were stored in a comparison table and sorted by model accuracy.

### Best Performing Model

Among all trained models, **Random Forest Classifier** achieved the highest overall accuracy and was selected as the final prediction model.

Additional analysis included:

- Confusion Matrix
- Classification Report
- Feature Importance Analysis

### Feature Importance

The Random Forest model identified the most influential features contributing to employee attrition:

- MonthlyIncome
- Age
- TotalWorkingYears
- DailyRate
- OverTime
- EmployeeNumber
- YearsAtCompany

### Model Export

The trained Random Forest model was saved to:

- `models/random_forest_model.pkl`

The feature importance table was exported to:

- `reports/feature_importance.csv`

### Outcome

- Successfully trained multiple ML models.
- Compared model performances.
- Selected the best-performing model.
- Analyzed feature importance.
- Saved the final model for future predictions.

---

# Project Structure

```text
EmployeeAttrition_AnushkaDas/
│
├── charts/
│   ├── age_distribution.png
│   ├── attrition_distribution.png
│   ├── correlation_heatmap.png
│   ├── department_attrition.png
│   ├── gender_attrition.png
│   ├── job_satisfaction.png
│   ├── monthly_income_distribution.png
│   └── overtime_attrition.png
│
├── data/
│   ├── WA_Fn-UseC_-HR-Employee-Attrition.csv
│   └── Employee_Attrition_Cleaned.csv
│
├── models/
│   └── random_forest_model.pkl
│
├── reports/
│   └── feature_importance.csv
│
├── Employee_Attrition_Prediction.ipynb
├── README.md
├── requirements.txt
└── .gitignore
```

---

# Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Joblib
- Jupyter Notebook
- VS Code
- Git
- GitHub

---

# Model Performance

| Model | Accuracy |
|--------|----------|
| Random Forest | **82.65%** |
| K-Nearest Neighbors | 78.91% |
| Decision Tree | 78.23% |
| Logistic Regression | 65.31% |
| Support Vector Machine | 47.28% |

---

# Feature Importance

The top features affecting employee attrition include:

- MonthlyIncome
- Age
- TotalWorkingYears
- DailyRate
- OverTime
- EmployeeNumber
- YearsAtCompany
- MonthlyRate
- DistanceFromHome
- HourlyRate

---

# Future Improvements

- Hyperparameter tuning using GridSearchCV.
- Handle class imbalance using SMOTE.
- Implement XGBoost and LightGBM.
- Feature selection techniques.
- Deploy the model using Streamlit.
- Build REST APIs using Flask or FastAPI.

---

# Conclusion

This project demonstrates a complete end-to-end Machine Learning workflow, starting from data exploration and preprocessing to model training, evaluation, feature interpretation, and model persistence. The final Random Forest model provides a practical solution for predicting employee attrition while showcasing core data science and machine learning skills.

---

# Author

**Anushka Das**

AI & Machine Learning Enthusiast