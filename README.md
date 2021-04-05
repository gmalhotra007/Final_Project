# Final_Project
## Steps for pre-processing data (located on 'database/preprocessing' branch, merged with Development;

1. Firstly, three csv datasets were retreived from the VAERS webpage. These three files were read into a dataframe using pandas and Jupyter notebook. Of these three
csv files two were merged together, and a final two were exported as csv files, leaving us with one csv containing VAERS vaccine patient information, and the other containing
details about symptoms experienced and vaccines administered (VAERS_DATA_T1, and VAERS_DATA_T2). See 2021VAERS_FINALPROJECT_ERD.png for more details. 

2. These two csv files were then replicated in pgadmin as tables (SQL queries used are included in our branch). Once two matching tables were created the csv files were then 
imported using SQL queries. Before the importing process could complete, several rows were manually removed from each csv as they did not meet the... . Once the data had been
successfully imported into each table, they were merged on the common key, VAERS_ID. Once successfully merged, the index was dropped and a final, cleaned csv (vaers_data_cleaned) was exported for use in machine learning analysis. 
