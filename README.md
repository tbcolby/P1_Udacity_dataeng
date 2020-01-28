# Udacity Data Engineering Project 1: Data Modeling with Postgres

Project Goals:
- Proper Table Creation, Properly Defined Star Schema including Fact and Dimensional Tables 
- ETL: Script Runs without errors, Properly Processes Data in Python 
- Well Documented Code, Clean and Modular
- Extra: Use COPY instead of INSERT to bulk insert LOG files
- Extra: Data Quality Checks
- Extra: Create a Dashboard for Analytic Queries on the new database

## Project Introduction

A startup called Sparkify wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. The analytics team is particularly interested in understanding what songs users are listening to. Currently, they don't have an easy way to query their data, which resides in a directory of JSON logs on user activity on the app, as well as a directory with JSON metadata on the songs in their app.

They'd like a data engineer to create a Postgres database with tables designed to optimize queries on song play analysis, and bring you on the project. Your role is to create a database schema and ETL pipeline for this analysis. You'll be able to test your database and ETL pipeline by running queries given to you by the analytics team from Sparkify and compare your results with their expected results.

## Data
### Song Datasets
Datasets provided by the Million Song Dataset: http://millionsongdataset.com/

**Data citation:**
  *Thierry Bertin-Mahieux, Daniel P.W. Ellis, Brian Whitman, and Paul Lamere. 
  The Million Song Dataset. In Proceedings of the 12th International Society
  for Music Information Retrieval Conference (ISMIR 2011), 2011.*

## Song Dimension Tables

**Songs**
|---|---|---|
| song_id   | TEXT PRIMARY KEY |      |
| title     | TEXT NOT NULL    |      |
| artist_id | TEXT NOT NULL    |      |
| year      | INT              |      |
| duration  | FLOAT NOT NULL   |      |

**Artists**
|---|---|---|
| artist_id | TEXT PRIMARY KEY |                                          |
| name      | TEXT NOT NULL    |                                          |
| location  | TEXT             |                                          |
| latitude  | FLOAT            | Consider PostGIS for future enhancements |
| longitude | FLOAT            | Consider PostGIS for future enhancements |


## Log Datasets
Datasets generated via Eventsim: https://github.com/Interana/eventsim



