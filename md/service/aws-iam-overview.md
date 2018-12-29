### Question 1:

Which service enables AWS customers to manage users and permissions in AWS?

- A. AWS Access Control Service (ACS)
- B. AWS Identity and Access Management (IAM)
- C. AWS Identity Manager (AIM)

<details><summary>Answer:</summary><p>
[B]

Categories:
[IAM]

Explanation:

Question 1@http://jayendrapatil.com/aws-iam-overview/

</p></details><hr>

### Question 2:

IAM provides several policy templates you can use to automatically assign permissions to the groups you create. The _____ policy template gives the Admins group permission to access all account resources, except your AWS account information

- A. Read Only Access
- B. Power User Access
- C. AWS Cloud Formation Read Only Access
- D. Administrator Access

<details><summary>Answer:</summary><p>
[D]

Categories:
[IAM]

Explanation:

Question 2@http://jayendrapatil.com/aws-iam-overview/

</p></details><hr>

### Question 3:

Every user you create in the IAM system starts with _________.

- A. Partial permissions
- B. Full permissions
- C. No permissions

<details><summary>Answer:</summary><p>
[C]

Categories:
[IAM]

Explanation:

Question 3@http://jayendrapatil.com/aws-iam-overview/

</p></details><hr>

### Question 4:

Groups can’t _____.

- A. be nested more than 3 levels
- B. be nested at all
- C. be nested more than 4 levels
- D. be nested more than 2 levels

<details><summary>Answer:</summary><p>
[B]

Categories:
[]

Explanation:

Question 4@http://jayendrapatil.com/aws-iam-overview/

</p></details><hr>

### Question 5:

The _____ service is targeted at organizations with multiple users or systems that use AWS products such as Amazon EC2, Amazon SimpleDB, and the AWS Management Console.

- A. Amazon RDS
- B. AWS Integrity Management
- C. AWS Identity and Access Management
- D. Amazon EMR

<details><summary>Answer:</summary><p>
[C]

Categories:
[RDS, EC2, EMR]

Explanation:

Question 5@http://jayendrapatil.com/aws-iam-overview/

</p></details><hr>

### Question 6:

An AWS customer is deploying an application that is composed of an AutoScaling group of EC2 Instances. The customers security policy requires that every outbound connection from these instances to any other service within the customers Virtual Private Cloud must be authenticated using a unique x.509 certificate that contains the specific instanceid. In addition an x.509 certificates must be designed by the customer’s Key management service in order to be trusted for authentication. Which of the following configurations will support these requirements?

- A. Configure an IAM Role that grants access to an Amazon S3 object containing a signed certificate and configure the Auto Scaling group to launch instances with this role. Have the instances bootstrap get the certificate from Amazon S3 upon first boot.
- B. Embed a certificate into the Amazon Machine Image that is used by the Auto Scaling group. Have the launched instances generate a certificate signature request with the instance’s assigned instance-id to the Key management service for signature.
- C. Configure the Auto Scaling group to send an SNS notification of the launch of a new instance to the trusted key management service. Have the Key management service generate a signed certificate and send it directly to the newly launched instance.
- D. Configure the launched instances to generate a new certificate upon first boot. Have the Key management service poll the AutoScaling group for associated instances and send new instances a certificate signature that contains the specific instance-id.

<details><summary>Answer:</summary><p>
[C]

Categories:
[S3, KMS, IAM, EC2, ASG, VPC, SNS]

Explanation:

Question 6@http://jayendrapatil.com/aws-iam-overview/

</p></details><hr>

### Question 7:

When assessing an organization AWS use of AWS API access credentials which of the following three credentials should be evaluated? Choose 3 answers

- A. Key pairs
- B. Console passwords
- C. Access keys
- D. Signing certificates
- E. Security Group memberships 

<details><summary>Answer:</summary><p>
[B, C, D]

Categories:
[SES, RDS]

Explanation:

Question 7@http://jayendrapatil.com/aws-iam-overview/

E: required for EC2 instance access

</p></details><hr>

### Question 8:

An organization has created 50 IAM users. The organization wants that each user can change their password but cannot change their access keys. How can the organization achieve this?

- A. The organization has to create a special password policy and attach it to each user
- B. The root account owner has to use CLI which forces each IAM user to change their password on first login
- C. By default each IAM user can modify their passwords
- D. Root account owner can set the policy from the IAM console under the password policy screen

<details><summary>Answer:</summary><p>
[D]

Categories:
[RDS, IAM]

Explanation:

Question 8@http://jayendrapatil.com/aws-iam-overview/

</p></details><hr>

### Question 9:

An organization has created 50 IAM users. The organization has introduced a new policy which will change the access of an IAM user. How can the organization implement this effectively so that there is no need to apply the policy at the individual user level?

- A. Use the IAM groups and add users as per their role to different groups and apply policy to group
- B. The user can create a policy and apply it to multiple users in a single go with the AWS CLI
- C. Add each user to the IAM role as per their organization role to achieve effective policy setup
- D. Use the IAM role and implement access at the role level

<details><summary>Answer:</summary><p>
[A]

Categories:
[IAM]

Explanation:

Question 9@http://jayendrapatil.com/aws-iam-overview/

</p></details><hr>

### Question 10:

Your organization’s security policy requires that all privileged users either use frequently rotated passwords or one-time access credentials in addition to username/password. Which two of the following options would allow an organization to enforce this policy for AWS users? Choose 2 answers

- A. Configure multi-factor authentication for privileged IAM users
- B. Create IAM users for privileged accounts ( )
- C. Implement identity federation between your organization’s Identity provider leveraging the IAM Security Token Service
- D. Enable the IAM single-use password policy option for privileged users 

<details><summary>Answer:</summary><p>
[A, B]

Categories:
[RDS, IAM]

Explanation:

Question 10@http://jayendrapatil.com/aws-iam-overview/

B: can set password policy

D: no such option the password expiration can be set from 1 to 1095 days

</p></details><hr>

### Question 11:

Your organization is preparing for a security assessment of your use of AWS. In preparation for this assessment, which two IAM best practices should you consider implementing? Choose 2 answers

- A. Create individual IAM users for everyone in your organization
- B. Configure MFA on the root account and for privileged IAM users
- C. Assign IAM users and groups configured with policies granting least privilege access
- D. Ensure all users have been assigned and are frequently rotating a password, access ID/secret key, and X.509 certificate

<details><summary>Answer:</summary><p>
[B, C]

Categories:
[SES, IAM]

Explanation:

Question 11@http://jayendrapatil.com/aws-iam-overview/

</p></details><hr>

### Question 12:

A company needs to deploy services to an AWS region which they have not previously used. The company currently has an AWS identity and Access Management (IAM) role for the Amazon EC2 instances, which permits the instance to have access to Amazon DynamoDB. The company wants their EC2 instances in the new region to have the same privileges. How should the company achieve this?

- A. Create a new IAM role and associated policies within the new region
- B. Assign the existing IAM role to the Amazon EC2 instances in the new region
- C. Copy the IAM role and associated policies to the new region and attach it to the instances
- D. Create an Amazon Machine Image (AMI) of the instance and copy it to the desired region using the AMI Copy feature

<details><summary>Answer:</summary><p>
[B]

Categories:
[IAM, EC2, DynamoDB]

Explanation:

Question 12@http://jayendrapatil.com/aws-iam-overview/

</p></details><hr>

### Question 13:

After creating a new IAM user which of the following must be done before they can successfully make API calls?

- A. Add a password to the user.
- B. Enable Multi-Factor Authentication for the user.
- C. Assign a Password Policy to the user.
- D. Create a set of Access Keys for the user

<details><summary>Answer:</summary><p>
[D]

Categories:
[IAM]

Explanation:

Question 13@http://jayendrapatil.com/aws-iam-overview/

</p></details><hr>

### Question 14:

An organization is planning to create a user with IAM. They are trying to understand the limitations of IAM so that they can plan accordingly. Which of the below mentioned statements is not true with respect to the limitations of IAM?

- A. One IAM user can be a part of a maximum of 5 groups 
- B. Organization can create 100 groups per AWS account
- C. One AWS account can have a maximum of 5000 IAM users
- D. One AWS account can have 250 roles

<details><summary>Answer:</summary><p>
[A]

Categories:
[IAM]

Explanation:

Question 14@http://jayendrapatil.com/aws-iam-overview/

A: https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_iam-limits.html

</p></details><hr>

### Question 15:

Within the IAM service a GROUP is regarded as a:

- A. A collection of AWS accounts
- B. It’s the group of EC2 machines that gain the permissions specified in the GROUP.
- C. There’s no GROUP in IAM, but only USERS and RESOURCES.
- D. A collection of users.

<details><summary>Answer:</summary><p>
[D]

Categories:
[IAM, EC2]

Explanation:

Question 15@http://jayendrapatil.com/aws-iam-overview/

</p></details><hr>

### Question 16:

Is there a limit to the number of groups you can have?

- A. Yes for all users except root
- B. No
- C. Yes unless special permission granted
- D. Yes for all users

<details><summary>Answer:</summary><p>
[D]

Categories:
[]

Explanation:

Question 16@http://jayendrapatil.com/aws-iam-overview/

</p></details><hr>

### Question 17:

What is the default maximum number of MFA devices in use per AWS account (at the root account level)?

- A. 1
- B. 5
- C. 15
- D. 10

<details><summary>Answer:</summary><p>
[A]

Categories:
[]

Explanation:

Question 17@http://jayendrapatil.com/aws-iam-overview/

</p></details><hr>

### Question 18:

When you use the AWS Management Console to delete an IAM user, IAM also deletes any signing certificates and any access keys belonging to the user.

- A. FALSE
- B. This is configurable
- C. TRUE

<details><summary>Answer:</summary><p>
[C]

Categories:
[IAM]

Explanation:

Question 18@http://jayendrapatil.com/aws-iam-overview/

</p></details><hr>

### Question 19:

You are setting up a blog on AWS. In which of the following scenarios will you need AWS credentials? (Choose 3)

- A. Sign in to the AWS management console to launch an Amazon EC2 instance
- B. Sign in to the running instance to instance some software 
- C. Launch an Amazon RDS instance
- D. Log into your blog’s content management system to write a blog post 
- E. Post pictures to your blog on Amazon S3

<details><summary>Answer:</summary><p>
[A, C, E]

Categories:
[S3, RDS, EC2]

Explanation:

Question 19@http://jayendrapatil.com/aws-iam-overview/

B: needs ssh keys

D: need to authenticate using blog authentication

</p></details><hr>

### Question 20:

An organization has 500 employees. The organization wants to set up AWS access for each department. Which of the below mentioned options is a possible solution?

- A. Create IAM roles based on the permission and assign users to each role
- B. Create IAM users and provide individual permission to each
- C. Create IAM groups based on the permission and assign IAM users to the groups
- D. It is not possible to manage more than 100 IAM users with AWS

<details><summary>Answer:</summary><p>
[C]

Categories:
[IAM]

Explanation:

Question 20@http://jayendrapatil.com/aws-iam-overview/

</p></details><hr>

### Question 21:

An organization has hosted an application on the EC2 instances. There will be multiple users connecting to the instance for setup and configuration of application. The organization is planning to implement certain security best practices. Which of the below mentioned pointers will not help the organization achieve better security arrangement?

- A. Apply the latest patch of OS and always keep it updated.
- B. Allow only IAM users to connect with the EC2 instances with their own secret access key
- C. Disable the password-based login for all the users. All the users should use their own keys to connect with the instance securely.
- D. Create a procedure to revoke the access rights of the individual user when they are not required to connect to EC2 instance anymore for the purpose of application configuration.

<details><summary>Answer:</summary><p>
[B]

Categories:
[IAM, EC2]

Explanation:

Question 21@http://jayendrapatil.com/aws-iam-overview/

B: http://aws.amazon.com/articles/1233/

B: . 

</p></details><hr>

