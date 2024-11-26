# House Pricing Prediction

This project uses machine learning techniques to predict house prices based on various features such as square footage, number of rooms, location, and other relevant factors. We apply **Ridge Regression** to model the relationship between these features and the target variable (price) while addressing issues like overfitting.

## Project Goal

The primary goal of this project is to develop a predictive model for house prices in King County, USA. Given the various factors affecting house prices, such as the size of the house, location, and other attributes, the model aims to predict the price of a house based on these input features.

### Regression Technique Used
We use **Ridge Regression**, a type of **linear regression** that includes an L2 regularization term to prevent overfitting. Ridge Regression is particularly useful when dealing with high-dimensional datasets where there are multiple features that could potentially cause the model to fit the training data too closely (overfitting). By adding a penalty for large coefficients, Ridge helps improve the model’s generalization to new, unseen data.

### Underfitting vs Overfitting
- **Underfitting** occurs when a model is too simple to capture the underlying patterns in the data. It typically leads to poor performance both on the training set and the test set. For example, if we used a linear regression without any feature transformations or regularization, the model might fail to capture non-linear relationships in the data, leading to underfitting.
  
- **Overfitting**, on the other hand, happens when a model is too complex and captures noise or random fluctuations in the training data, leading to excellent performance on the training set but poor generalization to new data. This is often seen when models have too many features or overly complex relationships between the features and target variable. Ridge Regression helps mitigate this by penalizing large coefficients, ensuring the model remains more generalized.

## Project Workflow

The project follows these key steps to achieve a balance between underfitting and overfitting:

1. **Data Preprocessing**: 
   - The dataset is loaded, cleaned, and preprocessed. This includes handling missing values, encoding categorical variables, and scaling numerical features. Proper preprocessing ensures that the data is in a suitable form for modeling.
   
2. **Feature Engineering**:
   - **Polynomial Features** are created from the existing features to capture non-linear relationships in the data. This step is crucial to improve the model’s ability to fit the data more accurately while avoiding underfitting.
   
3. **Model Training**:
   - A **Ridge Regression** model is trained using the processed data. The Ridge model is regularized to prevent overfitting by introducing a penalty on the magnitude of the coefficients.
   
4. **Model Evaluation**:
   - The model is evaluated using the **R-squared (R²)** score, which measures how well the model explains the variance in the target variable (house prices). An R² score close to 1.0 indicates that the model is effectively capturing the relationship between the features and the target, while a low score suggests the model may not be learning the underlying patterns well.

## Files in this Repository

- **House_Sales_in_King_Count_USA.ipynb**: The Jupyter notebook that contains the code for data preprocessing, feature engineering, model training, and evaluation.

