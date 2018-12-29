### Question 1:

You would like to create a mirror image of your production environment in another region for disaster recovery purposes. Which of the following AWS resources do not need to be recreated in the second region? (Choose 2 answers)

- A. Route 53 Record Sets
- B. IAM Roles
- C. Elastic IP Addresses (EIP) 
- D. EC2 Key Pairs 
- E. Launch configurations
- F. Security Groups 

<details><summary>Answer:</summary><p>
[A, B]

Categories:
[SES, IAM, EC2, Route 53]

Explanation:

Question 1@http://jayendrapatil.com/aws-global-vs-regional-vs-az-resources/

C: are specific to a region

D: are specific to a region

F: are specific to a region

</p></details><hr>

### Question 2:

When using the following AWS services, which should be implemented in multiple Availability Zones for high availability solutions? Choose 2 answers

- A. Amazon DynamoDB 
- B. Amazon Elastic Compute Cloud (EC2)
- C. Amazon Elastic Load Balancing
- D. Amazon Simple Notification Service (SNS) 
- E. Amazon Simple Storage Service (S3) 

<details><summary>Answer:</summary><p>
[B, C]

Categories:
[S3, EC2, SNS, DynamoDB, ELB]

Explanation:

Question 2@http://jayendrapatil.com/aws-global-vs-regional-vs-az-resources/

A: already replicates across AZs

D: Global Managed Service

E: Global Managed Service

</p></details><hr>

### Question 3:

What is the scope of an EBS volume?

- A. VPC
- B. Region
- C. Placement Group
- D. Availability Zone

<details><summary>Answer:</summary><p>
[D]

Categories:
[EBS, VPC]

Explanation:

Question 3@http://jayendrapatil.com/aws-global-vs-regional-vs-az-resources/

</p></details><hr>

### Question 4:

What is the scope of AWS IAM?

- A. Global
- B. Availability Zone
- C. Region
- D. Placement Group

<details><summary>Answer:</summary><p>
[A]

Categories:
[IAM]

Explanation:

Question 4@http://jayendrapatil.com/aws-global-vs-regional-vs-az-resources/

A: IAM resources are all global; there is not regional constraint

</p></details><hr>

### Question 5:

What is the scope of an EC2 EIP?

- A. Placement Group
- B. Availability Zone
- C. Region
- D. VPC

<details><summary>Answer:</summary><p>
[C]

Categories:
[EC2, VPC]

Explanation:

Question 5@http://jayendrapatil.com/aws-global-vs-regional-vs-az-resources/

C: http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/resources.html

C: An Elastic IP address is tied to a region and can be associated only with an instance in the same region. Refer

</p></details><hr>

### Question 6:

What is the scope of an EC2 security group?

- A. Availability Zone
- B. Placement Group
- C. Region
- D. VPC

<details><summary>Answer:</summary><p>
[C]

Categories:
[EC2, VPC]

Explanation:

Question 6@http://jayendrapatil.com/aws-global-vs-regional-vs-az-resources/

C: A security group is tied to a region and can be assigned only to instances in the same region

</p></details><hr>

