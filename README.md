# Prediction Model for H1NI Vaccine Uptake
![H1N1](https://github.com/Mitchege/H1NI-Vaccine-Model/blob/main/H1N1VACCINE.jpeg)



## Overview
The goal of this project is to build a predictive model determining whether people got H1N1 vaccines using information shared about their backgrounds, opinions, and health behaviors. This will be important for stakeholders such as NGOs and the government.


## Dependecies

*python3

*numpy

*pandas

*seaborn

*sklearn

*scipy.stats

*statsmodels

*matplotlib

*scipy

The project is divided into the following sections:

## Business understanding
i. Main objective

ii. Objectives

iii. Data understanding

iv Data preparation

v. Exploratory data analysis

vi. Modeling

vii. Conclusion

viii. Recommendations

ix. Future improvement Ideas

## Business Understanding


Vaccines provide immunization for individuals, and enough immunization in a community can further reduce the spread of diseases. However, it was noted in a study that numerous participants expressed reluctance or hesitation towards getting vaccinated.
Vaccine hesitancy is a well-known phenomenon, and the World Health Organization recognizes it as one of the top ten threats to global health. 
Having a comprehensive knowledge of the traits linked to individuals' vaccination behavior can aid in the planning and implementation of future public health initiatives by the government or NGOs.


## Main objective

The goal of this project is to build a predictive model determining whether people got H1N1 vaccines using information shared about their backgrounds, opinions, and health behaviors.


### Specific Objectives

To identify the most significant features in determining whether an individual is vaccinated against H1N1.

To build a Decision Tree, Random Forest and SMV model that can accurately predict whether an individual is vaccinated against H1N1.

To assess the performance of the predictive models and identify the best one and potential areas for improvement.


### Data Understanding
#### Data Source
The dataset used for this project was obtained from  [Drivendata](https://www.drivendata.org/competitions/66/flu-shot-learning/)

### Data Description

The data was in csv format and contained training, test and label data. The dataset contained 26,707 rows and 38 columns. The 38 columns contained 26 numerical features and 12 categorical features.


### Data Preparation
The necessary libraries were imported and then the training and label dataset was loaded onto the notebook. 
The  training and label dataset was first merged, read and then checked to ensure that each column has an appropriate datatype. This also highlighted the columns with null values which would be tidied in the next few steps. Lastly, the various statistical measures in the data frame were checked for each feature. 
The data was then cleaned and pre-processed to ensure that it was complete for modeling purposes. This included identifying the null values, computing the percentage of the missing values and dropping columns with missing data greater than 10%. Later, a data frame of the remaining columns with missing values was created and the numerical and categorical columns were cleaned separately. For the numerical columns, the null values were replaced with the mode while for the categorical columns null values were replaced with ‘missing’. With the null values taken care off, all duplicated rows were identified and dropped accordingly and all columns relating to seasonal_vaccine were dropped. This was because H1N1 was selected as the target variable for the project.  


### Modeling
Data modeling process involved pre processing the data first. This involved feature selection which is the process of selecting a subset of the most important features or variables from a larger set of features. By conducting feature selection and deleting noisy, redundant, or irrelevant characteristics from the data, feature selection aims to improve the performance of machine learning systems. A heat map showing the correlations between the various features and target variable was plotted. Afterwards, all unecessary columns and features with low correlation with the target variable were dropped. Lastly, all categorical features were encoded using ordinal encoding and the dataframe split and scaled. 

The next steps involved building models using Decision Tree, Random Forest and SMV classifiers. The steps for each of these classifiers were similar and are broken down as follows:
i) Training a classifier.
ii) Making predictions for test data.
iii) Calculating accuracy, precsion and recall.
iv) Using GridSearchCV to tune the classifier’s hyperparamenters.
v) Insantiating the model with the best parameters from grid search.
vi) Making predictions for test data using the tuned model.
vii) Calculating accuracy, precsion and recall once more.
These steps were used in all models with the exception of decision tress where Bootdtrap Aggregation (Bagging) was carried out to reduce the variance of the model and improve its generalization performance.


### Conclusion
|Model | Accuracy | Precision | Recall | F1 |
|:--- |:--- |:--- |:--- |:--- |
|Decision Tree| 83% |76% |68% |71% |
|Random Forest| 83% |78% |67% |70% |
|SVM| 83% |77% |68% |71% |

The performance of the predictive model was evaluated using the precision score and recall score. The final model was found to have a precision score of 83%, and a recall score of 68%.

### Recommendations
The stakeholders (government and NGOs) should consider conducting mass education through awareness campaigns to reduce vaccine hesitation.

ii.The stakeholders should work with hospitals to encourage vaccine uptake through doctors recommendations.

iii.The stakeholders should focus on educating younger age groups on the importance of vaccinations.

### Future Improvement Ideas
1.Building a pipeline for this model.

2.Tuning the Random Forest classifier with a larger range.
