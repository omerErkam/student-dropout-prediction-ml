# Predicting Students' Academic Success and Dropout Using Machine Learning

## 📌 Project Overview
Dropout in higher education has significant adverse impacts on students, institutions, and socioeconomic growth. This project addresses the critical need for early intervention by developing a supervised machine learning classification model to identify at-risk students early in their academic journey. 

Using a comprehensive dataset from the UCI Machine Learning Repository containing 4,424 student records across 36 demographic, socioeconomic, and academic attributes, this project systematically evaluates 18 machine learning algorithms[cite: 1]. The final solution provides a highly precise early-warning system to flag potential dropouts for timely institutional support[cite: 1].

## 🛠️ Tech Stack & Tools
*   **Programming Language:** Python[cite: 1]
*   **Environment:** Jupyter Lab[cite: 1]
*   **Data Manipulation & Analysis:** pandas, NumPy (implied for CSV handling and array operations)[cite: 1]
*   **Machine Learning Libraries:** scikit-learn, XGBoost[cite: 1]
*   **Data Visualization:** Matplotlib, Seaborn (implied for generated plots, matrices, and ROC curves)[cite: 1]

## 🔬 Methodology
The project follows a rigorous end-to-end data science pipeline to reproduce and validate the findings from the base research paper[cite: 1, 2]:

1.  **Data Preprocessing:** 
    *   Converted discrete variables (e.g., Marital status) into categorical formats[cite: 1].
    *   Handled data consistency by synchronizing enrolled and graduated numbers and checking for duplicate records[cite: 1].
    *   Identified and removed outliers utilizing the Interquartile Range (IQR) method ($1.5 \times IQR$)[cite: 1].
2.  **Exploratory Data Analysis (EDA) & Feature Selection:**
    *   Visualized data distributions using histograms and boxplots[cite: 1].
    *   Conducted bivariate analysis against the target variable for key academic features[cite: 1].
    *   Utilized a $\Phi_k$ correlation matrix, systematically dropping variables with a correlation coefficient of $<0.4$ to the final outcome, reducing the feature space to the 7 most predictive attributes[cite: 1].
3.  **Model Training:**
    *   Implemented a 70% training and 30% testing data split[cite: 1].
    *   Trained and evaluated 18 distinct machine learning models (including Neural Networks, Logistic Regression, SVM, Random Forest, Bagging Classifiers, XGBoost, and Stacking Classifiers)[cite: 1].
4.  **Evaluation Strategy:**
    *   Developed custom Python functions to calculate Accuracy, Precision, Recall, F1 Score, AUC ROC, and Confusion Matrices[cite: 1].
    *   Prioritized **Precision** over Recall to minimize false positives, as predicting a student will graduate when they will actually drop out is considered a higher risk than the reverse[cite: 1].

## 📊 Results & Evaluation
The comparative analysis of the 18 models revealed that the **Tuned XGBoost** and **Stacking Classifier** (equipped with AdaBoost and Gradient Boost) yielded the best overall performance[cite: 1]. 

*   **Top Performance:** Both models achieved an impressive **AUC of 0.94**[cite: 1].
*   **Final Model Selection:** The **Stacking Classifier** was selected as the optimal model due to its superior Precision score, effectively minimizing false-positive predictions[cite: 1].
*   **Feature Importance:** The most critical predictors of student success were academic performance metrics, specifically: *Curricular units 2nd semester (approved)*, *Curricular units 1st semester (approved)*, and *Curricular units 1st semester (enrolled)*[cite: 1].
