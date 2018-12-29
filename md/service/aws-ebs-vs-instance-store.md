### Question 1:

EC2 EBS-backed (EBS root) instance is stopped, what happens to the data on any ephemeral store volumes?

- A. Data is automatically saved in an EBS volume.
- B. Data is unavailable until the instance is restarted.
- C. Data will be deleted and will no longer be accessible.
- D. Data is automatically saved as an EBS snapshot.

<details><summary>Answer:</summary><p>
[]

Categories:
[EC2, EBS]

Explanation:

Question 1@http://jayendrapatil.com/aws-ebs-vs-instance-store/

</p></details><hr>

### Question 2:

When an EC2 instance that is backed by an S3-based AMI is terminated, what happens to the data on the root volume?

- A. Data is automatically saved as an EBS snapshot.
- B. Data is automatically saved as an EBS volume.
- C. Data is unavailable until the instance is restarted.
- D. Data is automatically deleted.

<details><summary>Answer:</summary><p>
[]

Categories:
[S3, EC2, EBS]

Explanation:

Question 2@http://jayendrapatil.com/aws-ebs-vs-instance-store/

</p></details><hr>

### Question 3:

Which of the following will occur when an EC2 instance in a VPC (Virtual Private Cloud) with an associated Elastic IP is stopped and started? (Choose 2 answers)

- A. The Elastic IP will be dissociated from the instance
- B. All data on instance-store devices will be lost
- C. All data on EBS (Elastic Block Store) devices will be lost
- D. The ENI (Elastic Network Interface) is detached
- E. The underlying host for the instance is changed

<details><summary>Answer:</summary><p>
[]

Categories:
[EC2, EBS, VPC]

Explanation:

Question 3@http://jayendrapatil.com/aws-ebs-vs-instance-store/

</p></details><hr>

### Question 4:

Which of the following provides the fastest storage medium?

- A. Amazon S3
- B. Amazon EBS using Provisioned IOPS (PIOPS)
- C. SSD Instance (ephemeral) store
- D. AWS Storage Gateway

<details><summary>Answer:</summary><p>
[C]

Categories:
[S3, Storage Gateway, EBS]

Explanation:

Question 4@http://jayendrapatil.com/aws-ebs-vs-instance-store/

C: (SSD Instance Storage provides 100,000 IOPS on some instance types, much faster than any network-attached storage)

</p></details><hr>

