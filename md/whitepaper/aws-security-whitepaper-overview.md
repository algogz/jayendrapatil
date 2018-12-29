### Question 1:

In the shared security model, AWS is responsible for which of the following security best practices (check all that apply) :

- A. Penetration testing
- B. Operating system account security management 
- C. Threat modeling
- D. User group access management 
- E. Static code analysis 

<details><summary>Answer:</summary><p>
[]

Categories:
[]

Explanation:

Question 1@http://jayendrapatil.com/aws-security-whitepaper-overview/

B: User responsibility

D: User responsibility

E: AWS development cycle responsibility

</p></details><hr>

### Question 2:

You are running a web-application on AWS consisting of the following components an Elastic Load Balancer (ELB) an Auto-Scaling Group of EC2 instances running Linux/PHP/Apache, and Relational DataBase Service (RDS) MySQL. Which security measures fall into AWS’s responsibility?

- A. Protect the EC2 instances against unsolicited access by enforcing the principle of least-privilege access 
- B. Protect against IP spoofing or packet sniffing
- C. Assure all communication between EC2 instances and ELB is encrypted 
- D. Install latest security patches on ELB. RDS and EC2 instances 

<details><summary>Answer:</summary><p>
[]

Categories:
[RDS, EC2, ELB]

Explanation:

Question 2@http://jayendrapatil.com/aws-security-whitepaper-overview/

A: User responsibility

C: User responsibility

D: User responsibility

</p></details><hr>

### Question 3:

In AWS, which security aspects are the customer’s responsibility? Choose 4 answers

- A. Controlling physical access to compute resources 
- B. Patch management on the EC2 instances operating system
- C. Encryption of EBS (Elastic Block Storage) volumes
- D. Life-cycle management of IAM credentials
- E. Decommissioning storage devices 
- F. Security Group and ACL (Access Control List) settings

<details><summary>Answer:</summary><p>
[]

Categories:
[IAM, EC2, EBS]

Explanation:

Question 3@http://jayendrapatil.com/aws-security-whitepaper-overview/

A: AWS responsibility

E: AWS responsibility

</p></details><hr>

### Question 4:

Per the AWS Acceptable Use Policy, penetration testing of EC2 instances:

- A. May be performed by AWS, and will be performed by AWS upon customer request.
- B. May be performed by AWS, and is periodically performed by AWS.
- C. Are expressly prohibited under all circumstances.
- D. May be performed by the customer on their own instances with prior authorization from AWS.
- E. May be performed by the customer on their own instances, only if performed from EC2 instances

<details><summary>Answer:</summary><p>
[]

Categories:
[EC2]

Explanation:

Question 4@http://jayendrapatil.com/aws-security-whitepaper-overview/

</p></details><hr>

### Question 5:

Which is an operational process performed by AWS for data security?

- A. AES-256 encryption of data stored on any shared storage device 
- B. Decommissioning of storage devices using industry-standard practices
- C. Background virus scans of EBS volumes and EBS snapshots 
- D. Replication of data across multiple AWS Regions 
- E. Secure wiping of EBS data when an EBS volume is unmounted 

<details><summary>Answer:</summary><p>
[B]

Categories:
[EBS]

Explanation:

Question 5@http://jayendrapatil.com/aws-security-whitepaper-overview/

A: User responsibility

C: No virus scan is performed by AWS on User instances

D: AWS does not replicate data across regions unless done by User

E: data is not wiped off on EBS volume when unmounted and it can be remounted on other EC2 instance

</p></details><hr>

