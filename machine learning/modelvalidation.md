Building a machine learning model to predict house prices involves a systematic approach to selecting data and applying specific coding steps. Here is a detailed breakdown of that process:

### 1. Data Selection and Cleaning
Initially, datasets often contain too many variables to analyze all at once. You start by selecting a few columns based on intuition, using the `.columns` property to view your options. 
*   **Handling Missing Values:** Real-world data often has gaps where information wasn't recorded. For beginners, the simplest solution is to use `dropna(axis=0)`, which removes houses with missing data from the analysis.

### 2. Defining Target (y) and Features (X)
To train a model, you must divide your data into two specific parts:
*   **The Prediction Target (y):** This is what you want to predict. By convention, this single column is saved as **y**. For example, in the Melbourne data, `y = melbourne_data.Price`.
*   **The Features (X):** These are the inputs used to determine the price, such as 'Rooms', 'Bathroom', and 'Landsize'. These are stored in a DataFrame called **X** by providing a list of column names in brackets. 

### 3. Verifying the Data
Before building the model, it is a best practice to visually inspect your data. 
*   **`X.describe()`:** This provides a statistical summary (mean, min, max, etc.) to help you spot outliers or errors.
*   **`X.head()`:** This displays the top five rows so you can ensure the data looks as expected.

### 4. The Four-Step Modeling Process
Using the **scikit-learn** library (imported as `sklearn`), you follow four logical steps to create and use your model:
1.  **Define:** You choose the model type—such as a `DecisionTreeRegressor`—and specify a `random_state`. Setting `random_state` to a specific number (like 0 or 1) ensures that the model produces the exact same results every time you run the code.
2.  **Fit:** You use `melbourne_model.fit(X, y)` to capture patterns from the data. This is considered the "heart of modeling".
3.  **Predict:** Once the model is fitted, you use the `.predict()` function to estimate the prices of houses.
4.  **Evaluate:** Finally, you measure the accuracy of those predictions.

Does the logic of separating "features" from the "target" make sense to you, or would you like to see how we verify if the predictions were actually accurate?