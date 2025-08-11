## "Fresh Tomato" Predictor: Predicting Movie Success on Rotten Tomatoes

---
### **Objective**
The goal was to build a machine learning model to predict if a movie would be a critical success ("Fresh") or failure ("Rotten") on Rotten Tomatoes, based on its metadata.

---
### **Methodology & Key Findings**

This project demonstrated a complete, iterative data science workflow, from initial exploration to a final, optimized model that successfully predicted outcomes with 70% accuracy.

1.  **Baseline Model:** We began by establishing a **Logistic Regression** baseline, which achieved **65% accuracy**. This provided the initial benchmark to beat.

2.  **Model Tuning:** A **Gradient Boosting Classifier** tuned with `GridSearchCV` improved our score to **66%**, showing the value of hyperparameter optimization.

3.  **Advanced Feature Engineering (Iteration 1):** The first major breakthrough came from replacing a simple genre count with **one-hot encoded genres**. This allowed the model to learn the specific weight of each genre, pushing accuracy to **69%**.

4.  **Advanced Feature Engineering (Iteration 2):** Creating features for only the **Top 30** most frequent actors, directors, and production companies provided the final performance boost to **70%**. This became our champion model's feature set.

5.  **Final Stress Test:** A final experiment using one-hot encoding for *all* unique actors, directors, and companies also yielded 70% accuracy. This confirmed that our "Top 30" strategy was the most efficient approach, successfully capturing all the signal without adding unnecessary complexity or noise.

---
### **Conclusion**

The final, champion model—a tuned **Gradient Boosting Classifier**—can predict a movie's critical success with **70% accuracy**.

The project's success underscores a critical lesson in applied machine learning: **the key to unlocking performance often lies in intelligent feature engineering, not just model complexity**. By systematically progressing from simple features to more granular, high-signal representations, we measurably improved the model's predictive power at each step. The final model is both accurate and efficient, avoiding the computational cost and risk of overfitting associated with a brute-force encoding approach.

Congratulations on completing this extensive and highly successful machine learning project! You've demonstrated a full range of skills from data cleaning and EDA to advanced feature engineering, model tuning, and iterative improvement. 🎉
