

# Talent Analytics – Fairness-Aware Modeling

Welcome! This project simulates a realistic hiring and retention pipeline using **synthetic candidate data**. It's designed to help you explore bias in machine learning models – without relying on sensitive real-world data.

---

## What’s Inside

- **5,000 synthetic candidates** with text and structured features  
- **Bias injection** based on manager behavior and demographic traits  
- **Explainable ML models** for hiring and retention using SHAP  
- **Fairness breakdowns** with annotated visualizations  
- **CSV + plot outputs** ready for dashboarding

---

## Quick Start

1. **Clone the repo**  
   ```bash
   git clone https://github.com/htleffew/hiring_analytics_simulator.git
   ```

2. **Install dependencies**  
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the full pipeline**  
   ```bash
   python main.py
   ```

4. **Review outputs**  
   - `synthetic_talent_data.csv`  
   - `shap_summary_hiring_model.png`  
   - `fairness_hired_ethnicity.png`
