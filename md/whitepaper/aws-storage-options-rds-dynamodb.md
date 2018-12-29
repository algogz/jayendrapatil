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

Question 1@http://jayendrapatil.com/aws-storage-options-rds-dynamodb/

</p></details><hr>

### Question 2:

A client application requires operating system privileges on a relational database server. What is an appropriate configuration for highly available database architecture?

- A. A standalone Amazon EC2 instance
- B. Amazon RDS in a Multi-AZ configuration
- C. Amazon EC2 instances in a replication configuration utilizing a single Availability Zone
- D. Amazon EC2 instances in a replication configuration utilizing two different Availability Zones

<details><summary>Answer:</summary><p>
[D]

Categories:
[RDS, EC2]

Explanation:

Question 2@http://jayendrapatil.com/aws-storage-options-rds-dynamodb/

</p></details><hr>

### Question 3:

You are developing a new mobile application and are considering storing user preferences in AWS, which would provide a more uniform cross-device experience to users using multiple mobile devices to access the application. The preference data for each user is estimated to be 50KB in size. Additionally 5 million customers are expected to use the application on a regular basis. The solution needs to be cost-effective, highly available, scalable and secure, how would you design a solution to meet the above requirements?

- A. Setup an RDS MySQL instance in 2 availability zones to store the user preference data. Deploy a public facing application on a server in front of the database to manage security and access credentials
- B. Setup a DynamoDB table with an item for each user having the necessary attributes to hold the user preferences. The mobile application will query the user preferences directly from the DynamoDB table. Utilize STS. Web Identity Federation, and DynamoDB Fine Grained Access Control to authenticate and authorize access 
- C. Setup an RDS MySQL instance with multiple read replicas in 2 availability zones to store the user preference data .The mobile application will query the user preferences from the read replicas. Leverage the MySQL user management and access privilege system to manage security and access credentials.
- D. Store the user preference data in S3 Setup a DynamoDB table with an item for each user and an item attribute pointing to the user’ S3 object. The mobile application will retrieve the S3 URL from DynamoDB and then access the S3 object directly utilize STS, Web identity Federation, and S3 ACLs to authenticate and authorize access.

<details><summary>Answer:</summary><p>
[B]

Categories:
[S3, RDS, DynamoDB]

Explanation:

Question 3@http://jayendrapatil.com/aws-storage-options-rds-dynamodb/

B: DynamoDB provides high availability as it synchronously replicates data across three facilities within an AWS Region and scalability as it is designed to scale its provisioned throughput up or down while still remaining available. Also suitable for storing user preference data

</p></details><hr>

### Question 4:

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

Question 4@http://jayendrapatil.com/aws-storage-options-rds-dynamodb/

</p></details><hr>

### Question 5:

You are designing a file -sharing service. This service will have millions of files in it. Revenue for the service will come from fees based on how much storage a user is using. You also want to store metadata on each file, such as title, description and whether the object is public or private. How do you achieve all of these goals in a way that is economical and can scale to millions of users?

- A. Store all files in Amazon Simple Storage Service (53). Create a bucket for each user. Store metadata in the filename of each object, and access it with LIST commands against the S3 API.
- B. Store all files in Amazon 53. Create Amazon DynamoDB tables for the corresponding key -value pairs on the associated metadata, when objects are uploaded.
- C. Create a striped set of 4000 IOPS Elastic Load Balancing volumes to store the data. Use a database running in Amazon Relational Database Service (RDS) to store the metadata.
- D. Create a striped set of 4000 IOPS Elastic Load Balancing volumes to store the data. Create Amazon DynamoDB tables for the corresponding key-value pairs on the associated metadata, when objects are uploaded.

<details><summary>Answer:</summary><p>
[B]

Categories:
[S3, RDS, DynamoDB, ELB]

Explanation:

Question 5@http://jayendrapatil.com/aws-storage-options-rds-dynamodb/

</p></details><hr>

### Question 6:

Company ABCD has recently launched an online commerce site for bicycles on AWS. They have a “Product” DynamoDB table that stores details for each bicycle, such as, manufacturer, color, price, quantity and size to display in the online store. Due to customer demand, they want to include an image for each bicycle along with the existing details. Which approach below provides the least impact to provisioned throughput on the “Product” table?

- A. Serialize the image and store it in multiple DynamoDB tables
- B. Create an “Images” DynamoDB table to store the Image with a foreign key constraint to the “Product” table
- C. Add an image data type to the “Product” table to store the images in binary format
- D. Store the images in Amazon S3 and add an S3 URL pointer to the “Product” table item for each image

<details><summary>Answer:</summary><p>
[D]

Categories:
[S3, DynamoDB]

Explanation:

Question 6@http://jayendrapatil.com/aws-storage-options-rds-dynamodb/

</p></details><hr>

