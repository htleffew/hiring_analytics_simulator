#FAQ

## Section 1: Technical Questions

### Q1: Is this real data? Can I use it in production?
No. This dataset is 100% synthetic, generated using `Faker` and programmatic rules. It’s designed for demonstration, testing, and education – not real-world deployment.

### Q2: How is bias introduced into the dataset?
Bias is added by simulating manager behaviors. Specific managers are assigned higher "penalty rates" against certain demographic traits (e.g., race, gender, age, accommodation requests). This affects the likelihood of being hired or retained.

### Q3: Can I swap in my own model instead of the Random Forests?
Yes. The modeling pipeline is modular. You can plug in any classifier that supports `.fit()` and `.predict_proba()`.

### Q4: How are SHAP values calculated?
SHAP values are calculated using `TreeExplainer` on the trained Random Forest. Text data is preprocessed via TF-IDF + Truncated SVD. Feature names are extracted using `get_feature_names_out()` from the pipeline.

### Q5: Does this notebook support group fairness metrics (e.g., equalized odds)?
Not yet. This version focuses on exploratory drift and disparity analysis using outcome rates and false positive/negative differences. However, the data structure supports additional metrics with minimal effort.

### Q6: Can I run this in Google Colab?
Yes. It runs in Colab with minimal setup. All dependencies are installable via pip.

---

## Section 2: Stakeholder & Decision-Maker Questions

### Q1: Are the results in this dataset real?
No. The data and decisions are simulated to reflect real-world patterns. They help demonstrate how bias might emerge – but no real people are represented here.

### Q2: Why are you showing hiring rates by ethnicity or gender? Isn’t that risky?
This simulation is designed to surface disparities safely. In a real system, this type of breakdown would be used to detect and correct unfair trends—not to make hiring decisions.

### Q3: What does a SHAP plot tell me?
It shows what influenced a model’s decision. For example, it might reveal that “JobTitle” and “Resume text” were strong predictors – or flag that “Gender” had unintended influence.

### Q4: What should I do if I see bias in the outputs?
The goal here is to explore what *could* happen. If this were real data, seeing disparities would trigger a deeper audit or corrective action. You can use this synthetic setup to rehearse that process safely.

### Q5: Can I use this to train my team?
Yes. The project is licensed for educational and internal use. It’s designed to support training around bias detection, model explainability, and ethical AI practices.

### Q6: What are the limitations of this simulation?
It doesn't capture every nuance of real human behavior or policy. It simplifies retention, treats bias as binary, and assumes manager behavior is fixed. But it’s a useful sandbox for asking the right questions.
