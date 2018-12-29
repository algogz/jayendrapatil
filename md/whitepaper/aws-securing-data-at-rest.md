### Question 1:

How can you secure data at rest on an EBS volume?

- A. Encrypt the volume using the S3 server-side encryption service
- B. Attach the volume to an instance using EC2’s SSL interface.
- C. Create an IAM policy that restricts read and write access to the volume.
- D. Write the data randomly instead of sequentially.
- E. Use an encrypted file system on top of the EBS volume

<details><summary>Answer:</summary><p>
[E]

Categories:
[S3, IAM, EC2, EBS]

Explanation:

Question 1@http://jayendrapatil.com/aws-securing-data-at-rest/

</p></details><hr>

### Question 2:

Your company policies require encryption of sensitive data at rest. You are considering the possible options for protecting data while storing it at rest on an EBS data volume, attached to an EC2 instance. Which of these options would allow you to encrypt your data at rest? (Choose 3 answers)

- A. Implement third party volume encryption tools
- B. Do nothing as EBS volumes are encrypted by default
- C. Encrypt data inside your applications before storing it on EBS
- D. Encrypt data using native data encryption drivers at the file system level
- E. Implement SSL/TLS for all services running on the server

<details><summary>Answer:</summary><p>
[A, C, D]

Categories:
[EC2, EBS]

Explanation:

Question 2@http://jayendrapatil.com/aws-securing-data-at-rest/

A: —

</p></details><hr>

### Question 3:

A company is storing data on Amazon Simple Storage Service (S3). The company’s security policy mandates that data is encrypted at rest. Which of the following methods can achieve this? Choose 3 answers

- A. Use Amazon S3 server-side encryption with AWS Key Management Service managed keys
- B. Use Amazon S3 server-side encryption with customer-provided keys
- C. Use Amazon S3 server-side encryption with EC2 key pair.
- D. Use Amazon S3 bucket policies to restrict access to the data at rest.
- E. Encrypt the data on the client-side before ingesting to Amazon S3 using their own master key
- F. Use SSL to encrypt the data while in transit to Amazon S3.

<details><summary>Answer:</summary><p>
[A, B, E]

Categories:
[S3, KMS, EC2]

Explanation:

Question 3@http://jayendrapatil.com/aws-securing-data-at-rest/

</p></details><hr>

### Question 4:

Which 2 services provide native encryption

- A. Amazon EBS
- B. Amazon Glacier
- C. Amazon Redshift 
- D. Amazon RDS 
- E. Amazon Storage Gateway

<details><summary>Answer:</summary><p>
[B, E]

Categories:
[RDS, Glacier, Storage Gateway, EBS, Redshift]

Explanation:

Question 4@http://jayendrapatil.com/aws-securing-data-at-rest/

C: is optional

D: is optional

</p></details><hr>

### Question 5:

With which AWS services CloudHSM can be used (select 2)

- A. S3
- B. DynamoDb
- C. RDS
- D. ElastiCache
- E. Amazon Redshift

<details><summary>Answer:</summary><p>
[C, E]

Categories:
[S3, RDS, ElastiCache, DynamoDB, Redshift]

Explanation:

Question 5@http://jayendrapatil.com/aws-securing-data-at-rest/

</p></details><hr>

