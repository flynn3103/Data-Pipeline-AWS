# Music Data Pipeline Projects

<img src="https://miro.medium.com/max/1400/1*zHsRLXWzeNYHtanEDeY3YQ.jpeg">

## Business understanding
We assume that user of Sparkify can be either Premium or Free Tier subscription, The premium plan with subscription fee and enjoy more songs without advertisements.
As an end user, he/she can do:

* Upgrade from free tier to Premium subscription
* Downgrade from Premium to free tier
* Drop their account and leave the service

The goals are:

* Analyse data
* Extract insights to identify churn indicators
* Build machine learning model to help predict potential churn ones
## Dataset
This is a public dataset named Million Song Dataset and can be download under json from <a href="http://millionsongdataset.com/">here</a> 
* Contains 18 columns which has the information of customers(gender, name, etc.) and API events(login, playing next song, etc.)
* Experiment period: 2018–10–01 to 2018–12–01
>
    {
        "ts":1543621857000,
        "userId":"300011",
        "sessionId":500,
        "page":"NextSong",
        "auth":"Logged In",
        "method":"PUT",
        "status":200,
        "level":"paid",
        "itemInSession":37,
        "location":"New York-Newark-Jersey City,NY-NJ-PA",
        "userAgent":"Mozilla/5.0 (compatible; MSIE 9.0; Windows NT 6.1; WOW64; Trident/5.0)",
        "lastName":"House",
        "firstName":"Emilia",
        "registration":1538336771000,
        "gender":"F",
        "artist":"Olive",
        "song":"You\\'re Not Alone",
        "length":264.12363
    }
>

## Task Summary
1. Write Dockerfile for set up enviroment using **Spark, Hadoop, Postgres, Airflow**, etc
2. Design data warehouse & build ETL Pipeline :
    * from raw json data into *PostgreSQL* locally for testing
    * from *S3 Storage* into *AWS Redshift* 
    * from *S3 Storage* into *AWS EMR* 
3. Streamming data for analyzing data using Kafka
4. Extract insights from data using PySpark
5. Predict churn rate on Sparkify services
