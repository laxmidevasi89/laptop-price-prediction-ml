# Laptop Price Prediction Using Machine Learning
## Project Overview
This project focuses on building an end-to-end machine learning pipeline to predict laptop prices based on hardware specifications and features.
It includes data cleaning, feature engineering, preprocessing, model training, evaluation, and model saving using Python and Scikit-learn.
The goal is to understand key factors influencing laptop prices and build an accurate regression model suitable for real-world deployment.
# Problem Statement
Laptop prices vary widely depending on specifications like processor, RAM, storage, graphics, display, and brand.
The objective of this project is to predict the price of a laptop given its specifications using machine learning techniques.
# Dataset Description
The dataset contains 1020 laptop records with the following key features:
-  Brand
-  Processor brand & generation
-  Number of cores
-  RAM size & type
-  Storage capacity & type
-  Graphics brand
-  Display size & resolution
-  Touchscreen availability
-  Operating system
-  Energy efficient units
## Target Variable:
- Price
## Tools & Technologies Used
- Programming Language: Python
- Libraries:
  - **NumPy**
  - **Pandas**
  - **Matplotlib**
  - **Seaborn**
  -**Scikit-learn**
  - **Joblib**

##  Project Workflow
 *  **Data Loading & Exploration**
- Checked data types, missing values, and distributions
* Data Cleaning
- Dropped irrelevant columns (Name, Rating, index)
- Filled missing numerical values with median
- Filled missing categorical values with mode
- Converted boolean features to numerical format
* Feature Engineering
-  Created screen resolution feature
- Calculated screen area (in megapixels)
- Categorized CPU generations into performance levels (Basic, Good, Strong)
* Preprocessing
- One-Hot Encoding for categorical features
- Standard Scaling for numerical features
-  Used ColumnTransformer and Pipeline
* Model Building
- Random Forest Regressor
- 80–20 train-test split
* Model Evaluation
- MAE
- RMSE
- R² Score
- Residual analysis
- Feature importance visualization
* Model Saving
Saved trained model using joblib for deployment

##  Model Performance
Metric	Value
MAE	₹13,269
RMSE	₹24,705
R² Score	0.8276

 **The model explains ~83% variance in laptop prices**

## Key Insights
- RAM size and type significantly influence laptop prices
- Processor generation and CPU level are major price drivers
- Brand and graphics type play a strong role
- High-end laptops show larger prediction errors due to premium pricing

## Visualizations Included
- Actual vs Predicted Price Scatter Plot
- Residual Plots
- Error Distribution Histogram
- Feature Importance Bar Chart
- MAE vs RMSE Comparison

## Project Structure
* Laptop-Price-Prediction
-  laptop_price_model.pkl
-  README.md
-  laptop_price_prediction.ipynb
-  dataset
- Laptop Data.csv
  
## How to Run the Project
- Clone the repository
git clone https://github.com/your-username/laptop-price-prediction.git
- Install dependencies
pip install -r requirements.txt
- Run the notebook or Python script
  
## Future Improvements
- Hyperparameter tuning using GridSearchCV
- Compare with XGBoost / Gradient Boosting
- Handle high-price outliers
- Build a Streamlit web app for live predictions
