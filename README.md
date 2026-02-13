# Employee Retention Analysis Using Logistic Regression


 ## Project Overview

Employee attrition is a major challenge for organizations. High turnover increases recruitment costs, reduces productivity, and impacts company performance.

This project performs Exploratory Data Analysis (EDA) and builds a Logistic Regression model to predict whether an employee will leave the company based on key workplace factors.

## Objectives

Perform exploratory data analysis to determine variables impacting employee retention.

Analyze the impact of salary on employee retention.

Analyze the relationship between department and employee attrition.

Build a Logistic Regression model using selected features.

Measure the accuracy of the model.

## Data

The dataset used: HR Employee Dataset

Main features include:

satisfaction_level

last_evaluation

number_project

average_montly_hours

time_spend_company

Work_accident

promotion_last_5years

sales (Department)

salary

left (Target Variable)

Target Variable:

left = 1 → Employee left

left = 0 → Employee stayed

##  Exploratory Data Analysis


1️⃣ Correlation Analysis

A correlation heatmap was generated to identify variables strongly associated with employee attrition.

Key Findings:

Employees with low satisfaction levels were more likely to leave.

Higher average monthly hours correlated with higher attrition.

Longer time spent in company increased the likelihood of leaving.

Lack of promotion in the last 5 years increased attrition.

2️⃣ Salary vs Retention

Bar chart analysis showed:

Employees with low salary had significantly higher attrition.

Employees with high salary had lower probability of leaving.

This suggests salary is a strong predictor of retention.

3️⃣ Department vs Retention

Departmental analysis revealed:

Certain departments (e.g., sales, technical) showed higher turnover.

Management and higher-paying departments showed lower attrition.

 ## Model Building

A Logistic Regression model was used because:

The target variable (left) is binary.

It is suitable for classification problems.

It provides interpretable results.

Steps Performed:

Converted categorical variables using one-hot encoding.

Split data into training and testing sets (70% / 30%).

Trained Logistic Regression model.

Evaluated performance using accuracy score.

 ## Model Performance


Model Accuracy: ~75% – 80%

Evaluation Metrics Used:

Accuracy Score

Confusion Matrix

Classification Report

The model performs reasonably well in predicting employee attrition.

 ## Technologies Used

Python

Pandas

NumPy

Matplotlib

Seaborn

Scikit-learn

Google Colab

## How to Run

Clone the repository:

git clone https://github.com/yourusername/employee-retention-project.git


Open the notebook in Google Colab or Jupyter Notebook.

Ensure the dataset file is available in the project directory.

Run all cells sequentially.

## Project Structure
employee-retention-project/
│
├── HR_comma_sep 1.csv
├── employee_retention.ipynb
└── README.md

## Conclusion

This project demonstrates how data analysis and machine learning can help organizations:

Identify drivers of employee attrition

Improve HR decision-making

Develop better retention strategies

By leveraging predictive analytics, companies can proactively reduce turnover and improve workforce stability.

 ## Author

Mildred Ewenrim Ebomah
