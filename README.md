# Fraud Detection Project

This project aims to detect fraudulent transactions in a dataset using machine learning techniques. The data is highly unbalanced, so we handle it by downsampling the non-fraudulent transactions. We use Logistic Regression to classify the transactions and evaluate the model's performance.

## Dataset

The dataset used for this project is `Fraud.csv`.

## Project Steps

1. **Data Loading and Exploration**: Load the dataset and explore its shape and distribution of fraud vs non-fraud transactions.

```python
import numpy as np 
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
import os

os.chdir('C:\\Users\\aakan\\Downloads\\')
df = pd.read_csv('Fraud.csv')
print(df.shape)

# Checking the number of fraud and not fraud transactions
print('Fraud:', len(df[df.isFraud == 1]))
print('Not fraud:', len(df[df.isFraud == 0]))
