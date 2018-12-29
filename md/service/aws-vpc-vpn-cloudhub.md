### Question 1:

You have in total 5 offices, and the entire employee related information is stored under AWS VPC instances. Now all the offices want to connect the instances in VPC using VPN. Which of the below help you to implement this?

- A. you can have redundant customer gateways between your data center and your VPC
- B. you can have multiple locations connected to the AWS VPN CloudHub
- C. You have to define 5 different static IP addresses in route table.
- D. 1 and 2
- E. 1,2 and 3

<details><summary>Answer:</summary><p>
[D]

Categories:
[SES, VPC]

Explanation:

Question 1@http://jayendrapatil.com/aws-vpc-vpn-cloudhub/

</p></details><hr>

### Question 2:

You have in total 15 offices, and the entire employee related information is stored under AWS VPC instances. Now all the offices want to connect the instances in VPC using VPN. What problem do you see in this scenario?

- A. You can not create more than 1 VPN connections with single VPC 
- B. You can not create more than 10 VPN connections with single VPC 
- C. When you create multiple VPN connections, the virtual private gateway can not sends network traffic to the appropriate VPN connection using statically assigned routes. 
- D. Statically assigned routes cannot be configured in case of more than 1 VPN with virtual private gateway. 
- E. None of above

<details><summary>Answer:</summary><p>
[E]

Categories:
[VPC]

Explanation:

Question 2@http://jayendrapatil.com/aws-vpc-vpn-cloudhub/

A: Can be created

B: soft limit can be extended

C: Can route the traffic to correct connection

D: can be configured

</p></details><hr>

### Question 3:

You have been asked to virtually extend two existing data centers into AWS to support a highly available application that depends on existing, on-premises resources located in multiple data centers and static content that is served from an Amazon Simple Storage Service (S3) bucket. Your design currently includes a dual-tunnel VPN connection between your CGW and VGW. Which component of your architecture represents a potential single point of failure that you should consider changing to make the solution more highly available?

- A. Add another VGW in a different Availability Zone and create another dual-tunnel VPN connection.
- B. Add another CGW in a different data center and create another dual-tunnel VPN connection.
- C. Add a second VGW in a different Availability Zone, and a CGW in a different data center, and create another dual-tunnel.
- D. No changes are necessary: the network architecture is currently highly available.

<details><summary>Answer:</summary><p>
[B]

Categories:
[S3, SES]

Explanation:

Question 3@http://jayendrapatil.com/aws-vpc-vpn-cloudhub/

B: http://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_VPN.html

</p></details><hr>

### Question 4:

You are designing network connectivity for your fat client application. The application is designed for business travelers who must be able to connect to it from their hotel rooms, cafes, public Wi-Fi hotspots, and elsewhere on the Internet. You do not want to publish the application on the Internet. Which network design meets the above requirements while minimizing deployment and operational costs? [PROFESSIONAL]

- A. Implement AWS Direct Connect, and create a private interface to your VPC. Create a public subnet and place your application servers in it. 
- B. Implement Elastic Load Balancing with an SSL listener that terminates the back-end connection to the application. 
- C. Configure an IPsec VPN connection, and provide the users with the configuration details. Create a public subnet in your VPC, and place your application servers in it. 
- D. Configure an SSL VPN solution in a public subnet of your VPC, then install and configure SSL VPN client software on all user computers. Create a private subnet in your VPC and place your application servers in it.

<details><summary>Answer:</summary><p>
[D]

Categories:
[VPC, ELB, Direct Connect]

Explanation:

Question 4@http://jayendrapatil.com/aws-vpc-vpn-cloudhub/

A: High Cost and does not minimize deployment

B: Needs to be published to internet

C: Instances still in public subnet are internet accessible

D: Cost effective and can be in private subnet as well

</p></details><hr>

### Question 5:

You are designing a connectivity solution between on-premises infrastructure and Amazon VPC Your server’s on-premises will De communicating with your VPC instances You will De establishing IPSec tunnels over the internet You will be using VPN gateways and terminating the IPsec tunnels on AWS-supported customer gateways. Which of the following objectives would you achieve by implementing an IPSec tunnel as outlined above? (Choose 4 answers) [PROFESSIONAL]

- A. End-to-end protection of data in transit
- B. End-to-end Identity authentication
- C. Data encryption across the Internet
- D. Protection of data in transit over the Internet
- E. Peer identity authentication between VPN gateway and customer gateway
- F. Data integrity protection across the Internet

<details><summary>Answer:</summary><p>
[C, D, E, F]

Categories:
[SES, VPC]

Explanation:

Question 5@http://jayendrapatil.com/aws-vpc-vpn-cloudhub/

</p></details><hr>

### Question 6:

A development team that is currently doing a nightly six-hour build which is lengthening over time on-premises with a large and mostly under utilized server would like to transition to a continuous integration model of development on AWS with multiple builds triggered within the same day. However, they are concerned about cost, security and how to integrate with existing on-premises applications such as their LDAP and email servers, which cannot move off-premises. The development environment needs a source code repository; a project management system with a MySQL database resources for performing the builds and a storage location for QA to pick up builds from. What AWS services combination would you recommend to meet the development team’s requirements? [PROFESSIONAL]

- A. A Bastion host Amazon EC2 instance running a VPN server for access from on-premises, Amazon EC2 for the source code repository with attached Amazon EBS volumes, Amazon EC2 and Amazon RDS MySQL for the project management system, EIP for the source code repository and project management system, Amazon SQL for a build queue, An Amazon Auto Scaling group of Amazon EC2 instances for performing builds and Amazon Simple Email Service for sending the build output. 
- B. An AWS Storage Gateway for connecting on-premises software applications with cloud-based storage securely, Amazon EC2 for the resource code repository with attached Amazon EBS volumes, Amazon EC2 and Amazon RDS MySQL for the project management system, EIPs for the source code repository and project management system, Amazon Simple Notification Service for a notification initiated build, An Auto Scaling group of Amazon EC2 instances for performing builds and Amazon S3 for the build output. 
- C. An AWS Storage Gateway for connecting on-premises software applications with cloud-based storage securely, Amazon EC2 for the resource code repository with attached Amazon EBS volumes, Amazon EC2 and Amazon RDS MySQL for the project management system, EIPs for the source code repository and project management system, Amazon SQS for a build queue, An Amazon Elastic Map Reduce (EMR) cluster of Amazon EC2 instances for performing builds and Amazon CloudFront for the build output. 
- D. A VPC with a VPN Gateway back to their on-premises servers, Amazon EC2 for the source-code repository with attached Amazon EBS volumes, Amazon EC2 and Amazon RDS MySQL for the project management system, EIPs for the source code repository and project management system, SQS for a build queue, An Auto Scaling group of EC2 instances for performing builds and S3 for the build output.

<details><summary>Answer:</summary><p>
[D]

Categories:
[S3, SES, RDS, CloudFront, SQS, EC2, Storage Gateway, ASG, EBS, VPC, SNS, EMR]

Explanation:

Question 6@http://jayendrapatil.com/aws-vpc-vpn-cloudhub/

A: Bastion is not for VPN connectivity also SES should not be used

B: Storage Gateway does provide secure connectivity but still needs VPN. SNS alone cannot handle builds

C: Storage Gateway does not provide secure connectivity, still needs VPN. EMR is not ideal for performing builds as it needs normal EC2 instances

D: VPN gateway is required for secure connectivity. SQS for build queue and EC2 for builds

</p></details><hr>

