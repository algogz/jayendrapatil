### Question 1:

What does RRS stand for when talking about S3?

- A. Redundancy Removal System
- B. Relational Rights Storage
- C. Regional Rights Standard
- D. Reduced Redundancy Storage

<details><summary>Answer:</summary><p>
[D]

Categories:
[S3]

Explanation:

Question 1@http://jayendrapatil.com/aws-s3-storage-classes/

</p></details><hr>

### Question 2:

What is the durability of S3 RRS?

- A. 99.99%
- B. 99.95%
- C. 99.995%
- D. 99.999999999%

<details><summary>Answer:</summary><p>
[A]

Categories:
[S3]

Explanation:

Question 2@http://jayendrapatil.com/aws-s3-storage-classes/

</p></details><hr>

### Question 3:

What is the Reduced Redundancy option in Amazon S3?

- A. Less redundancy for a lower cost
- B. It doesn’t exist in Amazon S3, but in Amazon EBS.
- C. It allows you to destroy any copy of your files outside a specific jurisdiction.
- D. It doesn’t exist at all

<details><summary>Answer:</summary><p>
[A]

Categories:
[S3, EBS]

Explanation:

Question 3@http://jayendrapatil.com/aws-s3-storage-classes/

</p></details><hr>

### Question 4:

An application is generating a log file every 5 minutes. The log file is not critical but may be required only for verification in case of some major issue. The file should be accessible over the internet whenever required. Which of the below mentioned options is a best possible storage solution for it?

- A. AWS S3
- B. AWS Glacier
- C. AWS RDS
- D. AWS S3 RRS

<details><summary>Answer:</summary><p>
[D]

Categories:
[S3, RDS, Glacier]

Explanation:

Question 4@http://jayendrapatil.com/aws-s3-storage-classes/

D: Reduced Redundancy Storage (RRS) is an Amazon S3 storage option that enables customers to store noncritical, reproducible data at lower levels of redundancy than Amazon S3’s standard storage. RRS is designed to sustain the loss of data in a single facility.

</p></details><hr>

### Question 5:

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

Question 5@http://jayendrapatil.com/aws-s3-storage-classes/

B: http://docs.aws.amazon.com/AmazonS3/latest/dev/restoring-objects.html

B: After the object is restored the storage class still remains GLACIER.

</p></details><hr>

### Question 6:

Your department creates regular analytics reports from your company’s log files. All log data is collected in Amazon S3 and processed by daily Amazon Elastic Map Reduce (EMR) jobs that generate daily PDF reports and aggregated tables in CSV format for an Amazon Redshift data warehouse. Your CFO requests that you optimize the cost structure for this system. Which of the following alternatives will lower costs without compromising average performance of the system or data integrity for the raw data? [PROFESSIONAL]

- A. Use reduced redundancy storage (RRS) for PDF and CSV data in Amazon S3. Add Spot instances to Amazon EMR jobs. Use Reserved Instances for Amazon Redshift. 
- B. Use reduced redundancy storage (RRS) for all data in S3. Use a combination of Spot instances and Reserved Instances for Amazon EMR jobs. Use Reserved instances for Amazon Redshift
- C. Use reduced redundancy storage (RRS) for all data in Amazon S3. Add Spot Instances to Amazon EMR jobs. Use Reserved Instances for Amazon Redshift 
- D. Use reduced redundancy storage (RRS) for PDF and CSV data in S3. Add Spot Instances to EMR jobs. Use Spot Instances for Amazon Redshift. 

<details><summary>Answer:</summary><p>
[B]

Categories:
[S3, EMR, Redshift]

Explanation:

Question 6@http://jayendrapatil.com/aws-s3-storage-classes/

A: Spot instances impacts performance

B: Combination of the Spot and reserved with guarantee performance and help reduce cost. Also, RRS would reduce cost and guarantee data integrity, which is different from data durability

C: Spot instances impacts performance

D: Spot instances impacts performance

</p></details><hr>

### Question 7:

Which of the below mentioned options can be a good use case for storing content in AWS RRS?

- A. Storing mission critical data Files
- B. Storing infrequently used log files
- C. Storing a video file which is not reproducible
- D. Storing image thumbnails

<details><summary>Answer:</summary><p>
[D]

Categories:
[]

Explanation:

Question 7@http://jayendrapatil.com/aws-s3-storage-classes/

</p></details><hr>

### Question 8:

A newspaper organization has an on-premises application which allows the public to search its back catalogue and retrieve individual newspaper pages via a website written in Java. They have scanned the old newspapers into JPEGs (approx. 17TB) and used Optical Character Recognition (OCR) to populate a commercial search product. The hosting platform and software is now end of life and the organization wants to migrate its archive to AWS and produce a cost efficient architecture and still be designed for availability and durability. Which is the most appropriate? [PROFESSIONAL]

- A. Use S3 with reduced redundancy to store and serve the scanned files, install the commercial search application on EC2 Instances and configure with auto-scaling and an Elastic Load Balancer. 
- B. Model the environment using CloudFormation. Use an EC2 instance running Apache webserver and an open source search application, stripe multiple standard EBS volumes together to store the JPEGs and search index. 
- C. Use S3 with standard redundancy to store and serve the scanned files, use CloudSearch for query processing, and use Elastic Beanstalk to host the website across multiple availability zones.
- D. Use a single-AZ RDS MySQL instance to store the search index and the JPEG images use an EC2 instance to serve the website and translate user queries into SQL. 
- E. Use a CloudFront download distribution to serve the JPEGs to the end users and Install the current commercial search product, along with a Java Container for the website on EC2 instances and use Route53 with DNS round-robin. 

<details><summary>Answer:</summary><p>
[C]

Categories:
[S3, SES, RDS, CloudFront, EC2, EBS, CloudFormation, CloudSearch, Elastic Beanstalk]

Explanation:

Question 8@http://jayendrapatil.com/aws-s3-storage-classes/

A: RRS impacts durability and commercial search would add to cost

B: Using EBS is not cost effective for storing files

C: Standard S3 and Elastic Beanstalk provides availability and durability, Standard S3 and CloudSearch provides cost effective storage and search

D: RDS is not ideal and cost effective to store files, Single AZ impacts availability

E: CloudFront needs a source and using commercial search product is not cost effective

</p></details><hr>

### Question 9:

A research scientist is planning for the one-time launch of an Elastic MapReduce cluster and is encouraged by her manager to minimize the costs. The cluster is designed to ingest 200TB of genomics data with a total of 100 Amazon EC2 instances and is expected to run for around four hours. The resulting data set must be stored temporarily until archived into an Amazon RDS Oracle instance. Which option will help save the most money while meeting requirements? [PROFESSIONAL]

- A. Store ingest and output files in Amazon S3. Deploy on-demand for the master and core nodes and spot for the task nodes.
- B. Optimize by deploying a combination of on-demand, RI and spot-pricing models for the master, core and task nodes. Store ingest and output files in Amazon S3 with a lifecycle policy that archives them to Amazon Glacier. 
- C. Store the ingest files in Amazon S3 RRS and store the output files in S3. Deploy Reserved Instances for the master and core nodes and on-demand for the task nodes. 
- D. Deploy on-demand master, core and task nodes and store ingest and output files in Amazon S3 RRS 

<details><summary>Answer:</summary><p>
[A]

Categories:
[S3, RDS, Glacier, EC2]

Explanation:

Question 9@http://jayendrapatil.com/aws-s3-storage-classes/

B: Master and Core must be RI or On Demand. Cannot be Spot

C: Need better durability for ingest file. Spot instances can be used for task nodes for cost saving.

D: Input must be in S3 standard

</p></details><hr>

