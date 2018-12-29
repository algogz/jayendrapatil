### Question 1:

After launching an instance that you intend to serve as a NAT (Network Address Translation) device in a public subnet you modify your route tables to have the NAT device be the target of internet bound traffic of your private subnet. When you try and make an outbound connection to the Internet from an instance in the private subnet, you are not successful. Which of the following steps could resolve the issue?

- A. Attaching a second Elastic Network interface (ENI) to the NAT instance, and placing it in the private subnet
- B. Attaching an Elastic IP address to the instance in the private subnet
- C. Attaching a second Elastic Network Interface (ENI) to the instance in the private subnet, and placing it in the public subnet
- D. Disabling the Source/Destination Check attribute on the NAT instance

<details><summary>Answer:</summary><p>
[D]

Categories:
[]

Explanation:

Question 1@http://jayendrapatil.com/aws-vpc-nat/

</p></details><hr>

### Question 2:

You manually launch a NAT AMI in a public subnet. The network is properly configured. Security groups and network access control lists are property configured. Instances in a private subnet can access the NAT. The NAT can access the Internet. However, private instances cannot access the Internet. What additional step is required to allow access from the private instances?

- A. Enable Source/Destination Check on the private Instances.
- B. Enable Source/Destination Check on the NAT instance.
- C. Disable Source/Destination Check on the private instances
- D. Disable Source/Destination Check on the NAT instance

<details><summary>Answer:</summary><p>
[D]

Categories:
[]

Explanation:

Question 2@http://jayendrapatil.com/aws-vpc-nat/

</p></details><hr>

### Question 3:

A user has created a VPC with public and private subnets. The VPC has CIDR 20.0.0.0/16. The private subnet uses CIDR 20.0.1.0/24 and the public subnet uses CIDR 20.0.0.0/24. The user is planning to host a web server in the public subnet (port 80. and a DB server in the private subnet (port 3306.. The user is configuring a security group of the NAT instance. Which of the below mentioned entries is not required for the NAT security group?

- A. For Inbound allow Source: 20.0.1.0/24 on port 80
- B. For Outbound allow Destination: 0.0.0.0/0 on port 80
- C. For Inbound allow Source: 20.0.0.0/24 on port 80
- D. For Outbound allow Destination: 0.0.0.0/0 on port 443

<details><summary>Answer:</summary><p>
[C]

Categories:
[SES, VPC]

Explanation:

Question 3@http://jayendrapatil.com/aws-vpc-nat/

C: http://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_NAT_Instance.html#NATSG

</p></details><hr>

### Question 4:

A web company is looking to implement an external payment service into their highly available application deployed in a VPC. Their application EC2 instances are behind a public facing ELB. Auto scaling is used to add additional instances as traffic increases. Under normal load the application runs 2 instances in the Auto Scaling group but at peak it can scale 3x in size. The application instances need to communicate with the payment service over the Internet, which requires whitelisting of all public IP addresses used to communicate with it. A maximum of 4 whitelisting IP addresses are allowed at a time and can be added through an API. How should they architect their solution?

- A. Route payment requests through two NAT instances setup for High Availability and whitelist the Elastic IP addresses attached to the NAT instances
- B. Whitelist the VPC Internet Gateway Public IP and route payment requests through the Internet Gateway. 
- C. Whitelist the ELB IP addresses and route payment requests from the Application servers through the ELB. 
- D. Automatically assign public IP addresses to the application instances in the Auto Scaling group and run a script on boot that adds each instances public IP address to the payment validation whitelist API. 

<details><summary>Answer:</summary><p>
[A]

Categories:
[SES, EC2, ASG, VPC, ELB]

Explanation:

Question 4@http://jayendrapatil.com/aws-vpc-nat/

B: Internet gateway is only to route traffic

C: ELB does not have a fixed IP address

D: would exceed the allowed 4 IP addresses

</p></details><hr>

