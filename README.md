# Engage2Value: From Clicks to Conversions Contest Link : https://www.kaggle.com/competitions/engage-2-value-from-clicks-to-conversions
# Engage2Value: From Clicks to Conversions


This repository contains a machine learning solution for the **Engage2Value: From Clicks to Conversions** competition. The project's goal is to predict a customer’s purchase value based on their multi-session behavior across various digital touchpoints.

## 📝 Overview

The notebook implements a comprehensive solution for predicting customer purchase values. It includes extensive exploratory data analysis (EDTA), feature engineering, and multiple regression models to achieve the best possible predictive performance.

-   **Goal**: Predict customer purchase value based on digital behavior patterns.
-   **Evaluation Metric**: R² score between the predicted and true target values.
-   **Target Variable**: `purchaseValue` - the total amount spent during a session.

## 📊 Dataset Description

The dataset captures detailed session-level information from a large-scale digital commerce platform. Each row corresponds to a unique user session and includes data on user behavior, acquisition channels, device information, and geographical location.

### Key Feature Categories:

* **User Behavior & Session Metrics**: `totalHits`, `pageViews`, `totals.bounces`, `new_visits`, `sessionNumber`.
* **Device & Technical Attributes**: `deviceType`, `os`, `browser`, `screenSize`, `device.language`.
* **Traffic & Marketing Source**: `userChannel`, `trafficSource`, `trafficSource.medium`, `trafficSource.keyword`.
* **Geographical Context**: `geoNetwork.city`, `locationCountry`, `geoNetwork.continent`.

## ⚙️ Technical Approach

The solution follows a structured approach to building a robust prediction model:

1.  **Data Loading & Initial Exploration**: The training and test datasets are loaded, and a basic overview is performed to understand the data's shape and structure.
2.  **Exploratory Data Analysis (EDTA)**: A deep dive into the data to understand distributions, identify missing values, and uncover relationships between features. This includes analyzing the target variable, numeric and categorical features, and visualizing data patterns.
3.  **Feature Engineering & Preprocessing**:
    * **Imputation**: Missing numerical values are filled using the median, while categorical missing values are replaced with the mode.
    * **Target Encoding**: High-cardinality categorical features are transformed using target encoding.
    * **Scaling**: Numerical features are scaled using `RobustScaler` to handle outliers effectively.
4.  **Modeling**: A variety of regression models are trained and evaluated to find the best-performing one. The models used include:
    * Linear Models (e.g., `LinearRegression`, `Lasso`, `Ridge`)
    * Ensemble & Tree-based Models (e.g., `RandomForestRegressor`, `AdaBoostRegressor`, `XGBoost`)
    * Other Regressors (e.g., `KNeighborsRegressor`, `SVR`)
5.  **Model Evaluation & Submission**: Models are evaluated based on the R² score, and a submission file is generated in the specified format.

