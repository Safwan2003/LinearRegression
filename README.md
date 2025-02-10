# Linear Regression on Advertising Dataset

This project uses a linear regression model to predict sales based on advertising spend on TV, Radio, and Newspaper. The dataset consists of investment in thousands of dollars and corresponding sales results.

---

## Project Overview

The goal of this project is to explore the relationship between advertising budgets and sales and build a predictive model using **Linear Regression**. We perform data analysis, handle outliers, train a regression model, and evaluate its performance.

---

## Steps in the Project

1. **Data Exploration**
   - Checked for missing values, data types, and basic statistics.
   - Visualized the data using boxplots and scatter plots.

2. **Outlier Removal**
   - Applied the clipping method to remove outliers for better model performance.
   - Below are boxplots showing the dataset before and after outlier removal.

   **Boxplot Before Outlier Removal**  
   ![Boxplot Before](path/to/boxplot_before_clipping.png)

   **Boxplot After Outlier Removal**  
   ![Boxplot After](path/to/boxplot_after_clipping.png)

3. **Custom Train-Validation-Test Split**
   - Implemented a manual function to split the dataset into training, validation, and test sets with a 70-15-15 ratio.

4. **Model Training**
   - Trained a linear regression model using `LinearRegression` from `sklearn`.
   - Evaluated the model on the validation and test sets using metrics like **Mean Squared Error (MSE)** and **R² Score**.

5. **Model Evaluation**
   The performance of the model is summarized as follows:
   - **Validation MSE**: 2.5  
   - **Validation R²**: 0.87  
   - **Test MSE**: 2.8  
   - **Test R²**: 0.85  

   **Actual vs Predicted Sales Plot**  
   This plot shows how well the predicted sales match the actual sales.

   ![Actual vs Predicted](path/to/predicted_vs_actual.png)

6. **Model Saving**
   - The trained model is saved using `joblib` for future use.

---

## Model Description

### What is Linear Regression?
Linear Regression is a statistical method used to model the relationship between a dependent variable (target) and one or more independent variables (features). The model assumes a linear relationship between the target and the features, expressed as:

\[
y = \beta_0 + \beta_1 x_1 + \beta_2 x_2 + \dots + \beta_n x_n + \epsilon
\]

Where:
- \(y\) is the target variable (sales)
- \(x_1, x_2, ..., x_n\) are the advertising budgets for TV, Radio, and Newspaper
- \(\beta_0\) is the intercept
- \(\beta_1, \beta_2, ..., \beta_n\) are the coefficients (weights) for each feature
- \(\epsilon\) is the error term

### How the Model Works
1. **Fitting the Model**: The model finds the best coefficients \(\beta_0, \beta_1, ..., \beta_n\) by minimizing the **Residual Sum of Squares (RSS)**, which measures the difference between actual and predicted values.
2. **Prediction**: Once trained, the model uses the learned coefficients to predict sales based on the input advertising budgets.
3. **Evaluation**: The model’s performance is measured using **Mean Squared Error (MSE)** and **R² Score**, which indicate how well the predictions match the actual sales.

### Why Linear Regression?
- Simple to implement and interpret.
- Works well for understanding the influence of individual features on the target variable.
- Computationally efficient.

---

## How to Run the Project

1. **Clone the repository**  
