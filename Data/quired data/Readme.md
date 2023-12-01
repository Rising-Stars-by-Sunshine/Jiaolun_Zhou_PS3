This research directly use data fetched from the Internet, move to the processed data folder and you will get the data used in this research.
To help the audience better improve this research in the future, I put a piece of pseudo code here if any data query is needed in the future research.
# Import necessary libraries
import pandas as pd
from sklearn.preprocessing import StandardScaler
from sklearn.model_selection import train_test_split

# Load dataset
dataset = pd.read_csv("your_dataset.csv")

# Data preprocessing
# Drop irrelevant columns
dataset = dataset.drop(["irrelevant_column1", "irrelevant_column2"], axis=1)

# Handle missing values
dataset = dataset.dropna()  # Drop rows with missing values
# Or use imputation techniques for missing values

# Feature engineering
# Convert categorical variables to numerical using one-hot encoding
dataset = pd.get_dummies(dataset, columns=["categorical_feature1", "categorical_feature2"])

# Standardize numerical features
scaler = StandardScaler()
numerical_features = ["numerical_feature1", "numerical_feature2"]
dataset[numerical_features] = scaler.fit_transform(dataset[numerical_features])

# Split data into features and target variable
X = dataset.drop("target_variable", axis=1)
y = dataset["target_variable"]

# Split the dataset into training and testing sets
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

# Further processing or modeling steps can be added here...

# End of preprocessing
