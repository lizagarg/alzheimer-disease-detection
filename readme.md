# Dependencies
pip install pandas
pip install numpy
pip install matplotlib
pip install seaborn
pip install scipy
pip install scikit-learn

# Machine Learning Project 2024

Welcome! In this project, We worked on ALzhiemers disease prediction to analyze it and build model that predicts whether a patient is diagnosed with the condition.

## Step 1: Importing Libraries

The goal is to analyze health data, clean it up, explore patterns, and create models to predict diagnoses.

### Tools we Used:

- pandas: For organizing data.
- numpy: For calculations.
- matplotlib and seaborn: For creating graphs.
- scipy.stats: For statistics, (calculation of z-score).

## Step 2: Loading the Data

Data is Loaded using a csv (coma seperated values) file Downloaded from Kaggle

## Step 3: Understanding the Data

we explored the data to get an idea of what was in it:

1. Basic Stats: Found things like average age or BMI.
2. Data Info: Checked what type of data each column contains (e.g., numbers or categories) and looked for missing values.
3. Categorical vs. Numeric: Split the data into two groups:
   - Categorical: Columns like Gender, Smoking, and Diagnosis.
   - Numeric: Columns like Age, BMI, and blood pressure levels.

## Step 4: Exploring the Data

### Visualizing Categories:
we created bar charts to see how the data is distributed across different categories like gender, ethnicity, and education level.

### Checking for Odd Data:
we used boxplots to see if there were any extreme values (outliers) in the numeric columns.
No unusual outliers in the data were found

### Seeing Patterns:
we looked at the relationships between some features (e.g., MMSE, FunctionalAssessment, ADL) and the diagnosis. For example, scatter plots showed how changes in certain features are linked to the likelihood of a diagnosis.

## Step 5: Cleaning and Prepping the Data

### Converting Categories to Numbers:
Since machine learning models need numbers, we turned categorical data like "Yes" or "No" into numbers (1 for Yes, 0 for No).

### Handling Missing Values:
If any data was missing (like education level), we filled it with the most common value in that column.

### Scaling Numbers:
Features like Age and BMI have very different ranges, which could confuse the model. we scaled them so all the numbers are on the same level.

### Combining Related Features:
we simplified the data by combining related features (like cholesterol levels) into single columns using a PCA (Principal Component Analysis).

## Step 6: Splitting the Data

To train and test the models, we split the data into:

- Training Set: Used to teach the model.
- Test Set: Used to check how well the model learned.

## Step 7: Building the Models

we tested five models to see which works best:

1. Logistic Regression: A simple model for binary outcomes.
2. Random Forest: Combines decision trees for better predictions.
3. K-Nearest Neighbors (KNN): Uses nearby data points to make predictions.
4. Decision Tree: Breaks decisions into steps.
5. Support Vector Machine (SVM): Finds the best way to separate data.

we trained each model using the training data.

## Step 8: Making Predictions

After training, we asked each model to predict diagnoses using the test data.

## Step 9: Evaluating the Models

### Accuracy:
we measured how often each model was correct. 

**What we Found**: Each model performed differently, and we visualized their accuracies with a bar chart.

### Confusion Matrices:
These helped me see where models made mistakes, like predicting a diagnosis when there wasn’t one (false positives).

### Precision, Recall, and F1-Score:
These metrics gave a detailed look at each model:
- Precision: How accurate the positive predictions were.
- Recall: How many actual diagnoses were correctly predicted.
- F1-Score: A balance of precision and recall.
Random Forest Followed by Decision tree models had the best accuracy. KNN being the worst at prediction

1	Random Forest:	94.19%
2	K-Nearest Neighbors:	76.51%

## Conclusion

In this project, we explored and cleaned the data, created models, and compared their performance. 
This process showed how different models work and helped identify the best one for predicting diagnoses based on the available data.