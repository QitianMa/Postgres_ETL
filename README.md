## Project Discription
 A startup called Sparkify wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. The analytics team is particularly interested in understanding what songs users are listening to. Currently, they don't have an easy way to query their data, which resides in a directory of JSON logs on user activity on the app, as well as a directory with JSON metadata on the songs in their app.

## ETL Pipeline
Here I apply a star scheme with 1 fact table: sontplay_table and 4 dimension tables: user_table, song_table, artist_table and time_table. First I constract dimension tables and then construct fact table by the information of the 4 dimension tables.

## Data Model Schema
Fact Table:
songplay_table

songplay_id SERIAL PRIMARY KEY,
start_time bigint, 
user_id varchar, 
level varchar, 
song_id varchar,
artist_id varchar,
session_id varchar,
location varchar, 
user_agent varchar 

Dimension Table 1
user_table

user_id varchar,
first_name varchar,
last_name varchar,
gender varchar,
level varchar

Dimension Table 2
song_table

song_id varchar,
title varchar,
artist_id varchar,
year int,
duration real

Dimension Table 3
artist_table

artist_id varchar,
name varchar,
location varchar,
latitude real,
longitude real

Dimension Table 4
time_table

start_time bigint,
hour int,
day int,
week int,
month int,
year int, 
weekday int

## How to run scripts
1. python create_tables.py
2. python etl.py
=======
# Postgres_ETL
>>>>>>> ef220ae5b64d1cfc6f35300213afe4dc8f0699a4
