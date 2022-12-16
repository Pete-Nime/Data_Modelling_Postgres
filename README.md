# Data_Modelling_Postgres
Transform Sparkify heterogenous database into homogenous for the final query 

# Abstract 
Sparkigy (imiginary music app)  analyst wants to know the user activity on the number of the songs they have listen too. The songs file comes in the form of JSON logs and JSON metadata. They'd like a data engineer to create a Postgres database with tables designed to optimize queries on song play analysis, and bring you on the project. So that the Sparkify analytical team can query the structure data based on their objectives. 

# Facts & Dimensional Table
![QuickDBD-Free Diagram](https://user-images.githubusercontent.com/103359089/206372875-0e99bcd1-f9d9-449d-b2c2-cadae69cf818.png)

# Tools Employed in the project
Jupyterlalb

Postgres on the local PC host

Standard Query Language (SQL)
Python
 - psycopg2 (mainly involved running PostgreSQL )


# Resources Employed in the project
song Data Set
song_data/A/B/C/TRABCEI128F424C983.json
song_data/A/A/B/TRAABJL12903CDCF1A.json

Log Dataset
log_data/2018/11/2018-11-12-events.json
log_data/2018/11/2018-11-13-events.json

# Project Template
test.ipynb displays the first few rows of each table to check the database.
create_tables.py drops and creates your tables. Run this file to reset the tables before each time when running the ETL scripts.

etl.ipynb reads and processes a single file from song_data and log_data and loads the data into the tables. This notebook contains detailed instructions on the ETL process for each of the tables.

etl.py reads and processes files from song_data and log_data and loads them into the tables. Fill this out based on the work in the ETL notebook.

sql_queries.py contains all the facts and dimensions queries, and is imported into the last three files above.

# Execution Process
-Run python3 create_tables.py on the terminal 

-Run etl.py on the terminal to load data onto the staging table after running create_tables.py

-Run test.ipynb to see if the song file uploaded successfully on to the table. After running it, 
disconnect it so that create_tables.py, etl.py, etl.ipnb cand access the Sparkify database on Postgres. If not it will casue conflict. 

-Run etl.ipnb to process the entire dataset. 

-sql_queries.py specify all columns for each of the five tables with the right data types and conditions.
