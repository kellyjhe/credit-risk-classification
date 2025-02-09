# Credit Risk Classification

## 🔬 Analysis
The purpose of this analysis is to summarize the findings from using unsupervised machine learning to predict outcomes of loan risk. 

The financial information given by the data includes loan size, interest rate, borrower income, debt to income rate, number of accounts, derogatory marks, total debt, and the loan status (whether it is a high-risk or healthy loan). 

With this data, we aim to predict the loan status of future prospective clients given similar data, and whether the loan would be feasible or risky. This mostly includes the variable of y, which holds the value of loan_status. In the given data, loan_status results either a '0' or '1' value, with '0' indicating a healthy loan and '1' indicating a high-risk loan. By creating a logistic regression model, we can input test values to predict whether new data will result in a '0' or '1' for the y-variable.

The process began by splitting data into training and testing sets. I used the training sets to create the model and form an algorithm that can predict correct outcomes as closely as possible. By using the train_test_split function, we successfully split the data with a randomized state to ensure low bias. Then, we create a logistic regression model by using the training data X_train and y_train from our given data.

To create predictions, I used the X_test and y_test testing sets of the data. The classifier.predict function allows us to create predictions that I can input into a confusion matrix and classification report. These summarize the prediction accuracy of the logisitic regression model.

## 📍 Results
* Machine Learning Model 1:
    * Accuracy score: 0.99
    *    The accuracy score is the rate at which the model predicts correctly. This score tells us that the logistic regression model has an accuracy of 99%, which is high.
    * Precision:
    *    0: 1.00
    *    1: 0.84
    *       The precision tells us the proportion of all positive predictions made by a model that are actually correct. Here, the logistic regression model has a precision of 100% for predicting healthy loans, and a precision score of 84% for high-risk loans. This means that 100% of its predictions for healthy loans are correct, while its predictions for high-risk loans fall short. The higher the rate for the precision score, the more likely the model's positive predictions are correct.
    * Recall:
    *    0: 0.99
    *    1: 0.94
    *       The recall tells us the true positive rate or the proportion of all actual positives that were correctly predicted as positives. Here, the model has a 99% accuracy for predicting positives for healthy loans, and a 94% accuracy for predicting high-risk loans. These are both high percentages, which indicates that the model is effective at positive predictions.
 
## 📖 Summary
In summary, the logisitic regression model is fairly accurate at predictions because of the high scores it receives in the classification report. It excels better at predicting healthy loans compared to high-risk loans, since it scores higher for percentages related to the '0' variable. As an analyst, we aim to identify high-risk loans and would prefer '1' to be more accurately predicted because a false positive of a healthy loan that was predicted as high-risk is less dangerous that the other way around. 

Thus, this model could use some improvement to more accurately predict the variables that are more important to its credit analysts.
