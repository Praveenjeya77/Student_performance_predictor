# Student Performance Predictor

This project involves exploring a simulated student performance dataset, understanding the factors influencing exam scores, and building a predictive model to estimate a student's exam score based on various attributes.

## Project Overview

The main goal of this notebook is to:
1.  **Generate and load a sample student performance dataset.**
2.  **Perform Exploratory Data Analysis (EDA)** to understand data distributions, relationships, and identify key insights.
3.  **Build a simple linear regression model** to predict exam scores.
4.  **Implement an interactive interface** for users to input new student data and get instant score predictions.

## Dataset

The dataset `student_data.csv` contains simulated student performance records with the following features:
-   `study_hours`: Number of hours a student studies.
-   `past_scores`: Scores from previous exams or assessments.
-   `attendance`: Student's attendance percentage.
-   `habits`: A score representing good study habits.
-   `exam_score`: The final exam score (target variable).

## Key Findings from Analysis

-   **Data Overview:** The dataset comprises 1000 student records with no missing values.
-   **Exam Score Distribution:** Average exam score is approximately 79.51, with a standard deviation of 14.32. Scores range from 37.7 to 100.
-   **Feature Importance (Correlation with Exam Score):**
    -   `study_hours`: Strongest positive correlation (0.517).
    -   `past_scores`: Moderate positive correlation (0.470).
    -   `attendance`: Weaker positive correlation (0.222).
    -   `habits`: Weakest positive correlation (0.169).
-   **Performance Categories:**
    -   51.8% of students achieved 'Excellent' (80-100).
    -   38.0% achieved 'Good' (60-80).
    -   10.0% achieved 'Average' (40-60).
    -   Only 0.2% were in the 'Poor' category (below 40).
-   **Top Performers Characteristics (score $\ge$ 80):** On average, these students showed higher `study_hours` (6.11), `past_scores` (68.15), `attendance` (77.25%), and `habits` (3.14) compared to the overall average.

## Predictive Model

A Linear Regression model was trained to predict `exam_score` using `study_hours`, `past_scores`, `attendance`, and `habits` as predictors. The model coefficients indicate the positive influence of each feature on the exam score.

## How to Use the Interactive Predictor

After running all cells in the notebook, navigate to the final code cells related to prediction. You will be prompted to enter values for a new student's attributes:

1.  **Enter study hours (0-10):** (e.g., 6)
2.  **Enter past scores (30-95):** (e.g., 70)
3.  **Enter attendance (50-100):** (e.g., 90)
4.  **Enter habits score (1-5):** (e.g., 4)

The model will then output a predicted `exam_score` and categorize the student's performance (e.g., Excellent, Good, Average, Poor).

## Next Steps

-   Explore more advanced machine learning models for prediction.
-   Consider feature engineering to create new predictive variables.
-   Conduct further analysis on specific performance categories to identify underlying factors.
