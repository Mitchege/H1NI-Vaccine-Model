# H1NI-Vaccine-Modelling
## Overview
The goal of this project is to build a predictive model determining whether people got H1N1 vaccines using information shared about their backgrounds, opinions, and health behaviors. This will be important for stakeholders such as NGOs and the government.


## Dependecies

python3
numpy
pandas
seaborn
sklearn
scipy.stats
statsmodels
matplotlib
scipy

The project is divided into the following sections:

Business understanding
Main objective
Objectives
Data understanding
Data preparation
Exploratory data analysis
Modeling
Evaluation
Conclusion

## Business Understanding


Vaccines provide immunization for individuals, and enough immunization in a community can further reduce the spread of diseases. However, it was noted in a study that numerous participants expressed reluctance or hesitation towards getting vaccinated.
Vaccine hesitancy is a well-known phenomenon, and the World Health Organization recognizes it as one of the top ten threats to global health. 
Having a comprehensive knowledge of the traits linked to individuals' vaccination behavior can aid in the planning and implementation of future public health initiatives by the government or NGOs.


## Main objective
The goal of this project is to build a predictive model determining whether people got H1N1 vaccines using information shared about their backgrounds, opinions, and health behaviors.


Objectives
To identify the most significant features in determining insurance premiums

To build a linear regression model that can accurately predict insurance premiums based on input features from the Kaggle insurance premium prediction dataset.

To assess the performance of the predictive model and identify potential areas for improvement.

Data Understanding
Data Source
The dataset used for this project was obtained from Kaggle.

Data Description
The insurance.csv dataset contains 7 columns and 1338 observations (rows). The 7 columns contain 4 numerical features (age, bmi, children and expenses) and 3 categorical features (region, sex and smoker).

Data Preparation
The data was cleaned and pre-processed to ensure that it was in a usable form. This was done by removing duplicates and checking for outliers. The data was also validated against an external data source to ensure that it was in line with what it should be. Using exploratory data analysis, the data sets were analyzed and trends found by using statistics and visualizations to aid in comprehending the data set.

Modeling
Multiple linear regression was used to build the predictive model. In summary, the data modeling process for insurance premium prediction using Linear regression involved checking the correlation between the predictor and target variables, which resulted in weak correlations for all predictor variables. Binary encoding was used to convert the categorical data into a form that can be used by the Ordinary Least Squares (OLS) model. The Least Squares Method (LSM) was used to fit the model and it was found to be statistically significant with a probability of F-statistic below 0.05. The model was able to explain 74.8% of the variation in the insurance premium and had a Mean Absolute Percentage Error (MAPE) of 42.26%. However, it was also found that there existed a non-linear relationship between the predictors and the response variable and there was some evidence of heteroskedasticity as the residuals displayed a funnel-shape
A second model was fitted to to deal with the non-linear relationships between the predictor and response. The target, age and BMI was log transformed and fitted using OLS where the model's Adjusted R-squared increase to 76 %. The MAPE also reduced significantly to 23 %. The final model was fitted to further refine the non-linear relationships. After log-transforming the target and including interaction terms for between smoker, age and BMI, the final model improved further to record an R-squared of 82%. It also recorded a MAPE of 10 %

Evaluation
The performance of the predictive model was evaluated using several metrics including R-squared and Mean Absolute Percentage Error (MAPE). The final model was found to have an R-squared value of 0.821, a MAPE of 10%.

Recommendations
1.The company should consider implementing a higher premium for smokers, as the data indicates that they have a higher expected expense.

2.The company should also take into account the number of children when setting premiums, as this variable had a positive correlation with expenses.

3.The company can also consider offering discounted premiums for policyholders from the SouthWest and Northwest regions, as they had lower expected expenses compared to those from the SouthEast region.

4.The company should also consider collecting more data on other factors such as medical conditions, previous claims, lifestyle, and occupation to improve the accuracy of their pricing model.

5.The company can also consider offering discounts for individuals who maintain a healthy BMI, as this variable was negatively correlated with expenses.

6.The company should also consider the age of a policyholder when setting premiums, as this variable had a positive correlation with expenses.

7.The company should also consider the policyholders sex when setting premiums, as this variable had a positive correlation with expenses for males.

8.Finally, the company should consider using the developed model as a guide for pricing premiums, as it had a low MAPE of 10% which indicates that it is a good model for predicting expenses.

The model developed in this project can accurately predict insurance premiums for policyholders based on their characteristics. Insurance companies can use this model to manage risk and ensure financial stability by setting premiums that are aligned with the level of risk. Potential areas for improvement include further feature engineering and the use of other predictive modeling techniques.