### Question 1:

What does Amazon S3 stand for?

- A. Simple Storage Solution.
- B. Storage Storage Storage (triple redundancy Storage).
- C. Storage Server Solution.
- D. Simple Storage Service

<details><summary>Answer:</summary><p>
[D]

Categories:
[S3]

Explanation:

Question 1@http://jayendrapatil.com/aws-simple-storage-service-s3-overview/

</p></details><hr>

### Question 2:

What are characteristics of Amazon S3? Choose 2 answers

- A. Objects are directly accessible via a URL
- B. S3 should be used to host a relational database
- C. S3 allows you to store objects or virtually unlimited size
- D. S3 allows you to store virtually unlimited amounts of data
- E. S3 offers Provisioned IOPS

<details><summary>Answer:</summary><p>
[A, D]

Categories:
[S3]

Explanation:

Question 2@http://jayendrapatil.com/aws-simple-storage-service-s3-overview/

</p></details><hr>

### Question 3:

You are building an automated transcription service in which Amazon EC2 worker instances process an uploaded audio file and generate a text file. You must store both of these files in the same durable storage until the text file is retrieved. You do not know what the storage capacity requirements are. Which storage option is both cost-efficient and scalable?

- A. Multiple Amazon EBS volume with snapshots
- B. A single Amazon Glacier vault
- C. A single Amazon S3 bucket
- D. Multiple instance stores

<details><summary>Answer:</summary><p>
[C]

Categories:
[S3, Glacier, EC2, EBS, Instance Store]

Explanation:

Question 3@http://jayendrapatil.com/aws-simple-storage-service-s3-overview/

</p></details><hr>

### Question 4:

A user wants to upload a complete folder to AWS S3 using the S3 Management console. How can the user perform this activity?

- A. Just drag and drop the folder using the flash tool provided by S3
- B. Use the Enable Enhanced Folder option from the S3 console while uploading objects
- C. The user cannot upload the whole folder in one go with the S3 management console
- D. Use the Enable Enhanced Uploader option from the S3 console while uploading objects

<details><summary>Answer:</summary><p>
[D]

Categories:
[S3]

Explanation:

Question 4@http://jayendrapatil.com/aws-simple-storage-service-s3-overview/

D: NOTE – Its no longer supported by AWS

</p></details><hr>

### Question 5:

A media company produces new video files on-premises every day with a total size of around 100GB after compression. All files have a size of 1-2 GB and need to be uploaded to Amazon S3 every night in a fixed time window between 3am and 5am. Current upload takes almost 3 hours, although less than half of the available bandwidth is used. What step(s) would ensure that the file uploads are able to complete in the allotted time window?

- A. Increase your network bandwidth to provide faster throughput to S3
- B. Upload the files in parallel to S3 using mulipart upload
- C. Pack all files into a single archive, upload it to S3, then extract the files in AWS
- D. Use AWS Import/Export to transfer the video files

<details><summary>Answer:</summary><p>
[B]

Categories:
[S3, SES]

Explanation:

Question 5@http://jayendrapatil.com/aws-simple-storage-service-s3-overview/

</p></details><hr>

### Question 6:

A company is deploying a two-tier, highly available web application to AWS. Which service provides durable storage for static content while utilizing lower Overall CPU resources for the web tier?

- A. Amazon EBS volume
- B. Amazon S3
- C. Amazon EC2 instance store
- D. Amazon RDS instance

<details><summary>Answer:</summary><p>
[B]

Categories:
[S3, RDS, EC2, EBS, Instance Store]

Explanation:

Question 6@http://jayendrapatil.com/aws-simple-storage-service-s3-overview/

</p></details><hr>

### Question 7:

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

Question 7@http://jayendrapatil.com/aws-simple-storage-service-s3-overview/

</p></details><hr>

### Question 8:

When you put objects in Amazon S3, what is the indication that an object was successfully stored?

- A. Each S3 account has a special bucket named_s3_logs. Success codes are written to this bucket with a timestamp and checksum.
- B. A success code is inserted into the S3 object metadata.
- C. A HTTP 200 result code and MD5 checksum, taken together, indicate that the operation was successful.
- D. Amazon S3 is engineered for 99.999999999% durability. Therefore there is no need to confirm that data was inserted.

<details><summary>Answer:</summary><p>
[C]

Categories:
[S3]

Explanation:

Question 8@http://jayendrapatil.com/aws-simple-storage-service-s3-overview/

</p></details><hr>

### Question 9:

You have private video content in S3 that you want to serve to subscribed users on the Internet. User IDs, credentials, and subscriptions are stored in an Amazon RDS database. Which configuration will allow you to securely serve private content to your users?

- A. Generate pre-signed URLs for each user as they request access to protected S3 content
- B. Create an IAM user for each subscribed user and assign the GetObject permission to each IAM user
- C. Create an S3 bucket policy that limits access to your private content to only your subscribed users’ credentials
- D. Create a CloudFront Origin Identity user for your subscribed users and assign the GetObject permission to this user

<details><summary>Answer:</summary><p>
[A]

Categories:
[S3, RDS, CloudFront, IAM]

Explanation:

Question 9@http://jayendrapatil.com/aws-simple-storage-service-s3-overview/

</p></details><hr>

### Question 10:

You run an ad-supported photo sharing website using S3 to serve photos to visitors of your site. At some point you find out that other sites have been linking to the photos on your site, causing loss to your business. What is an effective method to mitigate this?

- A. Remove public read access and use signed URLs with expiry dates.
- B. Use CloudFront distributions for static content.
- C. Block the IPs of the offending websites in Security Groups.
- D. Store photos on an EBS volume of the web server.

<details><summary>Answer:</summary><p>
[A]

Categories:
[S3, CloudFront, EBS]

Explanation:

Question 10@http://jayendrapatil.com/aws-simple-storage-service-s3-overview/

</p></details><hr>

### Question 11:

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

Question 11@http://jayendrapatil.com/aws-simple-storage-service-s3-overview/

</p></details><hr>

### Question 12:

What is the maximum number of S3 buckets available per AWS Account?

- A. 100 Per region
- B. There is no Limit
- C. 100 Per Account 
- D. 500 Per Account
- E. 100 Per IAM User

<details><summary>Answer:</summary><p>
[C]

Categories:
[S3, IAM]

Explanation:

Question 12@http://jayendrapatil.com/aws-simple-storage-service-s3-overview/

C: http://docs.aws.amazon.com/AmazonS3/latest/dev/BucketRestrictions.html

</p></details><hr>

### Question 13:

Your customer needs to create an application to allow contractors to upload videos to Amazon Simple Storage Service (S3) so they can be transcoded into a different format. She creates AWS Identity and Access Management (IAM) users for her application developers, and in just one week, they have the application hosted on a fleet of Amazon Elastic Compute Cloud (EC2) instances. The attached IAM role is assigned to the instances. As expected, a contractor who authenticates to the application is given a pre-signed URL that points to the location for video upload. However, contractors are reporting that they cannot upload their videos. Which of the following are valid reasons for this behavior? Choose 2 answers { “Version”: “2012-10-17”, “Statement”: [ { “Effect”: “Allow”, “Action”: “s3:*”, “Resource”: “*” } ] }

- A. The IAM role does not explicitly grant permission to upload the object. 
- B. The contractorsˈ accounts have not been granted “write” access to the S3 bucket. 
- C. The application is not using valid security credentials to generate the pre-signed URL.
- D. The developers do not have access to upload objects to the S3 bucket. 
- E. The S3 bucket still has the associated default permissions. 
- F. The pre-signed URL has expired.

<details><summary>Answer:</summary><p>
[C, F]

Categories:
[S3, IAM, EC2]

Explanation:

Question 13@http://jayendrapatil.com/aws-simple-storage-service-s3-overview/

A: The role has all permissions for all activities on S3

B: using pre-signed urls the contractors account don’t need to have access but only the creator of the pre-signed urls

D: developers are not uploading the objects but its using pre-signed urls

E: does not matter as long as the user has permission to upload

</p></details><hr>

