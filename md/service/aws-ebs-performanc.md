### Question 1:

A user is trying to pre-warm a blank EBS volume attached to a Linux instance. Which of the below mentioned steps should be performed by the user?

- A. There is no need to pre-warm an EBS volume (with latest update no pre-warming is needed)
- B. Contact AWS support to pre-warm
- C. Unmount the volume before pre-warming
- D. Format the device

<details><summary>Answer:</summary><p>
[B]

Categories:
[EBS]

Explanation:

Question 1@http://jayendrapatil.com/aws-ebs-performanc/

B: This used to be the case before, but pre warming is not necessary now

</p></details><hr>

### Question 2:

A user has created an EBS volume of 10 GB and attached it to a running instance. The user is trying to access EBS for first time. Which of the below mentioned options is the correct statement with respect to a first time EBS access?

- A. The volume will show a size of 8 GB
- B. The volume will show a loss of the IOPS performance the first time
- C. The volume will be blank
- D. If the EBS is mounted it will ask the user to create a file system

<details><summary>Answer:</summary><p>
[B]

Categories:
[EBS]

Explanation:

Question 2@http://jayendrapatil.com/aws-ebs-performanc/

B: the volume needed to be wiped cleaned before for new volumes, however pre warming is not needed any more

</p></details><hr>

### Question 3:

You are running a database on an EC2 instance, with the data stored on Elastic Block Store (EBS) for persistence At times throughout the day, you are seeing large variance in the response times of the database queries Looking into the instance with the isolate command you see a lot of wait time on the disk volume that the database’s data is stored on. What two ways can you improve the performance of the database’s storage while maintaining the current persistence of the data? Choose 2 answers

- A. Move to an SSD backed instance
- B. Move the database to an EBS-Optimized Instance
- C. Use Provisioned IOPs EBS
- D. Use the ephemeral storage on an m2.4xLarge Instance Instead

<details><summary>Answer:</summary><p>
[B, C]

Categories:
[EC2, EBS]

Explanation:

Question 3@http://jayendrapatil.com/aws-ebs-performanc/

</p></details><hr>

### Question 4:

You have launched an EC2 instance with four (4) 500 GB EBS Provisioned IOPS volumes attached. The EC2 Instance is EBS-Optimized and supports 500 Mbps throughput between EC2 and EBS. The two EBS volumes are configured as a single RAID 0 device, and each Provisioned IOPS volume is provisioned with 4,000 IOPS (4000 16KB reads or writes) for a total of 16,000 random IOPS on the instance. The EC2 Instance initially delivers the expected 16,000 IOPS random read and write performance. Sometime later in order to increase the total random I/O performance of the instance, you add an additional two 500 GB EBS Provisioned IOPS volumes to the RAID. Each volume is provisioned to 4,000 IOPS like the original four for a total of 24,000 IOPS on the EC2 instance Monitoring shows that the EC2 instance CPU utilization increased from 50% to 70%, but the total random IOPS measured at the instance level does not increase at all. What is the problem and a valid solution?

- A. Larger storage volumes support higher Provisioned IOPS rates: increase the provisioned volume storage of each of the 6 EBS volumes to 1TB.
- B. EBS-Optimized throughput limits the total IOPS that can be utilized use an EBS-Optimized instance that provides larger throughput. ( )
- C. Small block sizes cause performance degradation, limiting the I’O throughput, configure the instance device driver and file system to use 64KB blocks to increase throughput.
- D. RAID 0 only scales linearly to about 4 devices, use RAID 0 with 4 EBS Provisioned IOPS volumes but increase each Provisioned IOPS EBS volume to 6.000 IOPS.
- E. The standard EBS instance root volume limits the total IOPS rate, change the instant root volume to also be a 500GB 4,000 Provisioned IOPS volume

<details><summary>Answer:</summary><p>
[B]

Categories:
[EC2, EBS]

Explanation:

Question 4@http://jayendrapatil.com/aws-ebs-performanc/

B: http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-ec2-config.html

B: have limit on max throughput and would require larger instance types to provide 24000 IOPS 

</p></details><hr>

### Question 5:

A user has deployed an application on an EBS backed EC2 instance. For a better performance of application, it requires dedicated EC2 to EBS traffic. How can the user achieve this?

- A. Launch the EC2 instance as EBS provisioned with PIOPS EBS
- B. Launch the EC2 instance as EBS enhanced with PIOPS EBS
- C. Launch the EC2 instance as EBS dedicated with PIOPS EBS
- D. Launch the EC2 instance as EBS optimized with PIOPS EBS

<details><summary>Answer:</summary><p>
[D]

Categories:
[EC2, EBS]

Explanation:

Question 5@http://jayendrapatil.com/aws-ebs-performanc/

</p></details><hr>

