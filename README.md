# employee_attrition_prediction
A predictive analytics project that explores HR attrition patterns using a real-world employee dataset

Overview:
A predictive analytics project that explores HR attrition patterns using a real-world employee dataset. I engineered a complete machine learning pipeline, from exploratory data analysis and feature engineering to model building and optimization, to identify key drivers of employee turnover and predict attrition risk. The final tuned Random Forest Classifier achieved a strong balance of recall and precision, highlighting factors such as overtime, compensation, experience, and commute distance as major predictors of attrition.
The dataset contains demographic, performance, and satisfaction attributes for employees across various departments.

Process:
-Data Collection & Exploration: Imported and profiled HR employee data sourced from an open dataset (Kaggle / HR Analytics). Conducted exploratory analysis to understand variable distributions, correlations, and class imbalance.
-Data Preprocessing: Encoded categorical variables, standardized numeric features, and split the data into training and test sets. Addressed class imbalance through class weighting to emphasize accurate identification of employees likely to leave (recall-focused).
-Model Development:
Decision Tree Classifier: Baseline model to understand key splits and feature importance. Identified OverTime, MonthlyIncome, and TotalWorkingYears as major drivers.
Tuned Decision Tree: Implemented GridSearchCV to optimize max_depth, criterion, and min_samples_leaf for improved generalization.
Random Forest Classifier: Built a bagged ensemble model to mitigate overfitting and capture complex relationships.
Tuned Random Forest: Optimized n_estimators, max_features, and min_samples_leaf to achieve the best test-set performance.
Boosted Model (XGBoost): Explored gradient boosting as an optional extension to compare ensemble approaches.
Model Evaluation: Focused on recall to minimize false negatives (i.e., missing at-risk employees). Compared models using accuracy, precision, recall, and F1-score, along with feature importance visualizations.

-Key Findings:
Employees doing overtime with lower income and fewer total working years have a significantly higher attrition likelihood.
Long commute distances and absence of stock options further increase attrition risk.
The tuned Random Forest model achieved ~95% overall accuracy with 83% recall for the attrition class, making it the most balanced performer.
Interpretability: Feature importance plots and decision tree visualizations were used to extract transparent rules for HR decision-making.

-Technologies Used:
Python: pandas, NumPy, scikit-learn, Matplotlib, Seaborn, GridSearchCV, XGBoost

-Key Machine Learning Algorithms:
Decision Tree Classifier
Random Forest Classifier
Tuned Random Forest (GridSearchCV)
XGBoost Classifier
