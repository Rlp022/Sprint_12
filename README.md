## Implementing Numerical Methods for Predicting Used Car Market Value

Introduction Rusty Bargain, a used car sales service, is developing an application to quickly estimate the market value of a car. To support this initiative, a predictive model was constructed using historical data, including technical specifications, trim versions, and pricing details.

## Table of Contents

Data Exploration and Preprocessing
Model Training and Evaluation
Model Analysis
Conclusions

## 1. Data Exploration and Preprocessing
The dataset provided included a variety of features related to each car, such as technical specifications, trim versions, and prices. Key attributes included the date the profile was downloaded, vehicle body type, registration year, gearbox type, engine power, model, mileage, registration month, fuel type, brand, repair status, profile creation date, number of vehicle pictures, postal code of the profile owner, and the date of the user's last activity. The target variable for the model was the car's price.

The data underwent preprocessing to handle missing values, manage outliers, and encode categorical features to ensure the dataset was suitable for modeling.

## 2. Model Training and Evaluation
Four different models were trained to predict the car's market value: Linear Regression, Decision Tree Regression, Random Forest Regression, and LightGBM. The models' performance was assessed using the Root Mean Square Error (RMSE) metric, with the training and prediction times also recorded.

The Linear Regression model achieved an RMSE of 3328.4 with a runtime of 0.1 seconds.
The Decision Tree Regression model had an RMSE of 1906.2 with a runtime of 1.0 seconds.
The Random Forest Regression model achieved an RMSE of 1871.8 with a runtime of 15.2 seconds.
The LightGBM model had the best performance with an RMSE of 1575.7 but required 32.4 seconds to run.

## 3. Model Analysis 
The LightGBM model provided the most accurate predictions, boasting the lowest RMSE, though it required the longest runtime. Despite the increased runtime, the significant improvement in prediction accuracy made LightGBM the preferred choice.

The Random Forest model also performed well, with a slightly higher RMSE than LightGBM but with a shorter runtime. The Decision Tree model was the fastest among the tree-based models but had a considerably higher RMSE. Linear Regression was the quickest to run but had the highest RMSE, indicating less accurate predictions.

## 4. Conclusions

In conclusion, the LightGBM model emerged as the most effective for predicting used car market values based on the historical dataset, offering the best trade-off between accuracy (as measured by RMSE) and runtime.

Given the high dimensionality of the data due to numerous categorical variables, exploring dimensionality reduction techniques could further enhance model performance. In real-world applications, the choice between accuracy and runtime depends on the specific use case, where one might prioritize a slightly faster model with lower accuracy or vice versa.# Sprint_12
