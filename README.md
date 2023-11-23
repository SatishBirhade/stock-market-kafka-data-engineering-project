# Stock Market Kafka Real Time Data Engineering Project

## Introduction 
In this project, I have executed an End-To-End Data Engineering Project on Real-Time Stock Market Data using Kafka. I have used different technologies such as Python, Amazon Web Services (AWS), Apache Kafka, Glue, Athena, and SQL.

## Architecture 
<img src="Architecture.jpg">

## Technology Used
- Programming Language - Python
- Amazon Web Service (AWS)
1. S3 (Simple Storage Service)
2. Athena
3. Glue Crawler
4. Glue Catalog
5. EC2
- Apache Kafka

### Services used

1. **AWS S3 (Simple Storage Service) :** Its an object storage service that provides manufacturing scalability, data availability, security, and performance. Its a highly scalable object storage service that can store and retrieve any amount of data from anywhere on the web.It is commonly used to store and distribute large media files, data backups and static website files.
2. **AWS IAM :** This is nothing but identity and access management which enables us to manage access to AWS services and resources securely.
3. **AWS Glue :** A serverless data integration service that makes it easy to discover, prepare, and combine data for analytics, machine learning, and application development.
4. **AWS Glue Crawler :** AWS Glue Crawler is a fully managed service that automatically crawls the data sources, identifies data formats and infers schemas to create an AWS Glue Data Catalog.
5. **AWS Glue Data Catalog :** AWS Glue Data Catalog is a fully managed metadata repository that makes it easy to discover and manage data in AWS. We can use the Glue Data Catalog with other AWS services, such as Athena
6. **AWS Athena :** Athena is an interactive query service that makes it easy to analyze data in amazon s3 using standard SQL. We can use Athena to analyze data in Glue Data catalog or in other s3 buckets

### Dataset Used
This contains the information about the stockmarket dataset used in this project.
## Here is the dataset that i used : https://github.com/SatishBirhade/stock-market-kafka-data-engineering-project/tree/68e8d6817e5c212a768ea82ad5445339011cd1b7/Raw_Data

### Project Execution Flow
Loaded the indexProcessed.csv into python dataframe --> Kafka Producer keeps on generating the sample rows from this dataframe with the latency of 2s through topic : sreetopic1  --> Kafka Consumer consumes these messages using the same topic : sreetopic1 --> Kafka consumer also writes the data into s3 in json format with increasing count --> Glue crawler creates the data catalogs on s3 data --> Query this stock market data using Athena

#### Steps Executed

1. Downloaded some sample stock market data in the csv format.
2. Used python to simulate this data as simple dataframes and put into the kafka clusters. 
3. From kafka producer sent this sample data in kafka topics every 2s. 
4. Consumed this kafka topics using Kafka consumer and store the data into s3 in json format. 
5. Crawled the above data to create the Glue catalog tables and queried the data using the Athena.

### What did I learn?

Through this project, I gained valuable hands-on experience in various aspects of data engineering, including real-time data processing, data storage, and data querying. I honed my skills in using technologies such as Python, AWS, Apache Kafka, Glue, Athena, and SQL, and learned how to effectively integrate them to build a complete end-to-end solution. Additionally, I developed my ability to troubleshoot and overcome technical challenges, further strengthening my problem-solving skills. Overall, this project provided me with a comprehensive understanding of the complexities involved in real-time data analysis and reinforced my commitment to continuously improving my skills as a data engineer.


