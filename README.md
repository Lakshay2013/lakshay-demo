## Food-Nutrition and Metabolomics Data Analysis
This project demonstrates the application of machine learning to analyze and model the relationship between food nutrition data and metabolomics data, using Logistic Regression for classification. The pipeline handles missing data, performs feature engineering, scales the data, and tunes the model using Grid Search with cross-validation.

## Project Structure
FOOD-DATA-GROUP1.csv: Contains food nutrition data (features related to food).
MetXBioDB_Transformations.csv: Contains metabolomics data (features related to metabolites).
Python script that processes data, creates features, and trains a machine learning model.
Requirements
Python 3.x
pandas
scikit-learn
To install required dependencies, run:

## Dataset Description
Food Nutrition Data: Contains features related to food items such as Sodium, Protein, Calories, etc.
Metabolomics Data: Contains features related to metabolites found in the human body. This includes various biochemical transformations related to the human microbiome and its relationship with food intake.
Steps in the Project
Load Datasets:

Load food nutrition data and metabolomics data into pandas DataFrames.
Handle Missing Values:

Numerical columns are filled with the median value.
Categorical columns are filled with the mode (most frequent value).
Feature Engineering:

New feature Sodium_per_gram is created by dividing the Sodium content by Protein content.
Data Preprocessing:

Data is split into training and testing sets (80% training, 20% testing).
Features are standardized using StandardScaler to normalize the data.
Model Definition:

A Logistic Regression model is used for classification.
Hyperparameter Tuning:

A grid search is performed with cross-validation to tune hyperparameters of the Logistic Regression model (C, penalty, max_iter).
Model Evaluation:

The best hyperparameters are displayed after the grid search completes.
Usage
Prepare Data:

Ensure the dataset files (FOOD-DATA-GROUP1.csv, MetXBioDB_Transformations.csv) are in the correct path.
The data should be cleaned and formatted before running the script.
Run the Python Script:

Execute the script to preprocess the data, perform model training, and display the best hyperparameters.
bash
Copy code
python model.py
View Results:
The script will print out the best hyperparameters found through Grid Search.
Example Output
bash
Copy code
Best Hyperparameters: {'C': 1, 'penalty': 'l2', 'max_iter': 100}
Contributions
Feel free to fork this repository and submit pull requests to improve the analysis pipeline.
License
This project is licensed under the MIT License - see the LICENSE file for details.

