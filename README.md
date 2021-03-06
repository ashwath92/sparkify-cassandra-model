## Sparkify Cassandra Data Model

The purpose of this project is to create a suitable Apache Cassabndra data model which can be used to analyse user behaviour based on data in song play logs of a music streaming service.

### Requirements
Python 3.6 +
Apache Cassandra
Cassandra python package
Jupyter/Ipython

### Description of Data set
The data set used for this project is event data from a music streaming service. This data is availble in the form of a directory of CSV files partitioned by date. Here are examples of filepaths to two files in the dataset:

**event_data/2018-11-08-events.csv**
**event_data/2018-11-09-events.csv**

The data from the individual files in the event_data are combined and denormalised into a new consolidated csv file called event_data_new.csv. This file is used to insert data into our Apache Cassandra tables.

### Queries

The requirement is to create queries to ask the following three questions of the data
1. Give me the artist, song title and song's length in the music app history that was heard during sessionId = 338, and itemInSession = 4
2. Give me only the following: name of artist, song (sorted by itemInSession) and user (first and last name) for userid = 10, sessionid = 182
3. Give me every user name (first and last) in my music app history who listened to the song 'All Hands Against His Own'

### Description of files in repository

#### Ipython notebooks:
The Project_1B_Project_Template.ipynb notebook contains all of the queries and processing steps.

For each of the questions under 'Queries', a separate Apache Cassandra table is created with the required columns and primary keys (these are explained in the notebook). Data from the denormalised CSV file are inserted into the respective tables. This is followed by SELECT queries which directly answer the questions. Finally, the notebook ends with the required drop table statements.

#### events_data directory
This directory contains the input log data

#### event_datafile_new.csv
A denormalised version of the data in the events_data directory.

### Execution
Run the cells of Project_1B_Project_Template.ipynb in order. 
