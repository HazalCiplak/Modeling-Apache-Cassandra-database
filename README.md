# Modeling Apache Cassandra database

##### (Udacity Data Engineer Nano Degree Project 2)
---------------



**Introduction**

This Udacity Data Engineering nanodegree project creates an Apache Cassandra database for a music app, Sparkify. 



**The Goal**

The purpose of this project is, data modeling with Apache Cassandra. The data model includes a table for each of the following queries:

 - Give me the artist, song title and song's length in the music app history that was heard during sessionId = 338, and itemInSession = 4

 - Give me only the following: name of artist, song (sorted by itemInSession) and user (first and last name) for userid = 10, sessionid = 182

 - Give me every user name (first and last) in my music app history who listened to the song 'All Hands Against His Own'


**Database Source**

Source files are :
 - event_data/2018-11-08-events.csv
 - event_data/2018-11-09-events.csv

From these files  a denormalized dataset has been created:

 - event_datafile_new.csv

event_datafile_new.csv contains the following columns:

1. artist
2. firstName of user
3. gender of user
4. item number in session
5. last name of user
6. length of the song
7. level (paid or free song)
8. location of the user
9. sessionId
10. song title
11. userId


**Data Pipeline** 

1. Start with the raw csv data files as described in Dataset
2. For each row of the csv data, insert the data in the appropriate column.
3. Perform the Select query as described queries below

* select artist, song_title, song_length from song_list_by_sessionId WHERE sessionId=338 AND itemInSession=4
* select artist, song_title, user_firstname, user_lastname from artist_by_userId_and_sessionId WHERE userId=10 AND sessionId=182
* select user_firstname, user_lastname from user_by_song WHERE song_title='All Hands Against His Own' 


**To run the program**

Run each portion of Project_1B_Project_Template.ipynb.

-----

Hazal Ciplak