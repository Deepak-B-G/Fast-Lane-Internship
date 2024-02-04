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

## Conclusion:

The Random Forest Regressor model achieved a Mean Absolute Error (MAE) of approximately 197.44 on the test set, reflecting the average absolute difference between predicted and actual traffic volumes. Notably, temperature (temp) emerged as the most influential factor, contributing 40.37% to the model's decision-making. The month of the year (month) closely followed, accounting for around 25.18% of predictive power. Day of the week (day_of_week) and cloud cover (clouds_all) also played significant roles, contributing 18.86% and 14.70%, respectively. Rainfall (rain_1h) had a comparatively smaller impact (0.89%), while snowfall (snow_1h) and time of day (hour) showed negligible importance. In summary, the model underscores the importance of temperature and temporal factors in predicting traffic volume, aligning with expectations of weather and seasonal influences. While the model shows promise in forecasting, further refinement through hyperparameter tuning or considering additional features could enhance accuracy and generalization.


## Project 2: Stock Price Analysis

### Objective
Analyze and predict stock prices using LSTM.

### Dataset
Stock market data from Kaggle.

### Project Overview
1. **Feature Engineering**
   - Extracted relevant features such as time, day, and relevant economic indicators.
   - Created lag features to capture historical stock price patterns.

2. **Exploratory Data Analysis (EDA)**
   - Visualized stock information using Seaborn and Matplotlib to understand historical trends.
   - Analyzed risk based on previous stock performance.

3. **Stock Price Prediction using LSTM**
   - Utilized Long Short-Term Memory (LSTM) networks for predicting future stock prices.
   - Implemented a model using the yfinance library for NSE.

4. **Conclusion**
   - Summarized key findings and insights from the analysis, including predictions of future stock prices and identified factors influencing stock performance.

## Project 3: Healthcare Data Analysis for Diabetes Prediction

### Objective
Develop a model to predict diabetes likelihood based on patient health metrics.

### Dataset
Pima Indians Diabetes Database from Kaggle.

### Project Overview
1. **Data Collection**
   - Collected the Pima Indians Diabetes Database.
   - Ensured compliance with data protection and privacy regulations.

2. **Data Exploration**
   - Explored the dataset to understand feature distribution and diabetes outcome.
   - Identified missing values and outliers.

3. **Data Preprocessing**
   - Handled missing data through imputation and removal.
   - Normalized or standardized numerical features.
   - Encoded categorical variables into numerical formats if necessary.

4. **Exploratory Data Analysis (EDA)**
   - Visualized feature distribution and relationships with diabetes outcome.
   - Explored correlations between different features.
   - Evaluated feature importance for diabetes prediction using techniques like correlation analysis and feature importance from Random Forest models.

5. **Conclusion**
   - Summarized key findings and insights from the analysis, including feature importance for diabetes prediction and potential avenues for further research.

## How to Use This Repository

- Each project has its dedicated folder containing code files and datasets.
- Follow the README within each project folder for specific instructions.
