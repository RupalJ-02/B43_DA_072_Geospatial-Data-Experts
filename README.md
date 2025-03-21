# B43_DA_072_Geospatial-Data-Experts
---
# IBM HR Analytics Employee Attrition & Performance Prediction

## About

This project aims to predict employee attrition using a Logistic Regression model trained on the IBM HR Analytics Employee Attrition & Performance dataset. The dataset contains various features related to employee demographics, job satisfaction, work-life balance, and more. By analyzing these factors, the model identifies patterns and predicts whether an employee is likely to leave the company.

## Dataset

**Name:** IBM HR Analytics Employee Attrition & Performance

**Description:** This is a fictional dataset created by IBM data scientists to explore the factors that lead to employee attrition. It includes information on employee satisfaction, income, seniority, demographics, and other relevant attributes.

**Source:** The dataset is publicly available and can be accessed from Kaggle and other sources.

**Key Features:**

*   **Age:** Employee's age
*   **Attrition:** Whether the employee left the company (Yes/No)
*   **BusinessTravel:** Frequency of business travel
*   **DailyRate:** Daily rate of pay
*   **Department:** Department the employee works in
*   **DistanceFromHome:** Distance from home to work
*   **Education:** Education level (1-5)
*   **EducationField:** Field of education
*   **EmployeeCount:** (Always 1)
*   **EmployeeNumber:** Employee ID
*   **EnvironmentSatisfaction:** Satisfaction with the work environment (1-4)
*   **Gender:** Employee's gender
*   **HourlyRate:** Hourly rate of pay
*   **JobInvolvement:** Level of job involvement (1-4)
*   **JobLevel:** Job level
*   **JobRole:** Job role
*   **JobSatisfaction:** Satisfaction with the job (1-4)
*   **MaritalStatus:** Marital status
*   **MonthlyIncome:** Monthly income
*   **MonthlyRate:** Monthly rate of pay
*   **NumCompaniesWorked:** Number of companies worked for
*   **Over18:** Whether the employee is over 18 (always 'Y')
*   **OverTime:** Whether the employee works overtime (Yes/No)
*   **PercentSalaryHike:** Percentage salary hike
*   **PerformanceRating:** Performance rating (1-4)
*   **RelationshipSatisfaction:** Satisfaction with relationships at work (1-4)
*   **StandardHours:** Standard hours worked (always 80)
*   **StockOptionLevel:** Stock option level
*   **TotalWorkingYears:** Total years worked
*   **TrainingTimesLastYear:** Number of training times last year
*   **WorkLifeBalance:** Work-life balance (1-4)
*   **YearsAtCompany:** Years at the company
*   **YearsInCurrentRole:** Years in the current role
*   **YearsSinceLastPromotion:** Years since last promotion
*   **YearsWithCurrManager:** Years with the current manager




**Evaluation:** The model's performance is evaluated using metrics such as Accuracy, Precision, Recall, F1 Score, and ROC-AUC Score.

**Usage:**

1.  Upload the dataset (`hrdataset.csv`) to your Colab environment.
2.  Run the code cells to preprocess the data, train the model, and make predictions.
3.  Use the `predict_attrition` function to predict attrition for new data points.
