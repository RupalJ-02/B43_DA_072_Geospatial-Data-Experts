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

## Workflow

The code follows these steps:

**1. Data Loading and Initial Exploration**

*   Import necessary libraries (NumPy, Pandas, Scikit-learn, Matplotlib, Seaborn).
*   Load the dataset (`hrdataset.csv`) using `pd.read_csv()`.
*   Explore the dataset using `df.info()` to check data types and missing values and `df.head()` to view the first few rows.
*   Get the shape (rows and columns) of the dataset using `df.shape`.

**2. Data Preprocessing**

*   **Handling Missing Values:** Check for missing values in each column using `df.isna().sum()`. In this case, there are no missing values.
*   **Encoding Categorical Features:** Identify categorical columns using `df.select_dtypes(include=['object']).columns` and apply one-hot encoding using `pd.get_dummies()` with `drop_first=True` to avoid multicollinearity.
*   **Scaling Numerical Features:** Identify numerical columns using `df_encoded.select_dtypes(include=['int64', 'float64']).columns` and apply standard scaling using `StandardScaler()` to ensure features have similar ranges.

**3. Model Training**

*   **Data Splitting:** Split the data into training and testing sets using `train_test_split()` with a `test_size` of 0.2 and `random_state` for reproducibility. Stratify the split based on the target variable ('Attrition\_Yes') to ensure similar class distributions in both sets.
*   **Model Initialization:** Initialize a Logistic Regression model using `LogisticRegression()`.
*   **Model Training:** Train the model using `log_reg.fit()` with the training data (X\_train, y\_train).

**4. Model Evaluation**

*   **Predictions:** Make predictions on the test data using `log_reg.predict()` and predict probabilities using `log_reg.predict_proba()`.
*   **Performance Metrics:** Calculate evaluation metrics such as accuracy, precision, recall, F1 score, confusion matrix, and ROC-AUC score using functions from `sklearn.metrics`.
*   **Visualization:** Create visualizations like the ROC curve and confusion matrix using Matplotlib and Seaborn to understand the model's performance.

**5. Prediction Function**

*   Define a function `predict_attrition()` that takes input data, preprocesses it (if necessary), and uses the trained model to make a prediction.

**6. Example Prediction**

*   Provide a sample input dictionary with feature values.
*   Use the `predict_attrition()` function to make a prediction on the sample input.
*   Print the prediction result (whether attrition is predicted or not).


**Evaluation:** The model's performance is evaluated using metrics such as Accuracy, Precision, Recall, F1 Score, and ROC-AUC Score.

**Usage:**

1.  Upload the dataset (`hrdataset.csv`) to your Colab environment.
2.  Run the code cells to preprocess the data, train the model, and make predictions.
3.  Use the `predict_attrition` function to predict attrition for new data points.
