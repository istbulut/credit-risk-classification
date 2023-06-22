Analysis Report:

EVALUATING LOAN RISK

In this analysis from dataset of historical lending activity of a lending services company, we try to identify credit worthiness of  borrowers. 

Dataset has 77.536 data with "loan status" (dependent variable) of 75036 healthy loan "0" and  2500 high-risk loan  "1". 
We have 7 undependent variable to predict loan status (loan size, interest rate, borrower income, debt to income ratio, number of accounts, derogatory marks and total debt)
To predict "loan status" data has been splitted  as test and train (%75-%25)  and trained with Logistic Regression Model from "sklearn" library.
Then accuracy score, confusion matrix and classification report have been generated from predictions.
Logistic Regression model has been also applied to resampled training data, for this, "RandomOverSampler" from  "imbalanced-learn" library has been used
(with labels of equal number of data points "0"=56271  and  "1" = 56271).

Machine Learning Model 1:

Accuracy Score: 0.9919

                    precision    recall      f1-score     support

           0       1.00             0.99      1.00            18765
           1       0.85             0.91      0.88             619


Machine Learning Model 2 (balanced data):

Accuracy Score:  0.9938

                    precision    recall      f1-score     support

           0       1.00            0.99       1.00             18765
           1       0.84            0.99       0.91             619


Summary: 

From classification report of Model 1 ( "0"= 75036 and  "1"= 2500), it can be seen that model is more successsful to predict "0" (health loans) and less able to predict credit risk "1".
Looking at dependent variable,  since the data is unbalanced on behalf of "0" so  it can not reflect "1" risky loans very well.
Even though accuracy scores are very high in both models and precision scores are very similar, recall values seems as  better determiner for the predictions and for strenght of models.
Especially, if it is more important to identify risky customers ("1"), it is better to use over sampled balanced data (Model 2)  for the model prediction,
because it is more successfull to identify risky customers than Model 1 with recall 0.99 >0.91.
Also higher f1-score (0.91> 0.88)  in Model 2 - balanced data shows that there is better/higher presicion and recall measurement in Model 2.

