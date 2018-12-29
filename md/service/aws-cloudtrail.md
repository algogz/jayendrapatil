### Question 1:

You currently operate a web application in the AWS US-East region. The application runs on an auto-scaled layer of EC2 instances and an RDS Multi-AZ database. Your IT security compliance officer has tasked you to develop a reliable and durable logging solution to track changes made to your EC2, IAM and RDS resources. The solution must ensure the integrity and confidentiality of your log data. Which of these solutions would you recommend?

- A. Create a new CloudTrail trail with one new S3 bucket to store the logs and with the global services option selected. Use IAM roles, S3 bucket policies and Multi Factor Authentication (MFA) Delete on the S3 bucket that stores your logs. ( )
- B. Create a new CloudTrail with one new S3 bucket to store the logs. Configure SNS to send log file delivery notifications to your management system. Use IAM roles and S3 bucket policies on the S3 bucket that stores your logs. 
- C. Create a new CloudTrail trail with an existing S3 bucket to store the logs and with the global services option selected Use S3 ACLs and Multi Factor Authentication (MFA) Delete on the S3 bucket that stores your logs. 
- D. Create three new CloudTrail trails with three new S3 buckets to store the logs one for the AWS Management console, one for AWS SDKs and one for command line tools. Use IAM roles and S3 bucket policies on the S3 buckets that store your logs 

<details><summary>Answer:</summary><p>
[A]

Categories:
[S3, RDS, IAM, EC2, SNS, CloudTrail]

Explanation:

Question 1@http://jayendrapatil.com/aws-cloudtrail/

A: Single New bucket with global services option for IAM and MFA delete for confidentiality

B: Missing Global Services for IAM

C: Existing bucket prevents confidentiality

D: 3 buckets not needed, Missing Global services options

</p></details><hr>

### Question 2:

Which of the following are true regarding AWS CloudTrail? Choose 3 answers

- A. CloudTrail is enabled globally
- B. was not enabled by default, however, it is enabled by default as per the latest
- C. CloudTrail is enabled on a per-region basis
- D. CloudTrail is enabled on a per-service basis 
- E. Logs can be delivered to a single Amazon S3 bucket for aggregation
- F. CloudTrail is enabled for all available services within a region. 
- G. Logs can only be processed and delivered to the region in which they are generated. 

<details><summary>Answer:</summary><p>
[A, B, C, E]

Categories:
[S3, CloudTrail]

Explanation:

Question 2@http://jayendrapatil.com/aws-cloudtrail/

A: it can be enabled for all regions and also per region basis

B: https://aws.amazon.com/blogs/aws/new-amazon-web-services-extends-cloudtrail-to-all-aws-customers/

B: CloudTrail is enabled by default 

C: it can be enabled for all regions and also per region basis

D: once enabled it is applicable for all the supported services, service can’t be selected

F: is enabled only for CloudTrail supported services

G: can be logged to bucket in any region

</p></details><hr>

### Question 3:

An organization has configured the custom metric upload with CloudWatch. The organization has given permission to its employees to upload data using CLI as well SDK. How can the user track the calls made to CloudWatch?

- A. The user can enable logging with CloudWatch which logs all the activities
- B. Use CloudTrail to monitor the API calls
- C. Create an IAM user and allow each user to log the data using the S3 bucket
- D. Enable detailed monitoring with CloudWatch

<details><summary>Answer:</summary><p>
[B]

Categories:
[S3, IAM, CloudWatch, CloudTrail]

Explanation:

Question 3@http://jayendrapatil.com/aws-cloudtrail/

</p></details><hr>

### Question 4:

A user is trying to understand the CloudWatch metrics for the AWS services. It is required that the user should first understand the namespace for the AWS services. Which of the below mentioned is not a valid namespace for the AWS services?

- A. AWS/StorageGateway
- B. AWS/CloudTrail ( )
- C. AWS/ElastiCache
- D. AWS/SWF

<details><summary>Answer:</summary><p>
[B]

Categories:
[SWF, CloudWatch, ElastiCache, CloudTrail]

Explanation:

Question 4@http://jayendrapatil.com/aws-cloudtrail/

B: http://docs.aws.amazon.com/AmazonCloudWatch/latest/DeveloperGuide/aws-namespaces.html

</p></details><hr>

### Question 5:

Your CTO thinks your AWS account was hacked. What is the only way to know for certain if there was unauthorized access and what they did, assuming your hackers are very sophisticated AWS engineers and doing everything they can to cover their tracks?

- A. Use CloudTrail Log File Integrity Validation
- B. Use AWS Config SNS Subscriptions and process events in real time.
- C. Use CloudTrail backed up to AWS S3 and Glacier.
- D. Use AWS Config Timeline forensics.

<details><summary>Answer:</summary><p>
[A]

Categories:
[S3, Glacier, SNS, CloudTrail]

Explanation:

Question 5@http://jayendrapatil.com/aws-cloudtrail/

A: http://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-log-file-validation-intro.html

A: . 

</p></details><hr>

### Question 6:

Your CTO has asked you to make sure that you know what all users of your AWS account are doing to change resources at all times. She wants a report of who is doing what over time, reported to her once per week, for as broad a resource type group as possible. How should you do this?

- A. Create a global AWS CloudTrail Trail. Configure a script to aggregate the log data delivered to S3 once per week and deliver this to the CTO.
- B. Use CloudWatch Events Rules with an SNS topic subscribed to all AWS API calls. Subscribe the CTO to an email type delivery on this SNS Topic.
- C. Use AWS IAM credential reports to deliver a CSV of all uses of IAM User Tokens over time to the CTO.
- D. Use AWS Config with an SNS subscription on a Lambda, and insert these changes over time into a DynamoDB table. Generate reports based on the contents of this table.

<details><summary>Answer:</summary><p>
[A]

Categories:
[S3, SES, IAM, CloudWatch, SNS, DynamoDB, Lambda, CloudTrail]

Explanation:

Question 6@http://jayendrapatil.com/aws-cloudtrail/

</p></details><hr>

