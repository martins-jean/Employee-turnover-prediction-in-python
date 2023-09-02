# Employee Turnover Prediction in Python
Analyzed the factors contributing to employee turnover in order to help potential retention efforts.

## Project Overview

Used a predictive model based on a decision tree classifier in order to identify and assess various turnover risk factors.

## Reproducibility Guidelines

<details>
  <summary>Exploratory data analysis</summary>
  1. Import the necessary packages. <br>
  2. Load the dataset from its GitHub repository and transform into a Pandas dataframe. <br>
  3. Describe the contents of our dataset further. <br>
  4. Look for unique values. <br>
</details>

<details>
  <summary>Data transformation</summary>
  1. Change the type of the salary column to categorical. <br>
  2. Reorder the categories. <br>
  3. Encode the categories with integer values. <br>
  4. Get dummies and save them in a new dataframe. <br>
  5. Drop the accounting column to avoid dummy trap. <br>
  6. Drop the old column department column as it is no longer needed. <br>
  7. Join the new dataframe departments to your new employee dataset. <br>
</details>

<details>
  <summary>Examining various statistics</summary>
  1. Get the total number of observations and save it in a variable. <br>
  2. Print the number of employees who stayed / left. <br>
  3. Print the percentage of employees who stayed / left. <br>
  4. Build a correlation matrix to evaluate the relationships between features. <br>
</details>

<details>
  <summary>Splitting the data</summary>
  1. Set the target (dependent variable) which needs to be predicted. <br>
  2. Drop the churn column in order to obtain our features matrix. <br>
  3. Split the data into a training set and a testing set using scikit-learn to increase generalization and avoid overfitting. <br>
</details>

<details>
  <summary>Building the decision tree classifier</summary>
  1. Recall the number of employees who stayed versus those who left. <br>
  2. Calculate the gini index. <br>
  3. Gini index in case of splitting by variable A or B. <br>
  4. Check which Gini is lower and use it for spliting. <br>
  5. Apply a decision tree model to fit features to the target in the training set. <br>
  6. Check the accuracy score of the prediction for the training set. <br>
  7. Check the accuracy score of the prediction for the test set. <br>
  8. Import the tree graphical visualization export function. <br>
  9. Apply Decision Tree model to fit features to the target. <br>
  10. Export the tree to a dot file. <br>
</details>

<details>
  <summary>Pruning the tree</summary>
  1. Initialize the DecisionTreeClassifier while limiting the depth of the tree to 5. <br>
  2. Fit the model. <br>
  3. Print the accuracy of the prediction for the training set. <br>
  4. Print the accuracy of the prediction for the test set. <br>
</details>

<details>
  <summary>Limiting the sample size</summary>
  1. Initialize the DecisionTreeClassifier while limiting the sample size in leaves to 100. <br>
  2. Fit the model. <br>
  3. Print the accuracy of the prediction (in percentage points) for the training set. <br>
  4. Print the accuracy of the prediction (in percentage points) for the test set. <br>
</details>

<details>
  <summary>Model evaluation</summary>
  1. Import the function to calculate precision score. <br>
  2. Predict whether employees will churn using the test set. <br>
  3. Calculate precision score by comparing target_test with the prediction. <br>
  4. Import the function to calculate recall score. <br>
  5. Use the initial model to predict churn. <br>
  6. Calculate recall score by comparing target_test with the prediction. <br>
  7. Import the function to calculate ROC/AUC score. <br>
  8. Use initial model to predict churn (based on features_test). <br>
  9. Calculate ROC/AUC score by comparing target_test with the prediction. <br>
  10. Initialize the DecisionTreeClassifier. <br>
  11. Fit the model. <br>
  12. Print the accuracy of the prediction (in percentage points) for the test set. <br>
  13. Print the recall score. <br>
  14. Print the ROC/AUC score. <br>
  15. Initialize the model. <br>
  16. Fit it to the training component. <br>
  17. Make predictions using test component. <br>
  18. Print the recall score for the balanced model. <br>
  19. Print the ROC/AUC score for the balanced model. <br>
</details>

<details>
  <summary>Hyperparameter tuning</summary>
  1. Import the function for implementing cross validation. <br>
  2. Use that function to print the cross validation score for 10 folds. <br>
  3. Generate values for maximum depth. <br>
  4. Generate values for minimum sample size. <br>
  5. Create the dictionary with parameters to be checked. <br>
  6. import the GridSearchCV function. <br>
  7. Set up parameters. <br>
  8. Initialize the param_search function using the GridSearchCV function, initial model and parameters above. <br>
  9. Fit the param_search to the training dataset. <br>
  10. Print the best parameters found. <br>
  11. Initialize the model. <br>
  12. Fit it to the training component. <br>
  13. Make prediction using test component. <br>
  14. Calculate feature importances. <br>
  15. Create a list of features. <br>
  16. Save the results inside a DataFrame using feature_list as an index. <br>
  17. Sort values to learn most important features. <br>
  18. Select only features with relative importance higher than 1%. <br>
  19. Create a list from those features. <br>
  20. Transform both features_train and features_test components to include only selected features. <br>
  21. Initialize the model. <br>
  22. Fit it to the training component. <br>
  23. Make prediction using test component. <br>
  24. Print the general accuracy of the model_best. <br>
  25. Print the recall score of the model predictions. <br>
  26. Print the ROC/AUC score of the model predictions. <br>
</details>
