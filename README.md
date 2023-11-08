# credit-risk-classification
In this challenge, I was tasked as an analyst to train and build a model to evaluate it based on loan risk. Dataset of historical lending activity was from peer-to-peer lending services were used. 
The purpose of the model is to identify the creditworthiness of borrowers.
To begin with, I split the dataset into 2 by creating a y column with the "loan status" column and X feature label with the remaining columns in the dataframe.
I applied my knowledge of logistic regression to fit logistic regression model using the train data. The prediction was saved for the testing data labels by using the testing feature data and the fitted model.
The model performance was evaluated by calculating the accuracy score and generating confusion matrix and printing the classification report as seen below.

Accuracy score 
0.9924164259182832
 
Confusion matrix.
 array([[18679,    80],
       [   67,   558]], dtype=int64)

Classification Report.
               precision    recall  f1-score   support

Class Purple       1.00      1.00      1.00     18759
Class Yellow       0.87      0.89      0.88       625

    accuracy                           0.99     19384
   macro avg       0.94      0.94      0.94     19384
weighted avg       0.99      0.99      0.99     19384

A second model was created by using the randomoversampler library to resample the training data to reevaluate the firts model.
Logistic regression and resampled data were used to fit the model and make predictions. 
Metrics for oversampled data.
Accuracy Score: 0.9952022286421791

Confusion Matrix of Resampled Data: 
[[18668    91]
 [    2   623]]
            precision    recall  f1-score   support

           0       1.00      1.00      1.00     18759
           1       0.87      1.00      0.93       625

    accuracy                           1.00     19384
   macro avg       0.94      1.00      0.96     19384
weighted avg       1.00      1.00      1.00     19384

The main aim of this analysis is to use machine learning specifically supervised learning to to determine how best we can predict if a person is healthy(low risk) or unhealthy (hifh risk) if they were to be given a loan.
The purpose of this project i sto predict the credit worthiness of borrowers.
To begin with, I split the dataset into 2 by creating a y column with the "loan status" column and X feature label with the remaining columns in the dataframe.
I applied my knowledge of logistic regression to fit logistic regression model using the train data. The prediction was saved for the testing data labels by using the testing feature data and the fitted model.
The model performance was evaluated by calculating the accuracy score and generating confusion matrix and printing the classification report as seen below.

THe results of my analysis is posted above.
The accuracy score for the first model is approximately 99%. The model is very efficient in predictinh healthy loan with a recal of 100% for low risk and 89% for high risk loan.
THe confusion matrix generated 67 false positive and 80 false negatives.

The accuracy score for the second model is 99.5%. The recall from classification report show 100% prediction for both low risk and high risk loan. We could also see a 2 false positives and 91 false negatives from the confusion matrix.

In summary, I can conclude that the second model is best fit for predicting high risk loan, while the first is best for predicting low risk loan. Based upon the nuber of false positives in each model's confusion matrix.
I will recommend second model for the fact that it has less false positives compared to the first model's.


