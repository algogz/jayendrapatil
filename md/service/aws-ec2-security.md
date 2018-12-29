### Question 1:

You launch an Amazon EC2 instance without an assigned AWS identity and Access Management (IAM) role. Later, you decide that the instance should be running with an IAM role. Which action must you take in order to have a running Amazon EC2 instance with an IAM role assigned to it?

- A. Create an image of the instance, and register the image with an IAM role assigned and an Amazon EBS volume mapping.
- B. Create a new IAM role with the same permissions as an existing IAM role, and assign it to the running instance.
- C. Create an image of the instance, add a new IAM role with the same permissions as the desired IAM role, and deregister the image with the new role assigned.
- D. Create an image of the instance, and use this image to launch a new instance with the desired IAM role assigned 

<details><summary>Answer:</summary><p>
[B]

Categories:
[IAM, EC2, EBS]

Explanation:

Question 1@http://jayendrapatil.com/aws-ec2-security/

B: https://aws.amazon.com/about-aws/whats-new/2017/02/new-attach-an-iam-role-to-your-existing-amazon-ec2-instance/

B: As per AWS , this is possible now

D: This was correct before, as it was not possible to add an IAM role to an existing instance

</p></details><hr>

### Question 2:

What does the following command do with respect to the Amazon EC2 security groups? ec2-revoke RevokeSecurityGroupIngress

- A. Removes one or more security groups from a rule.
- B. Removes one or more security groups from an Amazon EC2 instance.
- C. Removes one or more rules from a security group
- D. Removes a security group from our account.

<details><summary>Answer:</summary><p>
[C]

Categories:
[EC2]

Explanation:

Question 2@http://jayendrapatil.com/aws-ec2-security/

</p></details><hr>

### Question 3:

Which of the following cannot be used in Amazon EC2 to control who has access to specific Amazon EC2 instances?

- A. Security Groups
- B. IAM System
- C. SSH keys
- D. Windows passwords

<details><summary>Answer:</summary><p>
[B]

Categories:
[RDS, IAM, EC2]

Explanation:

Question 3@http://jayendrapatil.com/aws-ec2-security/

</p></details><hr>

### Question 4:

You must assign each server to at least _____ security group

- A. 3
- B. 2
- C. 4
- D. 1

<details><summary>Answer:</summary><p>
[D]

Categories:
[]

Explanation:

Question 4@http://jayendrapatil.com/aws-ec2-security/

</p></details><hr>

### Question 5:

A company is building software on AWS that requires access to various AWS services. Which configuration should be used to ensure that AWS credentials (i.e., Access Key ID/Secret Access Key combination) are not compromised?

- A. Enable Multi-Factor Authentication for your AWS root account.
- B. Assign an IAM role to the Amazon EC2 instance
- C. Store the AWS Access Key ID/Secret Access Key combination in software comments.
- D. Assign an IAM user to the Amazon EC2 Instance.

<details><summary>Answer:</summary><p>
[B]

Categories:
[IAM, EC2]

Explanation:

Question 5@http://jayendrapatil.com/aws-ec2-security/

</p></details><hr>

### Question 6:

Which of the following items are required to allow an application deployed on an EC2 instance to write data to a DynamoDB table? Assume that no security keys are allowed to be stored on the EC2 instance. (Choose 2 answers)

- A. Create an IAM Role that allows write access to the DynamoDB table
- B. Add an IAM Role to a running EC2 instance.
- C. Create an IAM User that allows write access to the DynamoDB table.
- D. Add an IAM User to a running EC2 instance.
- E. Launch an EC2 Instance with the IAM Role included in the launch configuration 

<details><summary>Answer:</summary><p>
[A, B]

Categories:
[IAM, EC2, DynamoDB]

Explanation:

Question 6@http://jayendrapatil.com/aws-ec2-security/

B: https://aws.amazon.com/about-aws/whats-new/2017/02/new-attach-an-iam-role-to-your-existing-amazon-ec2-instance/

B: As per AWS , this is possible now

E: This was correct before, as it was not possible to add an IAM role to an existing instance

</p></details><hr>

### Question 7:

You have an application running on an EC2 Instance, which will allow users to download files from a private S3 bucket using a pre-assigned URL. Before generating the URL the application should verify the existence of the file in S3. How should the application use AWS credentials to access the S3 bucket securely?

- A. Use the AWS account access Keys the application retrieves the credentials from the source code of the application.
- B. Create a IAM user for the application with permissions that allow list access to the S3 bucket launch the instance as the IAM user and retrieve the IAM user’s credentials from the EC2 instance user data.
- C. Create an IAM role for EC2 that allows list access to objects in the S3 bucket. Launch the instance with the role, and retrieve the role’s credentials from the EC2 Instance metadata
- D. Create an IAM user for the application with permissions that allow list access to the S3 bucket. The application retrieves the IAM user credentials from a temporary directory with permissions that allow read access only to the application user.

<details><summary>Answer:</summary><p>
[C]

Categories:
[S3, IAM, EC2]

Explanation:

Question 7@http://jayendrapatil.com/aws-ec2-security/

</p></details><hr>

### Question 8:

A user has created an application, which will be hosted on EC2. The application makes calls to DynamoDB to fetch certain data. The application is using the DynamoDB SDK to connect with from the EC2 instance. Which of the below mentioned statements is true with respect to the best practice for security in this scenario?

- A. The user should attach an IAM role with DynamoDB access to the EC2 instance
- B. The user should create an IAM user with DynamoDB access and use its credentials within the application to connect with DynamoDB
- C. The user should create an IAM role, which has EC2 access so that it will allow deploying the application
- D. The user should create an IAM user with DynamoDB and EC2 access. Attach the user with the application so that it does not use the root account credentials

<details><summary>Answer:</summary><p>
[A]

Categories:
[IAM, EC2, DynamoDB]

Explanation:

Question 8@http://jayendrapatil.com/aws-ec2-security/

</p></details><hr>

### Question 9:

Your application is leveraging IAM Roles for EC2 for accessing object stored in S3. Which two of the following IAM policies control access to you S3 objects.

- A. An IAM trust policy allows the EC2 instance to assume an EC2 instance role.
- B. An IAM access policy allows the EC2 role to access S3 objects
- C. An IAM bucket policy allows the EC2 role to access S3 objects. 
- D. An IAM trust policy allows applications running on the EC2 instance to assume as EC2 role 
- E. An IAM trust policy allows applications running on the EC2 instance to access S3 objects. 

<details><summary>Answer:</summary><p>
[A, B]

Categories:
[S3, IAM, EC2]

Explanation:

Question 9@http://jayendrapatil.com/aws-ec2-security/

C: Bucket policy is defined with S3 and not with IAM

D: Trust policy allows EC2 instance to assume the role

E: Applications can access S3 through EC2 assuming the role

</p></details><hr>

### Question 10:

You have an application running on an EC2 Instance, which will allow users to download files from a private S3 bucket using a pre-assigned URL. Before generating the URL the application should verify the existence of the file in S3. How should the application use AWS credentials to access the S3 bucket securely?

- A. Use the AWS account access Keys the application retrieves the credentials from the source code of the application.
- B. Create a IAM user for the application with permissions that allow list access to the S3 bucket launch the instance as the IAM user and retrieve the IAM user’s credentials from the EC2 instance user data.
- C. Create an IAM role for EC2 that allows list access to objects in the S3 bucket. Launch the instance with the role, and retrieve the role’s credentials from the EC2 Instance metadata
- D. Create an IAM user for the application with permissions that allow list access to the S3 bucket. The application retrieves the IAM user credentials from a temporary directory with permissions that allow read access only to the application user.

<details><summary>Answer:</summary><p>
[C]

Categories:
[S3, IAM, EC2]

Explanation:

Question 10@http://jayendrapatil.com/aws-ec2-security/

</p></details><hr>

