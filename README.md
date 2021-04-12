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

### Database
- Database used
    - PostgresSQL
    - AWS for cloud storage
- Description of Database
    - Joins Used: FULL OUTER JOIN
    - Primary key used: VAERS_ID

### Machine Learning Algorithm 

- ML used:
    - Logistic Regression
    - Single Deep Neural Networks

- Description of preliminary data preprocessing
    - Dropped the columns 
    - Merged the dataframe into one and exported the csv

- Description of preliminary feature engineering and preliminary feature selection 
    - Changed dates (objects)columns to datetime
    - Determined uniques values in each column 
    - Determined the value counts of the columns needed 
    - Dropped the columns which were could not be `hot encoded`

- Description of how data was split into training and testing sets
    - Split and scale data
        - split data into features and targets 

- Explanation of Model choice including Limitation and Benefits
    - Logistic Regression
        - Advantages:

            `Logistic Regression` is typically used to predict binary outcomes, meaning that there are only two possible outcomes. The model analyzes the available data, and when presented with a new sample, mathematically determines its probability of belonging to a class. If the probability is above a certain cutoff point, the sample is assigned to that class. If the probability is less than the cutoff point, the sample is assigned to the other class. For example determining if a person will vote "Yes" or "No" on an issues based on things like income, location, and family size.

    - Challenges:
        - Logisitc Regression, Single and deep Neural Networks, used with the dataframe at the time (with lots of features) were too prone to overfitting
        - We are now experimenting with cleaning more the data and trying also unsupervised ML to correct this problem.



    - Neural Networks
        - Advantages:

            `Neural Networks` are advanced form of machine learning that recognizes patterns and features in input data and provides a clear quantitative output. They can create a classification algorithm that determines if an input belongs in one category versus another. Therefore, neural network models can be an alternative to many of the models we have learned throughout the course, such as, logistic regression, or multiple linear regression.

## Steps for pre-processing data ('database/preprocessing' branch, merged with Development);

1. Firstly, three csv datasets were retreived from the VAERS webpage (Resources). These three files were read into dataframes using pandas and Jupyter notebook. The patient symptom csv, and vaccine csv were merged together. Two fies were exported, one csv containing VAERS vaccine patient information, and the other containing
details about symptoms experienced and vaccines administered (VAERS_DATA_T1, and VAERS_DATA_T2). See 2021VAERS_FINALPROJECT_ERD.png. 

2. These two csv files were then replicated in pgadmin as tables (SQL queries used are included in our branch). Once two tables were created the csv files were then 
imported using SQL queries. Before the importing process was complete, several rows were manually removed from each csv as they produced an error due to the specified quatation character import setting. Once the data had been successfully imported into each table, they were merged on the common key, VAERS_ID. Once successfully merged, the index was dropped and a final, cleaned csv (vaers_data_cleaned) was exported for use in the machine learning analysis. 

#### Link to Google Slides:

(https://docs.google.com/presentation/d/1AURmMfk4XuFyFQcLU9xwtiExaIyWukNlSQ7n1PLqNVw/edit?skip_itp2_check=true&pli=1#slide=id.gce3735f4c5_0_0) [link]

#### Dashboard Link:
(https://public.tableau.com/profile/gurnoor8216#!/vizhome/Dashboard1_16180058448220/Dashboard1) [Link]