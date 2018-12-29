### Question 1:

What is Amazon Glacier?

- A. You mean Amazon “Iceberg”: it’s a low-cost storage service.
- B. A security tool that allows to “freeze” an EBS volume and perform computer forensics on it.
- C. A low-cost storage service that provides secure and durable storage for data archiving and backup
- D. It’s a security tool that allows to “freeze” an EC2 instance and perform computer forensics on it.

<details><summary>Answer:</summary><p>
[C]

Categories:
[Glacier, EC2, EBS]

Explanation:

Question 1@http://jayendrapatil.com/aws-glacier/

</p></details><hr>

### Question 2:

Amazon Glacier is designed for: (Choose 2 answers)

- A. Active database storage
- B. Infrequently accessed data
- C. Data archives
- D. Frequently accessed data
- E. Cached session data

<details><summary>Answer:</summary><p>
[B, C]

Categories:
[SES, Glacier]

Explanation:

Question 2@http://jayendrapatil.com/aws-glacier/

</p></details><hr>

### Question 3:

An organization is generating digital policy files which are required by the admins for verification. Once the files are verified they may not be required in the future unless there is some compliance issue. If the organization wants to save them in a cost effective way, which is the best possible solution?

- A. AWS RRS
- B. AWS S3
- C. AWS RDS
- D. AWS Glacier

<details><summary>Answer:</summary><p>
[D]

Categories:
[S3, RDS, Glacier]

Explanation:

Question 3@http://jayendrapatil.com/aws-glacier/

</p></details><hr>

### Question 4:

A user has moved an object to Glacier using the life cycle rules. The user requests to restore the archive after 6 months. When the restore request is completed the user accesses that archive. Which of the below mentioned statements is not true in this condition?

- A. The archive will be available as an object for the duration specified by the user during the restoration request
- B. The restored object’s storage class will be RRS
- C. The user can modify the restoration period only by issuing a new restore request with the updated period
- D. The user needs to pay storage for both RRS (restored) and Glacier (Archive) Rates

<details><summary>Answer:</summary><p>
[B]

Categories:
[SES, Glacier]

Explanation:

Question 4@http://jayendrapatil.com/aws-glacier/

B: http://docs.aws.amazon.com/AmazonS3/latest/dev/restoring-objects.html

B: After the object is restored the storage class still remains GLACIER.

</p></details><hr>

### Question 5:

To meet regulatory requirements, a pharmaceuticals company needs to archive data after a drug trial test is concluded. Each drug trial test may generate up to several thousands of files, with compressed file sizes ranging from 1 byte to 100MB. Once archived, data rarely needs to be restored, and on the rare occasion when restoration is needed, the company has 24 hours to restore specific files that match certain metadata. Searches must be possible by numeric file ID, drug name, participant names, date ranges, and other metadata. Which is the most cost-effective architectural approach that can meet the requirements?

- A. Store individual files in Amazon Glacier, using the file ID as the archive name. When restoring data, query the Amazon Glacier vault for files matching the search criteria. 
- B. Store individual files in Amazon S3, and store search metadata in an Amazon Relational Database Service (RDS) multi-AZ database. Create a lifecycle rule to move the data to Amazon Glacier after a certain number of days. When restoring data, query the Amazon RDS database for files matching the search criteria, and move the files matching the search criteria back to S3 Standard class. 
- C. Store individual files in Amazon Glacier, and store the search metadata in an Amazon RDS multi-AZ database. When restoring data, query the Amazon RDS database for files matching the search criteria, and retrieve the archive name that matches the file ID returned from the database query. 
- D. First, compress and then concatenate all files for a completed drug trial test into a single Amazon Glacier archive. Store the associated byte ranges for the compressed files along with other search metadata in an Amazon RDS database with regular snapshotting. When restoring data, query the database for files that match the search criteria, and create restored files from the retrieved byte ranges.
- E. Store individual compressed files and search metadata in Amazon Simple Storage Service (S3). Create a lifecycle rule to move the data to Amazon Glacier, after a certain number of days. When restoring data, query the Amazon S3 bucket for files matching the search criteria, and retrieve the file to S3 reduced redundancy in order to move it back to S3 Standard class. 

<details><summary>Answer:</summary><p>
[D]

Categories:
[S3, RDS, Glacier]

Explanation:

Question 5@http://jayendrapatil.com/aws-glacier/

A: Individual files are expensive and does not allow searching by participant names etc

B: As the data is not needed can be stored to Glacier directly and the data need not be moved back to S3 standard

C: Individual files and Multi-AZ is expensive

E: Once the data is moved from S3 to Glacier the metadata is lost, as Glacier does not have metadata and must be maintained externally

</p></details><hr>

### Question 6:

A user is uploading archives to Glacier. The user is trying to understand key Glacier resources. Which of the below mentioned options is not a Glacier resource?

- A. Notification configuration
- B. Archive ID
- C. Job
- D. Archive

<details><summary>Answer:</summary><p>
[B]

Categories:
[Glacier]

Explanation:

Question 6@http://jayendrapatil.com/aws-glacier/

</p></details><hr>

