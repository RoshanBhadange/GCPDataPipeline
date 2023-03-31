# GCPDataPipeline
 Problem statement
 To create  an end-to-end data pipeline that analyses the viewershipdata and helps the company comprehendthe user behaviorbetter
 
 Business Benefits:
 Based on the above analysis,the video on demand company will create a new business strategy to acquireand engagemore users, send offers/promotions to users,andreward video creatorswhose content garners high viewership
 
# Data Ingestion:

ingest the data for video_plays.xml and video_plays.csv files into HDFS

# Data Pre-Processing:
 Perform data  cleaning  steps  like  empty  string  replacements  with  actual  NULL,  data  type checks (including date format) and corrections/rejections, file name checks, empty file checks, malformed record checks,and rejection,etc on both the batch and streaming data
 
Create Lookup tables in any SQL/NoSQL database for the datasets video-creator.csv, user-subscn.csv, channel-geocd.csv, user-creator.csv 

# Data Enrichment:
Used the following considerations during data enrichment
✓If any value of like or dislike is NULL or absent, consider it as 0
✓If fields like Geo_cd and creator_id are NULL or absent, consult the lookup tables for fields Channel_id and Video_id respectively to get the values of Geo_cd and creator _id
✓If corresponding lookup entry is not found, consider therecord of beinginvalid


# Spark Batch Job:
This batch job will transorm and load the data into respective target table

# Real time Streaming Job:
This Job will load the data into Kafka topics
