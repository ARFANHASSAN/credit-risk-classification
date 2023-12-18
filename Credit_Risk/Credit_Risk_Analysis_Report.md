# Credit Risk Analysis Report
## An overview of the analysis:
------------------------------------------------------------------------------
Lending institutions extend loans or assets to borrowers with the expectation that borrowers will either return the asset or repay the loan. The emergence of Credit Risk occurs when a borrower fails to fulfill the repayment, leading to potential financial losses for the lender. Lenders evaluate this risk using diverse methods, and in this investigation, Machine Learning is employed to analyze a dataset comprising historical lending transactions from a peer-to-peer lending platform. The goal is to construct a model capable of evaluating the creditworthiness of borrowers.

Utilizing a machine learning model, I sought to categorize loans as either safe (low-risk) or risky (high-risk) based on the loan status provided by the lending company.

Upon scrutinizing the lending company's dataset, I devised a Logistic Regression Model that exhibited an impressive accuracy score of 99%. However, in differentiating non-healthy loans, the model's recall value is comparatively lower (0.91) in contrast to its recall value for healthy loans (0.99). This indicates that the model excels more in predicting loan status as healthy than in identifying loan status as non-healthy. The underlying cause of this dissimilarity lies in the dataset's imbalance, where a significant majority of the data corresponds to one class label—in this case, healthy loans substantially outnumber non-healthy loans.
*  As evident from the information provided below, the data exhibits a substantial imbalance.
![pic1]("C:\Users\bella\Desktop\credit-risk-classification\Credit_Risk\images\image 1.png")
*  In order to boost accuracy and augment the model's capability to categorize non-healthy loans effectively, we can employ the RandomOverSampler module from the imbalanced-learn library. This approach entails introducing additional instances of the minority class (non-healthy loans) to establish a more balanced dataset. The resulting oversampled data would be:
![pic2]("C:\Users\bella\Desktop\credit-risk-classification\Credit_Risk\images\image 2.png")

## The results:
------------------------------------------------------------------------------
## Machine Learning Model 1:

Model 1 Evaluation Metrics Overview:
Compared to the initial dataset, there is a higher count of healthy loans than unhealthy loans. The model exhibits a commendable overall accuracy of 99%, with a precision score of 100% for class 0 (representing healthy loans) and a respectable 85% precision for class 1 (indicating unhealthy loans). Moreover, the recall scores are notably strong, reaching 99% for predictions associated with class 0 and 91% for identifying high-risk loans labeled as class 1.
## Machine Learning Model 2:
Description of Model 2 Accuracy, Precision, and Recall Scores:

The accuracy score for this model is similarly impressive, standing at 99%. Upon reviewing the confusion matrix, it becomes evident that the oversampled data model excelled in predicting false negatives, with only 4 loans of type 0 being misclassified. Much like the preceding model, the precision score for type 0 loans remained at 100%, and for type 1 loans, it was 84%. Notably, the recall score improved for high-risk loans compared to the previous model.

## A summary:
-----------------------------------------------------------------------------
A lending institution aims to deploy a model that accurately distinguishes between healthy and non-healthy loans to mitigate potential costs. Misclassifying healthy loans as non-healthy may lead to customer loss, while misclassifying non-healthy loans as healthy can result in financial losses for the company.

The Logistic Regression model trained with oversampled data outperformed the model trained with imbalanced data. The approach of utilizing a balanced dataset contributed to enhanced accuracy and recall, thereby reducing errors in classifying non-healthy loans.

To mitigate risks, the lending company prioritizes minimizing false positives, where non-healthy loans are erroneously classified as healthy. Examining the confusion matrices:

Machine Learning Model 1 with imbalanced data:

56 false positives (actual value: healthy, predicted value: non-healthy)
102 false negatives (actual value: non-healthy, predicted value: healthy)
Machine Learning Model 2 with balanced data:

4 false positives (actual value: healthy, predicted value: non-healthy)
116 false negatives (actual value: non-healthy, predicted value: healthy)

Based on these outcomes, the model with balanced data is recommended as it significantly reduces false positives and enhances accuracy in classifying healthy and non-healthy loans.




