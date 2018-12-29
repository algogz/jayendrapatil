### Question 1:

IAM’s Policy Evaluation Logic always starts with a default ____________ for every request, except for those that use the AWS account’s root security credentials b

- A. Permit
- B. Deny
- C. Cancel

<details><summary>Answer:</summary><p>
[B]

Categories:
[IAM]

Explanation:

Question 1@http://jayendrapatil.com/aws-iam-access-management/

</p></details><hr>

### Question 2:

An organization has created 10 IAM users. The organization wants each of the IAM users to have access to a separate DynamoDB table. All the users are added to the same group and the organization wants to setup a group level policy for this. How can the organization achieve this?

- A. Define the group policy and add a condition which allows the access based on the IAM name
- B. Create a DynamoDB table with the same name as the IAM user name and define the policy rule which grants access based on the DynamoDB ARN using a variable
- C. Create a separate DynamoDB database for each user and configure a policy in the group based on the DB variable
- D. It is not possible to have a group level policy which allows different IAM users to different DynamoDB Tables

<details><summary>Answer:</summary><p>
[B]

Categories:
[IAM, DynamoDB]

Explanation:

Question 2@http://jayendrapatil.com/aws-iam-access-management/

</p></details><hr>

### Question 3:

An organization has setup multiple IAM users. The organization wants that each IAM user accesses the IAM console only within the organization and not from outside. How can it achieve this?

- A. Create an IAM policy with the security group and use that security group for AWS console login
- B. Create an IAM policy with a condition which denies access when the IP address range is not from the organization
- C. Configure the EC2 instance security group which allows traffic only from the organization’s IP range
- D. Create an IAM policy with VPC and allow a secure gateway between the organization and AWS Console

<details><summary>Answer:</summary><p>
[B]

Categories:
[SES, IAM, EC2, VPC]

Explanation:

Question 3@http://jayendrapatil.com/aws-iam-access-management/

</p></details><hr>

### Question 4:

Can I attach more than one policy to a particular entity?

- A. Yes always
- B. Only if within GovCloud
- C. No
- D. Only if within VPC

<details><summary>Answer:</summary><p>
[A]

Categories:
[VPC]

Explanation:

Question 4@http://jayendrapatil.com/aws-iam-access-management/

</p></details><hr>

### Question 5:

A __________ is a document that provides a formal statement of one or more permissions.

- A. policy
- B. permission
- C. Role
- D. resource

<details><summary>Answer:</summary><p>
[A]

Categories:
[]

Explanation:

Question 5@http://jayendrapatil.com/aws-iam-access-management/

</p></details><hr>

### Question 6:

A __________ is the concept of allowing (or disallowing) an entity such as a user, group, or role some type of access to one or more resources.

- A. user
- B. AWS Account
- C. resource
- D. permission

<details><summary>Answer:</summary><p>
[D]

Categories:
[]

Explanation:

Question 6@http://jayendrapatil.com/aws-iam-access-management/

</p></details><hr>

### Question 7:

True or False: When using IAM to control access to your RDS resources, the key names that can be used are case sensitive. For example, aws:CurrentTime is NOT equivalent to AWS:currenttime.

- A. TRUE
- B. FALSE

<details><summary>Answer:</summary><p>
[B]

Categories:
[RDS, IAM]

Explanation:

Question 7@http://jayendrapatil.com/aws-iam-access-management/

B: http://docs.aws.amazon.com/directconnect/latest/UserGuide/using_iam.html#keys

</p></details><hr>

### Question 8:

A user has set an IAM policy where it allows all requests if a request from IP 10.10.10.1/32. Another policy allows all the requests between 5 PM to 7 PM. What will happen when a user is requesting access from IP 10.10.10.1/32 at 6 PM?

- A. IAM will throw an error for policy conflict
- B. It is not possible to set a policy based on the time or IP
- C. It will deny access
- D. It will allow access

<details><summary>Answer:</summary><p>
[D]

Categories:
[IAM]

Explanation:

Question 8@http://jayendrapatil.com/aws-iam-access-management/

</p></details><hr>

### Question 9:

Which of the following are correct statements with policy evaluation logic in AWS Identity and Access Management? Choose 2 answers.

- A. By default, all requests are denied
- B. An explicit allow overrides an explicit deny
- C. An explicit allow overrides default deny
- D. An explicit deny does not override an explicit allow
- E. By default, all request are allowed

<details><summary>Answer:</summary><p>
[A, C]

Categories:
[]

Explanation:

Question 9@http://jayendrapatil.com/aws-iam-access-management/

</p></details><hr>

### Question 10:

A web design company currently runs several FTP servers that their 250 customers use to upload and download large graphic files. They wish to move this system to AWS to make it more scalable, but they wish to maintain customer privacy and keep costs to a minimum. What AWS architecture would you recommend? [PROFESSIONAL]

- A. Ask their customers to use an S3 client instead of an FTP client. Create a single S3 bucket. Create an IAM user for each customer. Put the IAM Users in a Group that has an IAM policy that permits access to subdirectories within the bucket via use of the ‘username’ Policy variable.
- B. Create a single S3 bucket with Reduced Redundancy Storage turned on and ask their customers to use an S3 client instead of an FTP client. Create a bucket for each customer with a Bucket Policy that permits access only to that one customer. 
- C. Create an auto-scaling group of FTP servers with a scaling policy to automatically scale-in when minimum network traffic on the auto-scaling group is below a given threshold. Load a central list of ftp users from S3 as part of the user Data startup script on each Instance 
- D. Create a single S3 bucket with Requester Pays turned on and ask their customers to use an S3 client instead of an FTP client. Create a bucket tor each customer with a Bucket Policy that permits access only to that one customer. 

<details><summary>Answer:</summary><p>
[A]

Categories:
[S3, IAM]

Explanation:

Question 10@http://jayendrapatil.com/aws-iam-access-management/

B: https://aws.amazon.com/about-aws/whats-new/2015/08/amazon-s3-introduces-new-usability-enhancements/

B: Creating bucket for each user is not a scalable model, also 100 buckets are a limit earlier without extending which has since changed

C: Expensive

D: https://aws.amazon.com/about-aws/whats-new/2015/08/amazon-s3-introduces-new-usability-enhancements/

D: Creating bucket for each user is not a scalable model, also 100 buckets are a limit earlier without extending which has since changed

</p></details><hr>

