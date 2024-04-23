# Data-Engineer-Project
The Project I have done when Participated in Data Engineer Course From AI4E. 

## Introduction
* **Data is key to many human activities such as: bank, stock, social media, .... Actually, it should be called "BIG DATA". The problem is, how can we transport, transfer data from raw to the data we can use, just like the way me make delicious foods from raw ingredients. That's why we need data pipeline system for Storing, Transforming, Transporting, Extracting,... data.**
* **In this project, we will build a data pipeline for banking transaction, from Raw to "Cooked" data**

## Problem statement
### Data for Banking
Everyday, hour, minute, second, people use bank for sending, receiving money, called transaction

Transaction usually include:
* Date / Time
* User's information: ID, name, age, gender, .....
* Transaction ID
* Amount of money
* Type of Transaction
* ...
### Requirement for Transaction
--> **Transaction occur every second, data updated continuously to adapt user requirements, also need to store old version of data**
* Able to handle big data
* They must be updated continuously, real time, streaming
* Data Transformation
* Fault tolerance
* Cost Optimization
* History Retrievial
* Decision Making
.....
### Solution
That's why we need a **DATA PIPELINE** using technology to handle big data. That's the aim of this project
## Project Description
In this project, I build a Big Data PipeLine to handle Bank Data Flow, from raw source to useful data.
## Source
Assuming transaction data is store and update, adding continuously in a Database, this project use PosgreSQL for database management. It's look like

<img src="https://scontent.fhan3-2.fna.fbcdn.net/v/t39.30808-6/362289966_6165150346940955_2473050135674800960_n.jpg?_nc_cat=107&ccb=1-7&_nc_sid=5f2048&_nc_eui2=AeG4aMbTs4V1AQ3W7QzT4eVnODBNOP5h2TA4ME04_mHZMPK8ZkJKrsuMtJNFluKGdIxa6yY2bLOZEZaZKjr3f-Fk&_nc_ohc=vJTkF1yy60oAb7VlWrU&_nc_ht=scontent.fhan3-2.fna&oh=00_AfCfBzAgbZL01HqbQKhB94eQwz-_L3vbDl6bdwpbpsgCnQ&oe=662D61FD" width="400" alt="Screenshot of My Project">
