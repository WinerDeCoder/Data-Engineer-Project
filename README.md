# Data-Engineer-Project
The Project I have done when Participated in Data Engineer Course From AI4E. I used AWS service, all UI modification --> No Code.

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
In this project, I build a Big Data PipeLine to handle Bank Data Flow, from raw source to useful data. This pipeline should run automatically and update continuously,
## Source
Assuming transaction data is store and update, adding continuously in a Database, this project use PosgreSQL for database management. It's look like


<p align="center">
  <a href="https://getbootstrap.com" target="_blank" rel="noreferrer">
    <img src="https://asia-1-fileserver-2.stringee.com/0/asia-1_1_HSG0R0KB4R18LCY/1690256547-postgreSQL-la-gi.png" alt="cplusplus" alt="bootstrap" width="500" height="300" style="padding-left:20px;padding-right:20px" />
  </a>
  <a href="#">  <img src="[https://asia-1-fileserver-2.stringee.com/0/asia-1_1_HSG0R0KB4R18LCY/1690256547-postgreSQL-la-gi.png](https://scontent.fhan3-2.fna.fbcdn.net/v/t39.30808-6/362289966_6165150346940955_2473050135674800960_n.jpg?_nc_cat=107&ccb=1-7&_nc_sid=5f2048&_nc_eui2=AeG4aMbTs4V1AQ3W7QzT4eVnODBNOP5h2TA4ME04_mHZMPK8ZkJKrsuMtJNFluKGdIxa6yY2bLOZEZaZKjr3f-Fk&_nc_ohc=vJTkF1yy60oAb7VlWrU&_nc_ht=scontent.fhan3-2.fna&oh=00_AfCfBzAgbZL01HqbQKhB94eQwz-_L3vbDl6bdwpbpsgCnQ&oe=662D61FD)" alt="cplusplus" width="500" height="300" margin-right= "100px" ; />
  </a>
</p>

## Flow data step
### Raw Zone
* This is the landing zone for your initial, unprocessed data. Transaction from Database are crawled continuously to here.  
* It acts as a storage repository for the data exactly as it's received from various sources, such as sensors, social media feeds, or log files.
* The data in this zone is typically in its native format and may contain errors, inconsistencies, or duplicates.
* I also partition in rawzone by time ( hour, day, month ) for manageability and performance, especially for large datasets.
* The Raw Zone stores all incoming transaction data in a common format like Parquet files for easier management.

### Golden Zone
Data Transformation: The raw transaction data undergoes various transformations:

* Cleaning: Identify and remove duplicate transactions, correct invalid data entries, and standardize formatting inconsistencies.
* Enrichment: Add additional information to transactions by joining with customer data or account information. This might involve linking transactions to specific accounts, customers, or product categories.
* Validation: Ensure transactions adhere to business rules, like spending limits or fraud detection parameters.
Golden Zone Format:  The Golden Zone stores high-quality, standardized transaction data ready for further analysis. This data can be stored in a relational database or a data lake depending on the bank's infrastructure.

### Insight Zone
Data Preparation: The refined transaction data is further prepared for specific uses. This might involve:
  * Aggregation: Summarize transaction data by customer, account, product category, or time period.
  * Feature Engineering: Create new features from existing data for specific analytical purposes (e.g., average daily balance, spending patterns).
Insight Zone Storage: The Insight Zone stores the prepared data in a format suitable for analytics tools. This could be a data warehouse for reporting and business intelligence or a dedicated platform for machine learning algorithms (e.g., fraud detection, customer segmentation).

> [!NOTE}
> More detail about my work can be found in the report
