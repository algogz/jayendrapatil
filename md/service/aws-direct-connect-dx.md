### Question 1:

You are building a solution for a customer to extend their on-premises data center to AWS. The customer requires a 50-Mbps dedicated and private connection to their VPC. Which AWS product or feature satisfies this requirement?

- A. Amazon VPC peering
- B. Elastic IP Addresses
- C. AWS Direct Connect
- D. Amazon VPC virtual private gateway

<details><summary>Answer:</summary><p>
[C]

Categories:
[SES, VPC, Direct Connect]

Explanation:

Question 1@http://jayendrapatil.com/aws-direct-connect-dx/

</p></details><hr>

### Question 2:

Is there any way to own a direct connection to Amazon Web Services?

- A. You can create an encrypted tunnel to VPC, but you don’t own the connection.
- B. Yes, it’s called Amazon Dedicated Connection.
- C. No, AWS only allows access from the public Internet.
- D. Yes, it’s called Direct Connect

<details><summary>Answer:</summary><p>
[D]

Categories:
[VPC, Direct Connect]

Explanation:

Question 2@http://jayendrapatil.com/aws-direct-connect-dx/

</p></details><hr>

### Question 3:

An organization has established an Internet-based VPN connection between their on-premises data center and AWS. They are considering migrating from VPN to AWS Direct Connect. Which operational concern should drive an organization to consider switching from an Internet-based VPN connection to AWS Direct Connect?

- A. AWS Direct Connect provides greater redundancy than an Internet-based VPN connection.
- B. AWS Direct Connect provides greater resiliency than an Internet-based VPN connection.
- C. AWS Direct Connect provides greater bandwidth than an Internet-based VPN connection.
- D. AWS Direct Connect provides greater control of network provider selection than an Internet-based VPN connection.

<details><summary>Answer:</summary><p>
[C]

Categories:
[SES, Direct Connect]

Explanation:

Question 3@http://jayendrapatil.com/aws-direct-connect-dx/

</p></details><hr>

### Question 4:

Does AWS Direct Connect allow you access to all Availabilities Zones within a Region?

- A. Depends on the type of connection
- B. No
- C. Yes
- D. Only when there’s just one availability zone in a region. If there are more than one, only one availability zone can be accessed directly.

<details><summary>Answer:</summary><p>
[C]

Categories:
[Direct Connect]

Explanation:

Question 4@http://jayendrapatil.com/aws-direct-connect-dx/

</p></details><hr>

### Question 5:

A customer has established an AWS Direct Connect connection to AWS. The link is up and routes are being advertised from the customer’s end, however the customer is unable to connect from EC2 instances inside its VPC to servers residing in its datacenter. Which of the following options provide a viable solution to remedy this situation? (Choose 2 answers)

- A. Add a route to the route table with an IPSec VPN connection as the target
- B. Enable route propagation to the Virtual Private Gateway (VGW)
- C. Enable route propagation to the customer gateway (CGW)
- D. Modify the route table of all Instances using the ‘route’ command.
- E. Modify the Instances VPC subnet route table by adding a route back to the customer’s on-premises environment.

<details><summary>Answer:</summary><p>
[B, E]

Categories:
[SES, EC2, VPC, Direct Connect]

Explanation:

Question 5@http://jayendrapatil.com/aws-direct-connect-dx/

A: (deals with VPN)

C: (route propagation is enabled on VGW)

D: (no route command available)

</p></details><hr>

### Question 6:

A company has configured and peered two VPCs: VPC-1 and VPC-2. VPC-1 contains only private subnets, and VPC-2 contains only public subnets. The company uses a single AWS Direct Connect connection and private virtual interface to connect their on-premises network with VPC-1. Which two methods increase the fault tolerance of the connection to VPC-1? Choose 2 answers

- A. Establish a hardware VPN over the internet between VPC-2 and the on-premises network. 
- B. Establish a hardware VPN over the internet between VPC-1 and the on-premises network
- C. Establish a new AWS Direct Connect connection and private virtual interface in the same region as VPC-2 
- D. Establish a new AWS Direct Connect connection and private virtual interface in a different AWS region than VPC-1 
- E. Establish a new AWS Direct Connect connection and private virtual interface in the same AWS region as VPC-1

<details><summary>Answer:</summary><p>
[B, E]

Categories:
[SES, VPC, Direct Connect]

Explanation:

Question 6@http://jayendrapatil.com/aws-direct-connect-dx/

A: Peered VPC does not support Edge to Edge Routing

C: Peered VPC does not support Edge to Edge Routing

D: need to be in the same region as VPC-1

</p></details><hr>

### Question 7:

Your company previously configured a heavily used, dynamically routed VPN connection between your on premises data center and AWS. You recently provisioned a Direct Connect connection and would like to start using the new connection. After configuring Direct Connect settings in the AWS Console, which of the following options will provide the most seamless transition for your users?

- A. Delete your existing VPN connection to avoid routing loops configure your Direct Connect router with the appropriate settings and verity network traffic is leveraging Direct Connect.
- B. Configure your Direct Connect router with a higher BGP priority than your VPN router, verify network traffic is leveraging Direct Connect and then delete your existing VPN connection.
- C. Update your VPC route tables to point to the Direct Connect connection configure your Direct Connect router with the appropriate settings verify network traffic is leveraging Direct Connect and then delete the VPN connection.
- D. Configure your Direct Connect router, update your VPC route tables to point to the Direct Connect connection, configure your VPN connection with a higher BGP priority. And verify network traffic is leveraging the Direct Connect connection

<details><summary>Answer:</summary><p>
[C]

Categories:
[SES, VPC, Direct Connect]

Explanation:

Question 7@http://jayendrapatil.com/aws-direct-connect-dx/

</p></details><hr>

### Question 8:

You are designing the network infrastructure for an application server in Amazon VPC. Users will access all the application instances from the Internet as well as from an on-premises network The on-premises network is connected to your VPC over an AWS Direct Connect link. How would you design routing to meet the above requirements?

- A. Configure a single routing Table with a default route via the Internet gateway. Propagate a default route via BGP on the AWS Direct Connect customer router. Associate the routing table with all VPC subnets 
- B. Configure a single routing table with a default route via the internet gateway. Propagate specific routes for the on-premises networks via BGP on the AWS Direct Connect customer router. Associate the routing table with all VPC subnets.
- C. Configure a single routing table with two default routes: one to the internet via an Internet gateway the other to the on-premises network via the VPN gateway use this routing table across all subnets in your VPC. 
- D. Configure two routing tables one that has a default route via the Internet gateway and another that has a default route via the VPN gateway Associate both routing tables with each VPC subnet. 

<details><summary>Answer:</summary><p>
[B]

Categories:
[SES, VPC, Direct Connect]

Explanation:

Question 8@http://jayendrapatil.com/aws-direct-connect-dx/

A: propagating default route would cause conflict

C: there cannot be 2 default routes

D: as the instances has to be in public subnet and should have a single routing table associated with them

</p></details><hr>

### Question 9:

You are implementing AWS Direct Connect. You intend to use AWS public service end points such as Amazon S3, across the AWS Direct Connect link. You want other Internet traffic to use your existing link to an Internet Service Provider. What is the correct way to configure AWS Direct Connect for access to services such as Amazon S3?

- A. Configure a public Interface on your AWS Direct Connect link. Configure a static route via your AWS Direct Connect link that points to Amazon S3. Advertise a default route to AWS using BGP.
- B. Create a private interface on your AWS Direct Connect link. Configure a static route via your AWS Direct connect link that points to Amazon S3 Configure specific routes to your network in your VPC.
- C. Create a public interface on your AWS Direct Connect link. Redistribute BGP routes into your existing routing infrastructure advertise specific routes for your network to AWS
- D. Create a private interface on your AWS Direct connect link. Redistribute BGP routes into your existing routing infrastructure and advertise a default route to AWS.

<details><summary>Answer:</summary><p>
[C]

Categories:
[S3, VPC, Direct Connect]

Explanation:

Question 9@http://jayendrapatil.com/aws-direct-connect-dx/

</p></details><hr>

### Question 10:

You have been asked to design network connectivity between your existing data centers and AWS. Your application’s EC2 instances must be able to connect to existing backend resources located in your data center. Network traffic between AWS and your data centers will start small, but ramp up to 10s of GB per second over the course of several months. The success of your application is dependent upon getting to market quickly. Which of the following design options will allow you to meet your objectives?

- A. Quickly create an internal ELB for your backend applications, submit a DirectConnect request to provision a 1 Gbps cross connect between your data center and VPC, then increase the number or size of your DirectConnect connections as needed.
- B. Allocate EIPs and an Internet Gateway for your VPC instances to use for quick, temporary access to your backend applications, then provision a VPN connection between a VPC and existing on -premises equipment.
- C. Provision a VPN connection between a VPC and existing on -premises equipment, submit a DirectConnect partner request to provision cross connects between your data center and the DirectConnect location, then cut over from the VPN connection to one or more DirectConnect connections as needed.
- D. Quickly submit a DirectConnect request to provision a 1 Gbps cross connect between your data center and VPC, then increase the number or size of your DirectConnect connections as needed.

<details><summary>Answer:</summary><p>
[C]

Categories:
[SES, EC2, VPC, ELB]

Explanation:

Question 10@http://jayendrapatil.com/aws-direct-connect-dx/

</p></details><hr>

### Question 11:

You are tasked with moving a legacy application from a virtual machine running inside your datacenter to an Amazon VPC. Unfortunately this app requires access to a number of on-premises services and no one who configured the app still works for your company. Even worse there’s no documentation for it. What will allow the application running inside the VPC to reach back and access its internal dependencies without being reconfigured? (Choose 3 answers)

- A. An AWS Direct Connect link between the VPC and the network housing the internal services
- B. An Internet Gateway to allow a VPN connection. 
- C. An Elastic IP address on the VPC instance 
- D. An IP address space that does not conflict with the one on-premises
- E. Entries in Amazon Route 53 that allow the Instance to resolve its dependencies’ IP addresses 
- F. A VM Import of the current virtual machine

<details><summary>Answer:</summary><p>
[A, D, F]

Categories:
[SES, VPC, Route 53, Direct Connect]

Explanation:

Question 11@http://jayendrapatil.com/aws-direct-connect-dx/

A: VPN or a DX for communication

B: Virtual and Customer gateway is needed

C: Don’t need a EIP as private subnets can also interact with on-premises network

D: IP address cannot conflict

E: Route 53 is not required

F: VM Import to copy the VM to AWS as there is no documentation it can’t be configured from scratch

</p></details><hr>

