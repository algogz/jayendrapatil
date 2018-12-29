### Question 1:

A photo-sharing service stores pictures in Amazon Simple Storage Service (S3) and allows application sign-in using an OpenID Connect-compatible identity provider. Which AWS Security Token Service approach to temporary access should you use for the Amazon S3 operations?

- A. SAML-based Identity Federation
- B. Cross-Account Access
- C. AWS IAM users
- D. Web Identity Federation

<details><summary>Answer:</summary><p>
[D]

Categories:
[S3, IAM]

Explanation:

Question 1@http://jayendrapatil.com/iam-role-identity-providers-federation/

</p></details><hr>

### Question 2:

Which technique can be used to integrate AWS IAM (Identity and Access Management) with an on-premise LDAP (Lightweight Directory Access Protocol) directory service?

- A. Use an IAM policy that references the LDAP account identifiers and the AWS credentials.
- B. Use SAML (Security Assertion Markup Language) to enable single sign-on between AWS and LDAP
- C. Use AWS Security Token Service from an identity broker to issue short-lived AWS credentials
- D. Use IAM roles to automatically rotate the IAM credentials when LDAP credentials are updated.
- E. Use the LDAP credentials to restrict a group of users from launching specific EC2 instance types.

<details><summary>Answer:</summary><p>
[C]

Categories:
[IAM, EC2]

Explanation:

Question 2@http://jayendrapatil.com/iam-role-identity-providers-federation/

C: https://aws.amazon.com/blogs/aws/aws-identity-and-access-management-now-with-identity-federation/

C: . 

</p></details><hr>

### Question 3:

You are designing a photo sharing mobile app the application will store all pictures in a single Amazon S3 bucket. Users will upload pictures from their mobile device directly to Amazon S3 and will be able to view and download their own pictures directly from Amazon S3. You want to configure security to handle potentially millions of users in the most secure manner possible. What should your server-side application do when a new user registers on the photo-sharing mobile application? [PROFESSIONAL]

- A. Create a set of long-term credentials using AWS Security Token Service with appropriate permissions Store these credentials in the mobile app and use them to access Amazon S3.
- B. Record the user’s Information in Amazon RDS and create a role in IAM with appropriate permissions. When the user uses their mobile app create temporary credentials using the AWS Security Token Service ‘AssumeRole’ function. Store these credentials in the mobile app’s memory and use them to access Amazon S3. Generate new credentials the next time the user runs the mobile app.
- C. Record the user’s Information in Amazon DynamoDB. When the user uses their mobile app create temporary credentials using AWS Security Token Service with appropriate permissions. Store these credentials in the mobile app’s memory and use them to access Amazon S3 Generate new credentials the next time the user runs the mobile app.
- D. Create IAM user. Assign appropriate permissions to the IAM user Generate an access key and secret key for the IAM user, store them in the mobile app and use these credentials to access Amazon S3.
- E. Create an IAM user. Update the bucket policy with appropriate permissions for the IAM user Generate an access Key and secret Key for the IAM user, store them In the mobile app and use these credentials to access Amazon S3.

<details><summary>Answer:</summary><p>
[B]

Categories:
[S3, SES, RDS, IAM, DynamoDB]

Explanation:

Question 3@http://jayendrapatil.com/iam-role-identity-providers-federation/

</p></details><hr>

### Question 4:

Your company has recently extended its datacenter into a VPC on AWS to add burst computing capacity as needed Members of your Network Operations Center need to be able to go to the AWS Management Console and administer Amazon EC2 instances as necessary. You don’t want to create new IAM users for each NOC member and make those users sign in again to the AWS Management Console. Which option below will meet the needs for your NOC members? [PROFESSIONAL]

- A. Use OAuth 2.0 to retrieve temporary AWS security credentials to enable your NOC members to sign in to the AWS Management Console.
- B. Use Web Identity Federation to retrieve AWS temporary security credentials to enable your NOC members to sign in to the AWS Management Console.
- C. Use your on-premises SAML 2.O-compliant identity provider (IDP) to grant the NOC members federated access to the AWS Management Console via the AWS single sign-on (SSO) endpoint.
- D. Use your on-premises SAML 2.0-compliant identity provider (IDP) to retrieve temporary security credentials to enable NOC members to sign in to the AWS Management Console

<details><summary>Answer:</summary><p>
[C]

Categories:
[SES, IAM, EC2, VPC]

Explanation:

Question 4@http://jayendrapatil.com/iam-role-identity-providers-federation/

</p></details><hr>

### Question 5:

A corporate web application is deployed within an Amazon Virtual Private Cloud (VPC) and is connected to the corporate data center via an iPsec VPN. The application must authenticate against the on-premises LDAP server. After authentication, each logged-in user can only access an Amazon Simple Storage Space (S3) keyspace specific to that user. Which two approaches can satisfy these objectives? (Choose 2 answers) [PROFESSIONAL]

- A. Develop an identity broker that authenticates against IAM security Token service to assume a IAM role in order to get temporary AWS security credentials. The application calls the identity broker to get AWS temporary security credentials with access to the appropriate S3 bucket. 
- B. The application authenticates against LDAP and retrieves the name of an IAM role associated with the user. The application then calls the IAM Security Token Service to assume that IAM role. The application can use the temporary credentials to access the appropriate S3 bucket.
- C. Develop an identity broker that authenticates against LDAP and then calls IAM Security Token Service to get IAM federated user credentials The application calls the identity broker to get IAM federated user credentials with access to the appropriate S3 bucket.
- D. The application authenticates against LDAP the application then calls the AWS identity and Access Management (IAM) Security Token service to log in to IAM using the LDAP credentials the application can use the IAM temporary credentials to access the appropriate S3 bucket. 
- E. The application authenticates against IAM Security Token Service using the LDAP credentials the application uses those temporary AWS security credentials to access the appropriate S3 bucket. 

<details><summary>Answer:</summary><p>
[B, C]

Categories:
[S3, SES, IAM, VPC]

Explanation:

Question 5@http://jayendrapatil.com/iam-role-identity-providers-federation/

A: Needs to authenticate against LDAP and not IAM

B: Authenticates with LDAP and calls the AssumeRole

C: Custom Identity broker implementation, with authentication with LDAP and using federated token

D: Can’t login to IAM using LDAP credentials

E: Need to authenticate with LDAP

</p></details><hr>

### Question 6:

Company B is launching a new game app for mobile devices. Users will log into the game using their existing social media account to streamline data capture. Company B would like to directly save player data and scoring information from the mobile app to a DynamoDB table named Score Data When a user saves their game the progress data will be stored to the Game state S3 bucket. what is the best approach for storing data to DynamoDB and S3? [PROFESSIONAL]

- A. Use an EC2 Instance that is launched with an EC2 role providing access to the Score Data DynamoDB table and the GameState S3 bucket that communicates with the mobile app via web services.
- B. Use temporary security credentials that assume a role providing access to the Score Data DynamoDB table and the Game State S3 bucket using web identity federation
- C. Use Login with Amazon allowing users to sign in with an Amazon account providing the mobile app with access to the Score Data DynamoDB table and the Game State S3 bucket.
- D. Use an IAM user with access credentials assigned a role providing access to the Score Data DynamoDB table and the Game State S3 bucket for distribution with the mobile app.

<details><summary>Answer:</summary><p>
[B]

Categories:
[S3, IAM, EC2, DynamoDB]

Explanation:

Question 6@http://jayendrapatil.com/iam-role-identity-providers-federation/

</p></details><hr>

### Question 7:

A user has created a mobile application which makes calls to DynamoDB to fetch certain data. The application is using the DynamoDB SDK and root account access/secret access key to connect to DynamoDB from mobile. Which of the below mentioned statements is true with respect to the best practice for security in this scenario?

- A. User should create a separate IAM user for each mobile application and provide DynamoDB access with it
- B. User should create an IAM role with DynamoDB and EC2 access. Attach the role with EC2 and route all calls from the mobile through EC2
- C. The application should use an IAM role with web identity federation which validates calls to DynamoDB with identity providers, such as Google, Amazon, and Facebook
- D. Create an IAM Role with DynamoDB access and attach it with the mobile application

<details><summary>Answer:</summary><p>
[C]

Categories:
[IAM, EC2, DynamoDB]

Explanation:

Question 7@http://jayendrapatil.com/iam-role-identity-providers-federation/

</p></details><hr>

### Question 8:

You are managing the AWS account of a big organization. The organization has more than 1000+ employees and they want to provide access to the various services to most of the employees. Which of the below mentioned options is the best possible solution in this case?

- A. The user should create a separate IAM user for each employee and provide access to them as per the policy
- B. The user should create an IAM role and attach STS with the role. The user should attach that role to the EC2 instance and setup AWS authentication on that server
- C. The user should create IAM groups as per the organization’s departments and add each user to the group for better access control
- D. Attach an IAM role with the organization’s authentication service to authorize each user for various AWS services

<details><summary>Answer:</summary><p>
[D]

Categories:
[IAM, EC2]

Explanation:

Question 8@http://jayendrapatil.com/iam-role-identity-providers-federation/

</p></details><hr>

### Question 9:

Your fortune 500 company has under taken a TCO analysis evaluating the use of Amazon S3 versus acquiring more hardware The outcome was that all employees would be granted access to use Amazon S3 for storage of their personal documents. Which of the following will you need to consider so you can set up a solution that incorporates single sign-on from your corporate AD or LDAP directory and restricts access for each user to a designated user folder in a bucket? (Choose 3 Answers) [PROFESSIONAL]

- A. Setting up a federation proxy or identity provider
- B. Using AWS Security Token Service to generate temporary tokens
- C. Tagging each folder in the bucket
- D. Configuring IAM role
- E. Setting up a matching IAM user for every user in your corporate directory that needs access to a folder in the bucket

<details><summary>Answer:</summary><p>
[A, B, D]

Categories:
[S3, IAM]

Explanation:

Question 9@http://jayendrapatil.com/iam-role-identity-providers-federation/

</p></details><hr>

### Question 10:

An AWS customer is deploying a web application that is composed of a front-end running on Amazon EC2 and of confidential data that is stored on Amazon S3. The customer security policy that all access operations to this sensitive data must be authenticated and authorized by a centralized access management system that is operated by a separate security team. In addition, the web application team that owns and administers the EC2 web front-end instances is prohibited from having any ability to access the data that circumvents this centralized access management system. Which of the following configurations will support these requirements? [PROFESSIONAL]

- A. Encrypt the data on Amazon S3 using a CloudHSM that is operated by the separate security team. Configure the web application to integrate with the CloudHSM for decrypting approved data access operations for trusted end-users. 
- B. Configure the web application to authenticate end-users against the centralized access management system. Have the web application provision trusted users STS tokens entitling the download of approved data directly from Amazon S3
- C. Have the separate security team create and IAM role that is entitled to access the data on Amazon S3. Have the web application team provision their instances with this role while denying their IAM users access to the data on Amazon S3 
- D. Configure the web application to authenticate end-users against the centralized access management system using SAML. Have the end-users authenticate to IAM using their SAML token and download the approved data directly from S3. 

<details><summary>Answer:</summary><p>
[B]

Categories:
[S3, IAM, EC2]

Explanation:

Question 10@http://jayendrapatil.com/iam-role-identity-providers-federation/

A: S3 doesn’t integrate directly with CloudHSM, also there is no centralized access management system control

B: (Controlled access and admins cannot access the data as it needs authentication)

C: Web team would have access to the data

D: not the way SAML auth works and not sure if the centralized access management system is SAML complaint

</p></details><hr>

### Question 11:

What is web identity federation?

- A. Use of an identity provider like Google or Facebook to become an AWS IAM User.
- B. Use of an identity provider like Google or Facebook to exchange for temporary AWS security credentials.
- C. Use of AWS IAM User tokens to log in as a Google or Facebook user.
- D. Use of AWS STS Tokens to log in as a Google or Facebook user.

<details><summary>Answer:</summary><p>
[B]

Categories:
[IAM]

Explanation:

Question 11@http://jayendrapatil.com/iam-role-identity-providers-federation/

</p></details><hr>

### Question 12:

Games-R-Us is launching a new game app for mobile devices. Users will log into the game using their existing Facebook account and the game will record player data and scoring information directly to a DynamoDB table. What is the most secure approach for signing requests to the DynamoDB API?

- A. Create an IAM user with access credentials that are distributed with the mobile app to sign the requests
- B. Distribute the AWS root account access credentials with the mobile app to sign the requests
- C. Request temporary security credentials using web identity federation to sign the requests
- D. Establish cross account access between the mobile app and the DynamoDB table to sign the requests

<details><summary>Answer:</summary><p>
[C]

Categories:
[IAM, DynamoDB]

Explanation:

Question 12@http://jayendrapatil.com/iam-role-identity-providers-federation/

</p></details><hr>

### Question 13:

You are building a mobile app for consumers to post cat pictures online. You will be storing the images in AWS S3. You want to run the system very cheaply and simply. Which one of these options allows you to build a photo sharing application without needing to worry about scaling expensive uploads processes, authentication/authorization and so forth?

- A. Build the application out using AWS Cognito and web identity federation to allow users to log in using Facebook or Google Accounts. Once they are logged in, the secret token passed to that user is used to directly access resources on AWS, like AWS S3.
- B. Use JWT or SAML compliant systems to build authorization policies. Users log in with a username and password, and are given a token they can use indefinitely to make calls against the photo infrastructure.
- C. Use AWS API Gateway with a constantly rotating API Key to allow access from the client-side. Construct a custom build of the SDK and include S3 access in it.
- D. Create an AWS oAuth Service Domain ad grant public signup and access to the domain. During setup, add at least one major social media site as a trusted Identity Provider for users.

<details><summary>Answer:</summary><p>
[A]

Categories:
[S3, SES, API Gateway]

Explanation:

Question 13@http://jayendrapatil.com/iam-role-identity-providers-federation/

A: https://blogs.aws.amazon.com/security/post/Tx3SYCORF5EKRC0/How-Does-Amazon-Cognito-Relate-to-Existing-Web-Identity-Federation

A: Amazon Cognito is a superset of the functionality provided by web identity federation. Refer

</p></details><hr>

### Question 14:

The Marketing Director in your company asked you to create a mobile app that lets users post sightings of good deeds known as random acts of kindness in 80-character summaries. You decided to write the application in JavaScript so that it would run on the broadest range of phones, browsers, and tablets. Your application should provide access to Amazon DynamoDB to store the good deed summaries. Initial testing of a prototype shows that there aren’t large spikes in usage. Which option provides the most cost-effective and scalable architecture for this application? [PROFESSIONAL]

- A. Provide the JavaScript client with temporary credentials from the Security Token Service using a Token Vending Machine (TVM) on an EC2 instance to provide signed credentials mapped to an Amazon Identity and Access Management (IAM) user allowing DynamoDB puts and S3 gets. You serve your mobile application out of an S3 bucket enabled as a web site. Your client updates DynamoDB. (Single EC2 instance not a scalable architecture)
- B. Register the application with a Web Identity Provider like Amazon, Google, or Facebook, create an IAM role for that provider, and set up permissions for the IAM role to allow S3 gets and DynamoDB puts. You serve your mobile application out of an S3 bucket enabled as a web site. Your client updates DynamoDB.
- C. Provide the JavaScript client with temporary credentials from the Security Token Service using a Token Vending Machine (TVM) to provide signed credentials mapped to an IAM user allowing DynamoDB puts. You serve your mobile application out of Apache EC2 instances that are load-balanced and autoscaled. Your EC2 instances are configured with an IAM role that allows DynamoDB puts. Your server updates DynamoDB. (Is Scalable but Not cost effective)
- D. Register the JavaScript application with a Web Identity Provider like Amazon, Google, or Facebook, create an IAM role for that provider, and set up permissions for the IAM role to allow DynamoDB puts. You serve your mobile application out of Apache EC2 instances that are load-balanced and autoscaled. Your EC2 instances are configured with an IAM role that allows DynamoDB puts. Your server updates DynamoDB. (Is Scalable but Not cost effective)

<details><summary>Answer:</summary><p>
[B]

Categories:
[S3, IAM, EC2, DynamoDB]

Explanation:

Question 14@http://jayendrapatil.com/iam-role-identity-providers-federation/

B: (Can work with JavaScript SDK, is scalable and cost effective)

</p></details><hr>

