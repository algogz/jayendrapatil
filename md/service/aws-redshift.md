### Question 1:

With which AWS services CloudHSM can be used (select 2)

- A. S3
- B. DynamoDB
- C. RDS
- D. ElastiCache
- E. Amazon Redshift

<details><summary>Answer:</summary><p>
[C, E]

Categories:
[S3, RDS, ElastiCache, DynamoDB, Redshift]

Explanation:

Question 1@http://jayendrapatil.com/aws-redshift/

</p></details><hr>

### Question 2:

You have recently joined a startup company building sensors to measure street noise and air quality in urban areas. The company has been running a pilot deployment of around 100 sensors for 3 months. Each sensor uploads 1KB of sensor data every minute to a backend hosted on AWS. During the pilot, you measured a peak of 10 IOPS on the database, and you stored an average of 3GB of sensor data per month in the database. The current deployment consists of a load-balanced auto scaled Ingestion layer using EC2 instances and a PostgreSQL RDS database with 500GB standard storage. The pilot is considered a success and your CEO has managed to get the attention or some potential investors. The business plan requires a deployment of at least 100K sensors, which needs to be supported by the backend. You also need to store sensor data for at least two years to be able to compare year over year Improvements. To secure funding, you have to make sure that the platform meets these requirements and leaves room for further scaling. Which setup will meet the requirements?

- A. Add an SQS queue to the ingestion layer to buffer writes to the RDS instance 
- B. Ingest data into a DynamoDB table and move old data to a Redshift cluster
- C. Replace the RDS instance with a 6 node Redshift cluster with 96TB of storage 
- D. Keep the current architecture but upgrade RDS storage to 3TB and 10K provisioned IOPS 

<details><summary>Answer:</summary><p>
[B]

Categories:
[RDS, SQS, EC2, DynamoDB, Redshift]

Explanation:

Question 2@http://jayendrapatil.com/aws-redshift/

A: RDS instance will not support data for 2 years

B: Handle 10K IOPS ingestion and store data into Redshift for analysis

C: Does not handle the ingestion issue

D: RDS instance will not support data for 2 years

</p></details><hr>

### Question 3:

Which two AWS services provide out-of-the-box user configurable automatic backup-as-a-service and backup rotation options? Choose 2 answers

- A. Amazon S3
- B. Amazon RDS
- C. Amazon EBS
- D. Amazon Redshift

<details><summary>Answer:</summary><p>
[B, D]

Categories:
[S3, RDS, EBS, Redshift]

Explanation:

Question 3@http://jayendrapatil.com/aws-redshift/

</p></details><hr>

### Question 4:

Your department creates regular analytics reports from your company’s log files. All log data is collected in Amazon S3 and processed by daily Amazon Elastic Map Reduce (EMR) jobs that generate daily PDF reports and aggregated tables in CSV format for an Amazon Redshift data warehouse. Your CFO requests that you optimize the cost structure for this system. Which of the following alternatives will lower costs without compromising average performance of the system or data integrity for the raw data?

- A. Use reduced redundancy storage (RRS) for PDF and CSV data in Amazon S3. Add Spot instances to Amazon EMR jobs. Use Reserved Instances for Amazon Redshift. 
- B. Use reduced redundancy storage (RRS) for all data in S3. Use a combination of Spot instances and Reserved Instances for Amazon EMR jobs. Use Reserved instances for Amazon Redshift
- C. Use reduced redundancy storage (RRS) for all data in Amazon S3. Add Spot Instances to Amazon EMR jobs. Use Reserved Instances for Amazon Redshift 
- D. Use reduced redundancy storage (RRS) for PDF and CSV data in S3. Add Spot Instances to EMR jobs. Use Spot Instances for Amazon Redshift. 

<details><summary>Answer:</summary><p>
[B]

Categories:
[S3, EMR, Redshift]

Explanation:

Question 4@http://jayendrapatil.com/aws-redshift/

A: Spot instances impacts performance

B: Combination of the Spot and reserved with guarantee performance and help reduce cost. Also, RRS would reduce cost and guarantee data integrity, which is different from data durability

C: Spot instances impacts performance

D: Spot instances impacts performance and Spot instance not available for Redshift

</p></details><hr>

