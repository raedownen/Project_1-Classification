# Project_1-Classification
project description with goals
Churn Category: A high-level category for the customer’s reason for churning: Attitude, Competitor, Dissatisfaction, Other, Price. When they leave the company, all customers are asked about their reasons for leaving. Directly related to Churn Reason.



PLANNING

Project Description:  Using data acquired from CodeUp’s database, Telco Churn.Working through the data science pipeline, I will try find if the various elements have anything to do with whether a customer stop being a customer.

Project Goal: Navigate the data science pipeline.  Ask questions to see if whether a customer churns. Using the data to answer the questions.

Initial Thoughts: My initial hypothesis is that one of the 4 variables will be an indicator of churn.  It is just a matter of completing the manipulation of data.

Planning
Business stakeholders and end users often ask more general questions that are very hard to answer directly or extremely specific questions that are not going to achieve their underlying goal. This leads to miscommunication, time spent on work that is ultimately thrown away, or inadequate understanding of the underlying problem being investigated. As you gain experience with the data and domain, you gain a better understanding of problems and can ask more informative & specialized questions. Even then, however, it is important to work through this planning stage, as it is all too easy to get lost down a rabbit hole when working on a data science project.

The goal of this stage is to clearly define your goal(s), measures of success, and plans on how to achieve that.

The deliverable is documentation of your goal, your measure of success, and how you plan on getting there. If you haven't clearly defined success, you will not know when you have achieved it.

How to get there: You can get there by answering questions about the final product & formulating or identifying any initial hypotheses (from you or others).

Common questions include:

What will the end product look like?
What format will it be in?
Who will it be delivered to?
How will it be used?
How will I know I'm done?
What is my MVP?
How will I know it's good enough?
Formulating hypotheses

Is attribute V1 related to attribute V2?
Is the mean of target variable Y for subset A significantly different from that of subset B?
...




DATA ACQUISITION
Acquire
I retrieved my data from the Codeup databases using my acquire.py file
I retrieved my data on Tuesday, October 25, 2022
What is the size of your data? (columns and rows)
What does each observation represent?
What does each column represent?

Acquisition
AKA Data Gathering, Data Import, Data Wrangling (Acquisition + Prep)

The goal is to create a path from original data sources to the environment in which you will work with the data. You will gather data from sources in order to prepare and clean it in the next step. Many data scientists agree that this stage, along with the preparation stage, is where you will spend approximately 70-80% of your time.

The deliverable is a file, acquire.py, that contains the function(s) needed to reproduce the acquisition of data.

How to get there:

If the data source is SQL, you may need to do some clean-up, integration, aggregation or other manipulation of data in the SQL environment before reading the data into your python environment.
Using the Python library pandas, acquire the data into a dataframe using a function that reads from your source type, such as pandas.read_csv for acquiring data from a csv.
You may use Spark and/or Hive when acquiring data from a distributed environment, such as HDFS.
Examples of source types include RDBMS, NoSQL, HDFS, Cloud Files (S3, google drive), static local flat files (csv, txt, xlsx).

DATA PREP
Preparation
AKA Data Tidying, Data Cleansing, Data Wrangling (Aquisition + Prep)

The goal is to have data, split into 3 samples (train, validate, and test), in a format that can easily be explored, analyzed and visualized. The data is split so that we have a sample we can use to test our final model, one that was not used in the exploration of the data or the development of the model. This helps us understand the generality of the model.

The deliverable is a file, prep.py, that contains the function(s) needed to reproduce the preparation of the data. The resulting dataframes should be 3 samples, a dataframe for training the algorithms, a dataframe for validating the models developed on unseen data, a dataframe for testing the best performing model to ensure the model is able to be generalized on a final set of unseen data not 'overfitting' train, a validate and a test, roughly a 70%:20%:10% split (or somewhere between that and 50%:30%:20% ... depends on amount of data available).

The train dataset is for training our models. We also perform our exploratory data analysis on train.
The validate dataset serves two purposes. First, it is an "out of sample" dataset so that we can evaluate our models on unseen data to measure how well the model generalizes. Second, the validate set allows us to fine tune our hyperparameters.
The test dataset is our final out of sample dataset used to evaluate how well the models tuned on validate generalize on unseen data.
How to get there:

Python libraries: pandas, matplotlib, seaborn, scikit-learn.
Use pandas to perform tasks such as handling null values, outliers, normalizing text, binning of data, changing data types, etc.
Use matplotlib or seaborn to plot distributions of numeric attributes and target.
Use scikit-learn to split the data into train and test samples.

DATA EXPLORATION AND PRE-PROCESSING
Exploration and Pre-processing
AKA Exploratory Analysis/visualization, Feature Engineering, Feature Selection

The goal is to discover features that have the largest impact on the target variable, i.e. provide the most information gain, drive the outcome.

The deliverable is a file, preprocess.py, that contains the function(s) needed to reproduce the pre-processing of the data. The dataframe resulting from these functions should be one that is pre-processed, i.e. ready to be used in modeling. This means that attributes are reduced to features, features are in a numeric form, there are no missing values, and continuous and/or ordered values are scaled to be unitless.

How to get there:

Use python libraries: pandas, statsmodels, scipy, numpy, matplotlib, seaborn, scikit-learn.
Perform statistical testing to understand correlations, significant differences in variables, variable interdependencies, etc.
Create visualizations that demonstrate relationships across and within attributes and target.
Use domain knowledge and/or information gained through exploration to construct new features.
Remove features that are noisy, provide no valuable or new information, or are redundant.
Use scikit-learn's preprocessing algorithms (feature selection, feature engineering, dummy variables, binning, clustering, e.g.) to turn attributes into features.

Standing Orders for Exploration

Document your initial questions or assumptions. Write them down (in your README or notebook) so they are concrete and not in your head.

Document your takeaways after each visualization. Even if your takeaway is, "there is nothing interesting between var1 and target".

Document your answer to each question.

When you run statistical tests to answer your questions, Document your null and alternative hypothesis, the test you run, the test results, and your conclusion.

Document your takeaways, in case that wasn't clear. It is a huge component of your final deliverable/analysis.

Document your action plan. What are your next steps and/or new questions based on what you have learned? I recommend documenting, continuing through all of your questions, and then going back and taking action only after you have answered your initial questions.



FEATURE ENGINEERING
MODELING
Modeling
The goal is to create a robust and generalizable model that is a mapping between features and a target outcome.

The deliverable is a file, model.py, that contains functions for training the model (fit), predicting the target on new data, and evaluating results.

How to get there:

Python libraries: scikit-learn
Identify regression, classification, cross validataion, and/or other algorithms that are most appropriate.
Build your model:
Create the model object.
Fit the model to your training, or in-sample, observations.
Predict the target value on your training observations.
Evaluate results on the in-sample predictions.
Repeat as necessary with other algorithms or hyperparameters.
Using the best performing model, predict on test, out-of-sample, observations.
Evaluate results on the out-of-sample predictions.

TESTING
DELIVERYCONCLUSION
Delivery
The goal is to enable others to use what you have learned or developed through all the previous stages.

The deliverable could be of various types:

A pipeline.py file that takes new observations from acquisition to prediction using the previously built functions.
A fully deployed model.
A reproducible report and/or presentation with recommendations of actions to take based on original project goals.
Predictions made on a specific set of observations.
A dashboard for observing/monitoring the key drivers, or features, of the target variable.
How to get there:

Python sklearn's pipeline method.
Tableau for creating a report, presentation, story, or dashboard.
Jupyter notebook for creating a report or a framework to reproduce your research, e.g.
Flask to build a web server that provides a gateway to our model's predictions.
Questions to explore:
Is there a relationship between contract type and churn?
Are those with higher monthly charges more likely to churn?
Is there a point in the tenure that most customers do not get past?
Does gender play a role in churn?

instructions or an explanation of how someone else can reproduce your project and findings (What would someone need to be able to recreate your project on their own?)

key findings, recommendations, and takeaways from your project.