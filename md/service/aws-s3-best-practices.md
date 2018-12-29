### Question 1:

A media company produces new video files on-premises every day with a total size of around 100GB after compression. All files have a size of 1-2 GB and need to be uploaded to Amazon S3 every night in a fixed time window between 3am and 5am. Current upload takes almost 3 hours, although less than half of the available bandwidth is used. What step(s) would ensure that the file uploads are able to complete in the allotted time window?

- A. Increase your network bandwidth to provide faster throughput to S3
- B. Upload the files in parallel to S3 using multipart upload
- C. Pack all files into a single archive, upload it to S3, then extract the files in AWS
- D. Use AWS Import/Export to transfer the video files

<details><summary>Answer:</summary><p>
[B]

Categories:
[S3, SES]

Explanation:

Question 1@http://jayendrapatil.com/aws-s3-best-practices/

</p></details><hr>

### Question 2:

You are designing a web application that stores static assets in an Amazon Simple Storage Service (S3) bucket. You expect this bucket to immediately receive over 150 PUT requests per second. What should you do to ensure optimal performance?

- A. Use multi-part upload.
- B. Add a random prefix to the key names.
- C. Amazon S3 will automatically manage performance at this scale.
- D. Use a predictable naming scheme, such as sequential numbers or date time sequences, in the key names

<details><summary>Answer:</summary><p>
[B]

Categories:
[S3]

Explanation:

Question 2@http://jayendrapatil.com/aws-s3-best-practices/

</p></details><hr>

### Question 3:

You have an application running on an Amazon Elastic Compute Cloud instance, that uploads 5 GB video objects to Amazon Simple Storage Service (S3). Video uploads are taking longer than expected, resulting in poor application performance. Which method will help improve performance of your application?

- A. Enable enhanced networking
- B. Use Amazon S3 multipart upload
- C. Leveraging Amazon CloudFront, use the HTTP POST method to reduce latency.
- D. Use Amazon Elastic Block Store Provisioned IOPs and use an Amazon EBS-optimized instance

<details><summary>Answer:</summary><p>
[B]

Categories:
[S3, CloudFront, EBS]

Explanation:

Question 3@http://jayendrapatil.com/aws-s3-best-practices/

</p></details><hr>

### Question 4:

Which of the following methods gives you protection against accidental loss of data stored in Amazon S3? (Choose 2)

- A. Set bucket policies to restrict deletes, and also enable versioning
- B. By default, versioning is enabled on a new bucket so you don’t have to worry about it 
- C. Build a secondary index of your keys to protect the data 
- D. Back up your bucket to a bucket owned by another AWS account for redundancy

<details><summary>Answer:</summary><p>
[A, D]

Categories:
[S3]

Explanation:

Question 4@http://jayendrapatil.com/aws-s3-best-practices/

B: Not enabled by default

C: improves performance only

</p></details><hr>

### Question 5:

A startup company hired you to help them build a mobile application that will ultimately store billions of image and videos in Amazon S3. The company is lean on funding, and wants to minimize operational costs, however, they have an aggressive marketing plan, and expect to double their current installation base every six months. Due to the nature of their business, they are expecting sudden and large increases to traffic to and from S3, and need to ensure that it can handle the performance needs of their application. What other information must you gather from this customer in order to determine whether S3 is the right option?

- A. You must know how many customers that company has today, because this is critical in understanding what their customer base will be in two years. 
- B. You must find out total number of requests per second at peak usage.
- C. You must know the size of the individual objects being written to S3 in order to properly design the key namespace. 
- D. In order to build the key namespace correctly, you must understand the total amount of storage needs for each S3 bucket. (

<details><summary>Answer:</summary><p>
[B]

Categories:
[S3, SES]

Explanation:

Question 5@http://jayendrapatil.com/aws-s3-best-practices/

A: No. of customers do not matter

C: Size does not relate to the key namespace design but the count does

D: S3 provided unlimited storage the key namespace design would depend on the number)

</p></details><hr>

### Question 6:

A document storage company is deploying their application to AWS and changing their business model to support both free tier and premium tier users. The premium tier users will be allowed to store up to 200GB of data and free tier customers will be allowed to store only 5GB. The customer expects that billions of files will be stored. All users need to be alerted when approaching 75 percent quota utilization and again at 90 percent quota use. To support the free tier and premium tier users, how should they architect their application?

- A. The company should utilize an amazon simple workflow service activity worker that updates the users data counter in amazon dynamo DB. The activity worker will use simple email service to send an email if the counter increases above the appropriate thresholds.
- B. The company should deploy an amazon relational data base service relational database with a store objects table that has a row for each stored object along with size of each object. The upload server will query the aggregate consumption of the user in questions (by first determining the files store by the user, and then querying the stored objects table for respective file sizes) and send an email via Amazon Simple Email Service if the thresholds are breached. 
- C. The company should write both the content length and the username of the files owner as S3 metadata for the object. They should then create a file watcher to iterate over each object and aggregate the size for each user and send a notification via Amazon Simple Queue Service to an emailing service if the storage threshold is exceeded. 
- D. The company should create two separated amazon simple storage service buckets one for data storage for free tier users and another for data storage for premium tier users. An amazon simple workflow service activity worker will query all objects for a given user based on the bucket the data is stored in and aggregate storage. The activity worker will notify the user via Amazon Simple Notification Service when necessary 

<details><summary>Answer:</summary><p>
[A]

Categories:
[S3, SES, SWF, SQS, SNS]

Explanation:

Question 6@http://jayendrapatil.com/aws-s3-best-practices/

B: Good Approach to use RDS but with so many objects might not be a good option

C: List operations on S3 not feasible

D: List operations on S3 not feasible as well as SNS does not address email requirement

</p></details><hr>

### Question 7:

Your company host a social media website for storing and sharing documents. the web application allow users to upload large files while resuming and pausing the upload as needed. Currently, files are uploaded to your php front end backed by Elastic Load Balancing and an autoscaling fleet of amazon elastic compute cloud (EC2) instances that scale upon average of bytes received (NetworkIn) After a file has been uploaded. it is copied to amazon simple storage service(S3). Amazon Ec2 instances use an AWS Identity and Access Management (AMI) role that allows Amazon s3 uploads. Over the last six months, your user base and scale have increased significantly, forcing you to increase the auto scaling groups Max parameter a few times. Your CFO is concerned about the rising costs and has asked you to adjust the architecture where needed to better optimize costs. Which architecture change could you introduce to reduce cost and still keep your web application secure and scalable?

- A. Replace the Autoscaling launch Configuration to include c3.8xlarge instances; those instances can potentially yield a network throughput of 10gbps. 
- B. Re-architect your ingest pattern, have the app authenticate against your identity provider as a broker fetching temporary AWS credentials from AWS Secure token service (GetFederation Token). Securely pass the credentials and s3 endpoint/prefix to your app. Implement client-side logic to directly upload the file to amazon s3 using the given credentials and S3 Prefix. 
- C. Re-architect your ingest pattern, and move your web application instances into a VPC public subnet. Attach a public IP address for each EC2 instance (using the auto scaling launch configuration settings). Use Amazon Route 53 round robin records set and http health check to DNS load balance the app request this approach will significantly reduce the cost by bypassing elastic load balancing. 
- D. Re-architect your ingest pattern, have the app authenticate against your identity provider as a broker fetching temporary AWS credentials from AWS Secure token service (GetFederation Token). Securely pass the credentials and s3 endpoint/prefix to your app. Implement client-side logic that used the S3 multipart upload API to directly upload the file to Amazon s3 using the given credentials and s3 Prefix.

<details><summary>Answer:</summary><p>
[D]

Categories:
[S3, RDS, EC2, ASG, EBS, VPC, Route 53, ELB]

Explanation:

Question 7@http://jayendrapatil.com/aws-s3-best-practices/

A: no info of current size and might increase cost

B: will not provide the ability to handle pause and restarts

C: ELB is not the bottleneck

D: multipart allows one to start uploading directly to S3 before the actual size is known or complete data is downloaded

</p></details><hr>

### Question 8:

If an application is storing hourly log files from thousands of instances from a high traffic web site, which naming scheme would give optimal performance on S3?

- A. Sequential
- B. instanceID_log-HH-DD-MM-YYYY
- C. instanceID_log-YYYY-MM-DD-HH
- D. HH-DD-MM-YYYY-log_instanceID
- E. YYYY-MM-DD-HH-log_instanceID

<details><summary>Answer:</summary><p>
[D]

Categories:
[S3]

Explanation:

Question 8@http://jayendrapatil.com/aws-s3-best-practices/

D: HH will give some randomness to start with instead of instaneId where the first characters would be i-

</p></details><hr>

