### Question 1:

You are responsible for a legacy web application whose server environment is approaching end of life. You would like to migrate this application to AWS as quickly as possible, since the application environment currently has the following limitations: The VM’s single 10GB VMDK is almost full. The virtual network interface still uses the 10Mbps driver, which leaves your 100Mbps WAN connection completely underutilized. It is currently running on a highly customized Windows VM within a VMware environment: You do not have the installation media. This is a mission critical application with an RTO (Recovery Time Objective) of 8 hours. RPO (Recovery Point Objective) of 1 hour. How could you best migrate this application to AWS while meeting your business continuity requirements?

- A. Use the EC2 VM Import Connector for vCenter to import the VM into EC2
- B. Use Import/Export to import the VM as an EBS snapshot and attach to EC2. 
- C. Use S3 to create a backup of the VM and restore the data into EC2.
- D. Use the ec2-bundle-instance API to Import an Image of the VM into EC2 (only bundles an windows instance store instance)

<details><summary>Answer:</summary><p>
[A]

Categories:
[S3, SES, EC2, EBS, Instance Store]

Explanation:

Question 1@http://jayendrapatil.com/aws-ec2-vm-importexport/

B: Import/Export is used to transfer large amount of data

</p></details><hr>

### Question 2:

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

Question 2@http://jayendrapatil.com/aws-ec2-vm-importexport/

A: VPN or a DX for communication

B: Virtual and Customer gateway is needed

C: Don’t need a EIP as private subnets can also interact with on-premises network

D: IP address cannot conflict

E: Route 53 is not required

F: VM Import to copy the VM to AWS as there is no documentation it can’t be configured from scratch

</p></details><hr>

