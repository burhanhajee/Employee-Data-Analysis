# Employee Attrition: A Comprehensive Data Exploration
This project was originally done on my Kaggle.
## Introduction
In the current business milieu, where fluctuations in employee strength significantly affect a company's operations, it's crucial to gain insights into employee attrition. This initiative undertakes an in-depth analysis of the data concerning employees leaving, aiming to unearth pivotal patterns and insights crucial for workforce stability.

## Objectives
- **Identifying Key Influencers:** Our main thrust is on pinpointing the pivotal factors leading to employee exits. We scrutinize various elements like job roles, departmental dynamics, the equilibrium between work and personal life, tenure in the organisation, etc., to understand their bearing on staff departures.

- **Comparative Evaluation:** The project incorporates a comparative assessment of different employee characteristics, including age, educational background, job contentment, and earnings. The objective is to discern the distinctions in these aspects between employees who stay aboard and those who part ways with the organisation.

- **Department-Specific Insights:** By analysing attrition rates across diverse departments, we intend to detect department-specific trends, thereby providing valuable insights for bespoke HR strategies.

- **Exploring Predictive Indicators:** Our endeavour is to identify potential indicators that might foresee attrition, enabling organisations to proactively tackle factors leading to high staff turnover.

This endeavour is an invaluable asset for HR professionals, organisational leaders, and decision-makers, offering them profound insights into employee attrition. By pinpointing the undercurrents of turnover, it furnishes essential insights for developing strategies aimed at enhancing employee retention, boosting job satisfaction, and fostering a stable, efficacious workplace atmosphere.

In essence, this project leverages data analytics and visualisation to transform complex employee data into actionable insights, assisting organisations in informed decision-making regarding their human resource management.

## Data Origins
The data for this analysis comes from Kaggle, a renowned hub for data science challenges and datasets. We specifically use the IBM HR Analytics Employee Attrition & Performance dataset, which sheds light on the intricacies of employee turnover.

## Data Overview
- **Scope:** Our dataset includes information on 1,470 employees, making it a robust base for our study. It comprises 35 distinct variables, offering a broad perspective on employee traits and situations. The 'Attrition' variable stands out in this dataset. It's a binary indicator showing if an employee has exited the company ('Yes' or 'No'). This forms the central focus of our analysis.

- **Quantitative and Qualitative Attributes:** This includes both continuous and discrete figures like 'Age', 'DailyRate', 'DistanceFromHome', 'HourlyRate', 'MonthlyIncome', 'MonthlyRate', 'TotalWorkingYears', 'YearsAtCompany', 'YearsInCurrentRole', 'YearsSinceLastPromotion', and 'YearsWithCurrManager'. The categorical aspects include 'Attrition', 'BusinessTravel', 'Department', 'EducationField', 'Gender', 'JobRole', 'MaritalStatus', 'OverTime', and more.

- **Principal Employee Factors:** The dataset covers a range of attributes like demographic information (age, gender, marital status), job-related features (role, department, working conditions), and career history (tenure at the company, promotion history, role transitions).

### Key Insights and Observations
- **Work-Related Travel Patterns:** Most employees do not regularly travel for work, with variations in travel frequency among them.
- **Commute Distances:** Most employees have short commutes, but there is substantial variability among the workforce. Longer commutes are often associated with higher levels of employee turnover.
- **Work History and Gender:** Regardless of gender, individuals who have left the company tend to have worked at more companies than those who have stayed.
- **Age and Monthly Income:** There is a consistent positive correlation, indicating that as age increases, monthly income tends to rise. However, there is considerable income variation within each age group.
- **Career Tenure:** Employees are more likely to quit in the first 5 years at the company, with a less pronounced trend among long-term employees.

## Random Forest to Predict Attrition using GridSearchCV for Hypertuning
Random Forest is selected for its ability to handle complex interactions and provide insights into feature importance. GridSearchCV is used for hyperparameter tuning.

- **Optimal Parameters:**
  - max_depth: 10
  - max_features: 'auto'
  - min_samples_leaf: 2
  - min_samples_split: 2
  - n_estimators: 100

- **Model Performance:**
  - Accuracy: 0.8639455782312925
  - Confusion Matrix: [[376   4] [56   5]]
  - Classification Report:
    - No Attrition (0): Precision 0.87, Recall 0.99, F1-score 0.93
    - Attrition (1): Precision 0.56, Recall 0.08, F1-score 0.14
