### Technical documentation for Vaccine Adverse Reactions Analysis:

## Dataset - 

Vaccine Adverse Event Reporting System (VAERS) [dataset].(https://vaers.hhs.gov/data/datasets.html?)

## Database - Postgres SQL and AWS

Postgres SQL is implemented to store, organise and query data. Working with a large dataset and evolving data volume, Postgres seemed to be a great fit for organising project data.

AWS is also implemeted for cloud storage so data can be used and shared with current team members and future collaborators in a seamless and secure manner.


## Python Pandas and Jupyter Notebook 

Python pandas is a versatile and lightweight tool with a wide array of inbuilt functions for data pre-processing and cleaning that fit the project needs perfectly in processing project csv files, as well as other formats of data.
The files formats can also be easily changed back and forth to fit storage and analysis needs.

Jupyter Notebook is a popular data analytics playground where different programming environments can be set up and worked on concurrently with ease. 
This fits the project needs well as there are several machine learning models and SQL operations used, which need a variety of package installs in the same environment.

## Data cleaning techniques

The datasets were merged using Pandas merge method. As it is often needed in data cleaning, several columns which did not add value the end analysis or could have potentially skewed model predictions were dropped. 

The Panda dataframes in ready condition to be fed into the models for traiining, fitting and predicting, were loaded to PgAdmin.

This process would allow different team members, and future contributors to setup a local database of the project. The query editor of PgAdmin can be further used to query the data and further analyse or contribute to the existing database.

## Logistic Regression and Neural Networks

Lastly, to bring all the data together and answer the questions set out on the project planning stage; Logistic regression and Neural Networks are implemented to predict outcomes.
The outcomes are predicted based on the data used to train and fit the model.
