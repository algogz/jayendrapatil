### Question 1:

Fill in the blanks: _________ let you categorize your EC2 resources in different ways, for example, by purpose, owner, or environment.

- A. Wildcards
- B. Pointers
- C. Tags
- D. Special filters

<details><summary>Answer:</summary><p>
[C]

Categories:
[RDS, EC2]

Explanation:

Question 1@http://jayendrapatil.com/aws-resource-tags/

</p></details><hr>

### Question 2:

Please select the Amazon EC2 resource, which can be tagged.

- A. Key pairs
- B. Elastic IP addresses
- C. Placement groups
- D. Amazon EBS snapshots

<details><summary>Answer:</summary><p>
[D]

Categories:
[SES, EC2, EBS]

Explanation:

Question 2@http://jayendrapatil.com/aws-resource-tags/

</p></details><hr>

### Question 3:

Can the string value of ‘Key’ be prefixed with aws:?

- A. No
- B. Only for EC2 not S3
- C. Yes
- D. Only for S3 not EC

<details><summary>Answer:</summary><p>
[A]

Categories:
[S3, EC2]

Explanation:

Question 3@http://jayendrapatil.com/aws-resource-tags/

</p></details><hr>

### Question 4:

What is the maximum key length of a tag?

- A. 512 Unicode characters
- B. 64 Unicode characters
- C. 256 Unicode characters
- D. 128 Unicode characters

<details><summary>Answer:</summary><p>
[D]

Categories:
[]

Explanation:

Question 4@http://jayendrapatil.com/aws-resource-tags/

</p></details><hr>

### Question 5:

An organization has launched 5 instances: 2 for production and 3 for testing. The organization wants that one particular group of IAM users should only access the test instances and not the production ones. How can the organization set that as a part of the policy?

- A. Launch the test and production instances in separate regions and allow region wise access to the group 
- B. Define the IAM policy which allows access based on the instance ID 
- C. Create an IAM policy with a condition which allows access to only small instances 
- D. Define the tags on the test and production servers and add a condition to the IAM policy which allows access to specific tags

<details><summary>Answer:</summary><p>
[D]

Categories:
[IAM]

Explanation:

Question 5@http://jayendrapatil.com/aws-resource-tags/

A: possible using location constraint condition but not flexible

B: not flexible as it would change

C: not flexible as it would change

D: possible using ResourceTag condition

</p></details><hr>

### Question 6:

A user has launched multiple EC2 instances for the purpose of development and testing in the same region. The user wants to find the separate cost for the production and development instances. How can the user find the cost distribution?

- A. The user should download the activity report of the EC2 services as it has the instance ID wise data
- B. It is not possible to get the AWS cost usage data of single region instances separately
- C. User should use Cost Distribution Metadata and AWS detailed billing
- D. User should use Cost Allocation Tags and AWS billing reports

<details><summary>Answer:</summary><p>
[D]

Categories:
[EC2]

Explanation:

Question 6@http://jayendrapatil.com/aws-resource-tags/

</p></details><hr>

### Question 7:

An organization is using cost allocation tags to find the cost distribution of different departments and projects. One of the instances has two separate tags with the key/value as “InstanceName/HR”, “CostCenter/HR”. What will AWS do in this case?

- A. InstanceName is a reserved tag for AWS. Thus, AWS will not allow this tag
- B. AWS will not allow the tags as the value is the same for different keys
- C. AWS will allow tags but will not show correctly in the cost allocation report due to the same value of the two separate keys
- D. AWS will allow both the tags and show properly in the cost distribution report

<details><summary>Answer:</summary><p>
[D]

Categories:
[]

Explanation:

Question 7@http://jayendrapatil.com/aws-resource-tags/

</p></details><hr>

### Question 8:

A user is launching an instance. He is on the “Tag the instance” screen. Which of the below mentioned information will not help the user understand the functionality of an AWS tag?

- A. Each tag will have a key and value
- B. The user can apply tags to the S3 bucket
- C. The maximum value of the tag key length is 64 unicode characters
- D. AWS tags are used to find the cost distribution of various resources

<details><summary>Answer:</summary><p>
[C]

Categories:
[S3]

Explanation:

Question 8@http://jayendrapatil.com/aws-resource-tags/

</p></details><hr>

### Question 9:

Your system recently experienced down time during the troubleshooting process. You found that a new administrator mistakenly terminated several production EC2 instances. Which of the following strategies will help prevent a similar situation in the future? The administrator still must be able to:- launch, start stop, and terminate development resources. – launch and start production instances.

- A. Create an IAM user, which is not allowed to terminate instances by leveraging production EC2 termination protection. 
- B. Leverage resource based tagging along with an IAM user, which can prevent specific users from terminating production EC2 resources.
- C. Leverage EC2 termination protection and multi-factor authentication, which together require users to authenticate before terminating EC2 instances. 
- D. Create an IAM user and apply an IAM role, which prevents users from terminating production EC2 instances. 

<details><summary>Answer:</summary><p>
[B]

Categories:
[IAM, EC2]

Explanation:

Question 9@http://jayendrapatil.com/aws-resource-tags/

A: EC2 termination protection is enabled on EC2 instance

B: Identify production resources using tags and add explicit deny

C: Does not still prevent user from terminating instance

D: Role is not applied to User but assumed by the User also need a way to identify production EC2 instances

</p></details><hr>

### Question 10:

Your manager has requested you to tag EC2 instances to organize and manage a load balancer. Which of the following statements about tag restrictions is incorrect?

- A. The maximum key length is 127 Unicode characters.
- B. The maximum value length is 255 Unicode characters.
- C. Tag keys and values are case sensitive.
- D. The maximum number of tags per load balancer is 20.

<details><summary>Answer:</summary><p>
[D]

Categories:
[EC2]

Explanation:

Question 10@http://jayendrapatil.com/aws-resource-tags/

D: 0 is the limit

D: (5)

</p></details><hr>

### Question 11:

What is the maximum number of tags that a user can assign to an EC2 instance?

- A. 50
- B. 10
- C. 5
- D. 25

<details><summary>Answer:</summary><p>
[A]

Categories:
[EC2]

Explanation:

Question 11@http://jayendrapatil.com/aws-resource-tags/

</p></details><hr>

