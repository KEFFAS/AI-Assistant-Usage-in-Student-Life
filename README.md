# AI Assistant Usage in Student Life 

This repository contains my end-to-end **data science project** exploring how students use AI assistants.  
I performed data cleaning, exploratory data analysis, feature engineering, visualisations and built several classification models to predict outcomes like `FinalOutcome` and `UsedAgain`.

---

## 🎯 Objectives
- Understand usage patterns of AI assistants by student level, discipline and task type.
- Analyse session lengths, prompts and assistance levels.
- Engineer meaningful new features from raw data.
- Build and compare multiple machine learning models to predict student outcomes.

---

## 📚 Skills Demonstrated
- **Data Wrangling & EDA:**  
  Loading data, checking shape, dtypes, missing values, summary stats, unique values, grouping and aggregation.
- **Visualisation:**  
  Histograms, bar charts, countplots, boxplots, pie charts, scatterplots, line charts and heatmaps using `matplotlib` and `seaborn`.
- **Feature Engineering & Encoding:**  
  Date extraction (Year, Month, Day), label encoding and one-hot encoding for categorical features, new features like `PromptsPerMinute`, binning session lengths into Short/Medium/Long.
- **Machine Learning Models:**  
  Decision Tree, Logistic Regression, Random Forest, K-Nearest Neighbors, Naive Bayes, Gradient Boosting, XGBoost implemented with `scikit-learn` and `xgboost`.
- **Model Evaluation & Tuning:**  
  Accuracy, confusion matrix, classification report, cross-validation, GridSearchCV for hyperparameter tuning, and model comparison.

---

## 📝 Project Workflow

### 1. Basic EDA
- Loaded the dataset and displayed the first rows, shape, column names and dtypes.
- Checked for missing values and summary statistics for `SessionLengthMin` and `TotalPrompts`.
- Counted unique values in `StudentLevel`, `Discipline`, and `TaskType`; identified the most common task type.
- Calculated average session length per student level.

### 2. Visualisation
- Plotted histogram of session lengths, bar chart of session counts by student level, countplot of task types, and boxplot of session lengths grouped by level.
- Created pie chart of `FinalOutcome`, scatterplot of `SessionLengthMin` vs. `TotalPrompts`, line chart of average `AI_AssistanceLevel` over time, and heatmap of correlations.

### 3. GroupBy & Aggregations
- Computed average session length for each task type.
- Identified which discipline had most sessions.
- Compared average assistance levels across student levels.
- Found most common `FinalOutcome` for graduates and median session length per outcome.

### 4. Feature Engineering & Encoding
- Converted `SessionDate` into `Year`, `Month` and `Day`.
- Label-encoded `StudentLevel` and one-hot encoded `TaskType`.
- Created `PromptsPerMinute` and binned session lengths into Short, Medium, Long.

### 5. Machine Learning (Classification)
- Predicted `FinalOutcome` with Decision Tree, Random Forest, Naive Bayes, Gradient Boosting and XGBoost.
- Predicted `UsedAgain` with Logistic Regression, KNN and Gradient Boosting.
- Split dataset into 80% training / 20% testing sets.
- Evaluated models using accuracy, confusion matrix and classification report.

### 6. Model Evaluation & Hyperparameter Tuning
- Performed cross-validation for Logistic Regression.
- Tuned Decision Tree with GridSearchCV.
- Tuned Random Forest hyperparameters (`n_estimators`, `max_depth`).
- Compared all models on `UsedAgain` prediction to identify the best performer.

