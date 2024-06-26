# Bike Demand Prediction Model using Multiple Linear Regression

## Overview
This project aims to predict the demand for shared bikes post-Covid-19 lockdowns using machine learning techniques, specifically multiple linear regression. The goal is to assist BoomBikes in understanding the factors that influence bike demand, thereby optimizing their business strategy.

## Table of Contents
- [General Information](#general-information)
- [Technologies Used](#technologies-used)
- [Data Wrangling](#data-wrangling)
  - [Initial Data Exploration](#initial-data-exploration)
  - [Data Cleaning](#data-cleaning)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
  - [Univariate Analysis](#univariate-analysis)
  - [Segmented Analysis](#segmented-analysis)
  - [Bivariate Analysis](#bivariate-analysis)
  - [Multivariate Analysis](#multivariate-analysis)
- [Modeling](#modeling)
  - [Data Preprocessing](#data-preprocessing)
  - [Building the Model](#building-the-model)
  - [Model Evaluation](#model-evaluation)
- [Results and Discussion](#results-and-discussion)
- [Conclusion](#conclusion)
- [Acknowledgements](#acknowledgements)
- [Contact](#contact)

---

## General Information
This project utilizes a multiple linear regression model to predict bike demand based on various factors such as weather conditions, seasonality, and other demographic variables. The [dataset](day.csv) includes daily bike demand data across the American market, covering features like temperature, humidity, season, and more.

## Technologies Used
- Python 3.10.4
- JupyterLab 4.0.11
- scikit-learn 1.5.0
- pandas 2.1.4
- numpy 1.26.4
- matplotlib 3.8.4
- statsmodels 0.14.1
- seaborn 0.13.2

## Data Wrangling
### Initial Data Exploration
The dataset was initially analysed to ensure data integrity and understand its structure:
- Checked for duplicate rows and columns with all NULL values.
- Identified 7 categorical variables: 'season', 'mnth', 'yr', 'is_workingday', 'weather_condition'.

### Data Cleaning
Data cleaning involved preprocessing steps to prepare the dataset for analysis:
- Removed irrelevant columns and renamed columns for clarity.
- Converted categorical variables to meaningful labels and adjusted data types.
- Conducted outlier analysis (none identified) and prepared data for further analysis.

## Exploratory Data Analysis (EDA)
### Univariate Analysis
Explored distributions and summary statistics for individual variables:
- **Seasons:** Fall (188 entries) was the most frequent, followed by Summer (184), Spring (180), and Winter (178).
- **Years:** Both 2018 and 2019 had equal representation (365 entries each), with a slight skew towards 2018.
- **Months:** January had the highest frequency (62 entries), indicating peak bike demand.
- **Weather Conditions:** Clear weather conditions (463 entries) were most common.

### Segmented Analysis
Analyzed variables across different segments to understand patterns:
- **Working Days vs. Non-Working Days:** Bike usage was higher on working days across all seasons and weather conditions.
- **Seasonal Analysis:** Fall and Summer showed higher bike usage compared to Winter and Spring.
- **Monthly Trends:** Peak bike usage observed in August, March, May, and October.

### Bivariate Analysis
Explored relationships between pairs of variables:
- **Temperature vs. Bike Demand:** Positive correlation observed; higher temperatures correlated with increased bike rentals.
- **Weather Conditions vs. Bike Demand:** Clear weather conditions are associated with higher rentals compared to misty or rainy conditions.
- **Season vs. Bike Demand:** Fall and Summer seasons saw higher bike rentals.

### Multivariate Analysis
Investigated complex interactions between multiple variables:
- **Temperature, Humidity, Windspeed:** Analyzed their combined impact on bike demand.
- **Seasonality and Weather Conditions:** Explored how these factors influence bike rental patterns.

## Modeling
### Data Preprocessing
Prepared data for modeling:
- Encoded categorical variables and split data into training and testing sets.
- Applied feature scaling to ensure all variables contribute equally to the model.

### Building the Model
Developed a multiple linear regression model:
- Selected relevant features using techniques like Recursive Feature Elimination (RFE).
- Built the regression model using scikit-learn and evaluated its performance.

### Model Evaluation
Evaluated the model's performance:
- **R-squared Scores:** Train set = 0.834, Test set = 0.804, indicating good predictive capability.
- **Residual Analysis:** Confirmed assumptions of normality and homoscedasticity were met.

## Results and Discussion
- Identified key factors influencing bike demand post-Covid-19, including weather conditions, seasonality, and day types.
- Provided actionable insights for BoomBikes to optimize operations and marketing strategies.

## Conclusion
- This project successfully developed a robust multiple linear regression model for predicting bike demand.
- The model's insights can help BoomBikes adapt their business strategy to meet customer needs post-Covid-19 effectively.

## Acknowledgements
- Dataset provided by BoomBikes for analysis and model development.
- Inspired by similar projects in machine learning and predictive analytics.

## Contact
Created by [@AnkitSurana](https://github.com/AnkitSurana) - Feel free to reach out for any questions or collaborations!

---

This README provides a detailed overview of the project, from data exploration and cleaning to modeling and evaluation, with specific emphasis on the findings from exploratory data analysis and the predictive capabilities of the developed model.
