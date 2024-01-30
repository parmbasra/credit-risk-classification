# Module 12 Report Template

## Overview of the Analysis

The purpose of the analysis is to use historical lending activity of a company to peer-to-peer lending services. This model likely to predict the creditworthiness of borrowers on healthy and risky loans.

The financial information contains the following data where 0 being for healthy loans for about 75036 data nodes whereas 1 being the unhealthy loans conatins 2500 data nodes/records.

The data is imbalanced as explained in the above point.
loan_status
0    75036
1     2500

The stages of machine learning process used as follows:
  > Spliting the data into training and tests sets
  > Creating in Logistic Regression Model with original data
  > Predict a Logistic Regression Model with Resampled Training Data

Machine Learning Model 1 (Logistic Regression Model with original imbalanced data)
  >>> Confusion Matrix
      [[18655   110]
      [   36   583]]

  >>> Clasification Report 
                      pre       rec       spe        f1       geo       iba       sup

              0       1.00      0.99      0.94      1.00      0.97      0.94     18765
              1       0.84      0.94      0.99      0.89      0.97      0.93       619

      avg / total     0.99      0.99      0.94      0.99      0.97      0.94     19384

Machine Learning Model 2 (Logistic Regression Model using RandomOverSampler)
  >>> Confusion Matrix 
      [[18646   119]
      [    4   615]]

  >>> Classification Report
                        pre       rec       spe        f1       geo       iba       sup

                0       1.00      0.99      0.99      1.00      0.99      0.99     18765
                1       0.84      0.99      0.99      0.91      0.99      0.99       619

      avg / total       0.99      0.99      0.99      0.99      0.99      0.99     19384



In conclusion, both models performed very well in predictings the risker loans. The random over sampler method give better accuracy of 99.3% as compared to the original data one of 96.4%. Apart from that, the recall score is 99% for the random over sampler over the original data model which is having 94%. Futhermore, the precission for both the model is same for the healthy and unhealthy loans. In addition, random over sampler model seems better model as per accuracy and recall rate. This would be significant factor lending services to predict.



