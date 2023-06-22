# credit-risk-classification

In this assignment given by Birmingham University Data Boot Camp, credit worthiness of borrowers of a lending services company have been analyzed using a dataset of historical lending activity and by Supervised Machine Learning.

Firstly, the CSV file has been read and converted to Pandas Data Frame, separated as futures (X) and label (y). There are seven futures (loan size, interest rate, borrower income, debt to income ratio, number of accounts, derogatory marks and total debt) that affect loan status. Using “sklearn” library, data has been splitted and trained with Logistics Regression model, predictions have been made on testing data and accuracy score, confusion matrix, classification report have been generated. 

Secondly, in order to increase model’s efficiency regarding to high-risk loans, training data has been resampled with “RandomOverSampler” imported from “imblearn.over_sampling” library. The Logistic Regression model has been applied to balanced data and it has been found that using resampled data is more successful to predict loan risk.
