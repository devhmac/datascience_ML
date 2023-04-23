# Machine Learning

## Supervised Learning

Trained using labeled inputs/examples

Data often split into 3 sets

- Training data - Train model parameters
- Validation data - Used to determine what model hyperparameters to adjust
- Test data - used to get final performance metric

Final measure on test data is final performance metric, cant go back and adjust hyperparameters

## Machine Learning Errors

## Evaluating Classification Models

Classification models can only be correct or incorrect

- In the real world, not all correct or incorrect values are equal

### Accuracy

- Number of correct predictions / total predictions
- Useful when target classes are well balanced
- Not good with unbalanced classes
  - think only selecting false on T or F test and getting 50%

### Recall

- ability of model to find all relevant cases within dataset
- True Positives divided by True positives + false negatives

### Precision

- ability for model to identify only relevant data points within dataset
- True pos / true pos + False positives

Tradeoff between recall and precision

- Finding all relevant instances VS proportion of data points our model says is relevant, that actually were relevant

### F1 Score

- Harmonic mean of precision and recall - if you want to strike a balance you use this

F1 = 2 _ (precision _ recall) / (precision + recall)

- This is good because it punishes extreme difference between precision and recall

### Confusion matrix

- Generally will have to decide if its more important to fix/reduce false positives, or false negatives
  Eg - testing for an illness

| Predicted condition |               |                     |                     |     |
| ------------------- | ------------- | ------------------- | ------------------- | --- |
|                     |               | Prediction Positive | Prediction Negative |     |
| True                | Condition Pos | True Pos            | False Neg           |     |
| Condition           | Condition Neg | False Pos           | True Neg            |     |

### Evaluating Regression Models

- attempts to predict continuous values
  - Classification metrics not usefull for regression

### Mean Absolute Error

- Mean of absolute value of errors
  Diff between absolute value of true and predicted price, averaged across all predictions
  - Downside: Wont punish large errors

### Mean Squared Error

- more popular

Diff true value Minus predicted value Squared (dont need to take absolute value as square does that)

- larger errors noted more

Problem: if we're predicting dollars, our error is now in dollars squared, which is less useful than Mean absolute error, which would have error result in a dollar range

### Root Mean square Error(RMSE)

- Most popular!

Just take square root of mean squared error, punishes error, but returns Y's metrics

What is a good RMSE?

- Compare your error metric to the average value of the label in your dataset to get an intuition for overall performance

  ***

# Machine Learning with python

Data Aquisition -> Cleaning -> split data -> model training/building (half or third of data) ->testing -other half of segregated data -> deploy
