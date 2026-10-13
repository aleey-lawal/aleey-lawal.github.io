---
title: "BCG X Customer Churn Predictor"
excerpt: "Random Forest classifier predicting energy customer churn,
deployed as a live REST API using FastAPI — BCG X Data Science Job
Simulation project."
collection: portfolio
---

## Overview
Built an end-to-end ML classification pipeline predicting customer churn
for PowerCo, an energy company — as part of the BCG X Data Science Job
Simulation. Deployed as a production-grade REST API using FastAPI on
Render.com.

## Model Performance
- **Accuracy:** 90.39%
- **Precision:** 85.71%
- **Recall:** Low — due to class imbalance (~10% churn rate)
- **Trees:** 100 (Random Forest)

## Honest Assessment
The low recall is caused by class imbalance — only ~10% of customers
churn, so the model defaults to predicting "no churn" for most customers.
This limitation is displayed openly in the API. Proposed improvements
include class_weight='balanced' and SMOTE oversampling.

## Key Features Engineered
- Dec–Jan off-peak price differences
- Average and maximum price changes across time periods
- Customer tenure and contract duration
- Log-transformed consumption variables
- One-hot encoded sales channel and campaign origin

## How to Test the API
1. Click **"Try the API Interactively"** link below
2. Click **POST /predict → Try it out**
3. Paste customer data in JSON format
4. Click **Execute** to get the churn prediction

## Tech Stack
Python · scikit-learn · FastAPI · Uvicorn · Pandas · NumPy · Render.com

## Links
- 🚀 [Live API Homepage](https://bcgx-churn-predictor.onrender.com)
- 📖 [Try the API Interactively](https://bcgx-churn-predictor.onrender.com/docs)
- 💻 [GitHub Repo](https://github.com/aleey-lawal/bcgx-churn-predictor)
