### Question 1:

You are running a successful multi-tier web application on AWS and your marketing department has asked you to add a reporting tier to the application. The reporting tier will aggregate and publish status reports every 30 minutes from user-generated information that is being stored in your web applications database. You are currently running a Multi-AZ RDS MySQL instance for the database tier. You also have implemented ElastiCache as a database caching layer between the application tier and database tier. Please select the answer that will allow you to successfully implement the reporting tier with as little impact as possible to your database.

- A. Continually send transaction logs from your master database to an S3 bucket and generate the reports off the S3 bucket using S3 byte range requests.
- B. Generate the reports by querying the synchronously replicated standby RDS MySQL instance maintained through Multi-AZ 
- C. Launch a RDS Read Replica connected to your Multi-AZ master database and generate reports by querying the Read Replica.
- D. Generate the reports by querying the ElastiCache database caching tier. 

<details><summary>Answer:</summary><p>
[C]

Categories:
[S3, RDS, ElastiCache]

Explanation:

Question 1@http://jayendrapatil.com/aws-rds-replication-multi-az-read-replica/

B: Standby instance cannot be used as a scaling solution

D: ElasticCache does not maintain full data and is simply a caching solution

</p></details><hr>

### Question 2:

A company is deploying a new two-tier web application in AWS. The company has limited staff and requires high availability, and the application requires complex queries and table joins. Which configuration provides the solution for the company’s requirements?

- A. MySQL Installed on two Amazon EC2 Instances in a single Availability Zone 
- B. Amazon RDS for MySQL with Multi-AZ
- C. Amazon ElastiCache 
- D. Amazon DynamoDB 

<details><summary>Answer:</summary><p>
[B]

Categories:
[RDS, EC2, ElastiCache, DynamoDB]

Explanation:

Question 2@http://jayendrapatil.com/aws-rds-replication-multi-az-read-replica/

A: does not provide High Availaility out of the box

C: Just a caching solution

D: Not suitable for complex queries and joins

</p></details><hr>

### Question 3:

Your company is getting ready to do a major public announcement of a social media site on AWS. The website is running on EC2 instances deployed across multiple Availability Zones with a Multi-AZ RDS MySQL Extra Large DB Instance. The site performs a high number of small reads and writes per second and relies on an eventual consistency model. After comprehensive tests you discover that there is read contention on RDS MySQL. Which are the best approaches to meet these requirements? (Choose 2 answers)

- A. Deploy ElastiCache in-memory cache running in each availability zone
- B. Implement sharding to distribute load to multiple RDS MySQL instances 
- C. Increase the RDS MySQL Instance size and Implement provisioned IOPS 
- D. Add an RDS MySQL read replica in each availability zone

<details><summary>Answer:</summary><p>
[A, D]

Categories:
[RDS, EC2, ElastiCache, EBS]

Explanation:

Question 3@http://jayendrapatil.com/aws-rds-replication-multi-az-read-replica/

B: this is only a read contention, the writes work fine

C: not scalable this is only a read contention, the writes work fine

</p></details><hr>

### Question 4:

Your company has HQ in Tokyo and branch offices all over the world and is using logistics software with a multi-regional deployment on AWS in Japan, Europe and US. The logistic software has a 3-tier architecture and currently uses MySQL 5.6 for data persistence. Each region has deployed its own database. In the HQ region you run an hourly batch process reading data from every region to compute cross-regional reports that are sent by email to all offices this batch process must be completed as fast as possible to quickly optimize logistics. How do you build the database architecture in order to meet the requirements?

- A. For each regional deployment, use RDS MySQL with a master in the region and a read replica in the HQ region
- B. For each regional deployment, use MySQL on EC2 with a master in the region and send hourly EBS snapshots to the HQ region
- C. For each regional deployment, use RDS MySQL with a master in the region and send hourly RDS snapshots to the HQ region
- D. For each regional deployment, use MySQL on EC2 with a master in the region and use S3 to copy data files hourly to the HQ region
- E. Use Direct Connect to connect all regional MySQL deployments to the HQ region and reduce network latency for the batch process

<details><summary>Answer:</summary><p>
[A]

Categories:
[S3, SES, RDS, EC2, EBS, Direct Connect]

Explanation:

Question 4@http://jayendrapatil.com/aws-rds-replication-multi-az-read-replica/

</p></details><hr>

### Question 5:

What would happen to an RDS (Relational Database Service) multi-Availability Zone deployment if the primary DB instance fails?

- A. IP of the primary DB Instance is switched to the standby DB Instance.
- B. A new DB instance is created in the standby availability zone.
- C. The canonical name record (CNAME) is changed from primary to standby.
- D. The RDS (Relational Database Service) DB instance reboots.

<details><summary>Answer:</summary><p>
[C]

Categories:
[RDS]

Explanation:

Question 5@http://jayendrapatil.com/aws-rds-replication-multi-az-read-replica/

</p></details><hr>

### Question 6:

Your business is building a new application that will store its entire customer database on a RDS MySQL database, and will have various applications and users that will query that data for different purposes. Large analytics jobs on the database are likely to cause other applications to not be able to get the query results they need to, before time out. Also, as your data grows, these analytics jobs will start to take more time, increasing the negative effect on the other applications. How do you solve the contention issues between these different workloads on the same data?

- A. Enable Multi-AZ mode on the RDS instance
- B. Use ElastiCache to offload the analytics job data
- C. Create RDS Read-Replicas for the analytics work
- D. Run the RDS instance on the largest size possible

<details><summary>Answer:</summary><p>
[C]

Categories:
[SES, RDS, ElastiCache]

Explanation:

Question 6@http://jayendrapatil.com/aws-rds-replication-multi-az-read-replica/

</p></details><hr>

### Question 7:

Will my standby RDS instance be in the same Availability Zone as my primary?

- A. Only for Oracle RDS types
- B. Yes
- C. Only if configured at launch
- D. No

<details><summary>Answer:</summary><p>
[D]

Categories:
[RDS]

Explanation:

Question 7@http://jayendrapatil.com/aws-rds-replication-multi-az-read-replica/

</p></details><hr>

### Question 8:

Is creating a Read Replica of another Read Replica supported?

- A. Only in certain regions
- B. Only with MySQL based RDS
- C. Only for Oracle RDS types
- D. No

<details><summary>Answer:</summary><p>
[B]

Categories:
[RDS]

Explanation:

Question 8@http://jayendrapatil.com/aws-rds-replication-multi-az-read-replica/

</p></details><hr>

### Question 9:

A user is planning to set up the Multi-AZ feature of RDS. Which of the below mentioned conditions won’t take advantage of the Multi-AZ feature?

- A. Availability zone outage
- B. A manual failover of the DB instance using Reboot with failover option
- C. Region outage
- D. When the user changes the DB instance’s server type

<details><summary>Answer:</summary><p>
[C]

Categories:
[RDS]

Explanation:

Question 9@http://jayendrapatil.com/aws-rds-replication-multi-az-read-replica/

</p></details><hr>

### Question 10:

When you run a DB Instance as a Multi-AZ deployment, the “_____” serves database writes and reads

- A. secondary
- B. backup
- C. stand by
- D. primary

<details><summary>Answer:</summary><p>
[D]

Categories:
[]

Explanation:

Question 10@http://jayendrapatil.com/aws-rds-replication-multi-az-read-replica/

</p></details><hr>

### Question 11:

When running my DB Instance as a Multi-AZ deployment, can I use the standby for read or write operations?

- A. Yes
- B. Only with MSSQL based RDS
- C. Only for Oracle RDS instances
- D. No

<details><summary>Answer:</summary><p>
[D]

Categories:
[RDS]

Explanation:

Question 11@http://jayendrapatil.com/aws-rds-replication-multi-az-read-replica/

</p></details><hr>

### Question 12:

Read Replicas require a transactional storage engine and are only supported for the _________ storage engine

- A. OracleISAM
- B. MSSQLDB
- C. InnoDB
- D. MyISAM

<details><summary>Answer:</summary><p>
[C]

Categories:
[]

Explanation:

Question 12@http://jayendrapatil.com/aws-rds-replication-multi-az-read-replica/

</p></details><hr>

### Question 13:

A user is configuring the Multi-AZ feature of an RDS DB. The user came to know that this RDS DB does not use the AWS technology, but uses server mirroring to achieve replication. Which DB is the user using right now?

- A. MySQL
- B. Oracle
- C. MS SQL
- D. PostgreSQL

<details><summary>Answer:</summary><p>
[C]

Categories:
[SES, RDS]

Explanation:

Question 13@http://jayendrapatil.com/aws-rds-replication-multi-az-read-replica/

</p></details><hr>

### Question 14:

If I have multiple Read Replicas for my master DB Instance and I promote one of them, what happens to the rest of the Read Replicas?

- A. The remaining Read Replicas will still replicate from the older master DB Instance
- B. The remaining Read Replicas will be deleted
- C. The remaining Read Replicas will be combined to one read replica

<details><summary>Answer:</summary><p>
[A]

Categories:
[]

Explanation:

Question 14@http://jayendrapatil.com/aws-rds-replication-multi-az-read-replica/

</p></details><hr>

### Question 15:

If you have chosen Multi-AZ deployment, in the event of a planned or unplanned outage of your primary DB Instance, Amazon RDS automatically switches to the standby replica. The automatic failover mechanism simply changes the ______ record of the main DB Instance to point to the standby DB Instance.

- A. DNAME
- B. CNAME
- C. TXT
- D. MX

<details><summary>Answer:</summary><p>
[B]

Categories:
[RDS]

Explanation:

Question 15@http://jayendrapatil.com/aws-rds-replication-multi-az-read-replica/

</p></details><hr>

### Question 16:

When automatic failover occurs, Amazon RDS will emit a DB Instance event to inform you that automatic failover occurred. You can use the _____ to return information about events related to your DB Instance

- A. FetchFailure
- B. DescriveFailure
- C. DescribeEvents
- D. FetchEvents

<details><summary>Answer:</summary><p>
[C]

Categories:
[RDS]

Explanation:

Question 16@http://jayendrapatil.com/aws-rds-replication-multi-az-read-replica/

</p></details><hr>

### Question 17:

The new DB Instance that is created when you promote a Read Replica retains the backup window period.

- A. TRUE
- B. FALSE

<details><summary>Answer:</summary><p>
[A]

Categories:
[]

Explanation:

Question 17@http://jayendrapatil.com/aws-rds-replication-multi-az-read-replica/

</p></details><hr>

### Question 18:

Will I be alerted when automatic failover occurs?

- A. Only if SNS configured
- B. No
- C. Yes
- D. Only if Cloudwatch configured

<details><summary>Answer:</summary><p>
[A]

Categories:
[CloudWatch, SNS]

Explanation:

Question 18@http://jayendrapatil.com/aws-rds-replication-multi-az-read-replica/

</p></details><hr>

### Question 19:

Can I initiate a “forced failover” for my MySQL Multi-AZ DB Instance deployment?

- A. Only in certain regions
- B. Only in VPC
- C. Yes
- D. No

<details><summary>Answer:</summary><p>
[C]

Categories:
[VPC]

Explanation:

Question 19@http://jayendrapatil.com/aws-rds-replication-multi-az-read-replica/

</p></details><hr>

### Question 20:

A user is accessing RDS from an application. The user has enabled the Multi-AZ feature with the MS SQL RDS DB. During a planned outage how will AWS ensure that a switch from DB to a standby replica will not affect access to the application?

- A. RDS will have an internal IP which will redirect all requests to the new DB
- B. RDS uses DNS to switch over to standby replica for seamless transition
- C. The switch over changes Hardware so RDS does not need to worry about access
- D. RDS will have both the DBs running independently and the user has to manually switch over

<details><summary>Answer:</summary><p>
[B]

Categories:
[SES, RDS]

Explanation:

Question 20@http://jayendrapatil.com/aws-rds-replication-multi-az-read-replica/

</p></details><hr>

### Question 21:

Which of the following is part of the failover process for a Multi-AZ Amazon Relational Database Service (RDS) instance?

- A. The failed RDS DB instance reboots.
- B. The IP of the primary DB instance is switched to the standby DB instance.
- C. The DNS record for the RDS endpoint is changed from primary to standby.
- D. A new DB instance is created in the standby availability zone.

<details><summary>Answer:</summary><p>
[C]

Categories:
[RDS]

Explanation:

Question 21@http://jayendrapatil.com/aws-rds-replication-multi-az-read-replica/

</p></details><hr>

### Question 22:

Which of these is not a reason a Multi-AZ RDS instance will failover?

- A. An Availability Zone outage
- B. A manual failover of the DB instance was initiated using Reboot with failover
- C. To autoscale to a higher instance class 
- D. Master database corruption occurs
- E. The primary DB instance fails

<details><summary>Answer:</summary><p>
[D]

Categories:
[RDS]

Explanation:

Question 22@http://jayendrapatil.com/aws-rds-replication-multi-az-read-replica/

C: https://aws.amazon.com/rds/details/multi-az/

</p></details><hr>

### Question 23:

You need to scale an RDS deployment. You are operating at 10% writes and 90% reads, based on your logging. How best can you scale this in a simple way?

- A. Create a second master RDS instance and peer the RDS groups.
- B. Cache all the database responses on the read side with CloudFront.
- C. Create read replicas for RDS since the load is mostly reads.
- D. Create a Multi-AZ RDS installs and route read traffic to standby.

<details><summary>Answer:</summary><p>
[C]

Categories:
[SES, RDS, CloudFront]

Explanation:

Question 23@http://jayendrapatil.com/aws-rds-replication-multi-az-read-replica/

</p></details><hr>

### Question 24:

How does Amazon RDS multi Availability Zone model work?

- A. A second, standby database is deployed and maintained in a different availability zone from master, using synchronous replication.
- B. A second, standby database is deployed and maintained in a different availability zone from master using asynchronous replication.
- C. A second, standby database is deployed and maintained in a different region from master using asynchronous replication.
- D. A second, standby database is deployed and maintained in a different region from master using synchronous replication.

<details><summary>Answer:</summary><p>
[A]

Categories:
[RDS]

Explanation:

Question 24@http://jayendrapatil.com/aws-rds-replication-multi-az-read-replica/

A: http://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Concepts.MultiAZ.html

</p></details><hr>

### Question 25:

A customer is running an application in US-West (Northern California) region and wants to setup disaster recovery failover to the Asian Pacific (Singapore) region. The customer is interested in achieving a low Recovery Point Objective (RPO) for an Amazon RDS multi-AZ MySQL database instance. Which approach is best suited to this need?

- A. Synchronous replication
- B. Asynchronous replication
- C. Route53 health checks
- D. Copying of RDS incremental snapshots

<details><summary>Answer:</summary><p>
[B]

Categories:
[RDS]

Explanation:

Question 25@http://jayendrapatil.com/aws-rds-replication-multi-az-read-replica/

</p></details><hr>

### Question 26:

A user is using a small MySQL RDS DB. The user is experiencing high latency due to the Multi AZ feature. Which of the below mentioned options may not help the user in this situation?

- A. Schedule the automated back up in non-working hours
- B. Use a large or higher size instance
- C. Use PIOPS
- D. Take a snapshot from standby Replica

<details><summary>Answer:</summary><p>
[D]

Categories:
[RDS]

Explanation:

Question 26@http://jayendrapatil.com/aws-rds-replication-multi-az-read-replica/

</p></details><hr>

### Question 27:

Are Reserved Instances available for Multi-AZ Deployments?

- A. Only for Cluster Compute instances
- B. Yes for all instance types
- C. Only for M3 instance types

<details><summary>Answer:</summary><p>
[B]

Categories:
[]

Explanation:

Question 27@http://jayendrapatil.com/aws-rds-replication-multi-az-read-replica/

</p></details><hr>

### Question 28:

My Read Replica appears “stuck” after a Multi-AZ failover and is unable to obtain or apply updates from the source DB Instance. What do I do?

- A. You will need to delete the Read Replica and create a new one to replace it.
- B. You will need to disassociate the DB Engine and re associate it.
- C. The instance should be deployed to Single AZ and then moved to Multi- AZ once again
- D. You will need to delete the DB Instance and create a new one to replace it.

<details><summary>Answer:</summary><p>
[A]

Categories:
[]

Explanation:

Question 28@http://jayendrapatil.com/aws-rds-replication-multi-az-read-replica/

</p></details><hr>

### Question 29:

What is the charge for the data transfer incurred in replicating data between your primary and standby?

- A. No charge. It is free.
- B. Double the standard data transfer charge
- C. Same as the standard data transfer charge
- D. Half of the standard data transfer charge

<details><summary>Answer:</summary><p>
[A]

Categories:
[]

Explanation:

Question 29@http://jayendrapatil.com/aws-rds-replication-multi-az-read-replica/

</p></details><hr>

### Question 30:

A user has enabled the Multi AZ feature with the MS SQL RDS database server. Which of the below mentioned statements will help the user understand the Multi AZ feature better?

- A. In a Multi AZ, AWS runs two DBs in parallel and copies the data asynchronously to the replica copy
- B. In a Multi AZ, AWS runs two DBs in parallel and copies the data synchronously to the replica copy
- C. In a Multi AZ, AWS runs just one DB but copies the data synchronously to the standby replica
- D. AWS MS SQL does not support the Multi AZ feature

<details><summary>Answer:</summary><p>
[C]

Categories:
[RDS]

Explanation:

Question 30@http://jayendrapatil.com/aws-rds-replication-multi-az-read-replica/

</p></details><hr>

### Question 31:

A company is running a batch analysis every hour on their main transactional DB running on an RDS MySQL instance to populate their central Data Warehouse running on Redshift. During the execution of the batch their transactional applications are very slow. When the batch completes they need to update the top management dashboard with the new data. The dashboard is produced by another system running on-premises that is currently started when a manually-sent email notifies that an update is required The on-premises system cannot be modified because is managed by another team. How would you optimize this scenario to solve performance issues and automate the process as much as possible?

- A. Replace RDS with Redshift for the batch analysis and SNS to notify the on-premises system to update the dashboard
- B. Replace RDS with Redshift for the batch analysis and SQS to send a message to the on-premises system to update the dashboard
- C. Create an RDS Read Replica for the batch analysis and SNS to notify me on-premises system to update the dashboard
- D. Create an RDS Read Replica for the batch analysis and SQS to send a message to the on-premises system to update the dashboard.

<details><summary>Answer:</summary><p>
[C]

Categories:
[SES, RDS, SQS, SNS, Redshift]

Explanation:

Question 31@http://jayendrapatil.com/aws-rds-replication-multi-az-read-replica/

</p></details><hr>

