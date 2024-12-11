# GROUP-5-DSEB64B-FINAL-DATA-PREP
# Credit Risk Modeling Preprocessing

Welcome to the **Credit Risk Modeling Preprocessing** repository! This repository is dedicated to the preprocessing stage of a credit risk modeling project. The goal is to clean, transform, and engineer features from the raw data to enhance the predictive power of our models.

## Table of Contents
1. [Introduction](#introduction)
2. [Data Description](#data-description)
3. [Preprocessing Steps](#preprocessing-steps)
4. [Feature Engineering](#feature-engineering)
5. [Usage](#usage)
6. [Contributing](#contributing)
7. [License](#license)

## Introduction
Credit risk modeling aims to predict the likelihood of a customer paying a loan on-time. This repository focuses on the preprocessing steps required to transform raw data into a format suitable for machine learning models. Proper preprocessing is crucial for improving the model's accuracy and reliability.

## Data Description
The dataset contains various features related to loan applications, including client information, loan details, and previous credit history. The key tables include:
- **application_train/application_test**: Main tables with client and loan information.
- **bureau**: Previous credit history data from other institutions.
- **bureau_balance**: Monthly balance of credits in Credit Bureau.
- **previous_application**: Information on previous loan applications.
- **POS_CASH_balance**: Monthly balance of client's previous loans in Home Credit.
- **installments_payments**: Payment history data in Home Credit.
- **credit_card_balance**: Monthly balance of client's previous credit card loans in Home Credit.

## Preprocessing Steps
1. **Missing Value Handling**:
   - Replacing placeholders with `NaN` for certain date columns.
   - Imputing missing values for numerical and categorical features.

2. **Normalization and Scaling**:
   - Standardizing numerical features to have a mean of 0 and a standard deviation of 1.

3. **Encoding Categorical Features**:
   - Mapping ordinal categories to numerical values (e.g., education levels).
   - Target encoding for nominal categories.

## Feature Engineering
### Aggregated Features:
- **Credit History Aggregates**: Summarizing loan counts, types, and amounts.
- **Debt Ratios**: Calculating ratios of debts to credit amounts and overdues.
- **Payment Behavior**: Creating features to capture late payments, overpayments, and on-time payments.

### New Features:
- **FLAG_CONTACTS**: Total contact methods available for each client.
- **FLAG_DOCS**: Count of submitted documents.
- **FLAG_ADDRESS**: Count of verified address attributes.
- **EXP_HOUSE**: Total housing expenditure based on various housing attributes.
- **DAYS_LATE_PAYMENT**: Days a payment is late.
- **AMT_PAYMENT_INSTALMENT_RATIO**: Ratio of payment amount to installment amount.

## Usage
To run the preprocessing scripts and notebooks:
1. Clone the repository:
   ```sh
   git clone https://github.com/AllyPham04/GROUP-5-DSEB64B-FINAL-DATA-PREP.git

2. Install the required packages:
   ```sh
   pip install -r requirements.txt

3. Run the preprocessing and feature engineering notebooks:
   ```sh
   jupyter notebook notebooks/data_cleaning.ipynb
