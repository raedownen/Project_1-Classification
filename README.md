# Project_1-Classification
PLANNING

Project Description:  Using data acquired from CodeUp’s database, Telco Churn.Working through the data science pipeline, I will try find if the various elements have anything to do with whether a customer stop being a customer.

Project Goal: Navigate the data science pipeline.  Ask questions to see if whether a customer churns. Using the data to answer the questions.

Initial Thoughts: My initial hypothesis is that one of the 4 variables will be an indicator of churn.  It is just a matter of completing the manipulation of data.

DATA ACQUISITION
Acquire
I retrieved my data from the Codeup databases using my acquire.py file
I retrieved my data on Tuesday, October 25, 2022

Preparation
Data Preparation-
Using the telco_wrangle file, the data was prepared by correcting data types the data types, column names, and size. Object categories were encoded to binary. Outliers were not a concern since the data I was looking at was not continuous.

Data Splitting-
The telco wrangle file was also used to split the data. The data was first split into an 80% train (and validate) and 20% test. Then the 80% was again split, so that 56% was train data and 24% was the validate data.


DATA EXPLORATION AND PRE-PROCESSING
More than a quarter of the Telco customers churn. I ask the following questions and will use tests used in data science scenarios to determine if one of the four factors contributes more than the others to the customer churn percentage.


The 4 questions I examined were:
Does having tech support affect customer churn rates?
Does payment type affect customer churn rates?
Does being a senior citizen affect customer churn rates?
Does contract type affect customer churn rates?




TESTING
Chi Squared for all 4 questions and used decision trees on
the test data for tech support and its effect on churn, which returned 80% accuracy.

CONCLUSION
Summary
Having Tech Support would probably lower churn rates with senior citizens and may help retain month-to-month contract types.¶
I would like to further evaluate why electronic checks have such a high churn rate.
Recommendations
Offer Tech Support to all customers because it is vital to all customers as it is indicative of good customer service.