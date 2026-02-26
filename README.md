# 🌱 DigiCow Farmer Adoption Prediction Challenge

## 📌 Project Overview

**Can we predict which farmers will turn training into action?**

Access to high-quality agricultural training is only the first step toward improving farm productivity. The real challenge lies in identifying **which farmers actually adopt improved practices after training — and why**.

This project builds a machine learning solution to predict the probability that a farmer will adopt a DigiCow-supported practice within:

- **7 days**
- **90 days**
- **120 days**

The model uses **only the information available at the time of first training**, ensuring realistic, real-world deployment potential.

Early adoption prediction enables:
- Targeted follow-ups  
- Smarter resource allocation  
- Improved extension strategies  
- Higher impact of agricultural interventions  

---

## 🏢 About the Organizations

### 🌍 Digital Africa
Launched in 2018, **Digital Africa** strengthens the capacity of African digital entrepreneurs to design and scale disruptive innovations serving the real economy. The initiative is supported by multiple international partners, including the French Development Agency (AFD).

### 🚜 DigiCow Africa LTD
**DigiCow Africa LTD** is an award-winning Kenyan Agritech company founded in 2018 (formerly FarmingTech Solutions).

- Named *Most Innovative Agritech in Kenya* (World Bank Challenge, 2019)
- Part of the *Disruptive Agricultural Technologies “1 Million Farmer Platform”*
- Currently working with **200,000+ farmers**
- Develops mobile-based digital extension tools
- Enables data-driven decision-making across the agricultural ecosystem

---

## 🎯 Problem Statement

The objective is to predict adoption probabilities within three time windows:

- `TX_07` → Adoption within 7 days  
- `TX_90` → Adoption within 90 days  
- `TX_120` → Adoption within 120 days  

This is a **multi-target probabilistic classification problem** with imbalanced classes.

---

## 📊 Evaluation Metric

This challenge uses a **multi-metric evaluation framework**.

### Final Score = Weighted Average of:

- **Log Loss (75%)**
  - Encourages well-calibrated probability predictions  
  - Penalizes confident but incorrect predictions heavily  

- **ROC-AUC (25%)**
  - Measures ranking performance  
  - Evaluates how well adopters are ranked above non-adopters  
  - Provides stability for imbalanced datasets  

---

## 📁 Submission Format

The submission file must contain predicted probabilities for each target:

`ID TX_07_AUC TX_07_LogLoss TX_90_AUC TX_90_LogLoss TX_120_AUC TX_120_LogLoss`
`ID_KYOSSX 0 0 0 0 0 0`
`ID_ADB87D 0 0 0 0 0 0`
`ID_XYZ13I 0 0 0 0 0 0`


Where:

- `TX_` stands for **Target**
- Each value represents a predicted probability

---

## 🏆 Results

- 🥇 **Top Model Score:** **0.97**
- 🚀 **My Best Model Score:** **0.93**

The performance demonstrates strong predictive power while maintaining reliable probability calibration.

---

## 🧠 Approach Summary

The modeling pipeline included:

- Data cleaning and preprocessing
- Feature engineering based only on training-time data
- Handling class imbalance
- Cross-validation with stratified folds
- Probability calibration
- Multi-target modeling strategy
- Hyperparameter tuning
- Ensemble experimentation

Special attention was given to:
- Preventing data leakage
- Ensuring realistic deployment assumptions
- Optimizing for Log Loss (primary metric)

---

## 🔍 Key Insights

- Adoption prediction is highly dependent on early behavioral indicators.
- Short-term (7-day) prediction behaves differently from medium-term (90/120-day) adoption.
- Probability calibration significantly improves leaderboard performance.
- Imbalance handling is critical for stable ROC-AUC performance.

---

## 🚀 Impact

Accurate early adoption prediction allows DigiCow and its partners to:

- Prioritize high-impact follow-ups
- Design personalized extension strategies
- Optimize field officer allocation
- Improve training program ROI
- Increase smallholder farmer productivity

This project demonstrates how machine learning can directly support agricultural transformation in Africa.

---

## 🛠 Tech Stack

- Python
- Pandas
- NumPy
- Scikit-learn
- LightGBM / XGBoost / CatBoost
- Cross-validation frameworks
- Probability calibration techniques

---

## 👤 Author

**Charles Mulinga**  
Data Analyst | Data Science Enthusiast | AI & Applied ML  
Focused on building real-world predictive systems for impact-driven organizations.

