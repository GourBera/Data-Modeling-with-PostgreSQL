# **Data Modeling with PostgreSQL**
Udacity Data Engineering Nanodegree


### **Introduction**
A startup called Sparkify wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. The analytics team is particularly interested in understanding what songs users are listening to. Currently, they don't have an easy way to query their data, which resides in a directory of JSON logs on user activity on the app, as well as a directory with JSON metadata on the songs in their app.


>They'd like to implement OLAP using Postgres database with tables designed to optimize queries on song play analysis. 
>> -	Data modelling with Postgres
>> -	Designing Database schema | fact and dimension tables for a star schema 
>> -	Building ETL pipeline using Python




### **Project Datasets**

> **Song Dataset**

The first dataset is a subset of real data from the Million Song Dataset. Each file is in JSON format and contains metadata about a song and the artist of that song. 


>> {"num_songs": 1, "artist_id": "ARJIE2Y1187B994AB7", "artist_latitude": null, "artist_longitude": null, "artist_location": "", "artist_name": "Line Renaud", "song_id": "SOUPIRU12A6D4FA1E1", "title": "Der Kleine Dompfaff", "duration": 152.92036, "year": 0}


> **Log Dataset**

The second dataset consists of log files in JSON format generated by this event simulator based on the songs in the dataset above. These simulate activity logs from a music streaming app based on specified configurations, partitioned by year and month...
 



### **Schema for Song Play Analysis**

#### **Fact Table**

> **songplays** - records in log data associated with song plays i.e. records with page NextSong
>> - songplay_id
>> - start_time
>> - user_id
>> - level
>> - song_id
>> - artist_id
>> - session_id
>> - location
>> - user_agent


#### **Dimension Tables**

> **users - users in the app**
>> - user_id
>> - first_name
>> - last_name
>> - gender
>> - level

> **songs** - songs in music database
>> - song_id
>> - title
>> - artist_id
>> - year
>> - duration

> **artists** - artists in music database
>> - artist_id
>> - name
>> - location
>> - latitude
>> - longitude

> **time** - timestamps of records in songplays broken down into specific units
>> - start_time
>> - hour
>> - day
>> - week
>> - month
>> - year
>> - weekday



### **END-T0-END Execution Process**

> Steps to be followed as mension bellow:
>> 1. Execute: sql_queries.py | Verify no ERROR
>> 2. Execute: create_tables.py | Verify no ERROR
>> 3. Execute: etl.py | Verify no ERROR
>> 4. Execute: test.ipynb | Verify data has been loded successfully


