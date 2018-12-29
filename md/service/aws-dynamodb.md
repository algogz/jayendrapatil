### Question 1:

Which of the following are use cases for Amazon DynamoDB? Choose 3 answers

- A. Storing BLOB data.
- B. Managing web sessions
- C. Storing JSON documents
- D. Storing metadata for Amazon S3 objects
- E. Running relational joins and complex updates.
- F. Storing large amounts of infrequently accessed data.

<details><summary>Answer:</summary><p>
[B, C, D]

Categories:
[S3, SES, DynamoDB]

Explanation:

Question 1@http://jayendrapatil.com/aws-dynamodb/

</p></details><hr>

### Question 2:

You are configuring your company’s application to use Auto Scaling and need to move user state information. Which of the following AWS services provides a shared data store with durability and low latency?

- A. AWS ElastiCache Memcached 
- B. Amazon Simple Storage Service 
- C. Amazon EC2 instance storage 
- D. Amazon DynamoDB

<details><summary>Answer:</summary><p>
[D]

Categories:
[S3, EC2, ASG, ElastiCache, DynamoDB]

Explanation:

Question 2@http://jayendrapatil.com/aws-dynamodb/

A: does not allow writes

B: does not provide low latency

C: not durable

</p></details><hr>

### Question 3:

Does Dynamo DB support in-place atomic updates?

- A. It is not defined
- B. No
- C. Yes
- D. It does support in-place non-atomic updates

<details><summary>Answer:</summary><p>
[C]

Categories:
[]

Explanation:

Question 3@http://jayendrapatil.com/aws-dynamodb/

</p></details><hr>

### Question 4:

What is the maximum write throughput I can provision for a single Dynamic DB table?

- A. 1,000 write capacity units
- B. 100,000 write capacity units
- C. Dynamic DB is designed to scale without limits, but if you go beyond 10,000 you have to contact AWS first
- D. 10,000 write capacity units

<details><summary>Answer:</summary><p>
[C]

Categories:
[]

Explanation:

Question 4@http://jayendrapatil.com/aws-dynamodb/

</p></details><hr>

### Question 5:

For a DynamoDB table, what happens if the application performs more reads or writes than your provisioned capacity?

- A. Nothing
- B. requests above the provisioned capacity will be performed but you will receive 400 error codes.
- C. requests above the provisioned capacity will be performed but you will receive 200 error codes.
- D. requests above the provisioned capacity will be throttled and you will receive 400 error codes.

<details><summary>Answer:</summary><p>
[D]

Categories:
[DynamoDB]

Explanation:

Question 5@http://jayendrapatil.com/aws-dynamodb/

</p></details><hr>

### Question 6:

In which of the following situations might you benefit from using DynamoDB? (Choose 2 answers)

- A. You need fully managed database to handle highly complex queries
- B. You need to deal with massive amount of “hot” data and require very low latency
- C. You need a rapid ingestion of clickstream in order to collect data about user behavior
- D. Your on-premises data center runs Oracle database, and you need to host a backup in AWS cloud

<details><summary>Answer:</summary><p>
[B, C]

Categories:
[SES, DynamoDB]

Explanation:

Question 6@http://jayendrapatil.com/aws-dynamodb/

</p></details><hr>

### Question 7:

You are designing a file-sharing service. This service will have millions of files in it. Revenue for the service will come from fees based on how much storage a user is using. You also want to store metadata on each file, such as title, description and whether the object is public or private. How do you achieve all of these goals in a way that is economical and can scale to millions of users? [PROFESSIONAL]

- A. Store all files in Amazon Simple Storage Service (S3). Create a bucket for each user. Store metadata in the filename of each object, and access it with LIST commands against the S3 API. 
- B. Store all files in Amazon S3. Create Amazon DynamoDB tables for the corresponding key-value pairs on the associated metadata, when objects are uploaded.
- C. Create a striped set of 4000 IOPS Elastic Load Balancing volumes to store the data. Use a database running in Amazon Relational Database Service (RDS) to store the metadata.
- D. Create a striped set of 4000 IOPS Elastic Load Balancing volumes to store the data. Create Amazon DynamoDB tables for the corresponding key-value pairs on the associated metadata, when objects are uploaded. 

<details><summary>Answer:</summary><p>
[B]

Categories:
[S3, RDS, DynamoDB, ELB]

Explanation:

Question 7@http://jayendrapatil.com/aws-dynamodb/

A: expensive and slow as it returns only 1000 items at a time

C: not economical with volumes

D: not economical with volumes

</p></details><hr>

### Question 8:

A utility company is building an application that stores data coming from more than 10,000 sensors. Each sensor has a unique ID and will send a datapoint (approximately 1KB) every 10 minutes throughout the day. Each datapoint contains the information coming from the sensor as well as a timestamp. This company would like to query information coming from a particular sensor for the past week very rapidly and want to delete all the data that is older than 4 weeks. Using Amazon DynamoDB for its scalability and rapidity, how do you implement this in the most cost effective way? [PROFESSIONAL]

- A. One table, with a primary key that is the sensor ID and a hash key that is the timestamp 
- B. One table, with a primary key that is the concatenation of the sensor ID and timestamp 
- C. One table for each week, with a primary key that is the concatenation of the sensor ID and timestamp 
- D. One table for each week, with a primary key that is the sensor ID and a hash key that is the timestamp

<details><summary>Answer:</summary><p>
[D]

Categories:
[DynamoDB]

Explanation:

Question 8@http://jayendrapatil.com/aws-dynamodb/

A: Single table impacts performance

B: Single table and concatenation impacts performance

C: Concatenation will cause queries would be slower, if at all

D: Composite key with Sensor ID and timestamp would help for faster queries

</p></details><hr>

### Question 9:

You have recently joined a startup company building sensors to measure street noise and air quality in urban areas. The company has been running a pilot deployment of around 100 sensors for 3 months. Each sensor uploads 1KB of sensor data every minute to a backend hosted on AWS. During the pilot, you measured a peak of 10 IOPS on the database, and you stored an average of 3GB of sensor data per month in the database. The current deployment consists of a load-balanced auto scaled Ingestion layer using EC2 instances and a PostgreSQL RDS database with 500GB standard storage. The pilot is considered a success and your CEO has managed to get the attention or some potential investors. The business plan requires a deployment of at least 100K sensors, which needs to be supported by the backend. You also need to store sensor data for at least two years to be able to compare year over year Improvements. To secure funding, you have to make sure that the platform meets these requirements and leaves room for further scaling. Which setup will meet the requirements? [PROFESSIONAL]

- A. Add an SQS queue to the ingestion layer to buffer writes to the RDS instance 
- B. Ingest data into a DynamoDB table and move old data to a Redshift cluster
- C. Replace the RDS instance with a 6 node Redshift cluster with 96TB of storage 
- D. Keep the current architecture but upgrade RDS storage to 3TB and 10K provisioned IOPS 

<details><summary>Answer:</summary><p>
[B]

Categories:
[RDS, SQS, EC2, DynamoDB, Redshift]

Explanation:

Question 9@http://jayendrapatil.com/aws-dynamodb/

A: RDS instance will not support data for 2 years

B: Handle 10K IOPS ingestion and store data into Redshift for analysis

C: Does not handle the ingestion issue

D: RDS instance will not support data for 2 years

</p></details><hr>

### Question 10:

Does Amazon DynamoDB support both increment and decrement atomic operations?

- A. No, neither increment nor decrement operations.
- B. Only increment, since decrement are inherently impossible with DynamoDB’s data model.
- C. Only decrement, since increment are inherently impossible with DynamoDB’s data model.
- D. Yes, both increment and decrement operations.

<details><summary>Answer:</summary><p>
[D]

Categories:
[DynamoDB]

Explanation:

Question 10@http://jayendrapatil.com/aws-dynamodb/

</p></details><hr>

### Question 11:

What is the data model of DynamoDB?

- A. “Items”, with Keys and one or more Attribute; and “Attribute”, with Name and Value.
- B. “Database”, which is a set of “Tables”, which is a set of “Items”, which is a set of “Attributes”.
- C. “Table”, a collection of Items; “Items”, with Keys and one or more Attribute; and “Attribute”, with Name and Value.
- D. “Database”, a collection of Tables; “Tables”, with Keys and one or more Attribute; and “Attribute”, with Name and Value.

<details><summary>Answer:</summary><p>
[C]

Categories:
[DynamoDB]

Explanation:

Question 11@http://jayendrapatil.com/aws-dynamodb/

</p></details><hr>

### Question 12:

In regard to DynamoDB, for which one of the following parameters does Amazon not charge you?

- A. Cost per provisioned write units
- B. Cost per provisioned read units
- C. Storage cost
- D. I/O usage within the same Region

<details><summary>Answer:</summary><p>
[D]

Categories:
[DynamoDB]

Explanation:

Question 12@http://jayendrapatil.com/aws-dynamodb/

</p></details><hr>

### Question 13:

Which statements about DynamoDB are true? Choose 2 answers.

- A. DynamoDB uses a pessimistic locking model
- B. DynamoDB uses optimistic concurrency control
- C. DynamoDB uses conditional writes for consistency
- D. DynamoDB restricts item access during reads
- E. DynamoDB restricts item access during writes

<details><summary>Answer:</summary><p>
[B, C]

Categories:
[SES, DynamoDB]

Explanation:

Question 13@http://jayendrapatil.com/aws-dynamodb/

</p></details><hr>

### Question 14:

Which of the following is an example of a good DynamoDB hash key schema for provisioned throughput efficiency?

- A. User ID, where the application has many different users.
- B. Status Code where most status codes is the same.
- C. Device ID, where one is by far more popular than all the others.
- D. Game Type, where there are three possible game types.

<details><summary>Answer:</summary><p>
[A]

Categories:
[DynamoDB]

Explanation:

Question 14@http://jayendrapatil.com/aws-dynamodb/

</p></details><hr>

### Question 15:

You are inserting 1000 new items every second in a DynamoDB table. Once an hour these items are analyzed and then are no longer needed. You need to minimize provisioned throughput, storage, and API calls. Given these requirements, what is the most efficient way to manage these Items after the analysis?

- A. Retain the items in a single table
- B. Delete items individually over a 24 hour period
- C. Delete the table and create a new table per hour
- D. Create a new table per hour

<details><summary>Answer:</summary><p>
[C]

Categories:
[DynamoDB]

Explanation:

Question 15@http://jayendrapatil.com/aws-dynamodb/

</p></details><hr>

### Question 16:

When using a large Scan operation in DynamoDB, what technique can be used to minimize the impact of a scan on a table’s provisioned throughput?

- A. Set a smaller page size for the scan
- B. Use parallel scans
- C. Define a range index on the table
- D. Prewarm the table by updating all items

<details><summary>Answer:</summary><p>
[A]

Categories:
[DynamoDB]

Explanation:

Question 16@http://jayendrapatil.com/aws-dynamodb/

A: http://docs.aws.amazon.com/amazondynamodb/latest/developerguide/QueryAndScanGuidelines.html

</p></details><hr>

### Question 17:

In regard to DynamoDB, which of the following statements is correct?

- A. An Item should have at least two value sets, a primary key and another attribute.
- B. An Item can have more than one attributes
- C. A primary key should be single-valued.
- D. An attribute can have one or several other attributes.

<details><summary>Answer:</summary><p>
[B]

Categories:
[DynamoDB]

Explanation:

Question 17@http://jayendrapatil.com/aws-dynamodb/

</p></details><hr>

### Question 18:

Which one of the following statements is NOT an advantage of DynamoDB being built on Solid State Drives?

- A. serve high-scale request workloads
- B. low request pricing
- C. high I/O performance of WebApp on EC2 instance
- D. low-latency response times

<details><summary>Answer:</summary><p>
[C]

Categories:
[EC2, DynamoDB]

Explanation:

Question 18@http://jayendrapatil.com/aws-dynamodb/

C: Not related to DynamoDB

</p></details><hr>

### Question 19:

Which one of the following operations is NOT a DynamoDB operation?

- A. BatchWriteItem
- B. DescribeTable
- C. BatchGetItem
- D. BatchDeleteItem

<details><summary>Answer:</summary><p>
[D]

Categories:
[DynamoDB]

Explanation:

Question 19@http://jayendrapatil.com/aws-dynamodb/

D: DeleteItem deletes a single item in a table by primary key, but BatchDeleteItem doesn’t exist

</p></details><hr>

### Question 20:

What item operation allows the retrieval of multiple items from a DynamoDB table in a single API call?

- A. GetItem
- B. BatchGetItem
- C. GetMultipleItems
- D. GetItemRange

<details><summary>Answer:</summary><p>
[B]

Categories:
[DynamoDB, EMR]

Explanation:

Question 20@http://jayendrapatil.com/aws-dynamodb/

</p></details><hr>

### Question 21:

An application stores payroll information nightly in DynamoDB for a large number of employees across hundreds of offices. Item attributes consist of individual name, office identifier, and cumulative daily hours. Managers run reports for ranges of names working in their office. One query is. “Return all Items in this office for names starting with A through E”. Which table configuration will result in the lowest impact on provisioned throughput for this query? [PROFESSIONAL]

- A. Configure the table to have a hash index on the name attribute, and a range index on the office identifier
- B. Configure the table to have a range index on the name attribute, and a hash index on the office identifier
- C. Configure a hash index on the name attribute and no range index
- D. Configure a hash index on the office Identifier attribute and no range index

<details><summary>Answer:</summary><p>
[B]

Categories:
[DynamoDB]

Explanation:

Question 21@http://jayendrapatil.com/aws-dynamodb/

</p></details><hr>

### Question 22:

You need to migrate 10 million records in one hour into DynamoDB. All records are 1.5KB in size. The data is evenly distributed across the partition key. How many write capacity units should you provision during this batch load?

- A. 6667
- B. 4166
- C. 5556
- D. 2778

<details><summary>Answer:</summary><p>
[C]

Categories:
[RDS, DynamoDB]

Explanation:

Question 22@http://jayendrapatil.com/aws-dynamodb/

C: http://docs.aws.amazon.com/amazondynamodb/latest/developerguide/HowItWorks.ProvisionedThroughput.html

C: ( 2 write units (1 for each 1KB) * 10 million/3600 secs, refer )

</p></details><hr>

### Question 23:

A meteorological system monitors 600 temperature gauges, obtaining temperature samples every minute and saving each sample to a DynamoDB table. Each sample involves writing 1K of data and the writes are evenly distributed over time. How much write throughput is required for the target table?

- A. 1 write capacity unit
- B. 10 write capacity units
- C. 60 write capacity units
- D. 600 write capacity units
- E. 3600 write capacity units

<details><summary>Answer:</summary><p>
[B]

Categories:
[DynamoDB]

Explanation:

Question 23@http://jayendrapatil.com/aws-dynamodb/

B: 1 write unit for 1K * 600 gauges/60 secs

</p></details><hr>

### Question 24:

You are building a game high score table in DynamoDB. You will store each user’s highest score for each game, with many games, all of which have relatively similar usage levels and numbers of players. You need to be able to look up the highest score for any game. What’s the best DynamoDB key structure?

- A. HighestScore as the hash / only key.
- B. GameID as the hash key, HighestScore as the range key.
- C. GameID as the hash / only key.
- D. GameID as the range / only key.

<details><summary>Answer:</summary><p>
[B]

Categories:
[DynamoDB]

Explanation:

Question 24@http://jayendrapatil.com/aws-dynamodb/

B: http://docs.aws.amazon.com/amazondynamodb/latest/developerguide/GuidelinesForTables.html#GuidelinesForTables.Partitions

B: hash (partition) key should be the GameID, and there should be a range key for ordering HighestScore. Refer

</p></details><hr>

### Question 25:

You are experiencing performance issues writing to a DynamoDB table. Your system tracks high scores for video games on a marketplace. Your most popular game experiences all of the performance issues. What is the most likely problem?

- A. DynamoDB’s vector clock is out of sync, because of the rapid growth in request for the most popular game.
- B. You selected the Game ID or equivalent identifier as the primary partition key for the table.
- C. Users of the most popular video game each perform more read and write requests than average.
- D. You did not provision enough read or write throughput to the table.

<details><summary>Answer:</summary><p>
[B]

Categories:
[DynamoDB]

Explanation:

Question 25@http://jayendrapatil.com/aws-dynamodb/

B: http://docs.aws.amazon.com/amazondynamodb/latest/developerguide/GuidelinesForTables.html#GuidelinesForTables.UniformWorkload

B: Refer Refer

</p></details><hr>

### Question 26:

You are writing to a DynamoDB table and receive the following exception:” ProvisionedThroughputExceededException”. Though according to your Cloudwatch metrics for the table, you are not exceeding your provisioned throughput. What could be an explanation for this?

- A. You haven’t provisioned enough DynamoDB storage instances
- B. You’re exceeding your capacity on a particular Range Key
- C. You’re exceeding your capacity on a particular Hash Key
- D. You’re exceeding your capacity on a particular Sort Key
- E. You haven’t configured DynamoDB Auto Scaling triggers

<details><summary>Answer:</summary><p>
[C]

Categories:
[CloudWatch, ASG, DynamoDB]

Explanation:

Question 26@http://jayendrapatil.com/aws-dynamodb/

C: Hash key determines the partition and hence the performance

</p></details><hr>

### Question 27:

Your company sells consumer devices and needs to record the first activation of all sold devices. Devices are not activated until the information is written on a persistent database. Activation data is very important for your company and must be analyzed daily with a MapReduce job. The execution time of the data analysis process must be less than three hours per day. Devices are usually sold evenly during the year, but when a new device model is out, there is a predictable peak in activation’s, that is, for a few days there are 10 times or even 100 times more activation’s than in average day. Which of the following databases and analysis framework would you implement to better optimize costs and performance for this workload? [PROFESSIONAL]

- A. Amazon RDS and Amazon Elastic MapReduce with Spot instances.
- B. Amazon DynamoDB and Amazon Elastic MapReduce with Spot instances.
- C. Amazon RDS and Amazon Elastic MapReduce with Reserved instances.
- D. Amazon DynamoDB and Amazon Elastic MapReduce with Reserved instances

<details><summary>Answer:</summary><p>
[B]

Categories:
[SES, RDS, DynamoDB]

Explanation:

Question 27@http://jayendrapatil.com/aws-dynamodb/

</p></details><hr>

