# CreditRisk
Columbia Data Analytics Boot Camp - Module 17 - Supervised Machine Learning and Credit Risk - In this module, I used Python to build and evaluate several machine learning models to predict credit risk. Being able to predict credit risk with machine learning helps banks and financial institutions predict anomalies, reduce risk cases, monitor portfolios, and provide recommendations on what to do in cases of fraud.

## What I Learned/Achieved:
- How to explain a machine learning algorithm's function in data analytics.
- How to create training and test groups from a given dataset.
- How to implement the logistic regression, decision tree, random forest, and support vector machine algorithms.
- How to compare the advantages and disadvantages of each supervised learning algorithm.
- How to determine which supervised learning algorithm is best used for a given dataset or scenario.
- How to use ensemble and resampling techniques to improve model performance.

## Results:
*Naive Random Oversampling* :
The balanced accuracy score is 60%. The precision is 99%. The recall score is 66%.
| | pre   |    rec   |    spe    |    f1   |    geo   |    iba   |    sup |
|-| ----- | -------- | --------- | ------- | -------- | -------- | ------ |
| high_risk |    0.01   |   0.56   |   0.65  |    0.02   |   0.60    |  0.36 |  104 |
| low_risk  |  1.00    |  0.65   |   0.56   |   0.79   |   0.60   |   0.37 |   17101 |
| avg / total |  0.99   |   0.65   | 0.56   |   0.78   |   0.60   |   0.37 |  17205 |

*SMOTE Oversampling* :
The balanced accuracy score is 59.3%. The precision score is 99%. The recall score is 68%.
| | pre   |    rec   |    spe    |    f1   |    geo   |    iba   |    sup |
|-| ----- | -------- | --------- | ------- | -------- | -------- | ------ |
| high_risk |    0.01   |   0.48   |   0.71  |    0.02   |   0.58    |  0.33 |  104 |
| low_risk  |  1.00    |  0.71   |   0.48   |   0.79   |   0.58   |   0.35 |   17101 |
| avg / total |  0.99   |   0.71   | 0.48   |   0.78   |   0.58   |   0.35 |  17205 |

*Undersampling* :
The balanced accuracy score is 59.3%. The precision is 99%. The recall score is 47%.
| | pre   |    rec   |    spe    |    f1   |    geo   |    iba   |    sup |
|-| ----- | -------- | --------- | ------- | -------- | -------- | ------ |
| high_risk |    0.01   |   0.60   |  0.47  |   0.01  |   0.53   |  0.28  |    104 |
| low_risk  |  0.99    |  0.47   |   0.60   |   0.63  |   0.53   |  0.27  |  17101 |
| avg / total |  0.99   |   0.47   | 0.60   |   0.63  |   0.53   |  0.27  |  17205 |

*Combination Over- and Under- Sampling* :
The balanced accuracy score is 64%. The precision score is 99%. The recall score is 58%.
| | pre   |    rec   |    spe    |    f1   |    geo   |    iba   |    sup |
|-| ----- | -------- | --------- | ------- | -------- | -------- | ------ |
| high_risk |  0.01    |   0.68   |  0.58  |   0.02  |   0.63   |  0.40  |    104 |
| low_risk  |  1.00    |   0.58   |  0.68   |   0.74  |   0.63   |  0.39  |  17101 |
| avg / total |  0.99  |   0.58   |  0.68   |   0.73  |   0.63   |  0.39  |  17205 |

*Balanced Random Forest Classifier* :
The balanced accuracy score is 63.25%. The precision score is 99%. The recall score is 88%. 
| | pre   |    rec   |    spe    |    f1   |    geo   |    iba   |    sup |
|-| ----- | -------- | --------- | ------- | -------- | -------- | ------ |
| high_risk |  0.03    |   0.67   |  0.88  |   0.06  |   0.77   |  0.58  |    92 |
| low_risk  |  1.00    |   0.88   |  0.67   |   0.94  |   0.77   |  0.61  |  17101 |
| avg / total |  0.99  |   0.88   |  0.68   |   0.93  |   0.77   |  0.61  |  17205 |

*Easy Ensemble AdaBoost* :
The balanced accurarcy score is 92.93%. The precision score is 99%. The recall score is 93%. 
| | pre   |    rec   |    spe    |    f1   |    geo   |    iba   |    sup |
|-| ----- | -------- | --------- | ------- | -------- | -------- | ------ |
| high_risk |  0.07    |   0.92   |  0.93  |   0.13  |   0.93   |  0.86  |    92 |
| low_risk  |  1.00    |   0.93   |  0.92   |   0.97  |   0.93   |  0.86  |  17101 |
| avg / total |  0.99  |   0.93   |  0.92   |   0.96  |   0.93   |  0.86  |  17205 |

## Summary
The precision rates for each of the machine learning models was high. The recall rate was not near as close to one as the precision rates for the same machine learning models. Depending on the bank, and their strategic positioning, different models can be used to achieve different results. There are some banks that offer lower interest rates to more "risky" consumers while other banks offer higher interest rates to "risky" consumers.

In further studies, I would use R to correlate the relationship between the bank's lending position and the riskiness of the consumers. By using this strategy for certain cases, I believe that banks looking to offer more capital to risky consumers will find their target market, while banks looking to limit their risk and retain capital can provide their cash asset to more qualified customers.

From investopedia.com, I read that the five aspects of consumer credit risk are "credit history, capacity to reapy capital borrowed, the loan's conditions, and associated collateral." These variables may change in other forms of lending, but for this analysis, I believe the machine learning models provide a good insight into possible calculations of risk associated with lending from one dataset.
