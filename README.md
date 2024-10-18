# YOUTUBE DATA ENGINEERING PROJECT

## Navigating 2023's New Channel Success

## Introduction

Welcome to my YouTube Data Engineering Project. In this initiative, I will be providing valuable insights into YouTube channels created in the year 2023, delving into their development over the course of the year. This project serves as a platform for me to showcase my expertise in utilizing advanced big data tools. By leveraging these tools, I aim to derive meaningful insights, facilitate efficient data collection, and ensure a seamless transition in the realm of data analytics. Join me as we explore the intricate dynamics of YouTube channel evolution through the lens of data engineering.


## Overview
YouTube is an American online video-sharing and social media platform that is owned by Google. Accessible globally, it stands as the second most visited website, surpassed only by Google itself. Every minute witnesses an astonishing 694,000 hours of video being streamed on YouTube, establishing it as a significant medium. Over the years, YouTube has evolved into a lucrative source of income for many individuals. A "YouTuber" is an individual who engages in the creation and dissemination of content on the YouTube platform.

The financial remuneration for YouTubers is diverse, emanating from various channels. If we exclusively consider earnings from YouTube's Partner Program, YouTubers accrue an average of $18 per 1,000 views. However, this is contingent upon meeting eligibility criteria, including a minimum of 1,000 subscribers and 4,000 watch hours within the preceding 12 months.

This project will specifically concentrate on YouTubers who initiated their channels in the year 2023, delving into their progress and achievements. While YouTube serves as a platform where substantial financial gains can be realized by content creators, it is imperative to acknowledge the inherent challenges faced by newcomers in every entrepreneurial endeavor.

## Architecture & Technologies
This architectural framework ensures a streamlined, automated, and scalable approach to handling YouTube channel data, from its extraction to transformation and final visualization.

![image](https://github.com/user-attachments/assets/7c7355ca-37e6-4f72-8d38-6de8c8b278de)

1. Docker: Containerization  
2. Apache Airflow: Orchestration
3. YouTube API Integration: New channels are extracted using the YouTube API.  
4. PostgreSQL Database: Extracted new channels are stored in a PostgreSQL database.  
5. Data Extraction: ChannelID data is extracted from the database.  
6. YouTube Data Update: Extracted data is sent back to YouTube using the YouTube API to retrieve updated statistics and snippet information.  
7. Boto3: Batch processing of the collected data.  
8. AWS S3 Storage: Collected data is transferred to an AWS S3 bucket.  
9. AWS Lambda Function: A Lambda function is triggered upon the arrival of data in the S3 bucket.  
10. AWS CloudWatch: Logging Lambda function execution and monitoring Lambda metrics.  
11. AWS Redshift Serverless Database: Lambda initiates the data upload to an AWS Redshift Serverless Data Warehouse.  
12. DBt Cloud: Scheduled weekly, DBt Cloud runs transformation processes on the data.  
13. Looker Studio: The finalized data is visualized on Data Studio.


## How to run the pipeline
* cd ./airflow
* docker-compose up -d
* cd ./postgres
* docker-compose up -d

-- Airflow Dags TreeView 
![image](https://github.com/user-attachments/assets/61977bbf-d9b6-44d0-9364-f28841948546)

-- AWS Lambda Task  
Cloudwatch logs  
![image](https://github.com/user-attachments/assets/862a0d69-9191-4bd0-a6e1-7f1ec1704f3c)
![image](https://github.com/user-attachments/assets/ab77ff9c-cbe2-4e87-bc3a-eee6dcebd948)

-- DBT Jobs  
Lineage graph
![image](https://github.com/user-attachments/assets/a7db8a41-ac4e-49f0-8a0f-ff6958ed9dcf)

DBT Scheduler
![image](https://github.com/user-attachments/assets/a8dc88bd-2a8f-4801-892b-69af76080014)

DBT Documentation
![image](https://github.com/user-attachments/assets/6d6bb5ee-51c9-46c2-a257-62b5feb9e46c)

 
## Result
![image](https://github.com/user-attachments/assets/6bda66f0-cbd4-48c3-b9c2-5f61bfb84d4e)

  
![image](https://github.com/user-attachments/assets/7a7c6199-83a5-4760-81b6-3f41dcbfafe0)

To be eligible for YouTube's Partner Program, a YouTube channel must have a minimum of 1000 subscribers and 4,000 watch hours within the preceding 12 months. Excluding the 12-month criteria, let's analyze the percentage of channels from each month with over 1,000 subscribers and 4,000 watch hours.  
![Uploading image.png…]()

## Requirement
* [YouTube API Documentation](https://developers.google.com/youtube/v3/docs/)  
* [Obtain a YouTube API Key](https://console.cloud.google.com/apis)  
* Docker desktop
* AWS account


## contact
* [Elijah Ajala](https://linkedin.com/in/elijahajala/)
* [Project link](https://github.com/dMagnifico/Pipeline-for-Youtube-data)
