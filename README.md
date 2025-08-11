## "Fresh Tomato" Predictor

---
### **Objective**
The goal was to build a machine learning model to predict if a movie would be a critical success ("Fresh") or failure ("Rotten") on Rotten Tomatoes, based on its metadata.

---
### **Methodology & Key Findings**

This project demonstrated a complete, end-to-end data science workflow, from initial exploration to a final, optimized model.

1.  **Baseline Model:** We began by establishing a **Logistic Regression** baseline, which achieved **65% accuracy**. This provided the initial benchmark to beat.

2.  **Initial Tuning:** An untuned Random Forest underperformed, but a **Gradient Boosting Classifier** tuned with `GridSearchCV` improved our accuracy to **66%**.

3.  **Advanced Feature Engineering (Iteration 1):** The first major breakthrough came from replacing a simple genre count with **one-hot encoded genres**. This allowed the model to learn the specific weight of each genre, pushing accuracy to **69%**.

4.  **Advanced Feature Engineering (Iteration 2):** The final improvement was achieved by adding one-hot encoded features for the **Top 30 most frequent actors, directors, and production companies**. This provided the model with highly specific, influential signals, achieving our final best score.

---
### **Conclusion & Final Model**

The final model, a tuned **Gradient Boosting Classifier**, achieved a peak accuracy of **70%**.

The project's success underscores a critical lesson in machine learning: performance gains are most often realized through thoughtful and iterative **feature engineering**. While model selection and tuning are important, the quality and granularity of the features provided to the model are what ultimately unlock its predictive power. We systematically progressed from simple features to highly specific ones, with each step providing a measurable lift in performance.

Congratulations on completing this extensive and highly successful machine learning project! You've demonstrated a full range of skills from data cleaning and EDA to advanced feature engineering, model tuning, and iterative improvement. 🎉
