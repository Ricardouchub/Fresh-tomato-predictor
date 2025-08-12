# Predicting Movie Success on Rotten Tomatoes with Machine Learning

<p align="left">
  <img src="https://img.shields.io/badge/Project_Complete-%E2%9C%94-2ECC71?style=flat-square&logo=checkmarx&logoColor=white" alt="Project Complete"/>
  <img src="https://img.shields.io/badge/Python-3.9+-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python"/>
  <img src="https://img.shields.io/badge/Pandas-Data_Analysis-150458?style=flat-square&logo=pandas&logoColor=white" alt="Pandas"/>
  <img src="https://img.shields.io/badge/scikit--learn-ML_Modeling-F7931E?style=flat-square&logo=scikit-learn&logoColor=white" alt="scikit-learn"/>
  <img src="https://img.shields.io/badge/XGBoost-Advanced_Model-5C2D91?style=flat-square&logo=xgboost&logoColor=white" alt="XGBoost"/>
  <img src="https://img.shields.io/badge/Seaborn-Visualization-3AA0E6?style=flat-square&logo=seaborn&logoColor=white" alt="Seaborn"/>
</p>

An in-depth analysis of movie metadata to build a Machine Learning model capable of predicting critical success and discovering which features define a hit film.

### [Notebook](https://github.com/Ricardouchub/Fresh-tomato-predictor/blob/main/Notebook.ipynb)

---

## **Table of Contents**
1. [Project Description](#1-project-description)
2. [Dataset](#2-dataset)
3. [EDA and Feature Engineering](#3-eda-and-feature-engineering)
4. [Modeling and Evaluation](#4-modeling-and-evaluation)
5. [Key Findings](#5-key-findings)
6. [Tools](#6-tools)
7. [Author](#7-author)

---

## **1. Project Description**
The objective of this project is to build and optimize a Machine Learning classification model to predict whether a movie will be a critical success ("Fresh") or a failure ("Rotten") on Rotten Tomatoes. The analysis focuses on using only the movie's metadata (genre, director, actors, etc.), simulating a prediction that could be made before its release and the publication of reviews.

The project covers a complete data science lifecycle, from initial cleaning and exploration to advanced feature engineering and model optimization to achieve maximum predictive performance.

---

## **2. Dataset**
This project uses the publicly available [Rotten Tomatoes Movies and Critic Reviews](https://www.kaggle.com/datasets/stefanoleone992/rotten-tomatoes-movies-and-critic-reviews-dataset) dataset from [Kaggle](https://www.kaggle.com). For this predictive analysis, the primary file used was:

`rotten_tomatoes_movies.csv`: Contains information on over 17,000 movies, including their rating, genre, director, actors, production company, and runtime.

---

## **3. EDA and Feature Engineering**
Before modeling, an exhaustive data preparation and feature creation process was carried out:

* **Exploratory Data Analysis (EDA)**: The distribution of classes "Fresh" vs. "Rotten" was investigated, correlations between numerical variables were analyzed using heatmaps, and data integrity was validated.

* **Simple Feature Engineering**: Basic numerical features were created from text, such as `release_year`, `num_genres`, `num_directors`, and `num_actors`.

* **Advanced Feature Engineering**: To capture more complex signals, one-hot encoding techniques were implemented:

    * **Genres**: A binary column was created for each unique genre (e.g., genre_Comedy, genre_Drama).

    * **High-Impact Entities**: The Top 30 most frequent directors, actors, and production companies were identified, and binary columns were created for each. This proved to be an effective strategy for handling variables with thousands of unique values.

---

## **4. Modeling and Evaluation**
Multiple models were trained and evaluated in an iterative process to find the best performer:

  1. **Logistic Regression**: Established a solid baseline model with **65% accuracy**.

  2. **Gradient Boosting (Tuned)**: Using GridSearchCV, the model's hyperparameters were optimized, achieving **66% accuracy**.

  3. **Gradient Boosting with Advanced Features**: The champion model was the result of combining the optimized GradientBoostingClassifier with the most comprehensive feature set (including one-hot encoding for genres, actors, directors, and production companies) with **70% accuracy**

**Final Evaluation Results**
The final champion model, an optimized **Gradient Boosting Classifier** trained on the richest feature set, achieved a global accuracy of 70%. This result represented a 5-percentage-point improvement over the baseline model, demonstrating the success of the feature engineering and tuning process.

<img width="505" height="423" alt="image" src="https://github.com/user-attachments/assets/f8c40154-8250-4b84-be56-ff6f7a09b66e" />


---

## **5. Key Findings**
The project's analysis and modeling revealed several key findings:

**The 70% Ceiling**: The final model achieved a peak performance of 70%, suggesting that most of the predictive signal from the available metadata has been extracted. To surpass this threshold, additional data sources would likely be needed (e.g., marketing budget, trailer sentiment analysis).

**Feature Engineering is Key**: The most significant performance improvement did not come from more complex algorithms but from smarter feature engineering. Moving from simply counting genres to representing them individually (one-hot encoding) was the most important leap.

**"Top 30" as a Winning Strategy**: The technique of identifying and encoding only the most frequent entities proved to be the most efficient way to extract value from high-cardinality columns, avoiding performance issues and overfitting.

<img width="1209" height="844" alt="image" src="https://github.com/user-attachments/assets/63a21adf-19f0-4d3f-a94f-1d36a706395a" />


---

## **6. Tools**
**Language**: Python

**Libraries**:

* Pandas and NumPy for data manipulation and analysis.
    
* Scikit-learn for preprocessing, modeling, tuning with GridSearchCV, and evaluation.
    
* XGBoost for experimentation with advanced models.
    
* Matplotlib and Seaborn for data visualization.

---

## **7. Author**
**Ricardo Urdaneta**

Linkedin link
