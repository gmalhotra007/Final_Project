# Final Project

## Overview:
---

### Selected Topic
- Covid-19 vaccination in the US
    - US adverse reactions to vaccines in 2021
    - `DataSet`: Vaccine Adverse Event Reporting System (VAERS) website

### Reason of the selected topic
- Factors that have inspired our group to study this data and discover the real effects and implications of vaccines:
    - The global pandemic has entered a new stage through many countries receiving vaccines, and populations promptly vaccinating on a large scale. 
    - Recently, in March there has been controversial news surrounding the effects of these Covid vaccines, namely the AstroZenica vaccine in Europe.

### Description of source of data
- Source data includes three CSV files containing information from individuals in the USA who file with the VAERS and report  adverse effects after receiving  a licensed vaccine. 
    - These CSV files contains the information regarding the individual, the symptoms experienced, and the vaccine taken.
    - The files contain data from 2021 `from Jan 1st until March 13th`.

### Questions to answer by analyzing data 
- What characteristics do individuals share? 
- Who experience adverse reactions that result in death?
- Is there any correlation between our features and an adverse reaction/death?
- Are any groups more susceptible to experience an adverse reaction or death as a result of a Covid vaccination?

### Description of the Communication Protocols
- Using Slack 
    - created group including TA
- Daily updates on:
    - What are you working on next?
    - How much is covered?
    - If anyone is blocked or not blocked

### Exploratory Data Analysis 
- Technologies used for pre-processing
    - Python Pandas 
    - Jupyter Notebook
- anomalies encountered with the data
- Solution 

### Database
- Database used
    - PostgresSQL
    - AWS for cloud storage
- Description of Database
    - Joins Used: FULL OUTER JOIN
    - Primary key used: VAERS_ID

### Machine Learning Algorithm 
- Logistic Regression and Neural Networks

#### Logistic Regression
- Advantages:

     `Logistic Regression` is typically used to predict binary outcomes, meaning that there are only two possible outcomes. The model analyzes the available data, and when presented with a new sample, mathematically determines its probability of belonging to a class. If the probability is above a certain cutoff point, the sample is assigned to that class. If the probability is less than the cutoff point, the sample is assigned to the other class. For example determining if a person will vote "Yes" or "No" on an issues based on things like income, location, and family size.
- Limitation
- Accuracy 
- Challenges
- Solutions 

#### Neural Networks
- Advantages:

`Neural Networks` are advanced form of machine learning that recognizes patterns and features in input data and provides a clear quantitative output. They can create a classification algorithm that determines if an input belongs in one category versus another. Therefore, neural network models can be an alternative to many of the models we have learned throughout the course, such as, logistic regression, or multiple linear regression.

#### Summarization of Data Pipeline 