# Data-Science-Women-Techster
Salary Prediction Using Multiple Linear Regression
Project Overview

This project builds a Machine Learning model to help an HR department predict candidate salaries based on:

Years of Experience

Written Test Score (out of 10)

Interview Score (out of 10)

The model uses Multiple Linear Regression to determine salary based on these three features.

Dataset

File: hiring.csv

The dataset contains:

Column	Description
experience	Candidate's years of experience (some values written in words)
test_score(out of 10)	Written test score
interview_score(out of 10)	Interview score
salary($)	Salary offered

Data Preprocessing

The following preprocessing steps were performed:

Converted experience values written in words (e.g., "five", "two") to numeric values

Replaced missing experience values with 0

Filled missing test scores using the mean value

Renamed columns for easier handling


Machine Learning Model

We used:

LinearRegression (from sklearn)


The model equation:

Salary = b₀ + b₁(Experience) + b₂(Test Score) + b₃(Interview Score)



import pandas as pd
from sklearn.linear_model import LinearRegression

# Load dataset
df = pd.read_csv("hiring.csv")

# Rename columns
df.columns = ['experience', 'test_score', 'interview_score', 'salary']

# Convert word experience to numbers
word_to_num = {
    'zero': 0, 'one': 1, 'two': 2, 'three': 3, 'four': 4,
    'five': 5, 'six': 6, 'seven': 7, 'eight': 8,
    'nine': 9, 'ten': 10, 'eleven': 11, 'twelve': 12
}

df['experience'] = df['experience'].fillna('zero')
df['experience'] = df['experience'].apply(lambda x: word_to_num.get(str(x).lower(), x))

# Fill missing test scores
df['test_score'] = df['test_score'].fillna(df['test_score'].mean())

# Define features and target
X = df[['experience', 'test_score', 'interview_score']]
y = df['salary']

# Train model
model = LinearRegression()
model.fit(X, y)

# Predict salaries
predictions = model.predict([
    [2, 9, 6],
    [12, 10, 10]
])

predictions




Model Predictions
Experience	Test Score	Interview Score	Predicted Salary ($)
2	9	6	53,290.89
12	10	10	92,268.07


Technologies Used

Python

Google Colab

Pandas

Scikit-learn

Linear Regression




Conclusion

The Multiple Linear Regression model successfully predicts salaries based on candidate qualifications. This tool can assist HR departments in making consistent and data-driven salary decisions.
