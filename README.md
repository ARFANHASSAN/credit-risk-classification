# credit-risk-classification
Module-20-challenge


In this challenge, you will employ diverse techniques to train and assess a model focused on loan risk. Utilizing a dataset comprising historical lending transactions from a peer-to-peer lending services company, your task is to construct a model capable of discerning the creditworthiness of borrowers.
## Instructions:
The guidelines for this Challenge are categorized into the following subparts:

* Divide the Data into Training and Testing Sets

* Develop a Logistic Regression Model using the Original Data

* Generate a Credit Risk Analysis Report
## Split the Data into Training and Testing Sets:
Open the provided starter code notebook and follow these steps:

* Import the "lending_data.csv" data from the Resources folder into a Pandas DataFrame.

* Formulate the labels set (y) based on the “loan_status” column, and subsequently, construct the features (X) DataFrame using the remaining columns.

* Note that a value of 0 in the “loan_status” column signifies a healthy loan, while a value of 1 indicates a high risk of default.

* Segregate the data into training and testing datasets by employing the train_test_split method.
## Create a Logistic Regression Model with the Original Data:
Apply your understanding of logistic regression to carry out the following tasks:

* Train a logistic regression model using the provided training data (X_train and y_train).

* Utilize the fitted model to predict the labels for the testing data by employing the testing feature data (X_test).

* Assess the model's performance through the following steps:

* Create a confusion matrix.
* Display the classification report.
* Address the following question: To what extent does the logistic regression model effectively predict both the 0 (healthy loan) and 1 (high-risk loan) labels?
## Write a Credit Risk Analysis Report:
Compose a concise report detailing a summary and analysis of the performance of the machine learning models employed in this assignment. Draft this report as the README.md file within your GitHub repository.

Follow the structure outlined in the report template provided in the Starter_Code.zip, ensuring the inclusion of the following components:

Overview of the Analysis:
Explain the purpose and objective of conducting this analysis.

Results:
Present the outcomes using a bulleted list, encompassing the accuracy score, precision score, and recall score of the machine learning model.

Summary:
Provide a condensed recap of the machine learning model results. Justify your recommendation for or against the adoption of the model by the company. If you opt not to recommend the model, clarify the reasoning behind your decision.