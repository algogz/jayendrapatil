### Question 1:

Which of the following instance types are available as Amazon EBS-backed only? Choose 2 answers

- A. General purpose T2
- B. General purpose M3
- C. Compute-optimized C4
- D. Compute-optimized C3
- E. Storage-optimized 12

<details><summary>Answer:</summary><p>
[A, C]

Categories:
[EBS]

Explanation:

Question 1@http://jayendrapatil.com/aws-ec2-instance-types/

</p></details><hr>

### Question 2:

A t2.medium EC2 instance type must be launched with what type of Amazon Machine Image (AMI)?

- A. An Instance store Hardware Virtual Machine AMI
- B. An Instance store Paravirtual AMI
- C. An Amazon EBS-backed Hardware Virtual Machine AMI
- D. An Amazon EBS-backed Paravirtual AMI

<details><summary>Answer:</summary><p>
[C]

Categories:
[EC2, EBS, Instance Store]

Explanation:

Question 2@http://jayendrapatil.com/aws-ec2-instance-types/

</p></details><hr>

### Question 3:

You have identified network throughput as a bottleneck on your m1.small EC2 instance when uploading data Into Amazon S3 In the same region. How do you remedy this situation? Add an additional ENI

- A. Change to a larger Instance
- B. Use DirectConnect between EC2 and S3
- C. Use EBS PIOPS on the local volume

<details><summary>Answer:</summary><p>
[A]

Categories:
[S3, EC2, EBS]

Explanation:

Question 3@http://jayendrapatil.com/aws-ec2-instance-types/

</p></details><hr>

### Question 4:

You are using an m1.small EC2 Instance with one 300 GB EBS volume to host a relational database. You determined that write throughput to the database needs to be increased. Which of the following approaches can help achieve this? Choose 2 answers

- A. Use an array of EBS volumes
- B. Enable Multi-AZ mode.
- C. Place the instance in an Auto Scaling Groups
- D. Add an EBS volume and place into RAID 5 
- E. Increase the size of the EC2 Instance.
- F. Put the database behind an Elastic Load Balancer.

<details><summary>Answer:</summary><p>
[A, E]

Categories:
[EC2, ASG, EBS]

Explanation:

Question 4@http://jayendrapatil.com/aws-ec2-instance-types/

A: (Striping to increase throughput)

D: RAID 5 is not recommended as it provides parity and EBS volumes are already replicated across multiple servers in an Availability Zone for availability and durability, so AWS recommends striping for performance rather than durability

</p></details><hr>

### Question 5:

You are tasked with setting up a cluster of EC2 Instances for a NoSQL database. The database requires random read IO disk performance up to a 100,000 IOPS at 4KB block side per node. Which of the following EC2 instances will perform the best for this workload?

- A. A High-Memory Quadruple Extra Large (m2.4xlarge) with EBS-Optimized set to true and a PIOPs EBS volume
- B. A Cluster Compute Eight Extra Large (cc2.8xlarge) using instance storage
- C. High I/O Quadruple Extra Large (hi1.4xlarge) using instance storage
- D. A Cluster GPU Quadruple Extra Large (cg1.4xlarge) using four separate 4000 PIOPS EBS volumes in a RAID 0 configuration

<details><summary>Answer:</summary><p>
[C]

Categories:
[EC2, EBS]

Explanation:

Question 5@http://jayendrapatil.com/aws-ec2-instance-types/

</p></details><hr>

### Question 6:

You are implementing a URL whitelisting system for a company that wants to restrict outbound HTTP’S connections to specific domains from their EC2-hosted applications you deploy a single EC2 instance running proxy software and configure It to accept traffic from all subnets and EC2 instances in the VPC. You configure the proxy to only pass through traffic to domains that you define in its whitelist configuration You have a nightly maintenance window or 10 minutes where ail instances fetch new software updates. Each update Is about 200MB In size and there are 500 instances In the VPC that routinely fetch updates After a few days you notice that some machines are failing to successfully download some, but not all of their updates within the maintenance window The download URLs used for these updates are correctly listed in the proxy’s whitelist configuration and you are able to access them manually using a web browser on the instances What might be happening? (Choose 2 answers) [PROFESSIONAL]

- A. You are running the proxy on an undersized EC2 instance type so network throughput is not sufficient for all instances to download their updates in time.
- B. You have not allocated enough storage to the EC2 instance running me proxy so the network buffer is filling up causing some requests to fall
- C. You are running the proxy in a public subnet but have not allocated enough EIPs to support the needed network throughput through the Internet Gateway (IGW)
- D. You are running the proxy on a affluently-sized EC2 instance in a private subnet and its network throughput is being throttled by a NAT running on an undersized EC2 instance
- E. The route table for the subnets containing the affected EC2 instances is not configured to direct network traffic for the software update locations to the proxy.

<details><summary>Answer:</summary><p>
[A, D]

Categories:
[EC2, VPC]

Explanation:

Question 6@http://jayendrapatil.com/aws-ec2-instance-types/

</p></details><hr>

### Question 7:

You have been asked to design the storage layer for an application. The application requires disk performance of at least 100,000 IOPS in addition; the storage layer must be able to survive the loss of an individual disk, EC2 instance, or Availability Zone without any data loss. The volume you provide must have a capacity of at least 3TB. Which of the following designs will meet these objectives? [PROFESSIONAL]

- A. Instantiate an i2.8xlarge instance in us-east-1a. Create a RAID 0 volume using the four 800GB SSD ephemeral disks provided with the instance. Provision 3×1 TB EBS volumes attach them to the instance and configure them as a second RAID 0 volume. Configure synchronous, block-level replication from the ephemeral backed volume to the EBS-backed volume. 
- B. Instantiate an i2.8xlarge instance in us-east-1a. Create a RAID 0 volume using the four 800GB SSD ephemeral disks provided with the Instance Configure synchronous block-level replication to an identically configured Instance in us-east-1b.
- C. Instantiate a c3.8xlarge Instance in us-east-1. Provision an AWS Storage Gateway and configure it for 3 TB of storage and 100,000 IOPS. Attach the volume to the instance. 
- D. Instantiate a c3.8xlarge instance in us-east-1 provision 4x1TB EBS volumes, attach them to the instance, and configure them as a single RAID 5 volume Ensure that EBS snapshots are performed every 15 minutes. 
- E. Instantiate a c3 8xlarge Instance in us-east-1 Provision 3x1TB EBS volumes attach them to the instance, and configure them as a single RAID 0 volume Ensure that EBS snapshots are performed every 15 minutes. 

<details><summary>Answer:</summary><p>
[B]

Categories:
[EC2, Storage Gateway, EBS]

Explanation:

Question 7@http://jayendrapatil.com/aws-ec2-instance-types/

A: Same AZ will not survive the AZ loss

C: Need synchronous replication to prevent any data loss

D: RAID 5 not recommended by AWS and Need synchronous replication to prevent any data loss

E: Need synchronous replication to prevent any data loss

</p></details><hr>

