❤️ Heart Disease Prediction — Machine Learning Project
   * A complete end-to-end machine learning and data analysis project using Google Colab.

📘 Project Overview

This project builds a machine-learning model to predict the presence of heart disease using demographic, clinical, and ECG-based features.
The workflow includes exploratory data analysis (EDA), missing value handling, feature engineering, visualization, and model optimization using k-Nearest Neighbors.

The workflow includes:
 * Data loading & exploration
 * Data cleaning & preprocessing
 * Visualizing risk patterns
 * Feature engineering
 * k-NN model building
 * Hyperparameter tuning with GridSearchCV
 * Test accuracy evaluation


🧭 Objectives

* Understand key clinical indicators that correlate with heart disease
* Explore and visualize patient characteristics
* Build a clean, reliable dataset for modeling
* Train and optimize a k-Nearest Neighbors classifier
* Evaluate model performance using accuracy & confusion matrix


📂 Dataset

The dataset contains patient information including:
  * Age
  * Sex
  * Chest pain type
  * Blood pressure
  * Cholesterol
  * Resting ECG results
  * Exercise-induced angina
  * Maximum heart rate
  * Oldpeak (ST depression)
  * ST Slope
  * Heart Disease (target variable)


🔎 Exploratory Data Analysis (EDA)

📊 1. Categorical Feature Distributions

Countplots were created for features such as:
  * Sex
  * ChestPainType
  * FastingBS
  * RestingECG
  * ExerciseAngina
  * ST_Slope

These charts revealed strong imbalances and trends, especially in Sex and ChestPainType.

<img width="1315" height="1218" alt="image" src="https://github.com/user-attachments/assets/99099d29-b9e4-4fed-b73a-5832b4d8f019" />

⭐ Key Insight:

  * Males show a significantly higher rate of heart disease than females.
  * Asymptomatic chest pain (ASY) is strongly associated with heart disease.

🎯 2. Categorical Features vs Heart Disease

   * For each categorical variable, side-by-side bar charts were generated to compare distributions of:
   * Feature vs HeartDisease (0 or 1)

<img width="1315" height="917" alt="image" src="https://github.com/user-attachments/assets/77532d69-a26f-4af2-89b3-6422b9d1f624" />

⭐ Key Findings:

  * Patients with ExerciseAngina = Yes had a much higher incidence of heart disease.
  * ST Slope (Flat / Down) was one of the strongest ECG indicators of disease.
  * Typical angina was uncommon among heart disease patients.

🔧 3. Data Cleaning

The dataset included impossible values (e.g., Cholesterol = 0, RestingBP = 0) which were corrected using median imputation, grouped by disease status.
These steps ensure the dataset reflects real-world clinical ranges and improves model accuracy.


🧮 4. Feature Engineering & Encoding

 * Categorical columns were converted using one-hot encoding
 * Redundant dummy variables were removed using drop_first=True
 * Numerical predictors were scaled using MinMaxScaler for distance-based modeling.


🔥 5. Correlation Heatmap

A correlation heatmap was generated to highlight relationships among variables.
Top Predictive Features Identified:
 * MaxHR
 * Oldpeak
 * ExerciseAngina_Y
 * ST_Slope_Flat
 * ST_Slope_Up
 * Sex_M
These features were later used for model training.

<img width="1020" height="789" alt="image" src="https://github.com/user-attachments/assets/89adebba-cf7a-49f7-b4f7-6af1dd93c6e7" />

Highlights the clinical indicators most associated with heart disease.

🤖 Machine Learning Modeling

1️⃣ Baseline Models
  * A k-NN model was trained using one feature at a time to evaluate predictive strength.
  * This step identifies strong standalone predictors before multivariate modeling.

2️⃣ Feature Scaling
  * Because k-NN uses distance, MinMax scaling was applied to selected features.


3️⃣ Hyperparameter Tuning

GridSearchCV tested:
 * k values (1–20)
 * Distance metrics (Minkowski, Manhattan)
The best model achieved:
 *  Strong validation accuracy
 *  Optimal balance between bias & variance


📈 Final Model Performance
* Test Accuracy:  87.68

* Confusion Matrix
   * The confusion matrix visualizes correct vs incorrect predictions across both classes.

Interpretation:

  * True Positive = correctly identified heart disease
  * True Negative = correctly identified healthy patients
  * False Positive/Negative = misclassifications

<img width="498" height="432" alt="image" src="https://github.com/user-attachments/assets/420e17d5-5fc2-43ad-905c-0231e5629d1c" />

Shows model correctness and error type.


🧠 Key Insights

 * Exercise-induced angina and ST slope characteristics are strong indicators of heart disease.
 * Patients with asymptomatic chest pain have a much higher disease probability.
 * ECG features and maximum heart rate play critical roles in prediction.
 * With tuning, k-NN can perform surprisingly well on clinical tabular data.


🏁 Conclusion

This project demonstrates an end-to-end machine-learning workflow, from exploratory analysis to final model evaluation.
It provides strong portfolio value by showcasing:
 * Data cleaning
 * Medical dataset interpretation
 * Visual storytelling
 * k-NN modeling
 * Hyperparameter optimization.
   
 * Practical insight generation





