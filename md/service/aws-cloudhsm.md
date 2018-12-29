### Question 1:

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

Question 1@http://jayendrapatil.com/aws-cloudhsm/

</p></details><hr>

### Question 2:

An AWS customer is deploying a web application that is composed of a front-end running on Amazon EC2 and of confidential data that is stored on Amazon S3. The customer security policy that all access operations to this sensitive data must be authenticated and authorized by a centralized access management system that is operated by a separate security team. In addition, the web application team that owns and administers the EC2 web front-end instances is prohibited from having any ability to access the data that circumvents this centralized access management system. Which of the following configurations will support these requirements:

- A. Encrypt the data on Amazon S3 using a CloudHSM that is operated by the separate security team. Configure the web application to integrate with the CloudHSM for decrypting approved data access operations for trusted end-users. 
- B. Configure the web application to authenticate end-users against the centralized access management system. Have the web application provision trusted users STS tokens entitling the download of approved data directly from Amazon S3
- C. Have the separate security team create and IAM role that is entitled to access the data on Amazon S3. Have the web application team provision their instances with this role while denying their IAM users access to the data on Amazon S3 
- D. Configure the web application to authenticate end-users against the centralized access management system using SAML. Have the end-users authenticate to IAM using their SAML token and download the approved data directly from S3. 

<details><summary>Answer:</summary><p>
[B]

Categories:
[S3, IAM, EC2]

Explanation:

Question 2@http://jayendrapatil.com/aws-cloudhsm/

A: S3 doesn’t integrate directly with CloudHSM, also there is no centralized access management system control

B: (Controlled access and admins cannot access the data as it needs authentication)

C: Web team would have access to the data

D: not the way SAML auth works and not sure if the centralized access management system is SAML complaint

</p></details><hr>

