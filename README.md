# 🛡️ Telco Fraud & Anomaly Detection System
### Project: Revenue Protection Audit for XL Axiata (Simulation)

![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)
![Scikit-Learn](https://img.shields.io/badge/Machine_Learning-Isolation_Forest-orange.svg)
![Plotly](https://img.shields.io/badge/Dashboard-Interactive-green.svg)
![Pandas](https://img.shields.io/badge/Data_Analysis-Pandas_2.2-purple.svg)

## 📌 Business Context
Between 2017 and 2022, the telecommunications industry in Indonesia underwent a massive transition from legacy services (Voice/SMS) to data-centric 4G dominance. This shift created new vulnerabilities for **Revenue Leakage**. This project simulates an automated audit system designed to detect two high-impact anomalies:

1. **Simbox Fraud (Interconnect Bypass)**: The use of unauthorized SIM boxes to terminate international calls as local traffic, bypassing interconnect fees.
2. **Data Abuse & FUP Violation**: Identifying non-human data consumption patterns (e.g., illegal commercial tethering or bot servers) that degrade network quality for legitimate users.

## 🚀 Key Features
* **End-to-End Pipeline**: A complete workflow from raw CDR (Call Detail Record) simulation to automated feature engineering and detection.
* **Unsupervised Machine Learning**: Utilizes the **Isolation Forest** algorithm to detect "outlier" behavioral patterns without needing pre-labeled historical fraud data.
* **Feature Engineering**: Derived domain-specific metrics such as *Call-to-Destination Ratio* and *Data Usage Intensity*.
* **Financial Impact Assessment**: Quantifies detected anomalies into potential monetary loss (IDR) to provide actionable business insights.
* **Interactive Analytics Dashboard**: A high-performance HTML dashboard featuring logarithmic scatter plots and time-series trend analysis.

## 🏗️ Project Structure
```text
├── data/
│   ├── raw/             # Synthetic CDR & Session data
│   ├── processed/       # Scaled features & engineered metrics
│   └── results/         # List of flagged MSISDNs (Blacklist Suspects)
└── src/
    ├── traffic_simulator.py    # Generates human vs. machine behavior
    ├── feature_engineering.py  # Behavioral profiling logic
    ├── detector.py             # Isolation Forest ML implementation
    ├── dashboard_fraud.py      # Plotly-based UI generation
    └── main.py                 # Orchestrator script
