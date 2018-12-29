### Question 1:

You are moving an existing traditional system to AWS, and during the migration discover that there is a master server which is a single point of failure. Having examined the implementation of the master server you realize there is not enough time during migration to re-engineer it to be highly available, though you do discover that it stores its state in a local MySQL database. In order to minimize down-time you select RDS to replace the local database and configure master to use it, what steps would best allow you to create a self-healing architecture[PROFESSIONAL]

- A. Migrate the local database into multi-AWS RDS database. Place master node into a multi-AZ auto-scaling group with a minimum of one and maximum of one with health checks.
- B. Replicate the local database into a RDS read replica. Place master node into a Cross-Zone ELB with a minimum of one and maximum of one with health checks. 
- C. Migrate the local database into multi-AWS RDS database. Place master node into a Cross-Zone ELB with a minimum of one and maximum of one with health checks. 
- D. Replicate the local database into a RDS read replica. Place master node into a multi-AZ auto-scaling group with a minimum of one and maximum of one with health checks. 

<details><summary>Answer:</summary><p>
[A]

Categories:
[RDS, ELB]

Explanation:

Question 1@http://jayendrapatil.com/aws-high-availability-fault-tolerance-architecture-certification/

B: Read Replica does not provide HA and write capability and ELB does not have feature for Min and Max 1 and Cross Zone allows just the equal distribution of load across instances

C: ELB does not have feature for Min and Max 1 and Cross Zone allows just the equal distribution of load across instances

D: Read Replica does not provide HA and write capability

</p></details><hr>

### Question 2:

You are designing Internet connectivity for your VPC. The Web servers must be available on the Internet. The application must have a highly available architecture. Which alternatives should you consider? (Choose 2 answers)

- A. Configure a NAT instance in your VPC. Create a default route via the NAT instance and associate it with all subnets. Configure a DNS A record that points to the NAT instance public IP address 
- B. Configure a CloudFront distribution and configure the origin to point to the private IP addresses of your Web servers. Configure a Route53 CNAME record to your CloudFront distribution.
- C. Place all your web servers behind ELB. Configure a Route53 CNAME to point to the ELB DNS name.
- D. Assign EIPs to all web servers. Configure a Route53 record set with all EIPs. With health checks and DNS failover.

<details><summary>Answer:</summary><p>
[C, D]

Categories:
[SES, CloudFront, VPC, ELB]

Explanation:

Question 2@http://jayendrapatil.com/aws-high-availability-fault-tolerance-architecture-certification/

A: NAT is for internet connectivity for instances in private subnet

</p></details><hr>

### Question 3:

When deploying a highly available 2-tier web application on AWS, which combination of AWS services meets the requirements? 1. AWS Direct Connect 2. Amazon Route 53 3. AWS Storage Gateway 4. Elastic Load Balancing 4. Amazon EC2 5. Auto scaling 6. Amazon VPC 7. AWS Cloud Trail [PROFESSIONAL]

- A. 2,4,5 and 6
- B. 3,4,5 and 8
- C. 1 through 8
- D. 1,3,5 and 7
- E. 1,2,5 and 6

<details><summary>Answer:</summary><p>
[A]

Categories:
[EC2, Storage Gateway, ASG, VPC, Route 53, ELB, Direct Connect]

Explanation:

Question 3@http://jayendrapatil.com/aws-high-availability-fault-tolerance-architecture-certification/

</p></details><hr>

### Question 4:

Company A has hired you to assist with the migration of an interactive website that allows registered users to rate local restaurants. Updates to the ratings are displayed on the home page, and ratings are updated in real time. Although the website is not very popular today, the company anticipates that It will grow rapidly over the next few weeks. They want the site to be highly available. The current architecture consists of a single Windows Server 2008 R2 web server and a MySQL database running on Linux. Both reside inside an on -premises hypervisor. What would be the most efficient way to transfer the application to AWS, ensuring performance and high-availability? [PROFESSIONAL]

- A. Export web files to an Amazon S3 bucket in us-west-1. Run the website directly out of Amazon S3. Launch a multi-AZ MySQL Amazon RDS instance in us-west-1a. Import the data into Amazon RDS from the latest MySQL backup. Use Route 53 and create an alias record pointing to the elastic load balancer. 
- B. Launch two Windows Server 2008 R2 instances in us-west-1b and two in us-west-1a. Copy the web files from on premises web server to each Amazon EC2 web server, using Amazon S3 as the repository. Launch a multi-AZ MySQL Amazon RDS instance in us-west-2a. Import the data into Amazon RDS from the latest MySQL backup. Create an elastic load balancer to front your web servers. Use Route 53 and create an alias record pointing to the elastic load balancer.
- C. Use AWS VM Import/Export to create an Amazon Elastic Compute Cloud (EC2) Amazon Machine Image (AMI) of the web server. Configure Auto Scaling to launch two web servers in us-west-1a and two in us-west-1b. Launch a Multi-AZ MySQL Amazon Relational Database Service (RDS) instance in us-west-1b. Import the data into Amazon RDS from the latest MySQL backup. Use Amazon Route 53 to create a hosted zone and point an A record to the elastic load balancer. 
- D. Use AWS VM Import/Export to create an Amazon EC2 AMI of the web server. Configure auto-scaling to launch two web servers in us-west-1a and two in us-west-1b. Launch a multi-AZ MySQL Amazon RDS instance in us-west-1a. Import the data into Amazon RDS from the latest MySQL backup. Create an elastic load balancer to front your web servers. Use Amazon Route 53 and create an A record pointing to the elastic load balancer. 

<details><summary>Answer:</summary><p>
[B]

Categories:
[S3, SES, RDS, EC2, ASG, EBS, Route 53]

Explanation:

Question 4@http://jayendrapatil.com/aws-high-availability-fault-tolerance-architecture-certification/

A: Its an Interactive website, although it can be implemented using Javascript SDK, its a migration and the application would need changes. Also no use of ELB if hosted on S3 Its an Interactive website, although it can be implemented using Javascript SDK, its a migration and the application would need changes. Also no use of ELB if hosted on S3

B: Although RDS instance is in a different region which will impact performance, this is the only option that works.

C: does not create a load balancer

D: Need to create a aliased record without which the Route 53 pointing to ELB would not work

</p></details><hr>

### Question 5:

Your company runs a customer facing event registration site. This site is built with a 3-tier architecture with web and application tier servers and a MySQL database. The application requires 6 web tier servers and 6 application tier servers for normal operation, but can run on a minimum of 65% server capacity and a single MySQL database. When deploying this application in a region with three availability zones (AZs) which architecture provides high availability? [PROFESSIONAL]

- A. A web tier deployed across 2 AZs with 3 EC2 (Elastic Compute Cloud) instances in each AZ inside an Auto Scaling Group behind an ELB (elastic load balancer), and an application tier deployed across 2 AZs with 3 EC2 instances in each AZ inside an Auto Scaling Group behind an ELB. and one RDS (Relational Database Service) instance deployed with read replicas in the other AZ.
- B. A web tier deployed across 3 AZs with 2 EC2 (Elastic Compute Cloud) instances in each AZ inside an Auto Scaling Group behind an ELB (elastic load balancer) and an application tier deployed across 3 AZs with 2 EC2 instances in each AZ inside an Auto Scaling Group behind an ELB and one RDS (Relational Database Service) Instance deployed with read replicas in the two other AZs.
- C. A web tier deployed across 2 AZs with 3 EC2 (Elastic Compute Cloud) instances in each AZ inside an Auto Scaling Group behind an ELB (elastic load balancer) and an application tier deployed across 2 AZs with 3 EC2 instances m each AZ inside an Auto Scaling Group behind an ELS and a Multi-AZ RDS (Relational Database Service) deployment.
- D. A web tier deployed across 3 AZs with 2 EC2 (Elastic Compute Cloud) instances in each AZ Inside an Auto Scaling Group behind an ELB (elastic load balancer). And an application tier deployed across 3 AZs with 2 EC2 instances in each AZ inside an Auto Scaling Group behind an ELB. And a Multi-AZ RDS (Relational Database services) deployment.

<details><summary>Answer:</summary><p>
[D]

Categories:
[RDS, EC2, ASG, ELB]

Explanation:

Question 5@http://jayendrapatil.com/aws-high-availability-fault-tolerance-architecture-certification/

</p></details><hr>

### Question 6:

For a 3-tier, customer facing, inclement weather site utilizing a MySQL database running in a Region which has two AZs which architecture provides fault tolerance within the region for the application that minimally requires 6 web tier servers and 6 application tier servers running in the web and application tiers and one MySQL database? [PROFESSIONAL]

- A. A web tier deployed across 2 AZs with 6 EC2 (Elastic Compute Cloud) instances in each AZ inside an Auto Scaling Group behind an ELB (elastic load balancer), and an application tier deployed across 2 AZs with 6 EC2 instances in each AZ inside an Auto Scaling Group behind an ELB. and a Multi-AZ RDS (Relational Database Service) deployment.
- B. A web tier deployed across 2 AZs with 3 EC2 (Elastic Compute Cloud) instances in each A2 inside an Auto Scaling Group behind an ELB (elastic load balancer) and an application tier deployed across 2 AZs with 3 EC2 instances in each AZ inside an Auto Scaling Group behind an ELB and a Multi-AZ RDS (Relational Database Service) deployment.
- C. A web tier deployed across 2 AZs with 3 EC2 (Elastic Compute Cloud) instances in each AZ inside an Auto Scaling Group behind an ELB (elastic load balancer) and an application tier deployed across 2 AZs with 6 EC2 instances in each AZ inside an Auto Scaling Group behind an ELB and one RDS (Relational Database Service) Instance deployed with read replicas in the other AZs.
- D. A web tier deployed across 1 AZs with 6 EC2 (Elastic Compute Cloud) instances in each AZ Inside an Auto Scaling Group behind an ELB (elastic load balancer). And an application tier deployed in the same AZs with 6 EC2 instances inside an Auto scaling group behind an ELB and a Multi-AZ RDS (Relational Database services) deployment, with 6 stopped web tier EC2 instances and 6 stopped application tier EC2 instances all in the other AZ ready to be started if any of the running instances in the first AZ fails.

<details><summary>Answer:</summary><p>
[A]

Categories:
[RDS, EC2, ASG, ELB]

Explanation:

Question 6@http://jayendrapatil.com/aws-high-availability-fault-tolerance-architecture-certification/

A: As it needs Fault Tolerance with minimal 6 servers always available

</p></details><hr>

### Question 7:

You are designing a system which needs, at minimum, 8 m4.large instances operating to service traffic. When designing a system for high availability in the us-east-1 region, which has 6 Availability Zones, you company needs to be able to handle death of a full availability zone. How should you distribute the servers, to save as much cost as possible, assuming all of the EC2 nodes are properly linked to an ELB? Your VPC account can utilize us-east-1’s AZ’s a through f, inclusive.

- A. 3 servers in each of AZ’s a through d, inclusive.
- B. 8 servers in each of AZ’s a and b.
- C. 2 servers in each of AZ’s a through e, inclusive.
- D. 4 servers in each of AZ’s a through c, inclusive.

<details><summary>Answer:</summary><p>
[C]

Categories:
[EC2, VPC, ELB]

Explanation:

Question 7@http://jayendrapatil.com/aws-high-availability-fault-tolerance-architecture-certification/

C: http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-regions-availability-zones.html#concepts-regionsavailability- zones

C: You need to design for N+1 redundancy on Availability Zones. ZONE_COUNT = (REQUIRED_INSTANCES / INSTANCE_COUNT_PER_ZONE) + 1. To minimize cost, spread the instances across as many possible zones as you can. By using a though e, you are allocating 5 zones. Using 2 instances, you have 10 total instances. If a single zone fails, you have 4 zones left, with 2 instances each, for a total of 8 instances. By spreading out as much as possible, you have increased cost by only 25% and significantly de-risked an availability zone failure. Refer

</p></details><hr>

### Question 8:

You need your API backed by DynamoDB to stay online during a total regional AWS failure. You can tolerate a couple minutes of lag or slowness during a large failure event, but the system should recover with normal operation after those few minutes. What is a good approach? [PROFESSIONAL]

- A. Set up DynamoDB cross-region replication in a master-standby configuration, with a single standby in another region. Create an Auto Scaling Group behind an ELB in each of the two regions DynamoDB is running in. Add a Route53 Latency DNS Record with DNS Failover, using the ELBs in the two regions as the resource records.
- B. Set up a DynamoDB Multi-Region table. Create an Auto Scaling Group behind an ELB in each of the two regions DynamoDB is running in. Add a Route53 Latency DNS Record with DNS Failover, using the ELBs in the two regions as the resource records. 
- C. Set up a DynamoDB Multi-Region table. Create a cross-region ELB pointing to a cross-region Auto Scaling Group, and direct a Route53 Latency DNS Record with DNS Failover to the cross-region ELB. 
- D. Set up DynamoDB cross-region replication in a master-standby configuration, with a single standby in another region. Create a cross-region ELB pointing to a cross-region Auto Scaling Group, and direct a Route53 Latency DNS Record with DNS Failover to the cross-region ELB. 

<details><summary>Answer:</summary><p>
[A]

Categories:
[RDS, ASG, DynamoDB, ELB]

Explanation:

Question 8@http://jayendrapatil.com/aws-high-availability-fault-tolerance-architecture-certification/

A: http://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Streams.CrossRegionRepl.html

A: Use DynamoDB cross-regional replication version with two ELBs and ASGs with Route53 Failover and Latency DNS

B: No such thing as DynamoDB Multi-Region table before. However, global tables have been now introduced.

C: No such thing as Cross Region ELB or cross-region ASG

D: No such thing as DynamoDB cross-region table or cross-region ELB

</p></details><hr>

### Question 9:

You are putting together a WordPress site for a local charity and you are using a combination of Route53, Elastic Load Balancers, EC2 & RDS. You launch your EC2 instance, download WordPress and setup the configuration files connection string so that it can communicate to RDS. When you browse to your URL however, nothing happens. Which of the following could NOT be the cause of this.

- A. You have forgotten to open port 80/443 on your security group in which the EC2 instance is placed.
- B. Your elastic load balancer has a health check, which is checking a webpage that does not exist; therefore your EC2 instance is not in service.
- C. You have not configured an ALIAS for your A record to point to your elastic load balancer
- D. You have locked port 22 down to your specific IP address therefore users cannot access your site using HTTP/HTTPS

<details><summary>Answer:</summary><p>
[D]

Categories:
[RDS, EC2]

Explanation:

Question 9@http://jayendrapatil.com/aws-high-availability-fault-tolerance-architecture-certification/

</p></details><hr>

### Question 10:

A development team that is currently doing a nightly six-hour build which is lengthening over time on-premises with a large and mostly under utilized server would like to transition to a continuous integration model of development on AWS with multiple builds triggered within the same day. However, they are concerned about cost, security and how to integrate with existing on-premises applications such as their LDAP and email servers, which cannot move off-premises. The development environment needs a source code repository; a project management system with a MySQL database resources for performing the builds and a storage location for QA to pick up builds from. What AWS services combination would you recommend to meet the development team’s requirements? [PROFESSIONAL]

- A. A Bastion host Amazon EC2 instance running a VPN server for access from on-premises, Amazon EC2 for the source code repository with attached Amazon EBS volumes, Amazon EC2 and Amazon RDS MySQL for the project management system, EIP for the source code repository and project management system, Amazon SQL for a build queue, An Amazon Auto Scaling group of Amazon EC2 instances for performing builds and Amazon Simple Email Service for sending the build output. (Bastion is not for VPN connectivity also SES should not be used)
- B. An AWS Storage Gateway for connecting on-premises software applications with cloud-based storage securely, Amazon EC2 for the resource code repository with attached Amazon EBS volumes, Amazon EC2 and Amazon RDS MySQL for the project management system, EIPs for the source code repository and project management system, Amazon Simple Notification Service for a notification initiated build, An Auto Scaling group of Amazon EC2 instances for performing builds and Amazon S3 for the build output. (Storage Gateway does not provide secure connectivity, still needs VPN. SNS alone cannot handle builds)
- C. An AWS Storage Gateway for connecting on-premises software applications with cloud-based storage securely, Amazon EC2 for the resource code repository with attached Amazon EBS volumes, Amazon EC2 and Amazon RDS MySQL for the project management system, EIPs for the source code repository and project management system, Amazon SQS for a build queue, An Amazon Elastic Map Reduce (EMR) cluster of Amazon EC2 instances for performing builds and Amazon CloudFront for the build output. (Storage Gateway does not provide secure connectivity, still needs VPN. EMR is not ideal for performing builds as it needs normal EC2 instances)
- D. A VPC with a VPN Gateway back to their on-premises servers, Amazon EC2 for the source-code repository with attached Amazon EBS volumes, Amazon EC2 and Amazon RDS MySQL for the project management system, EIPs for the source code repository and project management system, SQS for a build queue, An Auto Scaling group of EC2 instances for performing builds and S3 for the build output.

<details><summary>Answer:</summary><p>
[D]

Categories:
[S3, SES, RDS, CloudFront, SQS, EC2, Storage Gateway, ASG, EBS, VPC, SNS, EMR]

Explanation:

Question 10@http://jayendrapatil.com/aws-high-availability-fault-tolerance-architecture-certification/

D: (VPN gateway is required for secure connectivity. SQS for build queue and EC2 for builds)

</p></details><hr>

