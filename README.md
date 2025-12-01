Housing Price Prediction – Machine Learning Project

This project predicts housing prices in California(the easily dataset i could find) using machine learning techniques applied to the California Housing dataset. The workflow covers data preprocessing, feature engineering, model training, evaluation, and a custom prediction function that estimates prices based on user inputs.

Project Contents

Housing.csv – dataset used for training and testing

house_price_prediction.ipynb – Jupyter Notebook containing the full workflow

Process Overview
1. Data Cleaning

Removed missing values

Ensured consistent data types

2. Feature Engineering

Applied log transformations to skewed features: total_rooms, total_bedrooms, population, households

Created additional ratio-based features:

bedroom_ratio (bedrooms per room)

household_rooms (rooms per household)

3. Encoding and Scaling

Converted the categorical feature ocean_proximity using one-hot encoding

Scaled numerical features using StandardScaler

Ensured consistent columns between train and test sets using reindex to avoid dummy variable mismatches

4. Visualization

Histograms for distribution analysis

Correlation heatmap

Latitude-longitude scatterplot showing price variations

Machine Learning Models

Linear Regression

Random Forest Regressor

Random Forest tuning using GridSearchCV

Model Performance

Linear Regression: ~0.82 R²

Random Forest: ~0.81 R²

GridSearchCV Model: ~0.66 R²

(Default Random Forest performed better than tuned configurations due to dataset characteristics.)

Price Prediction Function

A custom function is included to predict housing prices:

predict_price(latitude, longitude, rooms, bedrooms, population, households, location)


This function processes inputs, applies the same transformations used during training, and predicts the house price based on the trained model.

Tech Stack

Python

Pandas

NumPy

Matplotlib

Seaborn

Scikit-Learn

Jupyter Notebook
