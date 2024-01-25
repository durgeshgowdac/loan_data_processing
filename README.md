# Loan Dataset Cleaning

This repository contains code for cleaning and preprocessing a loan dataset using Python and pandas. The dataset is loaded into a pandas DataFrame, and various data cleaning operations are performed to ensure the dataset is suitable for analysis.

## Table of Contents

1. [Introduction](#introduction)
2. [Dataset Overview](#dataset-overview)
3. [Data Cleaning Operations](#data-cleaning-operations)
   1. [Dropping Duplicates](#1.-dropping-duplicates)
   2. [Data Standardization](#2.-data-standardization)
   3. [Handling Incorrect Records](#3.-handling-incorrect-records)
   4. [Handling Missing Values](#4.-handling-missing-values)
   5. [Converting Data Types](#5.-converting-data-types)
   6. [Outliers](#6.-outliers)
   7. [Dropping Irrelevant Columns](#7.-dropping-irrelevant-columns)
4. [Requirements](#requirements)
4. [Conclusion](#conclusion)

## Introduction

This project focuses on cleaning a loan dataset to prepare it for analysis. The dataset is loaded using pandas, and various data cleaning techniques are applied to address issues such as duplicates, inconsistent data, missing values, and outliers.

## Dataset Overview

The loan dataset consists of 13 columns, including 'UID', 'Marital_status', 'Dependents', 'Is_graduate', 'Income', 'Loan_amount', 'Term_months', 'Credit_score', 'approval_status', 'Age', 'Sex', 'Purpose', and 'Hobby'.

1. **UID:** Unique identifier for each loan application.
2. **Marital_status:** Marital status of the loan applicant (e.g., married, single, divorced).
3. **Dependents:** Number of dependents the applicant has.
4. **Is_graduate:** Indicates whether the applicant is a graduate (e.g., yes or no).
5. **Income:** The income of the loan applicant.
6. **Loan_amount:** The amount of the loan requested by the applicant.
7. **Term_months:** The term or duration of the loan in months.
8. **Credit_score:** The credit score of the applicant.
9. **Approval_status:** Indicates whether the loan was approved or not.
10. **Age:** Age of the loan applicant.
11. **Sex:** Gender of the loan applicant.
12. **Purpose:** Purpose of the loan (e.g., home purchase, education, business).
13. **Hobby:** Hobby of the loan applicant.


## Data Cleaning Operations

### 1. Dropping Duplicates

Duplicate rows are identified and removed from the dataset, both based on the entire row and specifically on the 'UID' column.

### 2. Data Standardization

String values in the 'Marital_status' and 'Sex' columns are standardized by converting them to uppercase. Additionally, 'M' and 'F' values in the 'Sex' column are replaced with 'Male' and 'Female', respectively.

### 3. Handling Incorrect Records

Negative values in the 'Age' column are replaced with a minimum valid age of 20.

### 4. Handling Missing Values

Missing values in the dataset are identified and addressed:
- 'Loan_amount', 'Term_months', and 'Age' columns are filled with their mean values.
- Missing values in the 'Is_graduate' column are filled with 'Graduate'.
- Rows with any remaining missing values are dropped.

### 5. Converting Data Types

Categorical data types are assigned to the 'Marital_status', 'Sex', and 'Is_graduate' columns. The 'Income' column is converted to the float data type.

### 6. Outliers

Outliers in the 'Income' column are identified and capped at the 10th and 90th percentiles.

### 7. Dropping Irrelevant Columns

The 'Hobby' column is dropped from the dataset.

### Requirements
- [pandas](http://pandas.pydata.org/)
- [NumPy](https://numpy.org/)

## Conclusion

The dataset cleaning process ensures that the data is consistent, free of duplicates, and suitable for further analysis. The cleaned dataset is ready for exploration and modeling in subsequent steps.

Colab Link:
You can use following link to view and comment on the project:
- [Loan Data Processing & Cleaning](https://colab.research.google.com/drive/11RdQgL_Kr88n-PSHamHqaoPmxZ0eTzRD?usp=sharing)
