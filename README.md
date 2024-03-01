# Spotify API ETL end to end Project

## Overview
### This project involves building an ETL (Extract, Transform, Load) pipeline utilizing the Spotify API on the AWS cloud platform. The primary objective is to gather data from the Spotify API, transform it into the desired format, and load it into the AWS data platform.

### Architecture
![Architecture Diagram](https://github.com/arrudaguilherme/spotify-end-to-end-data-engineering/blob/main/ETL_Architecture.png)

### Dataset/API

This API contains information about music artists, songs and albums. - [Spotify API](https://developer.spotify.com/documentation/web-api)

### Services Used

1. S3 (Simple Storage Service): Amazon Simple Storage Service (Amazon S3) is a scalable and highly durable cloud storage service provided by Amazon Web Services (AWS). It is designed to store and retrieve any amount of data from anywhere on the web. S3 offers a simple web services interface that allows developers to easily manage and organize their data in the form of objects, which can be text, images, videos, or any other type of file.

2. AWS Lambda: A serverless computing service provided by Amazon Web Services (AWS). It allows developers to run code without the need to provision or manage servers. AWS Lambda is designed to automatically scale and manage the infrastructure needed to run code, making it an ideal choice for event-driven and scalable applications.

3. CloudWatch: Amazon CloudWatch is a monitoring and observability service provided by Amazon Web Services (AWS). It enables users to collect, monitor, and analyze various metrics and logs from AWS resources, applications, and services. CloudWatch provides a comprehensive set of tools for gaining insights into the performance, operational health, and security of AWS environments.

4. Glue Crawler: A service provided by Amazon Web Services (AWS) as part of the AWS Glue data integration and ETL (Extract, Transform, Load) platform. The Glue Crawler is designed to automatically discover, catalog, and infer the schema of data stored in various data sources, making it easier to understand and use the data in AWS Glue ETL jobs.

5. Data Catalog: AWS Glue Data Catalog is a fully managed metadata repository provided by Amazon Web Services (AWS). It is a central component of the AWS Glue service, offering a unified and organized view of metadata for various data sources, making it easier to discover, understand, and manage data assets within the AWS environment.

6. Amazon Athena: Amazon Athena is a serverless, interactive query service provided by Amazon Web Services (AWS). It allows users to analyze and query data stored in Amazon S3 using standard SQL queries without the need for infrastructure provisioning or management. Athena is designed for simplicity and scalability, making it easy for users to gain insights from their data without the need to set up and maintain a database.

### Install Packages
```
pip install pandas
pip install numpy
pip install spotipy
```
### Execution Flow
Extract Data from API --> Lambda Trigger (every 1 hour) --> Run Extract Code --> Store Raw Data --> Trigger Transform Function --> Run Transformation Code --> Transform Data and Load --> Query using Amazon Athena.

