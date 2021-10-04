# Predict IPP (Individual Pension Plan) Contribution

A submission for [Garanti BBVA Teknoloji Data Science Challenge](https://www.kaggle.com/c/onlinedatasciencechallenge/).

**team:** Puffing Billy   
**members:** [@mustafahakkoz](https://github.com/mustafahakkoz)  [@Aysenuryilmazz](https://github.com/Aysenuryilmazz)  
**rank:** 24/72    
**score (RMSE):** 11940.12    
**dataset:** [Garanti IPP](https://www.kaggle.com/c/onlinedatasciencechallenge/data) A realistic dataset to determine the potential customers of **Individial Pension Plan (IPP)** and the possible amount that each one will be willing to pay as the additional contribution. Using external data is encouraged such as inflation data, salary payment days, exchange rates, seasonal temperature ...

- training dataset ( 32.38 MB, 174K rows, 40 cols)

- testing dataset ( 3.07 MB, 17K rows, 38 cols)

Implementation details can be found in notebooks.

---

#### Online Notebooks:

1. [EDA and preprocessing](https://www.kaggle.com/hakkoz/garanti-eda-preprocessing)

2. a. [BayesianOptimization with XGBoost](https://www.kaggle.com/hakkoz/garanti-bayesianoptimization-xgboost)  
   b. [BayesianOptimization with XGBoost and Out-of-Fold (OOF) predictions](https://www.kaggle.com/areukolateamleader/garanti-bayesianoptimization-xgboost-oofpreds)  
   c. [RandomGrid with XGBoost and Out-of-Fold (OOF) predictions](https://www.kaggle.com/hakkoz/garanti-randomgrid-xgboost-oofpreds)

---

#### Repo Content and Implementation Steps:

[**1.garanti-eda-preprocessing.ipynb**](https://github.com/mustafahakkoz/Predict_IPP_Contribution/blob/main/1.garanti-eda-preprocessing.ipynb)

- Handling missing data with IterativeImputer.

- Testing default XGBoost model with LabelEncoder, OneHotEncoder and QuantileTransformer.

[**2.a.garanti-bayesianoptimization-xgboost.ipynb**](https://github.com/mustafahakkoz/Predict_IPP_Contribution/blob/main/2.a.garanti-bayesianoptimization-xgboost.ipynb)

-  Bayesian optimization for tuning XGBoost on one hot encoded data.

[**2.b.garanti-bayesianoptimization-xgboost-oofpreds.ipynb**](https://github.com/mustafahakkoz/Predict_IPP_Contribution/blob/main/2.b.garanti-bayesianoptimization-xgboost-oofpreds.ipynb)

- Expanded search space of **Bayesian optimization** for tuning XGBoost.
- Straight and OOF (Out-of-Fold) predictions.
- Analyzing predictions and feature importances.

[**2.c.garanti-randomgrid-xgboost-oofpreds.ipynb**](https://github.com/mustafahakkoz/Predict_IPP_Contribution/blob/main/2.c.garanti-randomgrid-xgboost-oofpreds.ipynb)

- Expanded search space of **RandomGrid** for tuning XGBoost.
- Straight and OOF (Out-of-Fold) predictions.
- Analyzing predictions and feature importances.

---

#### Notes:

- We didin't use external data, it could have been beneficial.

- We focused on tuning models. Instead, we could have implement more extensive preprocessing (creating more features, more data mining, advanced null handling, more feature elimination etc.) to improve our scores.

- We should have try autoML techniques.
