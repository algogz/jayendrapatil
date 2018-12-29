### Question 1:

Please select the most correct answer regarding the persistence of the Amazon Instance Store

- A. The data on an instance store volume persists only during the life of the associated Amazon EC2 instance
- B. The data on an instance store volume is lost when the security group rule of the associated instance is changed.
- C. The data on an instance store volume persists even after associated Amazon EC2 instance is deleted

<details><summary>Answer:</summary><p>
[A]

Categories:
[EC2, Instance Store]

Explanation:

Question 1@http://jayendrapatil.com/aws-ec2-instance-store-storage/

</p></details><hr>

### Question 2:

A user has launched an EC2 instance from an instance store backed AMI. The user has attached an additional instance store volume to the instance. The user wants to create an AMI from the running instance. Will the AMI have the additional instance store volume data?

- A. Yes, the block device mapping will have information about the additional instance store volume
- B. No, since the instance store backed AMI can have only the root volume bundled
- C. It is not possible to attach an additional instance store volume to the existing instance store backed AMI instance
- D. No, since this is ephemeral storage it will not be a part of the AMI

<details><summary>Answer:</summary><p>
[A]

Categories:
[EC2, Instance Store]

Explanation:

Question 2@http://jayendrapatil.com/aws-ec2-instance-store-storage/

</p></details><hr>

### Question 3:

When an EC2 instance that is backed by an S3-based AMI Is terminated, what happens to the data on the root volume?

- A. Data is automatically saved as an EBS volume.
- B. Data is automatically saved as an EBS snapshot.
- C. Data is automatically deleted
- D. Data is unavailable until the instance is restarted.

<details><summary>Answer:</summary><p>
[C]

Categories:
[S3, EC2, EBS]

Explanation:

Question 3@http://jayendrapatil.com/aws-ec2-instance-store-storage/

</p></details><hr>

### Question 4:

A user has launched an EC2 instance from an instance store backed AMI. If the user restarts the instance, what will happen to the ephemeral storage data?

- A. All the data will be erased but the ephemeral storage will stay connected
- B. All data will be erased and the ephemeral storage is released
- C. It is not possible to restart an instance launched from an instance store backed AMI
- D. The data is preserved

<details><summary>Answer:</summary><p>
[D]

Categories:
[EC2, Instance Store]

Explanation:

Question 4@http://jayendrapatil.com/aws-ec2-instance-store-storage/

</p></details><hr>

### Question 5:

When an EC2 EBS-backed instance is stopped, what happens to the data on any ephemeral store volumes?

- A. Data will be deleted and will no longer be accessible
- B. Data is automatically saved in an EBS volume.
- C. Data is automatically saved as an EBS snapshot
- D. Data is unavailable until the instance is restarted

<details><summary>Answer:</summary><p>
[A]

Categories:
[EC2, EBS]

Explanation:

Question 5@http://jayendrapatil.com/aws-ec2-instance-store-storage/

</p></details><hr>

### Question 6:

A user has launched an EC2 Windows instance from an instance store backed AMI. The user has also set the Instance initiated shutdown behavior to stop. What will happen when the user shuts down the OS?

- A. It will not allow the user to shutdown the OS when the shutdown behavior is set to Stop
- B. It is not possible to set the termination behavior to Stop for an Instance store backed AMI instance
- C. The instance will stay running but the OS will be shutdown
- D. The instance will be terminated

<details><summary>Answer:</summary><p>
[B]

Categories:
[EC2, Instance Store]

Explanation:

Question 6@http://jayendrapatil.com/aws-ec2-instance-store-storage/

</p></details><hr>

### Question 7:

Which of the following will occur when an EC2 instance in a VPC (Virtual Private Cloud) with an associated Elastic IP is stopped and started? (Choose 2 answers)

- A. The Elastic IP will be dissociated from the instance
- B. All data on instance-store devices will be lost
- C. All data on EBS (Elastic Block Store) devices will be lost
- D. The ENI (Elastic Network Interface) is detached
- E. The underlying host for the instance is changed

<details><summary>Answer:</summary><p>
[B, E]

Categories:
[EC2, EBS, VPC]

Explanation:

Question 7@http://jayendrapatil.com/aws-ec2-instance-store-storage/

</p></details><hr>

