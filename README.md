# Predicting Heart Disease Risk Using Machine Learning Techniques

## Project Purpose
Heart disease is a leading cause of death, and identifying high-risk patients early supports
earlier intervention. This capstone project builds and compares machine learning models that
predict whether a patient has heart disease from routine clinical measurements, and then tests
how the best model's predictions respond to realistic changes in key risk factors.

## Dataset
- **Name:** UCI Heart Disease Data
- **Source:** Kaggle - https://www.kaggle.com/datasets/redwankarimsony/heart-disease-data

## Research Questions
1. Which patient characteristics have the strongest relationship with heart disease?
2. Does a neural network provide more accurate predictions than a baseline classification model?
3. How do changes in cholesterol, resting blood pressure, maximum heart rate, and exercise-related
   variables affect predicted heart disease risk?

## Analytical Approach
1. **Data cleaning & EDA:** built a binary target from the severity score, handled missing
   values, corrected impossible zeros, capped outliers at 1.5×IQR,
   one-hot encoded categoricals, standardized numeric features, and engineered
   age_group and chol_level.
2. **Baseline model:** a Decision Tree Classifier.
3. **Neural network:** a Keras feed-forward network (32 -> 16 -> 1, ReLU + sigmoid).
4. **Scenario analysis:** used the neural network to evaluate a baseline plus three
   what-if scenarios.
5. **Dashboard:** an interactive Power BI dashboard, updated with scenario results.

## Summary of Major Findings
- The strongest predictors were exercise-induced angina, ST depression, maximum heart rate, and the
  number of major vessels; cholesterol and resting blood pressure were weak on their own.
- The neural network outperformed the baseline (accuracy 0.804 vs 0.766, F1 0.827 vs 0.802).
- Scenario analysis: improving cardiovascular health lowered predicted risk the most
  (56.2% -> 45.7%), exercise-stress indicators raised it the most (-> 66.4%), and cholesterol/blood-
  pressure changes barely moved it, answering Research Question 3.
- Results are associational, not proof of real-world causation.

## Required Python Libraries or Dependencies
- Python 3.10+
- pandas, numpy
- scikit-learn
- matplotlib, seaborn
- tensorflow (Keras)

Installation command:
```
pip install pandas numpy scikit-learn matplotlib seaborn tensorflow
```

## Basic Instructions to Run the Notebook
1. Place `project_cleaned_data.csv` in the same folder as the notebook
2. Open `5.2 Project.ipynb` in Jupyter
3. Restart the kernel and run all cells from top to bottom
4. The notebook trains the model, runs the scenario analysis, and writes `scenario_results.csv`

## Important Files in the Repository
| File | Description |
|------|-------------|
| 5.2 Project.ipynb | Final scenario-analysis notebook |
| project_cleaned_data.csv | Cleaned dataset from Part 2, used to run the analysis |
| scenario_results.csv | Scenario comparison table exported by the notebook, feeds the dashboard |
| Project Dashboard.pbix | Power BI dashboard |
| 5.2 Project Final Report.docx | Comprehensive final report and dashboard appendix |
| Project Presentation.pptx | Project presentation |
| README.md | This file |

