 Measuring Accuracy with Validation
To know if a model is actually good, you need to measure its predictive accuracy
.
Mean Absolute Error (MAE): This is a key metric that calculates the average difference between the model's prediction and the actual price
. It answers the question: "On average, how far off are our predictions?"
.
The "In-Sample" Trap: A common mistake is testing a model on the same data used to train it
. This leads to "in-sample" scores that look perfect but fail on new data because the model might have memorized patterns that don't actually exist in the real world
.
Train-Test Split: To solve this, you use the train_test_split function to divide your data into two parts: training data to build the model and validation data to test it
.
2. Overfitting vs. Underfitting
Finding the right complexity for a model is a "sweet spot" challenge
:
Overfitting: This happens when a tree is too deep and has many leaves
. The model matches the training data almost perfectly but performs poorly on new data because it captures random noise rather than real patterns
.
Underfitting: This happens when a tree is too shallow
. It fails to capture important distinctions even in the training data, leading to poor accuracy across the board
.
3. Finding the Optimal Model
You can use the max_leaf_nodes argument to control the depth of your tree and prevent these issues
. By comparing the MAE of models with different leaf counts (e.g., 5, 50, 500, or 5000), you can identify the "optimal" size that provides the lowest error on validation data
.