# Normalization and Standardization 

## Difference between fit(), transform(), fit_transform(), predict() in sklearn

### Lifecycle

EDA -> FE(Feature Engineering) -> FS(Feature Selection) -> Model Creation -> Hyperparameter Tunning -> Model Deployment
|-----------------------------------------------------|   |----------------------------------------|   |---------------|
               Data Preprocessing                                     Model Training                           
               

## Data Preprocessing:
    Transformers: Used for "feature transformation".
    
**Example:** 
1. **StandardScaler: Convert the feature "μ = 0", "σ = 1 (Standard deviation)" 
2. **Min-Max Scaler
3. **PCA**
4. **Imputer: ** To handle the nan values



## Model Training:
    We have objects like "models". Only learning the parameters. Training models.
    
**Example: **
Linear Regression, Logistic Regression, RandomForest, Decision Tree, etc. ...

### Where we use fit(), transform(), fit_transform(), predict()?

fit(): fit() is used in "Standard Scaler" to compute **"σ and μ"**. 

transform(): After performing fit() we perform transform(). In transform() it perform normalization formula. (Changing the data)

fit_transform(): 
