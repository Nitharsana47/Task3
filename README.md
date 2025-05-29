#  House Price Prediction with Linear Regression

This project aims to build a machine learning model to predict house prices based on housing features using **Linear Regression**. It uses the `Housing.csv` dataset, which includes both numerical and categorical features.

---

## Project Overview

The goal is to predict the price of a house based on several attributes like:
- Area (in sq.ft)
- Number of bedrooms and bathrooms
- Presence of amenities (e.g., air conditioning, hot water, guest room)
- Location characteristics (main road access, preferred area)

---

## Workflow

1. **Data Loading**  
   The dataset `Housing.csv` is loaded into a DataFrame.

2. **Data Cleaning**  
   Categorical values are standardized (e.g., removing extra spaces, converting to lowercase).

3. **Feature Engineering**  
   Features are split into:
   - Numerical: area, bedrooms, bathrooms, stories, parking
   - Categorical: mainroad, guestroom, basement, airconditioning, hotwaterheating, prefarea, furnishingstatus

4. **Preprocessing**  
   - Categorical variables are encoded using One-Hot Encoding.
   - Numerical variables are used as-is.
   - A `ColumnTransformer` is used to automate this.

5. **Model Building**  
   - A pipeline is created combining preprocessing and a `LinearRegression` model.
   - Data is split into training and test sets (typically 80-20 split).
   - The model is trained using the training set.

6. **Evaluation**  
   - Model is evaluated using:
     - **Mean Absolute Error (MAE)**
     - **Mean Squared Error (MSE)**
     - **R² Score**
   - These metrics indicate how well the model predicts house prices.
   - A scatter plot is generated to compare actual vs predicted values.

---

## Result Interpretation

- **MAE and MSE** measure the average errors in price prediction.
- **R² Score (~0.65)** shows moderate performance — the model explains ~65% of the price variance.
- A better model can be achieved by:
  - Trying **non-linear models** (e.g., Decision Tree, Random Forest, Gradient Boosting)
  - **Feature scaling** or transforming skewed features
  - **Hyperparameter tuning**



