---
title: "BHCPF Accountability Tracker"
excerpt: "ML-powered public accountability dashboard tracking ₦57.1 billion
in Basic Health Care Provision Fund disbursements across 37 Nigerian states
and FCT — combining unsupervised anomaly detection with a facility-level
risk model to flag states and PHCs warranting further investigation."
collection: portfolio
---

## Overview
Built an end-to-end machine learning pipeline to track and scrutinise ₦57.1
billion disbursed under Nigeria's Basic Health Care Provision Fund (BHCPF),
Q1–Q3 2025. The project combines unsupervised anomaly detection at the state
level with a supervised facility risk model across 8,309 primary health care
(PHC) facilities, deployed as an interactive Streamlit dashboard with a
citizen-facing accountability map.

## Key Results
- **3 states flagged CRITICAL** (Borno, Kano, Katsina) — extreme Q2 disbursement spikes detected by all 3 anomaly methods
- **501 facilities** scored HIGH risk (score ≥ 0.80) across 8,309 tracked PHCs
- **ROC-AUC 0.793** — Random Forest facility risk classifier (300 trees)
- **Recall AT RISK 0.64** — catches 64 in 100 genuinely at-risk facilities
- Interactive map where citizens can navigate to any facility and verify its functional status on the ground

## Methodology
- **Anomaly Detection (Unsupervised):** Isolation Forest + Local Outlier Factor + Z-score composite (3-method consensus scoring)
- **Facility Risk Model (Supervised):** Random Forest classifier with 14 engineered features including efficiency index, gateway entropy, QoQ volatility, and functionality score
- **Data Sources:** NPHCDA disbursement records (Excel + PDF), PHC facility registry (8,309 facilities), NPC 2023 population projections

## Tech Stack
Python · scikit-learn · Streamlit · Pandas · NumPy · Plotly · pdfplumber · Joblib

## Links
- 🚀 [Live Streamlit App](https://public-health-funding-machine-learning-accountability-model-gw.streamlit.app)
- 🗺️ [Interactive Accountability Map](https://legendary-churros-fc5ebd.netlify.app)
- 💻 [GitHub Repo](https://github.com/aleey-lawal/public-health-funding-machine-learning-accountability-model)
