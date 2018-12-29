### Question 1:

Which features can be used to restrict access to data in S3? Choose 2 answers

- A. Set an S3 ACL on the bucket or the object.
- B. Create a CloudFront distribution for the bucket.
- C. Set an S3 bucket policy.
- D. Enable IAM Identity Federation
- E. Use S3 Virtual Hosting

<details><summary>Answer:</summary><p>
[A, C]

Categories:
[S3, CloudFront, IAM]

Explanation:

Question 1@http://jayendrapatil.com/aws-s3-permisions/

</p></details><hr>

### Question 2:

Which method can be used to prevent an IP address block from accessing public objects in an S3 bucket?

- A. Create a bucket policy and apply it to the bucket
- B. Create a NACL and attach it to the VPC of the bucket
- C. Create an ACL and apply it to all objects in the bucket
- D. Modify the IAM policies of any users that would access the bucket

<details><summary>Answer:</summary><p>
[A]

Categories:
[S3, IAM, VPC]

Explanation:

Question 2@http://jayendrapatil.com/aws-s3-permisions/

</p></details><hr>

### Question 3:

A user has granted read/write permission of his S3 bucket using ACL. Which of the below mentioned options is a valid ID to grant permission to other AWS accounts (grantee. using ACL?

- A. IAM User ID
- B. S3 Secure ID
- C. Access ID
- D. Canonical user ID

<details><summary>Answer:</summary><p>
[D]

Categories:
[S3, IAM]

Explanation:

Question 3@http://jayendrapatil.com/aws-s3-permisions/

</p></details><hr>

### Question 4:

A root account owner has given full access of his S3 bucket to one of the IAM users using the bucket ACL. When the IAM user logs in to the S3 console, which actions can he perform?

- A. He can just view the content of the bucket
- B. He can do all the operations on the bucket
- C. It is not possible to give access to an IAM user using ACL
- D. The IAM user can perform all operations on the bucket using only API/SDK

<details><summary>Answer:</summary><p>
[C]

Categories:
[S3, IAM]

Explanation:

Question 4@http://jayendrapatil.com/aws-s3-permisions/

</p></details><hr>

### Question 5:

A root AWS account owner is trying to understand various options to set the permission to AWS S3. Which of the below mentioned options is not the right option to grant permission for S3?

- A. User Access Policy
- B. S3 Object Policy
- C. S3 Bucket Policy
- D. S3 ACL

<details><summary>Answer:</summary><p>
[B]

Categories:
[S3]

Explanation:

Question 5@http://jayendrapatil.com/aws-s3-permisions/

</p></details><hr>

### Question 6:

A system admin is managing buckets, objects and folders with AWS S3. Which of the below mentioned statements is true and should be taken in consideration by the sysadmin?

- A. Folders support only ACL
- B. Both the object and bucket can have an Access Policy but folder cannot have policy
- C. Folders can have a policy
- D. Both the object and bucket can have ACL but folders cannot have ACL

<details><summary>Answer:</summary><p>
[D]

Categories:
[S3]

Explanation:

Question 6@http://jayendrapatil.com/aws-s3-permisions/

</p></details><hr>

### Question 7:

A user has created an S3 bucket which is not publicly accessible. The bucket is having thirty objects which are also private. If the user wants to make the objects public, how can he configure this with minimal efforts?

- A. User should select all objects from the console and apply a single policy to mark them public
- B. User can write a program which programmatically makes all objects public using S3 SDK
- C. Set the AWS bucket policy which marks all objects as public
- D. Make the bucket ACL as public so it will also mark all objects as public

<details><summary>Answer:</summary><p>
[C]

Categories:
[S3]

Explanation:

Question 7@http://jayendrapatil.com/aws-s3-permisions/

</p></details><hr>

### Question 8:

You need to configure an Amazon S3 bucket to serve static assets for your public-facing web application. Which methods ensure that all objects uploaded to the bucket are set to public read? Choose 2 answers

- A. Set permissions on the object to public read during upload.
- B. Configure the bucket ACL to set all objects to public read.
- C. Configure the bucket policy to set all objects to public read.
- D. Use AWS Identity and Access Management roles to set the bucket to public read.
- E. Amazon S3 objects default to public read, so no action is needed.

<details><summary>Answer:</summary><p>
[A, C]

Categories:
[S3]

Explanation:

Question 8@http://jayendrapatil.com/aws-s3-permisions/

</p></details><hr>

### Question 9:

Amazon S3 doesn’t automatically give a user who creates _____ permission to perform other actions on that bucket or object.

- A. a file
- B. a bucket or object
- C. a bucket or file
- D. a object or file

<details><summary>Answer:</summary><p>
[B]

Categories:
[S3]

Explanation:

Question 9@http://jayendrapatil.com/aws-s3-permisions/

</p></details><hr>

### Question 10:

A root account owner is trying to understand the S3 bucket ACL. Which of the below mentioned options cannot be used to grant ACL on the object using the authorized predefined group?

- A. Authenticated user group
- B. All users group
- C. Log Delivery Group
- D. Canonical user group

<details><summary>Answer:</summary><p>
[D]

Categories:
[S3]

Explanation:

Question 10@http://jayendrapatil.com/aws-s3-permisions/

</p></details><hr>

### Question 11:

A user is enabling logging on a particular bucket. Which of the below mentioned options may be best suitable to allow access to the log bucket?

- A. Create an IAM policy and allow log access
- B. It is not possible to enable logging on the S3 bucket
- C. Create an IAM Role, which has access to the log bucket
- D. Provide ACL for the logging group

<details><summary>Answer:</summary><p>
[D]

Categories:
[S3, IAM]

Explanation:

Question 11@http://jayendrapatil.com/aws-s3-permisions/

</p></details><hr>

### Question 12:

A user is trying to configure access with S3. Which of the following options is not possible to provide access to the S3 bucket / object?

- A. Define the policy for the IAM user
- B. Define the ACL for the object
- C. Define the policy for the object
- D. Define the policy for the bucket

<details><summary>Answer:</summary><p>
[C]

Categories:
[S3, IAM]

Explanation:

Question 12@http://jayendrapatil.com/aws-s3-permisions/

</p></details><hr>

### Question 13:

A user is having access to objects of an S3 bucket, which is not owned by him. If he is trying to set the objects of that bucket public, which of the below mentioned options may be a right fit for this action?

- A. Make the bucket public with full access
- B. Define the policy for the bucket
- C. Provide ACL on the object
- D. Create an IAM user with permission

<details><summary>Answer:</summary><p>
[C]

Categories:
[S3, IAM]

Explanation:

Question 13@http://jayendrapatil.com/aws-s3-permisions/

</p></details><hr>

### Question 14:

A bucket owner has allowed another account’s IAM users to upload or access objects in his bucket. The IAM user of Account A is trying to access an object created by the IAM user of account B. What will happen in this scenario?

- A. The bucket policy may not be created as S3 will give error due to conflict of Access Rights
- B. It is not possible to give permission to multiple IAM users
- C. AWS S3 will verify proper rights given by the owner of Account A, the bucket owner as well as by the IAM user B to the object
- D. It is not possible that the IAM user of one account accesses objects of the other IAM user

<details><summary>Answer:</summary><p>
[C]

Categories:
[S3, SES, IAM]

Explanation:

Question 14@http://jayendrapatil.com/aws-s3-permisions/

</p></details><hr>

