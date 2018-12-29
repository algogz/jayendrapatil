### Question 1:

A company is building software on AWS that requires access to various AWS services. Which configuration should be used to ensure that AWS credentials (i.e., Access Key ID/Secret Access Key combination) are not compromised?

- A. Enable Multi-Factor Authentication for your AWS root account.
- B. Assign an IAM role to the Amazon EC2 instance.
- C. Store the AWS Access Key ID/Secret Access Key combination in software comments.
- D. Assign an IAM user to the Amazon EC2 Instance.

<details><summary>Answer:</summary><p>
[B]

Categories:
[IAM, EC2]

Explanation:

Question 1@http://jayendrapatil.com/aws-iam-role/

</p></details><hr>

### Question 2:

A company is preparing to give AWS Management Console access to developers. Company policy mandates identity federation and role-based access control. Roles are currently assigned using groups in the corporate Active Directory. What combination of the following will give developers access to the AWS console? (Select 2) Choose 2 answers

- A. AWS Directory Service AD Connector
- B. AWS Directory Service Simple AD
- C. AWS Identity and Access Management groups
- D. AWS identity and Access Management roles
- E. AWS identity and Access Management users

<details><summary>Answer:</summary><p>
[A, D]

Categories:
[]

Explanation:

Question 2@http://jayendrapatil.com/aws-iam-role/

</p></details><hr>

### Question 3:

A customer needs corporate IT governance and cost oversight of all AWS resources consumed by its divisions. The divisions want to maintain administrative control of the discrete AWS resources they consume and keep those resources separate from the resources of other divisions. Which of the following options, when used together will support the autonomy/control of divisions while enabling corporate IT to maintain governance and cost oversight? Choose 2 answers

- A. Use AWS Consolidated Billing and disable AWS root account access for the child accounts.
- B. Enable IAM cross-account access for all corporate IT administrators in each child account.
- C. Create separate VPCs for each division within the corporate IT AWS account.
- D. Use AWS Consolidated Billing to link the divisions’ accounts to a parent corporate account.
- E. Write all child AWS CloudTrail and Amazon CloudWatch logs to each child account’s Amazon S3 ‘Log’ bucket.

<details><summary>Answer:</summary><p>
[B, D]

Categories:
[S3, IAM, CloudWatch, VPC, CloudTrail]

Explanation:

Question 3@http://jayendrapatil.com/aws-iam-role/

B: Provides IT governance

D: Will provide cost oversight

</p></details><hr>

### Question 4:

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

Question 4@http://jayendrapatil.com/aws-iam-role/

B: (With latest enhancement from AWS, IAM role can be assigned to a running EC2 instance)

E: (This was the correct answer before, as AWS did not allow IAM role to be added to an existing instance)

</p></details><hr>

### Question 5:

You are looking to migrate your Development (Dev) and Test environments to AWS. You have decided to use separate AWS accounts to host each environment. You plan to link each accounts bill to a Master AWS account using Consolidated Billing. To make sure you Keep within budget you would like to implement a way for administrators in the Master account to have access to stop, delete and/or terminate resources in both the Dev and Test accounts. Identify which option will allow you to achieve this goal. [PROFESSIONAL]

- A. Create IAM users in the Master account with full Admin permissions. Create cross-account roles in the Dev and Test accounts that grant the Master account access to the resources in the account by inheriting permissions from the Master account.
- B. Create IAM users and a cross-account role in the Master account that grants full Admin permissions to the Dev and Test accounts.
- C. Create IAM users in the Master account Create cross-account roles in the Dev and Test accounts that have full Admin permissions and grant the Master account access
- D. Link the accounts using Consolidated Billing. This will give IAM users in the Master account access to resources in the Dev and Test accounts

<details><summary>Answer:</summary><p>
[C]

Categories:
[IAM]

Explanation:

Question 5@http://jayendrapatil.com/aws-iam-role/

</p></details><hr>

### Question 6:

You have an application running on an EC2 Instance which will allow users to download flies from a private S3 bucket using a pre-assigned URL. Before generating the URL the application should verify the existence of the file in S3. How should the application use AWS credentials to access the S3 bucket securely? [PROFESSIONAL]

- A. Use the AWS account access Keys the application retrieves the credentials from the source code of the application.
- B. Create a IAM user for the application with permissions that allow list access to the S3 bucket launch the instance as the IAM user and retrieve the IAM user’s credentials from the EC2 instance user data.
- C. Create an IAM role for EC2 that allows list access to objects in the S3 bucket. Launch the instance with the role, and retrieve the role’s credentials from the EC2 Instance metadata
- D. Create an IAM user for the application with permissions that allow list access to the S3 bucket. The application retrieves the IAM user credentials from a temporary directory with permissions that allow read access only to the application user.

<details><summary>Answer:</summary><p>
[C]

Categories:
[S3, IAM, EC2]

Explanation:

Question 6@http://jayendrapatil.com/aws-iam-role/

</p></details><hr>

### Question 7:

An administrator is using Amazon CloudFormation to deploy a three tier web application that consists of a web tier and application tier that will utilize Amazon DynamoDB for storage when creating the CloudFormation template which of the following would allow the application instance access to the DynamoDB tables without exposing API credentials? [PROFESSIONAL]

- A. Create an Identity and Access Management Role that has the required permissions to read and write from the required DynamoDB table and associate the Role to the application instances by referencing an instance profile.
- B. Use the Parameter section in the Cloud Formation template to nave the user input Access and Secret Keys from an already created IAM user that has me permissions required to read and write from the required DynamoDB table.
- C. Create an Identity and Access Management Role that has the required permissions to read and write from the required DynamoDB table and reference the Role in the instance profile property of the application instance.
- D. Create an identity and Access Management user in the CloudFormation template that has permissions to read and write from the required DynamoDB table, use the GetAtt function to retrieve the Access and secret keys and pass them to the application instance through user-data.

<details><summary>Answer:</summary><p>
[C]

Categories:
[IAM, CloudFormation, DynamoDB]

Explanation:

Question 7@http://jayendrapatil.com/aws-iam-role/

</p></details><hr>

### Question 8:

An enterprise wants to use a third-party SaaS application. The SaaS application needs to have access to issue several API commands to discover Amazon EC2 resources running within the enterprise’s account. The enterprise has internal security policies that require any outside access to their environment must conform to the principles of least privilege and there must be controls in place to ensure that the credentials used by the SaaS vendor cannot be used by any other third party. Which of the following would meet all of these conditions? [PROFESSIONAL]

- A. From the AWS Management Console, navigate to the Security Credentials page and retrieve the access and secret key for your account.
- B. Create an IAM user within the enterprise account assign a user policy to the IAM user that allows only the actions required by the SaaS application create a new access and secret key for the user and provide these credentials to the SaaS provider.
- C. Create an IAM role for cross-account access allows the SaaS provider’s account to assume the role and assign it a policy that allows only the actions required by the SaaS application.
- D. Create an IAM role for EC2 instances, assign it a policy mat allows only the actions required tor the SaaS application to work, provide the role ARM to the SaaS provider to use when launching their application instances.

<details><summary>Answer:</summary><p>
[C]

Categories:
[IAM, EC2]

Explanation:

Question 8@http://jayendrapatil.com/aws-iam-role/

</p></details><hr>

### Question 9:

A user has created an application which will be hosted on EC2. The application makes calls to DynamoDB to fetch certain data. The application is using the DynamoDB SDK to connect with from the EC2 instance. Which of the below mentioned statements is true with respect to the best practice for security in this scenario?

- A. The user should attach an IAM role with DynamoDB access to the EC2 instance
- B. The user should create an IAM user with DynamoDB access and use its credentials within the application to connect with DynamoDB
- C. The user should create an IAM role, which has EC2 access so that it will allow deploying the application
- D. The user should create an IAM user with DynamoDB and EC2 access. Attach the user with the application so that it does not use the root account credentials

<details><summary>Answer:</summary><p>
[A]

Categories:
[IAM, EC2, DynamoDB]

Explanation:

Question 9@http://jayendrapatil.com/aws-iam-role/

</p></details><hr>

### Question 10:

A customer is in the process of deploying multiple applications to AWS that are owned and operated by different development teams. Each development team maintains the authorization of its users independently from other teams. The customer’s information security team would like to be able to delegate user authorization to the individual development teams but independently apply restrictions to the users permissions based on factors such as the users device and location. For example, the information security team would like to grant read-only permissions to a user who is defined by the development team as read/write whenever the user is authenticating from outside the corporate network. What steps can the information security team take to implement this capability? [PROFESSIONAL]

- A. Operate an authentication service that generates AWS STS tokens with IAM policies from application-defined IAM roles. 
- B. Add additional IAM policies to the application IAM roles that deny user privileges based on information security policy.
- C. Configure IAM policies that restrict modification of the application IAM roles only to the information security team. 
- D. Enable federation with the internal LDAP directory and grant the application teams permissions to modify users.

<details><summary>Answer:</summary><p>
[B]

Categories:
[IAM]

Explanation:

Question 10@http://jayendrapatil.com/aws-iam-role/

A: no user separation, will just help generate temporary tokens

B: Different policy with deny rules based on location, device and more restrictive wins

C: Authorization should still be in developers control

</p></details><hr>

### Question 11:

You are creating an Auto Scaling group whose Instances need to insert a custom metric into CloudWatch. Which method would be the best way to authenticate your CloudWatch PUT request?

- A. Create an IAM role with the Put MetricData permission and modify the Auto Scaling launch configuration to launch instances in that role
- B. Create an IAM user with the PutMetricData permission and modify the Auto Scaling launch configuration to inject the users credentials into the instance User Data
- C. Modify the appropriate Cloud Watch metric policies to allow the Put MetricData permission to instances from the Auto Scaling group
- D. Create an IAM user with the PutMetricData permission and put the credentials in a private repository and have applications on the server pull the credentials as needed

<details><summary>Answer:</summary><p>
[A]

Categories:
[IAM, CloudWatch, ASG]

Explanation:

Question 11@http://jayendrapatil.com/aws-iam-role/

</p></details><hr>

