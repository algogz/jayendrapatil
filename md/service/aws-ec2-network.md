### Question 1:

A user is launching an EC2 instance in the US East region. Which of the below mentioned options is recommended by AWS with respect to the selection of the availability zone?

- A. Always select the US-East-1-a zone for HA
- B. Do not select the AZ; instead let AWS select the AZ
- C. The user can never select the availability zone while launching an instance
- D. Always select the AZ while launching an instance

<details><summary>Answer:</summary><p>
[B]

Categories:
[EC2]

Explanation:

Question 1@http://jayendrapatil.com/aws-ec2-network/

</p></details><hr>

### Question 2:

You have multiple Amazon EC2 instances running in a cluster across multiple Availability Zones within the same region. What combination of the following should be used to ensure the highest network performance (packets per second), lowest latency, and lowest jitter? Choose 3 answers

- A. Amazon EC2 placement groups 
- B. Enhanced networking
- C. Amazon PV AMI 
- D. Amazon HVM AMI
- E. Amazon Linux 
- F. Amazon VPC

<details><summary>Answer:</summary><p>
[B, D, F]

Categories:
[EC2, VPC]

Explanation:

Question 2@http://jayendrapatil.com/aws-ec2-network/

A: would not work for multiple AZs

B: provides network performance, lowest latency

C: Needs HVM

E: Can work on other flavors of Unix as well

F: Enhanced networking works only in VPC

</p></details><hr>

### Question 3:

Regarding the attaching of ENI to an instance, what does ‘warm attach’ refer to?

- A. Attaching an ENI to an instance when it is stopped
- B. Attaching an ENI to an instance when it is running
- C. Attaching an ENI to an instance during the launch process

<details><summary>Answer:</summary><p>
[A]

Categories:
[]

Explanation:

Question 3@http://jayendrapatil.com/aws-ec2-network/

</p></details><hr>

### Question 4:

Can I detach the primary (eth0) network interface when the instance is running or stopped?

- A. Yes, You can.
- B. You cannot
- C. Depends on the state of the interface at the time

<details><summary>Answer:</summary><p>
[B]

Categories:
[]

Explanation:

Question 4@http://jayendrapatil.com/aws-ec2-network/

</p></details><hr>

### Question 5:

By default what are ENIs that are automatically created and attached to instances using the EC2 console set to do when the attached instance terminates?

- A. Remain as is
- B. Terminate
- C. Hibernate
- D. Pause

<details><summary>Answer:</summary><p>
[B]

Categories:
[EC2]

Explanation:

Question 5@http://jayendrapatil.com/aws-ec2-network/

</p></details><hr>

### Question 6:

Select the incorrect statement

- A. In Amazon EC2, the private IP addresses only returned to Amazon EC2 when the instance is stopped or terminated
- B. In Amazon VPC, an instance retains its private IP addresses when the instance is stopped.
- C. In Amazon VPC, an instance does NOT retain its private IP addresses when the instance is stopped
- D. In Amazon EC2, the private IP address is associated exclusively with the instance for its lifetime

<details><summary>Answer:</summary><p>
[C]

Categories:
[SES, EC2, VPC]

Explanation:

Question 6@http://jayendrapatil.com/aws-ec2-network/

</p></details><hr>

### Question 7:

To ensure failover capabilities, consider using a _____ for incoming traffic on a network interface”.

- A. primary public IP
- B. secondary private IP
- C. secondary public IP
- D. add on secondary IP

<details><summary>Answer:</summary><p>
[B]

Categories:
[]

Explanation:

Question 7@http://jayendrapatil.com/aws-ec2-network/

</p></details><hr>

### Question 8:

Which statements are true about Elastic Network Interface (ENI)? (Choose 2 answers)

- A. You can attach an ENI in one AZ to an instance in another AZ
- B. You can change the security group membership of an ENI
- C. You can attach an instance to tow different subnets within a VPC by using two ENIs
- D. You can attach an ENI in one VPC to an instance in another VPC

<details><summary>Answer:</summary><p>
[B, C]

Categories:
[VPC]

Explanation:

Question 8@http://jayendrapatil.com/aws-ec2-network/

</p></details><hr>

### Question 9:

A user is planning to host a web server as well as an app server on a single EC2 instance, which is a part of the public subnet of a VPC. How can the user setup to have two separate public IPs and separate security groups for both the application as well as the web server?

- A. Launch a VPC instance with two network interfaces. Assign a separate security group to each and AWS will assign a separate public IP to them. 
- B. Launch VPC with two separate subnets and make the instance a part of both the subnets.
- C. Launch a VPC instance with two network interfaces. Assign a separate security group and elastic IP to them.
- D. Launch a VPC with ELB such that it redirects requests to separate VPC instances of the public subnet.

<details><summary>Answer:</summary><p>
[C]

Categories:
[EC2, VPC, ELB]

Explanation:

Question 9@http://jayendrapatil.com/aws-ec2-network/

A: AWS cannot assign public IPs for instance with multiple ENIs

</p></details><hr>

### Question 10:

An organization has created multiple components of a single application for compartmentalization. Currently all the components are hosted on a single EC2 instance. Due to security reasons the organization wants to implement two separate SSLs for the separate modules although it is already using VPC. How can the organization achieve this with a single instance?

- A. Create a VPC instance, which will have both the ACL and the security group attached to it and have separate rules for each IP address.
- B. Create a VPC instance, which will have multiple network interfaces with multiple elastic IP addresses.
- C. You have to launch two instances each in a separate subnet and allow VPC peering for a single IP.
- D. Create a VPC instance, which will have multiple subnets attached to it and each will have a separate IP address.

<details><summary>Answer:</summary><p>
[B]

Categories:
[SES, EC2, VPC]

Explanation:

Question 10@http://jayendrapatil.com/aws-ec2-network/

</p></details><hr>

### Question 11:

Your system automatically provisions EIPs to EC2 instances in a VPC on boot. The system provisions the whole VPC and stack at once. You have two of them per VPC. On your new AWS account, your attempt to create a Development environment failed, after successfully creating Staging and Production environments in the same region. What happened?

- A. You didn’t choose the Development version of the AMI you are using.
- B. You didn’t set the Development flag to true when deploying EC2 instances.
- C. You hit the soft limit of 5 EIPs per region and requested a 6th.
- D. You hit the soft limit of 2 VPCs per region and requested a 3rd.

<details><summary>Answer:</summary><p>
[C]

Categories:
[EC2, VPC]

Explanation:

Question 11@http://jayendrapatil.com/aws-ec2-network/

C: There is a soft limit of 5 EIPs per Region for VPC on new accounts. The third environment could not allocate the 6th EIP

</p></details><hr>

### Question 12:

A user has created a VPC with a public subnet. The user has terminated all the instances, which are part of the subnet. Which of the below mentioned statements is true with respect to this scenario?

- A. The user cannot delete the VPC since the subnet is not deleted
- B. All network interface attached with the instances will be deleted
- C. When the user launches a new instance it cannot use the same subnet
- D. The subnet to which the instances were launched with will be deleted

<details><summary>Answer:</summary><p>
[B]

Categories:
[VPC]

Explanation:

Question 12@http://jayendrapatil.com/aws-ec2-network/

</p></details><hr>

