# 627Astro-mudie1
1
📘 Student Exam Score Prediction
🔹 Project Overview

This project predicts student exam performance (GradeClass) using factors such as study habits, GPA, absences, and parental support.
The goal is to build regression models that can identify which factors most strongly influence student outcomes and predict performance within a reasonable accuracy.

🔹 Problem Statement

Educational institutions often want to understand:

How much do study habits impact grades?

Can we predict which students are at risk of poor performance?

This is a supervised machine learning regression problem, where the target variable is GradeClass (encoded as 0 = best grade, 4 = lowest grade).

🔹 Dataset

Rows: 2,392 students

Columns: 15 features

Key Features:

StudyTimeWeekly → hours of study per week

Absences → number of classes missed

GPA → grade point average

ParentalSupport, ParentalEducation → family factors

Tutoring, Sports, Music, Volunteering, Extracurricular → activities

GradeClass → target (numeric, 0=best, 4=worst)

🔹 Data Preprocessing

Dropped non-informative columns (StudentID).

Converted boolean columns (e.g., Sports, Music, Volunteering) into integers (0/1).

Checked and removed duplicates.

Verified no missing values in the dataset.

Final dataset is fully numeric and ready for ML.

🔹 Exploratory Data Analysis (EDA)

GPA was the strongest predictor of grade.

Absences were strongly negatively correlated (more absences → worse grades).

StudyTimeWeekly showed a positive effect on grades (more study → better performance).

Parental support and parental education had moderate positive effects.

📊 Visuals:

Correlation heatmap showed GPA, Absences, and StudyTimeWeekly as most important features.

Scatter plots confirmed trends (e.g., more absences → lower grades).

🔹 Modeling & Results
1. Linear Regression (Baseline)

MAE: ~0.54

RMSE: ~0.74

R²: ~0.63
➡ Baseline model explains ~63% of variance in grades.

2. Polynomial Regression (Degree=2)

MAE: ~0.38 (improved)

RMSE: ~0.63

R²: ~0.73 (better fit, but some risk of overfitting)

3. Polynomial Regression (other runs)

Performance sometimes dropped (R² ≈ 0.59) → showing sensitivity to overfitting.

(Optional) 4. Random Forest Regression

Suggested next step for future work.

Captures non-linear relationships automatically.

🔹 Key Insights

GPA is the strongest single predictor of exam performance.

Absences negatively impact grades significantly.

Study time has diminishing returns, showing non-linear effects.

Family and support activities have moderate but meaningful influence.

🔹 Conclusion

Simple linear models can already predict exam performance within ~0.5 grade accuracy.

Polynomial regression improves fit but risks overfitting.

Tree-based models (Random Forest, Gradient Boosting) are promising next steps.

🔹 Future Work

Add new features (sleep, stress, participation, lifestyle).

Experiment with Random Forests, Gradient Boosting, and XGBoost.

Use cross-validation for more robust evaluation.

Deploy as a small app (e.g., Streamlit) for teachers/students to test scenarios.
