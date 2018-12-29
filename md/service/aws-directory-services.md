### Question 1:

The majority of your Infrastructure is on premises and you have a small footprint on AWS. Your company has decided to roll out a new application that is heavily dependent on low latency connectivity to LDAP for authentication. Your security policy requires minimal changes to the company’s existing application user management processes. What option would you implement to successfully launch this application?

- A. Create a second, independent LDAP server in AWS for your application to use for authentication 
- B. Establish a VPN connection so your applications can authenticate against your existing on-premises LDAP servers 
- C. Establish a VPN connection between your data center and AWS create a LDAP replica on AWS and configure your application to use the LDAP replica for authentication 
- D. Create a second LDAP domain on AWS establish a VPN connection to establish a trust relationship between your new and existing domains and use the new domain for authentication 

<details><summary>Answer:</summary><p>
[]

Categories:
[SES]

Explanation:

Question 1@http://jayendrapatil.com/aws-directory-services/

A: independent would not work for authentication as its a separate copy

B: not a low latency solution

C: RODCs low latency and minimal setup

D: Not minimal effort

</p></details><hr>

### Question 2:

A company is preparing to give AWS Management Console access to developers Company policy mandates identity federation and role-based access control. Roles are currently assigned using groups in the corporate Active Directory. What combination of the following will give developers access to the AWS console? (Select 2) Choose 2 answers

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

Question 2@http://jayendrapatil.com/aws-directory-services/

A: for Corporate Active directory

</p></details><hr>

### Question 3:

An Enterprise customer is starting their migration to the cloud, their main reason for migrating is agility, and they want to make their internal Microsoft Active Directory available to any applications running on AWS; this is so internal users only have to remember one set of credentials and as a central point of user control for leavers and joiners. How could they make their Active Directory secure, and highly available, with minimal on-premises infrastructure changes, in the most cost and time-efficient way? Choose the most appropriate

- A. Using Amazon Elastic Compute Cloud (EC2), they would create a DMZ using a security group; within the security group they could provision two smaller amazon EC2 instances that are running Openswan for resilient IPSEC tunnels, and two larger instance that are domain controllers; they would use multiple Availability Zones (Whats Openswan? Refer )
- B. Using VPC, they could create an extension to their data center and make use of resilient hardware IPSEC tunnels; they could then have two domain controller instances that are joined to their existing domain and reside within different subnets, in different Availability Zones 
- C. Within the customer’s existing infrastructure, they could provision new hardware to run Active Directory Federation Services; this would present Active Directory as a SAML2 endpoint on the internet; any new application on AWS could be written to authenticate using SAML2 
- D. The customer could create a stand-alone VPC with its own Active Directory Domain Controllers; two domain controller instances could be configured, one in each Availability Zone; new applications would authenticate with those domain controllers 

<details><summary>Answer:</summary><p>
[]

Categories:
[SES, EC2, VPC]

Explanation:

Question 3@http://jayendrapatil.com/aws-directory-services/

A: https://aws.amazon.com/articles/5472675506466066

B: highly available with 2 AZ’s, secure with VPN connection and minimal changes

C: not minimal on-premises hardware changes

D: not a central location, but a copy

</p></details><hr>

### Question 4:

A company needs to deploy virtual desktops to its customers in a virtual private cloud, leveraging existing security controls. Which set of AWS services and features will meet the company’s requirements?

- A. Virtual Private Network connection. AWS Directory Services, and ClassicLink 
- B. Virtual Private Network connection. AWS Directory Services, and Amazon Workspaces
- C. AWS Directory Service, Amazon Workspaces, and AWS Identity and Access Management 
- D. Amazon Elastic Compute Cloud, and AWS Identity and Access Management 

<details><summary>Answer:</summary><p>
[B]

Categories:
[Directory Services, VPC]

Explanation:

Question 4@http://jayendrapatil.com/aws-directory-services/

A: ClassicLink allows you to link an EC2-Classic instance to a VPC in your account, within the same region

B: WorkSpaces for Virtual desktops, and AWS Directory Services to authenticate to an existing on-premises AD through VPN

C: AD service needs a VPN connection to interact with an On-premise AD directory

D: Need WorkSpaces for virtual desktops

</p></details><hr>

### Question 5:

An Enterprise customer is starting their migration to the cloud, their main reason for migrating is agility and they want to make their internal Microsoft active directory available to any applications running on AWS, this is so internal users only have to remember one set of credentials and as a central point of user control for leavers and joiners. How could they make their active directory secure and highly available with minimal on-premises infrastructure changes in the most cost and time efficient way? Choose the most appropriate:

- A. Using Amazon EC2, they could create a DMZ using a security group, within the security group they could provision two smaller Amazon EC2 instances that are running Openswan for resilient IPSEC tunnels and two larger instances that are domain controllers, they would use multiple availability zones.
- B. Using VPC, they could create an extension to their data center and make use of resilient hardware IPSEC tunnels, they could then have two domain controller instances that are joined to their existing domain and reside within different subnets in different availability zones.
- C. Within the customer’s existing infrastructure, they could provision new hardware to run active directory federation services, this would present active directory as a SAML2 endpoint on the internet and any new application on AWS could be written to authenticate using SAML2 
- D. The customer could create a stand alone VPC with its own active directory domain controllers, two domain controller instances could be configured, one in each availability zone, new applications would authenticate with those domain controllers. 

<details><summary>Answer:</summary><p>
[B]

Categories:
[SES, EC2, VPC]

Explanation:

Question 5@http://jayendrapatil.com/aws-directory-services/

C: not a minimal change to the existing infrastructure

D: Standalone cannot use the same security

</p></details><hr>

### Question 6:

You run a 2000-engineer organization. You are about to begin using AWS at a large scale for the first time. You want to integrate with your existing identity management system running on Microsoft Active Directory, because your organization is a power-user of Active Directory. How should you manage your AWS identities in the simplest manner?

- A. Use a large AWS Directory Service Simple AD.
- B. Use a large AWS Directory Service AD Connector.
- C. Use a Sync Domain running on AWS Directory Service.
- D. Use an AWS Directory Sync Domain running on AWS Lambda.

<details><summary>Answer:</summary><p>
[B]

Categories:
[Lambda]

Explanation:

Question 6@http://jayendrapatil.com/aws-directory-services/

B: AD Connector can be used as power-user of Microsoft Active Directory. Simple AD only works with a subset of AD functionality

</p></details><hr>

