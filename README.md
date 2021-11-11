# Disaster Response Pipeline Project

## Table of Contents

1. [Project Motivation](#motivation)
2. [Project Description](#description)
3. [Data Preview](#data)
4. [Instructions](#instructions)


## Project Motivation<a name = 'motivation'></a>
This project is trying to automate the message classification process by ETL and machine learning pipeline. Using the real messages that were sent during disaster events, this web app will categorize these events and then send the messages to an appropriate disaster relief agency. 

## Project Description<a name='description'></a>
This disaster response pipeline used ETL, NLP and Machine learning pipeline to build a model based on 26207 messages, and then built a multi-classification model. After the model is built. we will deploy a web app to classify messages and also prioritize messages. 


## Data Preview<a name='data'></a>

The message data recorded 26207 messages, which is grouped in three genre: direct, social and news. The news genre is the biggest group, followed ba direct genre, and the genre of social is the least. 

![image](https://user-images.githubusercontent.com/26633604/141354670-9bc9bb39-debd-431a-9b91-876be78550cc.png)

After cleaned all the messages, we identified 36 categories, and the count of different categories is shown in the picture. "related", "aid related" and 'weather realted" are the three biggest groups, which accounts for 46% of all categories. 

![image](https://user-images.githubusercontent.com/26633604/141355598-ca33aca8-2f61-4b44-a7fb-97f79cb68b3a.png)

## Instructions<a name='instructions'></a>:
1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

2. Run the following command in the app's directory to run your web app.
    `python run.py`

3. Go to http://0.0.0.0:3001/
