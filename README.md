# Loan Predictor



The Loan Predictor is a Python script that utilizes a Support Vector Machine (SVM) classifier to predict whether a loan application will be approved or not based on various input features. This project includes data collection, data processing, model training, evaluation, and a predictive system for loan approval status.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [Data Collection and Processing](#data-collection-and-processing)
- [Model Training and Evaluation](#model-training-and-evaluation)
- [Predictive System](#predictive-system)


## Prerequisites

Before running the Loan Predictor script, make sure you have the following dependencies installed:

- Python (version >= 3.6)
- NumPy
- pandas
- seaborn
- scikit-learn

## Getting Started

1. Clone this GitHub repository to your local machine:

   ```bash
   git clone https://github.com/Suhaas-Suran/Loan-Prediction.git
## Usage

The Loan Predictor script can be used for the following tasks:

1. **Data Collection and Processing:** The script provides tools for loading, preprocessing, and exploring your loan applicant dataset.

2. **Model Training and Evaluation:** It trains a Support Vector Machine (SVM) classifier to predict loan approval based on historical data. Model accuracy is evaluated on both training and testing datasets.

3. **Predictive System:** You can use the trained model to make predictions for new loan applications. Simply provide input data, and the script will return a prediction of "Approved" or "Not Approved."

Feel free to modify the input data in the `new_data` dictionary to make predictions for various scenarios.
## Data Collection and Processing

The Loan Predictor script includes the following steps for data collection and processing:

1. **Importing Modules:** The script imports essential Python libraries such as NumPy, pandas, seaborn, and scikit-learn's SVM classifier.

2. **Loading the Dataset:** It loads the dataset from `Loan_Dataset.csv` using pandas and displays the initial rows to provide a data preview.

3. **Handling Missing Values:** Data preprocessing includes handling missing values, ensuring that the dataset is clean and complete.

4. **Converting Categorical Data:** Categorical values are converted into numerical ones to prepare the data for model training.

You can customize this section to provide more details about your specific data preprocessing steps if needed.
## Model Training and Evaluation

The Loan Predictor script trains and evaluates a Support Vector Machine (SVM) classifier as follows:

1. **Data Split:** The dataset is split into training (90%) and testing (10%) sets to assess the model's performance.

2. **Classifier Creation:** An SVM classifier with a linear kernel is created and trained on the training data.

3. **Model Accuracy:** The script calculates the accuracy of the trained model on both the training and testing datasets to gauge its effectiveness.

You can expand on this section to provide insights into the model's performance, additional evaluation metrics, or details about the SVM classifier.
## Predictive System

The Loan Predictor script includes a predictive system that allows you to make loan approval predictions for new data:

1. **Input Data:** Define a dictionary named `new_data` with input features for a loan application, including gender, marital status, income, credit history, and more.

2. **Prediction:** The `predict_loan_approval` function uses the trained model to predict whether the loan application is "Approved" or "Not Approved" based on the provided input data.

Here's an example of how to use the predictive system:

```python
new_data = pd.DataFrame({
    'Gender': ['Male'],
    'Married': ['Yes'],
    'Dependents': ['2'],
    'Education': ['Graduate'],
    'Self_Employed': ['No'],
    'ApplicantIncome': [5000],
    'CoapplicantIncome': [2000],
    'LoanAmount': [150],
    'Loan_Amount_Term': [360],
    'Credit_History': [1],
    'Property_Area': ['Semiurban']
})

# Predict loan approval for new data
result = predict_loan_approval(classifier, new_data)
print('Loan Status Prediction:', result)
