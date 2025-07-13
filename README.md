Data-Driven Insights from Stroke Prediction Dataset

Team Members:

Nischal Pokharel

Swarna Anjani Devershetty

Vishnu Mallam

Tejeswar Reddy Chemikala

Shyam Nath

Dataset Summary
We used the Stroke Prediction Dataset from Kaggle, which includes 5,110 records and 11 attributes such as age, gender, work type, marital status, average glucose level, BMI, and stroke status. The dataset includes both demographic and medical features, making it ideal for exploring predictive modeling and pattern mining in a healthcare context.

The target variable is stroke (1 = Yes, 0 = No).

Deliverable 1: Data Collection, Cleaning, and Exploration
Steps Taken:

Removed rows with invalid gender ("Other")

Filled missing BMI values using the median

Removed duplicate entries

Encoded categorical variables using one-hot encoding

Visualized distributions and relationships using histograms, boxplots, and countplots

Key Insights:

Older individuals and those with higher glucose levels were more likely to have experienced a stroke

Certain work types and marital status categories showed trends worth exploring in later modeling

Challenges:

Class imbalance (very few stroke cases compared to non-stroke cases)

Handling missing and inconsistent values

Deliverable 2: Regression Modeling and Performance Evaluation
Goal:
To use regression models to predict a continuous variable — average glucose level — from other features.

Models Built:

Linear Regression

Ridge Regression

Evaluation Metrics:

R² Score

Mean Squared Error (MSE)

Root Mean Squared Error (RMSE)

Cross-validation using 5 folds to assess generalizability

Results:
Both models performed similarly:

R² Score: ~0.09

MSE: ~0.0519

RMSE: ~0.2277

Insights:

Neither model was particularly strong due to the limited predictive power of the features

Cross-validation confirmed model stability, even if accuracy was low

Challenges:

Low R² value indicated weak relationships between features and the glucose level

Regression was not ideal for this dataset due to the nature of the target variable

Deliverable 3: Classification, Clustering, and Pattern Mining
Classification Models:

Decision Tree

k-Nearest Neighbors (k-NN)

Hyperparameter tuning was done using GridSearchCV

Evaluation Metrics:

Confusion matrix

Accuracy

F1 score

ROC curve and AUC

Clustering:

Used K-Means (k=3) with PCA for 2D visualization

Grouped patients into risk-based clusters (e.g., older individuals with high glucose vs. younger, healthier ones)

Association Rule Mining:

Applied Apriori algorithm after binning continuous variables

Discovered patterns like:
"Old age" + "High Glucose" + "Hypertension" → "Had Stroke"

Insights:

Decision Tree was more interpretable and slightly better than k-NN

Clustering showed natural patient groupings that could help in real-world risk categorization

Association rules helped reveal feature combinations that frequently occur with stroke cases

Challenges:

Class imbalance affected model performance

Preprocessing for rule mining (binning and encoding) was time-consuming

Some features did not contribute much and may have added noise

Tools and Libraries Used
Python (Pandas, NumPy, Matplotlib, Seaborn)

Scikit-learn for modeling and evaluation

Mlxtend for association rule mining
