
# Walkthrough: How the Project Works

This project simulates a realistic hiring and retention pipeline using synthetic data. It models how bias may arise from human decision-makers, and gives you tools to explore, visualize, and explain those dynamics.

## 1. Generate Candidates

We use `Faker` to build out realistic profiles:
- Resume blurbs
- Interview feedback
- Demographics
- Recruiter, team, manager assignments

## 2. Inject Bias

Manager-specific patterns affect hiring and retention based on:
- Race / ethnicity
- Gender identity
- Accommodation requests
- Age as a proxy for experience

This creates measurable disparities you can observe and audit.

## 3. Model Hiring & Retention

- Two Random Forest models are trained
- Structured + unstructured features
- Resume text processed with TF-IDF + SVD
- Model performance scored and compared

## 4. Explain Model Behavior

SHAP summary plots show:
- What drove each prediction
- Which features had the most impact
- Any problematic signals (like protected attributes)

## 5. Fairness Analysis

- Bar charts show outcome rates across groups
- Narrative statements highlight gaps (e.g., “Group A had highest hire rate…”)
- Plots exported to `.png` for use in reports or dashboards

## 6. Outputs

All major files are saved for you:
- `synthetic_talent_data.csv`
- SHAP and fairness visuals
- Narrative explanations
