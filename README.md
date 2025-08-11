# "Fresh Tomato" Predictor

---
### **Objective**
The goal was to build a machine learning model to predict if a movie would be a critical success ("Fresh") or failure ("Rotten") on Rotten Tomatoes, based on its metadata before reviews are published.

---
### **Methodology & Key Findings**

Our project followed a complete, iterative machine learning workflow:

1.  **Data Preparation & EDA:** We began by cleaning the dataset, handling missing values, and performing exploratory data analysis. Visualizations like class balance plots and heatmaps helped us understand the initial state of the data.

2.  **Feature Engineering:** We created valuable numerical features from raw text, including `release_year`, `num_genres`, `num_directors`, and `num_actors`. Categorical data like `content_rating` was processed using **One-Hot Encoding**.

3.  **Baseline Modeling:** We established a **Logistic Regression** model as our baseline, which achieved **65% accuracy**. This set the benchmark for all future experiments.

4.  **Iterative Improvement & Tuning:**
    * An out-of-the-box **Random Forest** underperformed (60% accuracy), demonstrating that more complex models require careful tuning.
    * Our best model was a **Gradient Boosting Classifier** tuned with `GridSearchCV`. This process found the optimal hyperparameters and pushed our performance to a peak of **66% accuracy**.
    * Further experiments, including adding more complex features (top 30 actors) and using state-of-the-art models like **XGBoost**, did not improve upon this score. This confirmed we had reached the performance ceiling for the current feature set.

---
### **Conclusion**

The final and best model, a tuned Gradient Boosting classifier, can predict whether a movie will be "Fresh" or "Rotten" with **66% accuracy**.

The most impactful features were a combination of basic movie metadata (`runtime`, `content_rating`) and simple engineered counts (`num_actors`, etc.), rather than more complex features like the specific identities of popular actors. This project highlights a realistic machine learning scenario where success is found not just in using powerful models, but in careful data preparation, iterative experimentation, and methodical hyperparameter tuning. To significantly break the 66% performance barrier, a new approach focusing on different data sources (e.g., social media sentiment, NLP on plot summaries) would likely be required.

This project represents a complete and thorough data science workflow, from initial question to final, evaluated model. 🎉
