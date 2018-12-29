### Question 1:

You are deploying an application to track GPS coordinates of delivery trucks in the United States. Coordinates are transmitted from each delivery truck once every three seconds. You need to design an architecture that will enable real-time processing of these coordinates from multiple consumers. Which service should you use to implement data ingestion?

- A. Amazon Kinesis
- B. AWS Data Pipeline
- C. Amazon AppStream
- D. Amazon Simple Queue Service

<details><summary>Answer:</summary><p>
[A]

Categories:
[SQS, Kinesis]

Explanation:

Question 1@http://jayendrapatil.com/aws-kinesis/

</p></details><hr>

### Question 2:

You are deploying an application to collect votes for a very popular television show. Millions of users will submit votes using mobile devices. The votes must be collected into a durable, scalable, and highly available data store for real-time public tabulation. Which service should you use?

- A. Amazon DynamoDB
- B. Amazon Redshift
- C. Amazon Kinesis
- D. Amazon Simple Queue Service

<details><summary>Answer:</summary><p>
[A]

Categories:
[SQS, Kinesis, DynamoDB, Redshift]

Explanation:

Question 2@http://jayendrapatil.com/aws-kinesis/

</p></details><hr>

### Question 3:

Your company is in the process of developing a next generation pet collar that collects biometric information to assist families with promoting healthy lifestyles for their pets. Each collar will push 30kb of biometric data In JSON format every 2 seconds to a collection platform that will process and analyze the data providing health trending information back to the pet owners and veterinarians via a web portal Management has tasked you to architect the collection platform ensuring the following requirements are met. Provide the ability for real-time analytics of the inbound biometric data Ensure processing of the biometric data is highly durable, elastic and parallel. The results of the analytic processing should be persisted for data mining. Which architecture outlined below will meet the initial requirements for the collection platform?

- A. Utilize S3 to collect the inbound sensor data analyze the data from S3 with a daily scheduled Data Pipeline and save the results to a Redshift Cluster.
- B. Utilize Amazon Kinesis to collect the inbound sensor data, analyze the data with Kinesis clients and save the results to a Redshift cluster using EMR. (  )
- C. Utilize SQS to collect the inbound sensor data analyze the data from SQS with Amazon Kinesis and save the results to a Microsoft SQL Server RDS instance.
- D. Utilize EMR to collect the inbound sensor data, analyze the data from EUR with Amazon Kinesis and save me results to DynamoDB.

<details><summary>Answer:</summary><p>
[B]

Categories:
[S3, RDS, SQS, Kinesis, DynamoDB, EMR, Redshift]

Explanation:

Question 3@http://jayendrapatil.com/aws-kinesis/

B: https://aws.amazon.com/about-aws/whats-new/2014/02/20/analyze-streaming-data-from-amazon-kinesis-with-amazon-elastic-mapreduce/

B: refer

</p></details><hr>

### Question 4:

Your customer is willing to consolidate their log streams (access logs, application logs, security logs etc.) in one single system. Once consolidated, the customer wants to analyze these logs in real time based on heuristics. From time to time, the customer needs to validate heuristics, which requires going back to data samples extracted from the last 12 hours? What is the best approach to meet your customer’s requirements?

- A. Send all the log events to Amazon SQS. Setup an Auto Scaling group of EC2 servers to consume the logs and apply the heuristics.
- B. Send all the log events to Amazon Kinesis develop a client process to apply heuristics on the logs
- C. Configure Amazon CloudTrail to receive custom logs, use EMR to apply heuristics the logs (CloudTrail is only for auditing)
- D. Setup an Auto Scaling group of EC2 syslogd servers, store the logs on S3 use EMR to apply heuristics on the logs (EMR is for batch analysis)

<details><summary>Answer:</summary><p>
[B]

Categories:
[S3, SQS, EC2, ASG, Kinesis, EMR, CloudTrail]

Explanation:

Question 4@http://jayendrapatil.com/aws-kinesis/

B: Can perform real time analysis and stores data for 24 hours which can be extended to 7 days

</p></details><hr>

### Question 5:

You require the ability to analyze a customer’s clickstream data on a website so they can do behavioral analysis. Your customer needs to know what sequence of pages and ads their customer clicked on. This data will be used in real time to modify the page layouts as customers click through the site to increase stickiness and advertising click-through. Which option meets the requirements for captioning and analyzing this data?

- A. Log clicks in weblogs by URL store to Amazon S3, and then analyze with Elastic MapReduce
- B. Push web clicks by session to Amazon Kinesis and analyze behavior using Kinesis workers
- C. Write click events directly to Amazon Redshift and then analyze with SQL
- D. Publish web clicks by session to an Amazon SQS queue men periodically drain these events to Amazon RDS and analyze with SQL

<details><summary>Answer:</summary><p>
[B]

Categories:
[S3, SES, RDS, SQS, Kinesis, EBS, Redshift]

Explanation:

Question 5@http://jayendrapatil.com/aws-kinesis/

</p></details><hr>

### Question 6:

Your social media monitoring application uses a Python app running on AWS Elastic Beanstalk to inject tweets, Facebook updates and RSS feeds into an Amazon Kinesis stream. A second AWS Elastic Beanstalk app generates key performance indicators into an Amazon DynamoDB table and powers a dashboard application. What is the most efficient option to prevent any data loss for this application?

- A. Use AWS Data Pipeline to replicate your DynamoDB tables into another region.
- B. Use the second AWS Elastic Beanstalk app to store a backup of Kinesis data onto Amazon Elastic Block Store (EBS), and then create snapshots from your Amazon EBS volumes.
- C. Add a second Amazon Kinesis stream in another Availability Zone and use AWS data pipeline to replicate data across Kinesis streams.
- D. Add a third AWS Elastic Beanstalk app that uses the Amazon Kinesis S3 connector to archive data from Amazon Kinesis into Amazon S3.

<details><summary>Answer:</summary><p>
[D]

Categories:
[S3, SES, Kinesis, EBS, DynamoDB, Elastic Beanstalk]

Explanation:

Question 6@http://jayendrapatil.com/aws-kinesis/

</p></details><hr>

### Question 7:

You need to replicate API calls across two systems in real time. What tool should you use as a buffer and transport mechanism for API call events?

- A. AWS SQS
- B. AWS Lambda
- C. AWS Kinesis
- D. AWS SNS

<details><summary>Answer:</summary><p>
[C]

Categories:
[SQS, Kinesis, SNS, Lambda]

Explanation:

Question 7@http://jayendrapatil.com/aws-kinesis/

C: AWS Kinesis is an event stream service. Streams can act as buffers and transport across systems for in-order programmatic events, making it ideal for replicating API calls across systems

</p></details><hr>

### Question 8:

You need to perform ad-hoc business analytics queries on well-structured data. Data comes in constantly at a high velocity. Your business intelligence team can understand SQL. What AWS service(s) should you look to first?

- A. Kinesis Firehose + RDS
- B. Kinesis Firehose + RedShift
- C. EMR using Hive
- D. EMR running Apache Spark

<details><summary>Answer:</summary><p>
[B]

Categories:
[RDS, Kinesis, EMR, Redshift]

Explanation:

Question 8@http://jayendrapatil.com/aws-kinesis/

B: https://aws.amazon.com/kinesis/firehose/details/

B: Kinesis Firehose provides a managed service for aggregating streaming data and inserting it into RedShift. RedShift also supports ad-hoc queries over well-structured data using a SQL-compliant wire protocol, so the business team should be able to adopt this system easily. Refer

</p></details><hr>

