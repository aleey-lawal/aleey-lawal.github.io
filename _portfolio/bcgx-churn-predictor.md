---
title: "BCG X PowerCo Customer Churn Predictor"
excerpt: "End-to-end machine learning pipeline predicting customer churn for
a major gas and electricity utility — combining feature engineering on pricing
and consumption data with a Random Forest classifier deployed as a
production-grade REST API using FastAPI."
collection: portfolio
---

## Overview
BCG X engaged to investigate why PowerCo, a major SME gas and electricity
utility, was experiencing significant customer churn. The central hypothesis
was that price sensitivity was the primary driver. This project builds a full
ML pipeline to test that hypothesis — from raw customer and pricing data
through to a deployed prediction API.

## Key Results
- **90.39% accuracy** and **85.71% precision** on the test set
- **14,606 customers** modelled across 26 features
- **Key finding:** Net margin and consumption patterns are stronger churn
  drivers than price sensitivity — partially challenging BCG's original hypothesis
- Deployed as a **production-grade REST API** using FastAPI
- Class imbalance (~10% churn rate) acknowledged openly; proposed fixes include
  `class_weight='balanced'`, SMOTE oversampling, and threshold tuning

## Methodology
- **EDA:** Analysed churn distribution, consumption patterns, tenure, and
  pricing behaviour across customer segments
- **Feature Engineering:** Engineered pricing differential features
  (Dec–Jan off-peak/peak differences, average and maximum monthly price gaps),
  plus tenure, months active, months to contract end, and months since renewal
- **Modelling:** Random Forest classifier (100 trees), 75/25 train/test split
- **Top churn drivers:** Net margin on electricity, 12-month consumption,
  gross margin on power, customer tenure, and price sensitivity features

## Tech Stack
Python · scikit-learn · FastAPI · Pandas · NumPy · Matplotlib · Seaborn

## Links
- 🚀  [Live App](https://bcgx-churn-predictor.onrender.com/)
- 💻  [GitHub Repo](https://github.com/aleey-lawal)
