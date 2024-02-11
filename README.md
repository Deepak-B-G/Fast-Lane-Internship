# Fast Lane Career Data Science Projects

Welcome to the Fast Lane Career Data Science Projects repository. In this repository, you will find three distinct data science projects focusing on Traffic Flow Prediction, Stock Price Analysis, and Healthcare Data Analysis for Diabetes Prediction.

## Project 1: Traffic Flow Prediction for Smart Cities

### Objective
Predict traffic flow patterns for optimal transportation in smart cities.

### Dataset
Metro Interstate Traffic Volume from UCI ML Repository.

### Project Overview

1.  **Data Preprocessing:**

- Imported necessary libraries and loaded the dataset using pandas.
- Checked for unique values in categorical variables (`holiday`, `weather_main`, `weather_description`).
- Checked for missing values in the dataset.
- Applied one-hot encoding to categorical variables and Min-Max scaling to numerical features (`temp`, `rain_1h`, `snow_1h`, `clouds_all`).
- Converted the 'date_time' column to datetime format and extracted time-related features (`hour`, `day_of_week`, `month`).
- Created lag features for 'traffic_volume' to capture temporal patterns.

2. **Exploratory Data Analysis (EDA):**

- Visualized the correlation matrix to understand relationships between numeric features.
- Plotted a histogram to show the distribution of traffic volume.
- Displayed a line plot to visualize how traffic volume changes over time.
- Utilized bar plots and boxplots to analyze the impact of weather categories and day of the week on traffic volume.

3.  **Feature Engineering:**

- Transformed the 'holiday' column into a binary numeric variable.
- Considered only numeric columns for calculating correlation.
- Generated lag features for the past 3 hours to capture temporal dependencies.

4.  **Machine Learning Model:**

- Selected relevant features (`temp`, `rain_1h`, `snow_1h`, `clouds_all`, `hour`, `day_of_week`, `month`) for predicting traffic volume.
- Split the dataset into training and testing sets.
- Employed a Random Forest Regressor model for traffic volume prediction.
- Evaluated the model performance using Mean Absolute Error (MAE).
- Visualized feature importance to understand the contribution of each feature to the model.

5. **Model Performance:**

The Random Forest Regressor model achieved a Mean Absolute Error (MAE) of approximately 197.44 on the test set, indicating the average absolute difference between predicted and actual traffic volumes.

6. **Feature Importance Analysis:**

The feature importance analysis reveals the following contributions to the model:

- Temperature (`temp`): 40.37%
- Month (`month`): 25.18%
- Day of the week (`day_of_week`): 18.86%
- Cloud cover (`clouds_all`): 14.70%
- Rainfall (`rain_1h`): 0.89%
- Snowfall (`snow_1h`): Negligible
- Time of day (`hour`): Negligible

## Conclusion

The Random Forest Regressor model achieved a Mean Absolute Error (MAE) of approximately 197.44 on the test set, reflecting the average absolute difference between predicted and actual traffic volumes. Notably, temperature (temp) emerged as the most influential factor, contributing 40.37% to the model's decision-making. The month of the year (month) closely followed, accounting for around 25.18% of predictive power. Day of the week (day_of_week) and cloud cover (clouds_all) also played significant roles, contributing 18.86% and 14.70%, respectively. Rainfall (rain_1h) had a comparatively smaller impact (0.89%), while snowfall (snow_1h) and time of day (hour) showed negligible importance. In summary, the model underscores the importance of temperature and temporal factors in predicting traffic volume, aligning with expectations of weather and seasonal influences. While the model shows promise in forecasting, further refinement through hyperparameter tuning or considering additional features could enhance accuracy and generalization.


## Project 2: Stock Analysis and Prediction

This repository contains an in-depth analysis of BTC's stock, providing valuable insights for investors and enthusiasts. The analysis covers a range of topics, including historical trends, risk assessment, moving averages, correlation analysis, and predictive modeling.

## Analysis Highlights:

1. **Change in Stock Price Over Time:**
   - Visualized adjusted closing prices to understand historical trends.
   - Explored total trading volume for insights into market activity.

2. **Daily Return Average:**
   - Calculated daily returns and visualized them through line plots and histograms.

3. **Moving Average:**
   - Computed moving averages (10, 20, 50 days) to identify trends and price fluctuations.

4. **Correlation Between Daily Returns:**
   - Analyzed correlation between daily returns of different stocks (AMZN, BTC, DPZ, NFLX).

5. **Investment Risk Assessment:**
   - Evaluated the trade-off between expected returns and risk using scatter plots.
   - Assessed risk tolerance based on the standard deviation of daily returns.

6. **Predicting BTC Closing Price:**
   - Utilized Long Short-Term Memory (LSTM) neural network for stock price prediction.
   - Examined model performance using Root Mean Squared Error (RMSE).

## Conclusion

The analysis presents a comprehensive overview of BTC's stock, encompassing historical trends, risk assessment, moving averages, correlation analysis, and predictive modeling. The adjusted closing price of BTC illustrates temporal fluctuations, aiding investors in understanding past market behavior. The exploration of daily returns, moving averages, and risk-return profiles for various stocks (AMZN, BTC, DPZ, NFLX) equips investors with insights into investment strategies and portfolio diversification. The LSTM predictive model attempts to forecast BTC's closing price, serving as a tool for future price speculation. However, it's imperative to acknowledge the inherent uncertainties and limitations associated with predictive modeling in financial markets. Overall, this analysis combines statistical metrics, visualizations, and predictive techniques to offer a holistic perspective on BTC's stock, empowering investors to make well-informed decisions.


## Project 3: Healthcare Data Analysis for Diabetes Prediction


This project aims to predict diabetes outcomes using the Pima Indians Diabetes Database. Below is a step-by-step overview of the project, including data collection, exploration, preprocessing, exploratory data analysis (EDA), and feature selection.

## Data Collection:

The Pima Indians Diabetes Database was used for this project, ensuring compliance with data protection and privacy regulations.

## Data Exploration:

The initial exploration of the dataset involved understanding the distribution of features and the diabetes outcome. Steps included:

- Visualizing feature distributions, such as glucose levels.
- Identifying missing values and outliers.

## Data Preprocessing:

To prepare the data for modeling, the following steps were taken:

- Handling missing data through imputation or removal.
- Normalizing or standardizing numerical features.
- Encoding categorical variables into numerical formats if necessary.

## Exploratory Data Analysis (EDA):

EDA was conducted to gain insights into feature distributions, relationships with diabetes outcomes, and potential patterns or trends. Key visualizations include:

- Histogram of Glucose levels.
- Pairplot of numerical features with diabetes outcome.
- Boxplots comparing feature distributions for each outcome.

## Feature Selection:

Feature selection is crucial for accurate predictions. In this project:

- Correlation analysis was performed to understand relationships between features.
- A Random Forest model was trained, and feature importance scores were obtained.

### Feature Importance from Random Forest Model:

1. **Glucose:** 0.259
2. **BMI:** 0.170
3. **Age:** 0.141
4. **DiabetesPedigreeFunction:** 0.124
5. **BloodPressure:** 0.088
6. **Pregnancies:** 0.077
7. **Insulin:** 0.076
8. **SkinThickness:** 0.066

The Random Forest model indicates that 'Glucose' is the most important feature for predicting diabetes outcomes, followed by 'BMI' and 'Age'.

## Conclusion

In conclusion, this diabetes prediction project successfully utilized the Pima Indians Diabetes Database to develop a predictive model. Through comprehensive data exploration, preprocessing, and exploratory data analysis (EDA), crucial insights into feature distributions, relationships, and potential patterns were gained. The Random Forest model, employed for feature selection, identified 'Glucose'(with 25.9%) as the most influential predictor of diabetes outcomes, emphasizing its pivotal role in the model's predictions. The comprehensive overview is provided in the readme. Md file serves as a valuable guide, encapsulating the project's methodology, key visualizations, and findings, thus offering a clear understanding of the undertaken steps and the significance of various features in predicting diabetes outcomes.
