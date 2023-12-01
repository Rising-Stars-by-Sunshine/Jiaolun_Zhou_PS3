# Data query process and how this data is got?
Visit https://www.daas-auto.com/supermarket_data_De/109.html and https://www.jdpower.com/cars/2022/acura/ilx. These two websites provide professional data about cars in China and oversea markets. This paper manually collects data of 400 cars and use this data for training and testing. If in the future publication, more data is needed, just visit these two websites and get more data.

# Screen shot for these two professional websites and where data for cars can be found
<img src="35714c9ab5987a2dc92d0fad4addf01.jpg" alt="Car website screenshot">

<img src="df27228f88ea53147aad99dd3498903.jpg" alt="Car website screenshot">

# How to use this notebook and the data?
First, go to the url provided and search for any car that can be included in this model. Remember to get all the data requeired in the model. This paper has also provided a sample collected by the author, which can be used in testing.

## Important
Data should include: Connector size;  Battery Size;  Distance Driven; model_year;  Range Buffer;  Driving Eff;  Inverter Eff;  Dispatch Time;  cylinders;  Maxpower;  weight

Then, download the model.py, this is a sample code used for analyzing the car information. Any code can be used, just make sure it's in line with SALib's requirement.

Lastly, rename your data file as "car_information.csv", name in the code can also be changed. You can run this data on your own computer!

### Brief introduction to SALib
SALib, or Sensitivity Analysis Library, is a powerful and versatile Python library used for conducting sensitivity analysis. Sensitivity analysis is a fundamental tool in data science and decision-making that helps assess the influence of input parameters on model outputs. SALib provides a range of techniques to perform global and local sensitivity analysis on models or simulations, making it valuable for a wide array of applications.

The library offers support for various sensitivity analysis methods, such as Sobol, Morris, FAST, and more. It allows users to quantify the importance of different input factors, detect nonlinear interactions, and understand the robustness of models. SALib is particularly useful in fields like environmental modeling, finance, engineering, and machine learning, where understanding parameter sensitivities and their impact is crucial.

SALib simplifies the sensitivity analysis process, making it accessible to both researchers and practitioners, and it is widely adopted in the data science community for enhancing model interpretability and decision-making.

### Data query and analysis process
In this piece of code, we directly import the data got from the website, which is linked at top of this article, and then analyze this piece of data using the model.py file in order to simulate the decision-making process of an AI in reality. We then analyze this decision-making process using morris imported from SALib, and we end up with a dot plot that covers all the parameters in a set, which shows us the most heavily weighted of all the parameters.

### Abstract

<img src="Interpretable Machine Learning for Autonomous Vehicles_ Bridging the Gap with eXplainable Artificial Intelligence (XAI) (3).png" alt="Abstract Word Cloud">


\documentclass{article}
\usepackage{geometry}
\usepackage{array}
\usepackage{booktabs}
\usepackage{graphicx}
\usepackage{float}
\usepackage{multirow}
\usepackage{caption}
\geometry{a4paper, total={170mm, 257mm, left=20mm, right=20mm, top=20mm, bottom=20mm}}

\begin{document}

\begin{table}[H]
\centering
\begin{tabular}{p{0.8\linewidth}}
\toprule
\textbf{Python Code} \\
\midrule
\begin{verbatim}
# Import necessary libraries
import pandas as pd
import numpy as np
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import StandardScaler, OneHotEncoder
from sklearn.impute import SimpleImputer
from sklearn.compose import ColumnTransformer
from sklearn.pipeline import Pipeline
from sklearn.ensemble import RandomForestClassifier
from sklearn.feature_selection import SelectFromModel
from sklearn.decomposition import PCA
from sklearn.model_selection import GridSearchCV
from sklearn.metrics import accuracy_score, classification_report, confusion_matrix
from imblearn.over_sampling import SMOTE
from imblearn.pipeline import Pipeline as ImbPipeline
import matplotlib.pyplot as plt
import seaborn as sns

# Load dataset
data = pd.read_csv("your_dataset.csv")

# Separate features and target variable
X = data.drop("target_variable", axis=1)
y = data["target_variable"]

# Define numerical and categorical features
numerical_features = X.select_dtypes(include=[np.number]).columns.tolist()
categorical_features = X.select_dtypes(include=[np.object]).columns.tolist()

# Create preprocessing transformers
numerical_transformer = Pipeline(steps=[
    ('imputer', SimpleImputer(strategy='mean')),
    ('scaler', StandardScaler())
])

categorical_transformer = Pipeline(steps=[
    ('imputer', SimpleImputer(strategy='most_frequent')),
    ('onehot', OneHotEncoder(handle_unknown='ignore'))
])

# Combine transformers into a preprocessor
preprocessor = ColumnTransformer(
    transformers=[
        ('num', numerical_transformer, numerical_features),
        ('cat', categorical_transformer, categorical_features)
    ])

# Split data into train and test sets
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

# Define the model
model = RandomForestClassifier(n_estimators=100, random_state=42)

# Feature selection using SelectFromModel
feature_selector = SelectFromModel(model)
X_train_selected = feature_selector.fit_transform(preprocessor.fit_transform(X_train), y_train)

# Principal Component Analysis (PCA) for dimensionality reduction
pca = PCA(n_components=0.95)
X_train_pca = pca.fit_transform(preprocessor.fit_transform(X_train))

# Combine feature selection and PCA into a preprocessor
combined_preprocessor = ColumnTransformer(
    transformers=[
        ('num', numerical_transformer, numerical_features),
        ('cat', categorical_transformer, categorical_features),
        ('feature_selection', feature_selector, X.columns),
        ('pca', pca, X.columns)
    ])

# Define SMOTE for handling imbalanced classes
smote = SMOTE(random_state=42)

# Create an imbalanced pipeline with SMOTE
imbalanced_pipeline = ImbPipeline(steps=[
    ('preprocessor', combined_preprocessor),
    ('smote', smote),
    ('model', model)
])

# Define hyperparameter grid for GridSearchCV
param_grid = {
    'model__n_estimators': [50, 100, 150],
    'model__max_depth': [None, 10, 20],
    'model__min_samples_split': [2, 5, 10]
}

# Perform GridSearchCV for hyperparameter tuning
grid_search = GridSearchCV(imbalanced_pipeline, param_grid, cv=5, scoring='accuracy')
grid_search.fit(X_train, y_train)

# Best hyperparameters
best_params = grid_search.best_params_

# Evaluate the model
y_pred = grid_search.predict(X_test)
accuracy = accuracy_score(y_test, y_pred)
classification_rep = classification_report(y_test, y_pred)
confusion_mat = confusion_matrix(y_test, y_pred)

# Print evaluation metrics and best hyperparameters
print(f"Best Hyperparameters: {best_params}")
print(f"Accuracy: {accuracy}")
print("Classification Report:\n", classification_rep)
print("Confusion Matrix:\n", confusion_mat)

# Visualize feature importance
feature_importance = pd.Series(grid_search.best_estimator_['model'].feature_importances_, index=X.columns)
sorted_feature_importance = feature_importance.sort_values(ascending=False)
plt.figure(figsize=(10, 6))
sns.barplot(x=sorted_feature_importance, y=sorted_feature_importance.index)
plt.title('Feature Importance')
plt.show()
\end{verbatim} \\
\bottomrule
\end{tabular}
\caption{Pseudo Code for Extensive Data Processing}
\end{table}

\end{document}
