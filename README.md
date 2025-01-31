Titanic Data Analysis and Machine Learning for Survival Prediction

Recently, I worked on analyzing the famous Titanic disaster dataset to build a machine learning model that predicts passengers' survival probabilities. This project involved data analysis, cleaning, feature engineering, and applying machine learning models. Let's go through the key steps of this project.

1. Data Loading and Analysis

First, I loaded the train.csv and test.csv datasets using the Pandas library and explored their structure. 
Key findings include:

✅ Age, Cabin, and Embarked columns contain missing values.

✅ Pclass (Ticket class), Fare (Ticket price), and Sex significantly influence survival probability.

✅ I created a new feature, FamilySize, by summing the SibSp and Parch columns.

2. Data Cleaning and Feature Engineering

💡 Filling Missing Values:

🔹 Age column - filled with the mean age value.

🔹 Embarked column - filled with the most frequently occurring value.

🔹 Cabin information - extracted the first letter to create a new column, "Deck."

💡 New Features Created:

🔹 FamilySize - indicates the size of a passenger's family.

🔹 FamilyGroup - categorizes passengers as single, small, or large families.

🔹 HasCabin - a binary column indicating whether a passenger had a cabin number.

💡 Correlation Analysis and Feature Reduction:

🔹 FamilyGroup_small and FamilyGroup_single had a high correlation of -0.86. FamilyGroup_small was retained, and the other was removed.

🔹 SibSp and Parch columns were removed since FamilySize was created.

3. Scaling and Encoding Data

🔹 StandardScaler was used to normalize Age and Fare columns.

🔹 Label Encoding was applied to convert Sex and Embarked into numeric values.

🔹 One-hot encoding was used for FamilyGroup categories.

4. Machine Learning Model Development

A Logistic Regression model was applied to predict Titanic passengers' survival probabilities.

✔ Model Accuracy (Accuracy Score):

🔹 Training dataset: 81%

🔹 Test dataset: 78%

✔ Precision, Recall, and F1 Score:

🔹 Small families had a higher survival probability.

🔹 First-class passengers had a better chance of survival.

🔹 Gender played a significant role - women had a higher survival probability than men.

