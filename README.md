[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/1lXY_Wlg)


## Project Overview
Every body in tech is farmiliar with Stack overflow. It has saved our careers countless times and continues to do so. Stack overflow is part of a network of questions and anwsers websites where questions, answers, and users are subject to a reputation award process. The primary purpose of each Stack Exchange site is to enable users to post questions and answer them. Users can vote on both answers and questions, and through this process users earn reputation points. https://en.wikipedia.org/wiki/Stack_Exchange.

The goal of this project to try and analyze the Stack Exchange data. It aims to develop a reliable and scalable data pipeline that integrates data from the different the Stack Exchange webistes into a centralized datalakehouse. The end product is answer the following questions:

1. Can we understand how current data engineers transitioned through different stages in their career through the questions, comments, answers and posts on stackoverflow code review?
2. Can we measure career growth of data engineers by the trend of their approved answers to questions and reputation on stack overflow?
3. Whats the data products, data stack and tools they have used over the years. Is there any trend?
4. Are data Engineers also software engineers? Whats the transition rate from software engineers to data engineers and vice versa?
5. Has the emergence of LLMS reduced the number of user engagement in stacokverflow ( Study user engagement)

## Scope of the project

### **1. Data Sources**
- The different stack Exchange websites dumps data every 3 months in the  The Internet Archive.
- Realtime data can also be accessed through the Stack Exchange API.
- The project will make use of both data dumps and realtime data

### **2. Key Features**

- **Automated Data Ingestion:** Daily data extraction from API and every quater from the data dump.
- **Data Transformation and Cleaning:** Utilizing pysaprk to transform and clean the data.
- **Data Quality Checks:** Implementing data quality checks to ensure data accuracy.
- **Data Visualization:** Creating interactive dashboards that update daily providing insights.


### **3. Tech Stack ( Might change)**
Given the lack of cloud budget to implement this project, I plan to use an a local dockerised data lakehouse made up of:
- **MinIO:** MinIO will act as the core service for underlying storage. It is a S3 Compatible Object Storage
- **Postgres:** Postgres will act as our backend service for Airflow database and Hive Metastore. It will also serve as the data warehouse.
- **Hive-Metastore:**
Hive Metastore to persist our data using database fashion and manage the metadata of dataset in MinIO.
- **Apache Spark:**  Now we have everything except Apache Spark for distributed computing

