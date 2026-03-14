# Loyalty Probability Prediction

This repository contains a machine learning project for predicting customer loyalty probability in the telecom industry, based on customer behavior data. The project is part of Abderahim's Thesis research.

## Overview

Customer churn prediction is crucial for telecom companies to retain customers and improve service quality. This project uses various machine learning algorithms to predict whether a customer is likely to churn (leave the service) based on features such as transaction history, wallet balance, operating hours, and more.

## Dataset

The dataset used is `telecom_churn.csv`, which includes the following features:

- `Churn`: Target variable (1 if churned, 0 otherwise)
- `time_last_transaction`: Time since last transaction
- `time_last_login`: Time since last login
- `price`: Price per transaction
- `quantity`: Order quantity
- `store_type`: Type of store
- `tva_precentage`: TVA percentage
- `tva_type`: TVA type
- `has_wallet`: Whether the customer has a wallet
- `balance`: Wallet balance
- `operating_hours`: Operating hours

## Exploratory Data Analysis (EDA)

The `eda/` folder contains visualizations from the exploratory data analysis, including distributions of churn, wallet balance, operating hours, and relationships between variables.

## Models

Three machine learning models are trained and evaluated:

1. **Logistic Regression**
2. **Random Forest**
3. **XGBoost**

Each model's folder in `models/` contains evaluation plots such as confusion matrices, ROC curves, precision-recall curves, learning curves, and predicted probability distributions.

## Results

Model performance comparison (from `comparision.csv`):

| Model              | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|--------------------|----------|-----------|--------|----------|---------|
| Logistic Regression| 0.859    | 0.56      | 0.144  | 0.230    | 0.813   |
| Random Forest      | 0.931    | 0.849     | 0.639  | 0.729    | 0.866   |
| XGBoost            | 0.921    | 0.824     | 0.577  | 0.679    | 0.859   |

Random Forest performs the best overall.

## Usage

1. **Prerequisites**: Python 3.x, Jupyter Notebook, required libraries (scikit-learn, pandas, matplotlib, numpy, xgboost)

2. **Installation**:
   ```bash
   pip install scikit-learn pandas matplotlib numpy xgboost
   ```

3. **Running the Notebook**:
   - Open `train.ipynb` in Jupyter Notebook.
   - Execute the cells to perform EDA, train models, and evaluate results.

4. **Data**: Ensure `telecom_churn.csv` is in the root directory.

## Project Structure

```
.
├── columns                 # List of dataset columns
├── comparision.csv         # Model performance comparison
├── telecom_churn.csv       # Dataset
├── train.ipynb             # Main training notebook
├── eda/                    # Exploratory data analysis plots
└── models/                 # Trained models and evaluation plots
    ├── logistic_regression/
    ├── random_forest/
    └── xgboost/
```

## Contributing

This is a part of a thesis project. For contributions or questions, please contact the author.
