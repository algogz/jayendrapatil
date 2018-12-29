### Question 1:

You have multiple Amazon EC2 instances running in a cluster across multiple Availability Zones within the same region. What combination of the following should be used to ensure the highest network performance (packets per second), lowest latency, and lowest jitter? Choose 3 answers

- A. Amazon EC2 placement groups 
- B. Enhanced networking
- C. Amazon PV AMI 
- D. Amazon HVM AMI ( )
- E. Amazon Linux 
- F. Amazon VPC

<details><summary>Answer:</summary><p>
[B, D, F]

Categories:
[EC2, VPC]

Explanation:

Question 1@http://jayendrapatil.com/aws-ec2-enhanced-networking/

A: would not work for multiple AZs

B: provides network performance, lowest latency

C: Requires HVM

D: Requires HVM

E: Can be on others as well

F: works only in VPC, can’t enable enhanced networking if the instance is in EC2-Classic

</p></details><hr>

### Question 2:

A group of researchers is studying the migration pattern of a beetle that eats and destroys gram. The researchers must process massive amounts of data and run statistics. Which one of the following options provides the high performance computing for this purpose.

- A. Configure an Autoscaling Scaling group to launch dozens of spot instances to run the statistical analysis simultaneously
- B. Launch AMI instances that support SR-IOV in a single Availability Zone
- C. Launch compute optimized (C4) instances in at least two Availability Zones
- D. Launch enhanced network type instances in a placement group

<details><summary>Answer:</summary><p>
[D]

Categories:
[]

Explanation:

Question 2@http://jayendrapatil.com/aws-ec2-enhanced-networking/

</p></details><hr>

