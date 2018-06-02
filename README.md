# NYC-Property-Regression
A real life case study of property price prediction based on data of New York.

# Project Background

In the case of a Real Estate Investment Trust (REIT), which invests in houses and apartments in New York state, 
part of the REIT business is try to predict the fair transaction price of a property before it's sold.
They do so to calibrate their internal pricing models and keep a pulse on the market.

In this project, the dataset represents the investment in houses, apartments, and condos within a small county in New York state.

# Current Working Solution

The REIT currently employs a third-party appraisal service for estimating the price of the property with their own expertise. 
In practice, the skill level of individual appraisers vary quite large. 

To estimate the mis-priced range, the REIT run a trial run to compare the actual transaction prices to the estimates from the appraiser.
It was found that the estimates given by inexperienced appraisers differs ***$70,000*** on average.

# The role as a data scientist

The REIT has decided to implement a data-driven approach to valuing properties instead 
of relying on the personal expertise from the appraiser.

The REIT currently have an untapped dataset of transaction prices for previous properties on the market. 
Our task is to build a real-estate pricing model using that dataset.

If we can build a model to predict transaction prices with an average error of under ***$70,000***, 
then the REIT can replace inexperienced appraisers with our model.

# Problem Specification and Scope

Deliverable: Trained model file
Machine learning task: Regression
Target variable: Transaction Price
Win condition: Avg. prediction error < $70,000, using Mean Absolute Error (MAE)

# Results & Development

[NYC_Property_Regression.ipynb](https://github.com/jsrpy/NYC-Property-Regression/blob/master/NYC_Property_Regression.ipynb)
contains the trial solution, with the following MAE (USD) of respective model:

* Random Forest (default): 46052
* Xgboost (default): 45025
* Lightgbm (tuned): 48051
* Catboost (default): 43525

Further improvements will be deployed using gridsearch and cross validation to tune the best parameters.

# Requirements
* pandas
* numpy
* matplotlib
* scikit-learn
* xgboost
* lightgbm
* catboost
