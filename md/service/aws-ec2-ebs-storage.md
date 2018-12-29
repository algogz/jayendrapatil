### Question 1:

_____ is a durable, block-level storage volume that you can attach to a single, running Amazon EC2 instance.

- A. Amazon S3
- B. Amazon EBS
- C. None of these
- D. All of these

<details><summary>Answer:</summary><p>
[B]

Categories:
[S3, EC2, EBS]

Explanation:

Question 1@http://jayendrapatil.com/aws-ec2-ebs-storage/

</p></details><hr>

### Question 2:

Which Amazon storage do you think is the best for my database-style applications that frequently encounter many random reads and writes across the dataset?

- A. None of these.
- B. Amazon Instance Storage
- C. Any of these
- D. Amazon EBS

<details><summary>Answer:</summary><p>
[D]

Categories:
[EBS]

Explanation:

Question 2@http://jayendrapatil.com/aws-ec2-ebs-storage/

</p></details><hr>

### Question 3:

What does Amazon EBS stand for?

- A. Elastic Block Storage
- B. Elastic Business Server
- C. Elastic Blade Server
- D. Elastic Block Store

<details><summary>Answer:</summary><p>
[D]

Categories:
[EBS]

Explanation:

Question 3@http://jayendrapatil.com/aws-ec2-ebs-storage/

</p></details><hr>

### Question 4:

Which Amazon Storage behaves like raw, unformatted, external block devices that you can attach to your instances?

- A. None of these.
- B. Amazon Instance Storage
- C. Amazon EBS
- D. All of these

<details><summary>Answer:</summary><p>
[C]

Categories:
[EBS]

Explanation:

Question 4@http://jayendrapatil.com/aws-ec2-ebs-storage/

</p></details><hr>

### Question 5:

A user has created numerous EBS volumes. What is the general limit for each AWS account for the maximum number of EBS volumes that can be created?

- A. 10000
- B. 5000
- C. 100
- D. 1000

<details><summary>Answer:</summary><p>
[B]

Categories:
[EBS]

Explanation:

Question 5@http://jayendrapatil.com/aws-ec2-ebs-storage/

</p></details><hr>

### Question 6:

Select the correct set of steps for exposing the snapshot only to specific AWS accounts

- A. Select Public for all the accounts and check mark those accounts with whom you want to expose the snapshots and click save.
- B. Select Private and enter the IDs of those AWS accounts, and click Save.
- C. Select Public, enter the IDs of those AWS accounts, and click Save.
- D. Select Public, mark the IDs of those AWS accounts as private, and click Save.

<details><summary>Answer:</summary><p>
[B]

Categories:
[]

Explanation:

Question 6@http://jayendrapatil.com/aws-ec2-ebs-storage/

</p></details><hr>

### Question 7:

If an Amazon EBS volume is the root device of an instance, can I detach it without stopping the instance?

- A. Yes but only if Windows instance
- B. No
- C. Yes
- D. Yes but only if a Linux instance

<details><summary>Answer:</summary><p>
[B]

Categories:
[EBS]

Explanation:

Question 7@http://jayendrapatil.com/aws-ec2-ebs-storage/

</p></details><hr>

### Question 8:

Can we attach an EBS volume to more than one EC2 instance at the same time?

- A. Yes
- B. No
- C. Only EC2-optimized EBS volumes.
- D. Only in read mode.

<details><summary>Answer:</summary><p>
[B]

Categories:
[EC2, EBS]

Explanation:

Question 8@http://jayendrapatil.com/aws-ec2-ebs-storage/

</p></details><hr>

### Question 9:

Do the Amazon EBS volumes persist independently from the running life of an Amazon EC2 instance?

- A. Only if instructed to when created
- B. Yes
- C. No

<details><summary>Answer:</summary><p>
[A]

Categories:
[EC2, EBS]

Explanation:

Question 9@http://jayendrapatil.com/aws-ec2-ebs-storage/

</p></details><hr>

### Question 10:

Can I delete a snapshot of the root device of an EBS volume used by a registered AMI?

- A. Only via API
- B. Only via Console
- C. Yes
- D. No

<details><summary>Answer:</summary><p>
[D]

Categories:
[EBS]

Explanation:

Question 10@http://jayendrapatil.com/aws-ec2-ebs-storage/

</p></details><hr>

### Question 11:

By default, EBS volumes that are created and attached to an instance at launch are deleted when that instance is terminated. You can modify this behavior by changing the value of the flag_____ to false when you launch the instance

- A. DeleteOnTermination
- B. RemoveOnDeletion
- C. RemoveOnTermination
- D. TerminateOnDeletion

<details><summary>Answer:</summary><p>
[A]

Categories:
[EBS]

Explanation:

Question 11@http://jayendrapatil.com/aws-ec2-ebs-storage/

</p></details><hr>

### Question 12:

Your company policies require encryption of sensitive data at rest. You are considering the possible options for protecting data while storing it at rest on an EBS data volume, attached to an EC2 instance. Which of these options would allow you to encrypt your data at rest? (Choose 3 answers)

- A. Implement third party volume encryption tools
- B. Do nothing as EBS volumes are encrypted by default
- C. Encrypt data inside your applications before storing it on EBS
- D. Encrypt data using native data encryption drivers at the file system level
- E. Implement SSL/TLS for all services running on the server

<details><summary>Answer:</summary><p>
[A, C, D]

Categories:
[EC2, EBS]

Explanation:

Question 12@http://jayendrapatil.com/aws-ec2-ebs-storage/

</p></details><hr>

### Question 13:

Which of the following are true regarding encrypted Amazon Elastic Block Store (EBS) volumes? Choose 2 answers

- A. Supported on all Amazon EBS volume types
- B. Snapshots are automatically encrypted
- C. Available to all instance types
- D. Existing volumes can be encrypted
- E. 

<details><summary>Answer:</summary><p>
[A, B, E]

Categories:
[EBS]

Explanation:

Question 13@http://jayendrapatil.com/aws-ec2-ebs-storage/

E: Shared volumes can be encrypted

</p></details><hr>

### Question 14:

How can you secure data at rest on an EBS volume?

- A. Encrypt the volume using the S3 server-side encryption service
- B. Attach the volume to an instance using EC2’s SSL interface.
- C. Create an IAM policy that restricts read and write access to the volume.
- D. Write the data randomly instead of sequentially.
- E. Use an encrypted file system on top of the EBS volume

<details><summary>Answer:</summary><p>
[E]

Categories:
[S3, IAM, EC2, EBS]

Explanation:

Question 14@http://jayendrapatil.com/aws-ec2-ebs-storage/

</p></details><hr>

### Question 15:

A user has deployed an application on an EBS backed EC2 instance. For a better performance of application, it requires dedicated EC2 to EBS traffic. How can the user achieve this?

- A. Launch the EC2 instance as EBS dedicated with PIOPS EBS
- B. Launch the EC2 instance as EBS enhanced with PIOPS EBS
- C. Launch the EC2 instance as EBS dedicated with PIOPS EBS
- D. Launch the EC2 instance as EBS optimized with PIOPS EBS

<details><summary>Answer:</summary><p>
[D]

Categories:
[EC2, EBS]

Explanation:

Question 15@http://jayendrapatil.com/aws-ec2-ebs-storage/

</p></details><hr>

### Question 16:

A user is trying to launch an EBS backed EC2 instance under free usage. The user wants to achieve encryption of the EBS volume. How can the user encrypt the data at rest?

- A. Use AWS EBS encryption to encrypt the data at rest ( )
- B. User cannot use EBS encryption and has to encrypt the data manually or using a third party tool 
- C. The user has to select the encryption enabled flag while launching the EC2 instance
- D. Encryption of volume is not available as a part of the free usage tier

<details><summary>Answer:</summary><p>
[A]

Categories:
[EC2, EBS]

Explanation:

Question 16@http://jayendrapatil.com/aws-ec2-ebs-storage/

A: Encryption is allowed on micro instances

B: Encryption was not allowed on micro instances before

</p></details><hr>

### Question 17:

A user is planning to schedule a backup for an EBS volume. The user wants security of the snapshot data. How can the user achieve data encryption with a snapshot?

- A. Use encrypted EBS volumes so that the snapshot will be encrypted by AWS
- B. While creating a snapshot select the snapshot with encryption
- C. By default the snapshot is encrypted by AWS
- D. Enable server side encryption for the snapshot using S3

<details><summary>Answer:</summary><p>
[A]

Categories:
[S3, EBS]

Explanation:

Question 17@http://jayendrapatil.com/aws-ec2-ebs-storage/

</p></details><hr>

### Question 18:

A user has launched an EBS backed EC2 instance. The user has rebooted the instance. Which of the below mentioned statements is not true with respect to the reboot action?

- A. The private and public address remains the same
- B. The Elastic IP remains associated with the instance
- C. The volume is preserved
- D. The instance runs on a new host computer

<details><summary>Answer:</summary><p>
[D]

Categories:
[EC2, EBS]

Explanation:

Question 18@http://jayendrapatil.com/aws-ec2-ebs-storage/

</p></details><hr>

### Question 19:

A user has launched an EBS backed EC2 instance. What will be the difference while performing the restart or stop/start options on that instance?

- A. For restart it does not charge for an extra hour, while every stop/start it will be charged as a separate hour
- B. Every restart is charged by AWS as a separate hour, while multiple start/stop actions during a single hour will be counted as a single hour
- C. For every restart or start/stop it will be charged as a separate hour
- D. For restart it charges extra only once, while for every stop/start it will be charged as a separate hour

<details><summary>Answer:</summary><p>
[A]

Categories:
[EC2, EBS]

Explanation:

Question 19@http://jayendrapatil.com/aws-ec2-ebs-storage/

</p></details><hr>

### Question 20:

A user has launched an EBS backed instance. The user started the instance at 9 AM in the morning. Between 9 AM to 10 AM, the user is testing some script. Thus, he stopped the instance twice and restarted it. In the same hour the user rebooted the instance once. For how many instance hours will AWS charge the user?

- A. 3 hours
- B. 4 hours
- C. 2 hours
- D. 1 hour

<details><summary>Answer:</summary><p>
[A]

Categories:
[EBS]

Explanation:

Question 20@http://jayendrapatil.com/aws-ec2-ebs-storage/

</p></details><hr>

### Question 21:

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

Question 21@http://jayendrapatil.com/aws-ec2-ebs-storage/

</p></details><hr>

### Question 22:

An organization wants to move to Cloud. They are looking for a secure encrypted database storage option. Which of the below mentioned AWS functionalities helps them to achieve this?

- A. AWS MFA with EBS
- B. AWS EBS encryption
- C. Multi-tier encryption with Redshift
- D. AWS S3 server-side storage

<details><summary>Answer:</summary><p>
[B]

Categories:
[S3, EBS, Redshift]

Explanation:

Question 22@http://jayendrapatil.com/aws-ec2-ebs-storage/

</p></details><hr>

### Question 23:

A user has stored data on an encrypted EBS volume. The user wants to share the data with his friend’s AWS account. How can user achieve this?

- A. Create an AMI from the volume and share the AMI
- B. Copy the data to an unencrypted volume and then share
- C. Take a snapshot and share the snapshot with a friend
- D. If both the accounts are using the same encryption key then the user can share the volume directly

<details><summary>Answer:</summary><p>
[B]

Categories:
[EBS]

Explanation:

Question 23@http://jayendrapatil.com/aws-ec2-ebs-storage/

</p></details><hr>

### Question 24:

A user is using an EBS backed instance. Which of the below mentioned statements is true?

- A. The user will be charged for volume and instance only when the instance is running
- B. The user will be charged for the volume even if the instance is stopped
- C. The user will be charged only for the instance running cost
- D. The user will not be charged for the volume if the instance is stopped

<details><summary>Answer:</summary><p>
[B]

Categories:
[EBS]

Explanation:

Question 24@http://jayendrapatil.com/aws-ec2-ebs-storage/

</p></details><hr>

### Question 25:

A user is planning to use EBS for his DB requirement. The user already has an EC2 instance running in the VPC private subnet. How can the user attach the EBS volume to a running instance?

- A. The user must create EBS within the same VPC and then attach it to a running instance.
- B. The user can create EBS in the same zone as the subnet of instance and attach that EBS to instance.
- C. It is not possible to attach an EBS to an instance running in VPC until the instance is stopped.
- D. The user can specify the same subnet while creating EBS and then attach it to a running instance.

<details><summary>Answer:</summary><p>
[B]

Categories:
[EC2, EBS, VPC]

Explanation:

Question 25@http://jayendrapatil.com/aws-ec2-ebs-storage/

B: Should be in the same AZ

</p></details><hr>

### Question 26:

A user is creating an EBS volume. He asks for your advice. Which advice mentioned below should you not give to the user for creating an EBS volume?

- A. Take the snapshot of the volume when the instance is stopped
- B. Stripe multiple volumes attached to the same instance
- C. Create an AMI from the attached volume
- D. Attach multiple volumes to the same instance

<details><summary>Answer:</summary><p>
[C]

Categories:
[EBS]

Explanation:

Question 26@http://jayendrapatil.com/aws-ec2-ebs-storage/

C: AMI is created from the snapshot

</p></details><hr>

### Question 27:

An EC2 instance has one additional EBS volume attached to it. How can a user attach the same volume to another running instance in the same AZ?

- A. Terminate the first instance and only then attach to the new instance
- B. Attach the volume as read only to the second instance
- C. Detach the volume first and attach to new instance
- D. No need to detach. Just select the volume and attach it to the new instance, it will take care of mapping internally

<details><summary>Answer:</summary><p>
[C]

Categories:
[EC2, EBS]

Explanation:

Question 27@http://jayendrapatil.com/aws-ec2-ebs-storage/

</p></details><hr>

### Question 28:

What is the scope of an EBS volume?

- A. VPC
- B. Region
- C. Placement Group
- D. Availability Zone

<details><summary>Answer:</summary><p>
[D]

Categories:
[EBS, VPC]

Explanation:

Question 28@http://jayendrapatil.com/aws-ec2-ebs-storage/

</p></details><hr>

