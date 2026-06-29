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

## Day 5 – Model Optimization & Validation

### Objective

The objective of this phase was to optimize the Random Forest model using hyperparameter tuning and validate whether the optimized model outperformed the baseline model.

---

### Cross Validation

To improve model reliability, **5-Fold Cross Validation** was performed using GridSearchCV. This technique evaluates the model across multiple training-validation splits to reduce the risk of overfitting.

Best Cross Validation Accuracy:

- **86.31%**

---

### Hyperparameter Tuning

The following Random Forest hyperparameters were optimized:

- Number of Trees (`n_estimators`)
- Maximum Tree Depth (`max_depth`)
- Minimum Samples Split (`min_samples_split`)

Best Parameters:

- n_estimators = 100
- max_depth = 20
- min_samples_split = 2

---

### Tuned Model Evaluation

The tuned Random Forest model was evaluated on the test dataset using:

- Accuracy
- Precision
- Recall
- F1 Score

Although the tuned model achieved a slightly higher overall accuracy, it resulted in lower Recall and F1 Score compared to the baseline Random Forest model.

---

### Final Model Selection

Employee attrition prediction is an imbalanced classification problem where identifying employees likely to leave is more important than maximizing overall accuracy.

Therefore, the original Random Forest model from Day 4 was retained as the final production model because it provided a better balance between Accuracy, Recall, and F1 Score.

---

### Outcome

At the end of Day 5:

- Cross Validation was successfully completed.
- Hyperparameter tuning was performed using GridSearchCV.
- The tuned model was evaluated and compared with the baseline model.
- The original Random Forest model was retained as the final production model.

---

## Day 6 – Model Interpretation & Business Insights

### Objective

The objective of this phase was to interpret the machine learning results and convert them into actionable business insights for HR decision-making.

---

### Feature Importance Analysis

The feature importance scores generated by the Random Forest model were analyzed to determine which employee attributes contribute most to attrition prediction.

The most influential features included:

- Monthly Income
- Age
- Total Working Years
- Daily Rate
- OverTime
- Employee Number
- Years At Company
- Monthly Rate
- Distance From Home
- Hourly Rate

---

### Business Insights

The feature importance results were translated into business-friendly insights to help HR teams understand the primary drivers of employee turnover.

The interpreted insights were exported to:

- reports/business_insights.csv

---

### HR Recommendations

Based on the analysis, the following recommendations were proposed:

- Review employee compensation strategies.
- Reduce excessive overtime.
- Improve work-life balance.
- Strengthen employee engagement.
- Support career development and internal growth.
- Improve retention strategies for experienced employees.
- Conduct regular employee satisfaction surveys.

---

### Visualization

A bar chart illustrating the Top 10 Employee Attrition Drivers was generated and saved as:

- charts/top10_attrition_drivers.png

This visualization highlights the relative importance of the most influential features used by the Random Forest model.

---

### Outcome

At the end of Day 6:

- Feature importance was analyzed.
- Business insights were generated.
- HR recommendations were documented.
- Business reports were exported.
- Visualizations were created to support HR decision-making.

---

# Day 7 – Business Insights, Recommendations & Project Completion

## Objective

The objective of the final phase was to interpret the machine learning model results, generate business recommendations, document project limitations, and prepare the project for real-world HR decision support.

---

## Final Model Review

The Random Forest Classifier remained the best-performing model after comparison with other machine learning algorithms and hyperparameter tuning.

The model was evaluated using:

- Confusion Matrix
- Classification Report
- Cross Validation
- Feature Importance Analysis

---

## Business Insights

Feature importance analysis revealed several important factors influencing employee attrition, including:

- Monthly Income
- Age
- Total Working Years
- Daily Rate
- OverTime
- Years At Company

These variables provide valuable insights into employee retention patterns.

---

## HR Recommendations

Based on the model findings, several recommendations were proposed:

- Improve employee compensation strategies.
- Reduce excessive overtime.
- Enhance career development opportunities.
- Increase employee engagement initiatives.
- Implement predictive monitoring for high-risk employees.

---

## Project Limitations

The project acknowledges several limitations:

- Historical dataset only.
- No external economic or organizational variables.
- Periodic retraining is recommended.

---

## Future Improvements

Possible future enhancements include:

- Explainable AI (SHAP)
- Real-time dashboard deployment
- Cloud API integration
- Deep learning models
- Enterprise HR system integration

---

## Outcome

At the end of Day 7:

- Final model evaluation completed.
- Business insights documented.
- HR recommendations developed.
- Project limitations identified.
- Future enhancements proposed.
- Project prepared for portfolio and deployment.

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
│   └── top10_attrition_driver.png   
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
│   └── business_insights.csv
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