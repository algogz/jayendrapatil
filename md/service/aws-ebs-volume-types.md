### Question 1:

You are designing an enterprise data storage system. Your data management software system requires mountable disks and a real filesystem, so you cannot use S3 for storage. You need persistence, so you will be using AWS EBS Volumes for your system. The system needs as low-cost storage as possible, and access is not frequent or high throughput, and is mostly sequential reads. Which is the most appropriate EBS Volume Type for this scenario?

- A. gp1
- B. io1
- C. standard
- D. gp2

<details><summary>Answer:</summary><p>
[C]

Categories:
[S3, EBS]

Explanation:

Question 1@http://jayendrapatil.com/aws-ebs-volume-types/

C: (Standard or Magnetic volumes are suited for cold workloads where data is infrequently accessed, or scenarios where the lowest storage cost is important)

</p></details><hr>

### Question 2:

Which EBS volume type is best for high performance NoSQL cluster deployments?

- A. io1
- B. gp1
- C. standard
- D. gp2

<details><summary>Answer:</summary><p>
[A]

Categories:
[EBS]

Explanation:

Question 2@http://jayendrapatil.com/aws-ebs-volume-types/

A: (io1 volumes, or Provisioned IOPS (PIOPS) SSDs, are best for: Critical business applications that require sustained IOPS performance, or more than 10,000 IOPS or 160 MiB/s of throughput per volume, like large database workloads, such as MongoDB.)

</p></details><hr>

### Question 3:

Provisioned IOPS Costs: you are charged for the IOPS and storage whether or not you use them in a given month.

- A. FALSE
- B. TRUE

<details><summary>Answer:</summary><p>
[B]

Categories:
[]

Explanation:

Question 3@http://jayendrapatil.com/aws-ebs-volume-types/

</p></details><hr>

### Question 4:

A user is trying to create a PIOPS EBS volume with 8 GB size and 200 IOPS. Will AWS create the volume?

- A. Yes, since the ratio between EBS and IOPS is less than 30
- B. No, since the PIOPS and EBS size ratio is less than 30
- C. No, the EBS size is less than 10 GB
- D. Yes, since PIOPS is higher than 100

<details><summary>Answer:</summary><p>
[A]

Categories:
[EBS]

Explanation:

Question 4@http://jayendrapatil.com/aws-ebs-volume-types/

</p></details><hr>

### Question 5:

A user has provisioned 2000 IOPS to the EBS volume. The application hosted on that EBS is experiencing less IOPS than provisioned. Which of the below mentioned options does not affect the IOPS of the volume?

- A. The application does not have enough IO for the volume
- B. Instance is EBS optimized
- C. The EC2 instance has 10 Gigabit Network connectivity
- D. Volume size is too large

<details><summary>Answer:</summary><p>
[D]

Categories:
[EC2, EBS]

Explanation:

Question 5@http://jayendrapatil.com/aws-ebs-volume-types/

</p></details><hr>

### Question 6:

A user is trying to create a PIOPS EBS volume with 4000 IOPS and 100 GB size. AWS does not allow the user to create this volume. What is the possible root cause for this?

- A. The ratio between IOPS and the EBS volume is higher than 30
- B. The maximum IOPS supported by EBS is 3000
- C. The ratio between IOPS and the EBS volume is lower than 50
- D. PIOPS is supported for EBS higher than 500 GB size

<details><summary>Answer:</summary><p>
[A]

Categories:
[EBS]

Explanation:

Question 6@http://jayendrapatil.com/aws-ebs-volume-types/

</p></details><hr>

