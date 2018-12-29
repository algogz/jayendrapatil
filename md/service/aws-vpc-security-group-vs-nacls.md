### Question 1:

Instance A and instance B are running in two different subnets A and B of a VPC. Instance A is not able to ping instance B. What are two possible reasons for this? (Pick 2 correct answers)

- A. The routing table of subnet A has no target route to subnet B
- B. The security group attached to instance B does not allow inbound ICMP traffic
- C. The policy linked to the IAM role on instance A is not configured correctly
- D. The NACL on subnet B does not allow outbound ICMP traffic

<details><summary>Answer:</summary><p>
[B, D]

Categories:
[IAM, VPC]

Explanation:

Question 1@http://jayendrapatil.com/aws-vpc-security-group-vs-nacls/

</p></details><hr>

### Question 2:

An instance is launched into a VPC subnet with the network ACL configured to allow all inbound traffic and deny all outbound traffic. The instance’s security group is configured to allow SSH from any IP address and deny all outbound traffic. What changes need to be made to allow SSH access to the instance?

- A. The outbound security group needs to be modified to allow outbound traffic.
- B. The outbound network ACL needs to be modified to allow outbound traffic.
- C. Nothing, it can be accessed from any IP address using SSH.
- D. Both the outbound security group and outbound network ACL need to be modified to allow outbound traffic.

<details><summary>Answer:</summary><p>
[B]

Categories:
[VPC]

Explanation:

Question 2@http://jayendrapatil.com/aws-vpc-security-group-vs-nacls/

</p></details><hr>

### Question 3:

From what services I can block incoming/outgoing IPs?

- A. Security Groups
- B. DNS
- C. ELB
- D. VPC subnet
- E. IGW
- F. NACL

<details><summary>Answer:</summary><p>
[F]

Categories:
[VPC, ELB]

Explanation:

Question 3@http://jayendrapatil.com/aws-vpc-security-group-vs-nacls/

</p></details><hr>

### Question 4:

What is the difference between a security group in VPC and a network ACL in VPC (chose 3 correct answers)

- A. Security group restricts access to a Subnet while ACL restricts traffic to EC2
- B. Security group restricts access to EC2 while ACL restricts traffic to a subnet
- C. Security group can work outside the VPC also while ACL only works within a VPC
- D. Network ACL performs stateless filtering and Security group provides stateful filtering
- E. Security group can only set Allow rule, while ACL can set Deny rule also

<details><summary>Answer:</summary><p>
[B, D, E]

Categories:
[EC2, VPC]

Explanation:

Question 4@http://jayendrapatil.com/aws-vpc-security-group-vs-nacls/

</p></details><hr>

### Question 5:

You are currently hosting multiple applications in a VPC and have logged numerous port scans coming in from a specific IP address block. Your security team has requested that all access from the offending IP address block be denied for the next 24 hours. Which of the following is the best method to quickly and temporarily deny access from the specified IP address block?

- A. Create an AD policy to modify Windows Firewall settings on all hosts in the VPC to deny access from the IP address block
- B. Modify the Network ACLs associated with all public subnets in the VPC to deny access from the IP address block
- C. Add a rule to all of the VPC 5 Security Groups to deny access from the IP address block
- D. Modify the Windows Firewall settings on all Amazon Machine Images (AMIs) that your organization uses in that VPC to deny access from the IP address block

<details><summary>Answer:</summary><p>
[B]

Categories:
[SES, VPC]

Explanation:

Question 5@http://jayendrapatil.com/aws-vpc-security-group-vs-nacls/

</p></details><hr>

### Question 6:

You have two Elastic Compute Cloud (EC2) instances inside a Virtual Private Cloud (VPC) in the same Availability Zone (AZ) but in different subnets. One instance is running a database and the other instance an application that will interface with the database. You want to confirm that they can talk to each other for your application to work properly. Which two things do we need to confirm in the VPC settings so that these EC2 instances can communicate inside the VPC? Choose 2 answers

- A. A network ACL that allows communication between the two subnets.
- B. Both instances are the same instance class and using the same Key-pair.
- C. That the default route is set to a NAT instance or Internet Gateway (IGW) for them to communicate.
- D. Security groups are set to allow the application host to talk to the database on the right port/protocol

<details><summary>Answer:</summary><p>
[A, D]

Categories:
[EC2, VPC]

Explanation:

Question 6@http://jayendrapatil.com/aws-vpc-security-group-vs-nacls/

</p></details><hr>

### Question 7:

A benefits enrollment company is hosting a 3-tier web application running in a VPC on AWS, which includes a NAT (Network Address Translation) instance in the public Web tier. There is enough provisioned capacity for the expected workload tor the new fiscal year benefit enrollment period plus some extra overhead Enrollment proceeds nicely for two days and then the web tier becomes unresponsive, upon investigation using CloudWatch and other monitoring tools it is discovered that there is an extremely large and unanticipated amount of inbound traffic coming from a set of 15 specific IP addresses over port 80 from a country where the benefits company has no customers. The web tier instances are so overloaded that benefit enrollment administrators cannot even SSH into them. Which activity would be useful in defending against this attack?

- A. Create a custom route table associated with the web tier and block the attacking IP addresses from the IGW (internet Gateway)
- B. Change the EIP (Elastic IP Address) of the NAT instance in the web tier subnet and update the Main Route Table with the new EIP
- C. Create 15 Security Group rules to block the attacking IP addresses over port 80
- D. Create an inbound NACL (Network Access control list) associated with the web tier subnet with deny rules to block the attacking IP addresses

<details><summary>Answer:</summary><p>
[D]

Categories:
[SES, CloudWatch, VPC]

Explanation:

Question 7@http://jayendrapatil.com/aws-vpc-security-group-vs-nacls/

</p></details><hr>

### Question 8:

Which of the following statements describes network ACLs? (Choose 2 answers)

- A. Responses to allowed inbound traffic are allowed to flow outbound regardless of outbound rules, and vice versa 
- B. Using network ACLs, you can deny access from a specific IP range
- C. Keep network ACL rules simple and use a security group to restrict application level access
- D. NACLs are associated with a single Availability Zone 

<details><summary>Answer:</summary><p>
[B, C]

Categories:
[SES]

Explanation:

Question 8@http://jayendrapatil.com/aws-vpc-security-group-vs-nacls/

A: are stateless

D: associated with Subnet

</p></details><hr>

### Question 9:

You are designing security inside your VPC. You are considering the options for establishing separate security zones and enforcing network traffic rules across different zone to limit Instances can communications. How would you accomplish these requirements? Choose 2 answers

- A. Configure a security group for every zone. Configure a default allow all rule. Configure explicit deny rules for the zones that shouldn’t be able to communicate with one another 
- B. Configure you instances to use pre-set IP addresses with an IP address range every security zone. Configure NACL to explicitly allow or deny communication between the different IP address ranges, as required for interzone communication
- C. Configure a security group for every zone. Configure allow rules only between zone that need to be able to communicate with one another. Use implicit deny all rule to block any other traffic
- D. Configure multiple subnets in your VPC, one for each zone. Configure routing within your VPC in such a way that each subnet only has routes to other subnets with which it needs to communicate, and doesn’t have routes to subnets with which it shouldn’t be able to communicate. 

<details><summary>Answer:</summary><p>
[B, C]

Categories:
[SES, VPC]

Explanation:

Question 9@http://jayendrapatil.com/aws-vpc-security-group-vs-nacls/

A: Security group does not allow deny rules

D: default routes are unmodifiable

</p></details><hr>

### Question 10:

Your entire AWS infrastructure lives inside of one Amazon VPC. You have an Infrastructure monitoring application running on an Amazon instance in Availability Zone (AZ) A of the region, and another application instance running in AZ B. The monitoring application needs to make use of ICMP ping to confirm network reachability of the instance hosting the application. Can you configure the security groups for these instances to only allow the ICMP ping to pass from the monitoring instance to the application instance and nothing else” If so how?

- A. No Two instances in two different AZ’s can’t talk directly to each other via ICMP ping as that protocol is not allowed across subnet (i.e. broadcast) boundaries 
- B. Yes Both the monitoring instance and the application instance have to be a part of the same security group, and that security group needs to allow inbound ICMP 
- C. Yes, The security group for the monitoring instance needs to allow outbound ICMP and the application instance’s security group needs to allow Inbound ICMP
- D. Yes, Both the monitoring instance’s security group and the application instance’s security group need to allow both inbound and outbound ICMP ping packets since ICMP is not a connection-oriented protocol 

<details><summary>Answer:</summary><p>
[C]

Categories:
[VPC]

Explanation:

Question 10@http://jayendrapatil.com/aws-vpc-security-group-vs-nacls/

A: Can communicate

B: Need not have to be part of same security group

C: is stateful, so just allow outbound ICMP from monitoring and inbound ICMP on monitored instance

D: Security groups are stateful

</p></details><hr>

### Question 11:

A user has configured a VPC with a new subnet. The user has created a security group. The user wants to configure that instances of the same subnet communicate with each other. How can the user configure this with the security group?

- A. There is no need for a security group modification as all the instances can communicate with each other inside the same subnet
- B. Configure the subnet as the source in the security group and allow traffic on all the protocols and ports
- C. Configure the security group itself as the source and allow traffic on all the protocols and ports
- D. The user has to use VPC peering to configure this

<details><summary>Answer:</summary><p>
[C]

Categories:
[VPC]

Explanation:

Question 11@http://jayendrapatil.com/aws-vpc-security-group-vs-nacls/

</p></details><hr>

### Question 12:

You are designing a data leak prevention solution for your VPC environment. You want your VPC Instances to be able to access software depots and distributions on the Internet for product updates. The depots and distributions are accessible via third party CDNs by their URLs. You want to explicitly deny any other outbound connections from your VPC instances to hosts on the Internet. Which of the following options would you consider?

- A. Configure a web proxy server in your VPC and enforce URL-based rules for outbound access Remove default routes.
- B. Implement security groups and configure outbound rules to only permit traffic to software depots.
- C. Move all your instances into private VPC subnets remove default routes from all routing tables and add specific routes to the software depots and distributions only.
- D. Implement network access control lists to all specific destinations, with an Implicit deny as a rule.

<details><summary>Answer:</summary><p>
[A]

Categories:
[VPC]

Explanation:

Question 12@http://jayendrapatil.com/aws-vpc-security-group-vs-nacls/

A: Security group and NACL cannot have URLs in the rules nor does the route

</p></details><hr>

### Question 13:

You have an EC2 Security Group with several running EC2 instances. You change the Security Group rules to allow inbound traffic on a new port and protocol, and launch several new instances in the same Security Group. The new rules apply:

- A. Immediately to all instances in the security group.
- B. Immediately to the new instances only.
- C. Immediately to the new instances, but old instances must be stopped and restarted before the new rules apply.
- D. To all instances, but it may take several minutes for old instances to see the changes.

<details><summary>Answer:</summary><p>
[A]

Categories:
[EC2]

Explanation:

Question 13@http://jayendrapatil.com/aws-vpc-security-group-vs-nacls/

</p></details><hr>

