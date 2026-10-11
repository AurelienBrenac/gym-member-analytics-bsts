# Gym Member Analytics: Churn Prediction & Marketing Inferences using BSTS & SHAP

This repository contains an end-to-end data science and business analytics pipeline engineered to solve core acquisition, behavioral retention, and marketing attribution challenges within high-volume, membership-based ecosystems (Value-Gym networks & Wearable tech platforms like Planet Fitness / WHOOP / Basic-Fit).

## 📊 Executive Workstreams
1. **Predictive Biomarker Churn Pipeline:** Blending transactional field attendance records with wearable telemetry data (Heart Rate Variability & Chronic Stress scores) via an advanced Gradient Boosting architecture (`HistGradientBoostingClassifier`).
2. **Causal Marketing Attribution:** Leveraging a native **Bayesian Structural Time Series (BSTS)** state-space model (`statsmodels.tsa.UnobservedComponents`) to construct a synthetic counterfactual twin, isolating true incremental marketing campaign lift from organic seasonal cycles (e.g., the classic January New Year rush).
3. **Model Interpretability (SHAP Suite):** Utilizing Shapley Additive exPlanations to open the tree-based "black box," map exact causal directions, and isolate complex non-linear interactive features without classical econometric multicollinearity inflation.

## 🔬 Core Insights & Domain Mechanics
- **The "Athlete Regularity" Edge:** Driven by SHAP dependency analysis, the architecture successfully isolates programmatic training adjustments (low-frequency check-in consistency combined with low chronic stress load) from genuine, fatigue-driven drop-out risks.
- **Biomarker Precursors:** Autonomic nervous system metrics (HRV streams) display a higher predictive and preventative weight regarding upcoming customer churn than standard demographic or contractual life cycle variables.

## 🎯 Productionization Architecture: Event-Driven CRM
Rather than executing static batch campaigns, this pipeline is architected to scale into an automated, continuous, trigger-based retention ecosystem:
- **Continuous Scoring:** Transactional logs and wearable feeds are processed daily via an inference API to generate real-time, individual member-level probability scores.
- **Automated Trigger-Based Workflows:** The moment a profile cross-validates a critical risk threshold (>75%), specialized webhooks fire targeted CRM micro-actions based on underlying SHAP vectors (e.g., pushing biomarker-driven recovery recommendations vs. engagement-driven attendance hooks).

## 🛠️ Setup & Notebook Execution
Ensure you have the required analytical libraries installed:
```bash
pip install pandas numpy scikit-learn statsmodels shap matplotlib
```
Run the complete interactive notebook layout:
```bash
jupyter notebook member_analytics_pipeline.ipynb
```
