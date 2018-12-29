### Question 1:

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

Question 1@http://jayendrapatil.com/aws-s3-data-protection/

</p></details><hr>

### Question 2:

A user has enabled versioning on an S3 bucket. The user is using server side encryption for data at Rest. If the user is supplying his own keys for encryption (SSE-C) which of the below mentioned statements is true?

- A. The user should use the same encryption key for all versions of the same object
- B. It is possible to have different encryption keys for different versions of the same object
- C. AWS S3 does not allow the user to upload his own keys for server side encryption
- D. The SSE-C does not work when versioning is enabled

<details><summary>Answer:</summary><p>
[B]

Categories:
[S3]

Explanation:

Question 2@http://jayendrapatil.com/aws-s3-data-protection/

</p></details><hr>

### Question 3:

A storage admin wants to encrypt all the objects stored in S3 using server side encryption. The user does not want to use the AES 256 encryption key provided by S3. How can the user achieve this?

- A. The admin should upload his secret key to the AWS console and let S3 decrypt the objects
- B. The admin should use CLI or API to upload the encryption key to the S3 bucket. When making a call to the S3 API mention the encryption key URL in each request
- C. S3 does not support client supplied encryption keys for server side encryption
- D. The admin should send the keys and encryption algorithm with each API call

<details><summary>Answer:</summary><p>
[D]

Categories:
[S3]

Explanation:

Question 3@http://jayendrapatil.com/aws-s3-data-protection/

</p></details><hr>

### Question 4:

A user has enabled versioning on an S3 bucket. The user is using server side encryption for data at rest. If the user is supplying his own keys for encryption (SSE-C), what is recommended to the user for the purpose of security?

- A. User should not use his own security key as it is not secure
- B. Configure S3 to rotate the user’s encryption key at regular intervals
- C. Configure S3 to store the user’s keys securely with SSL
- D. Keep rotating the encryption key manually at the client side

<details><summary>Answer:</summary><p>
[D]

Categories:
[S3]

Explanation:

Question 4@http://jayendrapatil.com/aws-s3-data-protection/

</p></details><hr>

### Question 5:

A system admin is planning to encrypt all objects being uploaded to S3 from an application. The system admin does not want to implement his own encryption algorithm; instead he is planning to use server side encryption by supplying his own key (SSE-C.. Which parameter is not required while making a call for SSE-C?

- A. x-amz-server-side-encryption-customer-key-AES-256
- B. x-amz-server-side-encryption-customer-key
- C. x-amz-server-side-encryption-customer-algorithm
- D. x-amz-server-side-encryption-customer-key-MD5

<details><summary>Answer:</summary><p>
[A]

Categories:
[S3]

Explanation:

Question 5@http://jayendrapatil.com/aws-s3-data-protection/

</p></details><hr>

### Question 6:

A customer is leveraging Amazon Simple Storage Service in eu-west-1 to store static content for a web-based property. The customer is storing objects using the Standard Storage class. Where are the customers objects replicated?

- A. A single facility in eu-west-1 and a single facility in eu-central-1
- B. A single facility in eu-west-1 and a single facility in us-east-1
- C. Multiple facilities in eu-west-1
- D. A single facility in eu-west-1

<details><summary>Answer:</summary><p>
[C]

Categories:
[S3]

Explanation:

Question 6@http://jayendrapatil.com/aws-s3-data-protection/

</p></details><hr>

### Question 7:

You are designing a personal document-archiving solution for your global enterprise with thousands of employee. Each employee has potentially gigabytes of data to be backed up in this archiving solution. The solution will be exposed to he employees as an application, where they can just drag and drop their files to the archiving system. Employees can retrieve their archives through a web interface. The corporate network has high bandwidth AWS DirectConnect connectivity to AWS. You have regulatory requirements that all data needs to be encrypted before being uploaded to the cloud. How do you implement this in a highly available and cost efficient way?

- A. Manage encryption keys on-premise in an encrypted relational database. Set up an on-premises server with sufficient storage to temporarily store files and then upload them to Amazon S3, providing a client-side master key. 
- B. Manage encryption keys in a Hardware Security Module(HSM) appliance on-premise server with sufficient storage to temporarily store, encrypt, and upload files directly into amazon Glacier. 
- C. Manage encryption keys in amazon Key Management Service (KMS), upload to amazon simple storage service (s3) with client-side encryption using a KMS customer master key ID and configure Amazon S3 lifecycle policies to store each object using the amazon glacier storage tier.
- D. Manage encryption keys in an AWS CloudHSM appliance. Encrypt files prior to uploading on the employee desktop and then upload directly into amazon glacier 

<details><summary>Answer:</summary><p>
[C]

Categories:
[S3, SES, KMS, Glacier]

Explanation:

Question 7@http://jayendrapatil.com/aws-s3-data-protection/

A: Storing temporary increases cost and not a high availability option

B: Not cost effective

C: with CSE-KMS the encryption happens at client side before the object is upload to S3 and KMS is cost effective as well

D: Not cost effective

</p></details><hr>

### Question 8:

A user has enabled server side encryption with S3. The user downloads the encrypted object from S3. How can the user decrypt it?

- A. S3 does not support server side encryption
- B. S3 provides a server side key to decrypt the object
- C. The user needs to decrypt the object using their own private key
- D. S3 manages encryption and decryption automatically

<details><summary>Answer:</summary><p>
[D]

Categories:
[S3]

Explanation:

Question 8@http://jayendrapatil.com/aws-s3-data-protection/

</p></details><hr>

### Question 9:

When uploading an object, what request header can be explicitly specified in a request to Amazon S3 to encrypt object data when saved on the server side?

- A. x-amz-storage-class
- B. Content-MD5
- C. x-amz-security-token
- D. x-amz-server-side-encryption

<details><summary>Answer:</summary><p>
[D]

Categories:
[S3]

Explanation:

Question 9@http://jayendrapatil.com/aws-s3-data-protection/

</p></details><hr>

