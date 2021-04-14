# Normalization and Standardization 

Dataset link: https://www.kaggle.com/pankajvermacool/titanic-traincsv

Classification Problem: Logistic Regression

## Difference between fit(), transform(), fit_transform(), predict() in sklearn

### Lifecycle

EDA -> FE(Feature Engineering) -> FS(Feature Selection) -> Model Creation -> Hyperparameter Tunning -> Model Deployment                          
               

## Data Preprocessing:
    Transformers: Used for "feature transformation".
    
Example: 
1. StandardScaler: Convert the feature "μ = 0", "σ = 1 (Standard deviation)" 
2. Min-Max Scaler
3. PCA
4. Imputer: To handle the nan values



## Model Training:
    We have objects like "models". Only learning the parameters. Training models.
    
Example:
**Linear Regression, Logistic Regression, RandomForest, Decision Tree, etc. ...**

### Where we use fit(), transform(), fit_transform(), predict()?

fit(): fit() is used in "Standard Scaler" to compute **"σ and μ"**. 

transform(): After performing fit() we perform transform(). In transform() it perform normalization formula. (Changing the data)

fit_transform():
    Input all features and o/p to the model firstly it perform fit(). fit() calculate parameters and weight. Then second it perform predict(). In predict() model input new data and using predict() function it generate o/p. 

* fit_transform() used in model, it has two main function 1. fit() 2. predict()

### What is difference in model and transformer?
* model: in model only fit() is used for training data and only predict() is used for test data.

* transformer: in transformer fit_transform() are used for traning data and only transform() is used for test data.('coz new data is already in preprocessed form)

* Transformer: (Used in Data Preprocessing phase)

  Training data: fit_transform() perform
  
  Test data: transform() perform
  
* Model: (Used in Model Creation phase)
  
  Training data: .fit() perform
  
  Test data: .predict() perform
