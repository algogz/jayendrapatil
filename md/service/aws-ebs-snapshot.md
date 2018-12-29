### Question 1:

An existing application stores sensitive information on a non-boot Amazon EBS data volume attached to an Amazon Elastic Compute Cloud instance. Which of the following approaches would protect the sensitive data on an Amazon EBS volume?

- A. Upload your customer keys to AWS CloudHSM. Associate the Amazon EBS volume with AWS CloudHSM. Remount the Amazon EBS volume.
- B. Create and mount a new, encrypted Amazon EBS volume. Move the data to the new volume. Delete the old Amazon EBS volume.
- C. Unmount the EBS volume. Toggle the encryption attribute to True. Re-mount the Amazon EBS volume.
- D. Snapshot the current Amazon EBS volume. Restore the snapshot to a new, encrypted Amazon EBS volume. Mount the Amazon EBS volume 

<details><summary>Answer:</summary><p>
[B]

Categories:
[EBS]

Explanation:

Question 1@http://jayendrapatil.com/aws-ebs-snapshot/

D: Need to create a snapshot, create an encrypted copy of snapshot and then create a EBS volume and mount it

</p></details><hr>

### Question 2:

Is it possible to access your EBS snapshots?

- A. Yes, through the Amazon S3 APIs.
- B. Yes, through the Amazon EC2 APIs
- C. No, EBS snapshots cannot be accessed; they can only be used to create a new EBS volume.
- D. EBS doesn’t provide snapshots.

<details><summary>Answer:</summary><p>
[B]

Categories:
[S3, EC2, EBS]

Explanation:

Question 2@http://jayendrapatil.com/aws-ebs-snapshot/

</p></details><hr>

### Question 3:

Which of the following approaches provides the lowest cost for Amazon Elastic Block Store snapshots while giving you the ability to fully restore data?

- A. Maintain two snapshots: the original snapshot and the latest incremental snapshot
- B. Maintain a volume snapshot; subsequent snapshots will overwrite one another
- C. Maintain a single snapshot the latest snapshot is both Incremental and complete
- D. Maintain the most current snapshot, archive the original and incremental to Amazon Glacier.

<details><summary>Answer:</summary><p>
[C]

Categories:
[Glacier]

Explanation:

Question 3@http://jayendrapatil.com/aws-ebs-snapshot/

</p></details><hr>

### Question 4:

Which procedure for backing up a relational database on EC2 that is using a set of RAIDed EBS volumes for storage minimizes the time during which the database cannot be written to and results in a consistent backup?

- A. Detach EBS volumes, 2. Start EBS snapshot of volumes, 3. Re-attach EBS volumes
- B. Stop the EC2 Instance. 2. Snapshot the EBS volumes
- C. Suspend disk I/O, 2. Create an image of the EC2 Instance, 3. Resume disk I/O
- D. Suspend disk I/O, 2. Start EBS snapshot of volumes, 3. Resume disk I/O
- E. Suspend disk I/O, 2. Start EBS snapshot of volumes, 3. Wait for snapshots to complete, 4. Resume disk I/O

<details><summary>Answer:</summary><p>
[E]

Categories:
[EC2, EBS]

Explanation:

Question 4@http://jayendrapatil.com/aws-ebs-snapshot/

</p></details><hr>

### Question 5:

How can an EBS volume that is currently attached to an EC2 instance be migrated from one Availability Zone to another?

- A. Detach the volume and attach it to another EC2 instance in the other AZ.
- B. Simply create a new volume in the other AZ and specify the original volume as the source.
- C. Create a snapshot of the volume, and create a new volume from the snapshot in the other AZ
- D. Detach the volume, then use the ec2-migrate-volume command to move it to another AZ.

<details><summary>Answer:</summary><p>
[C]

Categories:
[EC2, EBS]

Explanation:

Question 5@http://jayendrapatil.com/aws-ebs-snapshot/

</p></details><hr>

### Question 6:

How are the EBS snapshots saved on Amazon S3?

- A. Exponentially
- B. Incrementally
- C. EBS snapshots are not stored in the Amazon S3
- D. Decrementally

<details><summary>Answer:</summary><p>
[B]

Categories:
[S3, EBS]

Explanation:

Question 6@http://jayendrapatil.com/aws-ebs-snapshot/

</p></details><hr>

### Question 7:

EBS Snapshots occur _____

- A. Asynchronously
- B. Synchronously
- C. Weekly

<details><summary>Answer:</summary><p>
[A]

Categories:
[EBS]

Explanation:

Question 7@http://jayendrapatil.com/aws-ebs-snapshot/

</p></details><hr>

### Question 8:

What will be the status of the snapshot until the snapshot is complete?

- A. Running
- B. Working
- C. Progressing
- D. Pending

<details><summary>Answer:</summary><p>
[D]

Categories:
[]

Explanation:

Question 8@http://jayendrapatil.com/aws-ebs-snapshot/

</p></details><hr>

### Question 9:

Before I delete an EBS volume, what can I do if I want to recreate the volume later?

- A. Create a copy of the EBS volume (not a snapshot)
- B. Create and Store a snapshot of the volume
- C. Download the content to an EC2 instance
- D. Back up the data in to a physical disk

<details><summary>Answer:</summary><p>
[B]

Categories:
[EC2, EBS]

Explanation:

Question 9@http://jayendrapatil.com/aws-ebs-snapshot/

</p></details><hr>

### Question 10:

Which of the following are true regarding encrypted Amazon Elastic Block Store (EBS) volumes? Choose 2 answers

- A. Supported on all Amazon EBS volume types
- B. Snapshots are automatically encrypted
- C. Available to all instance types
- D. Existing volumes can be encrypted
- E. Shared volumes can be encrypted

<details><summary>Answer:</summary><p>
[A, B]

Categories:
[EBS]

Explanation:

Question 10@http://jayendrapatil.com/aws-ebs-snapshot/

</p></details><hr>

### Question 11:

Amazon EBS snapshots have which of the following two characteristics? (Choose 2.) Choose 2 answers

- A. EBS snapshots only save incremental changes from snapshot to snapshot
- B. EBS snapshots can be created in real-time without stopping an EC2 instance
- C. EBS snapshots can only be restored to an EBS volume of the same size or smaller 
- D. ( )

<details><summary>Answer:</summary><p>
[A, B, D]

Categories:
[EC2, EBS]

Explanation:

Question 11@http://jayendrapatil.com/aws-ebs-snapshot/

B: the snapshot can be taken real time however it will not be consistent and the recommended way is to stop or freeze the IO

C: EBS volume restored from snapshots need to be of the same size of larger size

D: Snapshots are specific to Region and can be used to create a volume in any AZ and does not depend on the original EBS volume AZ

D: EBS snapshots can only be restored and mounted to an instance in the same Availability Zone as the original EBS volume

</p></details><hr>

### Question 12:

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

Question 12@http://jayendrapatil.com/aws-ebs-snapshot/

A: http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSEncryption.html

</p></details><hr>

### Question 13:

A sys admin is trying to understand EBS snapshots. Which of the below mentioned statements will not be useful to the admin to understand the concepts about a snapshot?

- A. Snapshot is synchronous
- B. It is recommended to stop the instance before taking a snapshot for consistent data
- C. Snapshot is incremental
- D. Snapshot captures the data that has been written to the hard disk when the snapshot command was executed

<details><summary>Answer:</summary><p>
[A]

Categories:
[EBS]

Explanation:

Question 13@http://jayendrapatil.com/aws-ebs-snapshot/

</p></details><hr>

### Question 14:

When creation of an EBS snapshot is initiated but not completed, the EBS volume

- A. Cannot be detached or attached to an EC2 instance until me snapshot completes
- B. Can be used in read-only mode while me snapshot is in progress
- C. Can be used while the snapshot is in progress
- D. Cannot be used until the snapshot completes

<details><summary>Answer:</summary><p>
[C]

Categories:
[EC2, EBS]

Explanation:

Question 14@http://jayendrapatil.com/aws-ebs-snapshot/

</p></details><hr>

### Question 15:

You have a server with a 5O0GB Amazon EBS data volume. The volume is 80% full. You need to back up the volume at regular intervals and be able to re-create the volume in a new Availability Zone in the shortest time possible. All applications using the volume can be paused for a period of a few minutes with no discernible user impact. Which of the following backup methods will best fulfill your requirements?

- A. Take periodic snapshots of the EBS volume
- B. Use a third-party Incremental backup application to back up to Amazon Glacier
- C. Periodically back up all data to a single compressed archive and archive to Amazon S3 using a parallelized multi-part upload
- D. Create another EBS volume in the second Availability Zone attach it to the Amazon EC2 instance, and use a disk manager to mirror me two disks

<details><summary>Answer:</summary><p>
[A]

Categories:
[S3, Glacier, EC2, EBS]

Explanation:

Question 15@http://jayendrapatil.com/aws-ebs-snapshot/

</p></details><hr>

### Question 16:

A user is creating a snapshot of an EBS volume. Which of the below statements is incorrect in relation to the creation of an EBS snapshot?

- A. Its incremental
- B. It can be used to launch a new instance
- C. It is stored in the same AZ as the volume
- D. It is a point in time backup of the EBS volume

<details><summary>Answer:</summary><p>
[C]

Categories:
[EBS]

Explanation:

Question 16@http://jayendrapatil.com/aws-ebs-snapshot/

C: stored in the same region

</p></details><hr>

### Question 17:

A user has created a snapshot of an EBS volume. Which of the below mentioned usage cases is not possible with respect to a snapshot?

- A. Mirroring the volume from one AZ to another AZ
- B. Launch an instance
- C. Decrease the volume size
- D. Increase the size of the volume

<details><summary>Answer:</summary><p>
[C]

Categories:
[SES, EBS]

Explanation:

Question 17@http://jayendrapatil.com/aws-ebs-snapshot/

</p></details><hr>

### Question 18:

What is true of the way that encryption works with EBS?

- A. Snapshotting an encrypted volume makes an encrypted snapshot; restoring an encrypted snapshot creates an encrypted volume when specified / requested.
- B. Snapshotting an encrypted volume makes an encrypted snapshot when specified / requested; restoring an encrypted snapshot creates an encrypted volume when specified / requested.
- C. Snapshotting an encrypted volume makes an encrypted snapshot; restoring an encrypted snapshot always creates an encrypted volume.
- D. Snapshotting an encrypted volume makes an encrypted snapshot when specified / requested; restoring an encrypted snapshot always creates an encrypted volume.

<details><summary>Answer:</summary><p>
[C]

Categories:
[EBS]

Explanation:

Question 18@http://jayendrapatil.com/aws-ebs-snapshot/

</p></details><hr>

### Question 19:

Why are more frequent snapshots of EBS Volumes faster?

- A. Blocks in EBS Volumes are allocated lazily, since while logically separated from other EBS Volumes, Volumes often share the same physical hardware. Snapshotting the first time forces full block range allocation, so the second snapshot doesn’t need to perform the allocation phase and is faster.
- B. The snapshots are incremental so that only the blocks on the device that have changed after your last snapshot are saved in the new snapshot.
- C. AWS provisions more disk throughput for burst capacity during snapshots if the drive has been pre-warmed by snapshotting and reading all blocks.
- D. The drive is pre-warmed, so block access is more rapid for volumes when every block on the device has already been read at least one time.

<details><summary>Answer:</summary><p>
[B]

Categories:
[EBS]

Explanation:

Question 19@http://jayendrapatil.com/aws-ebs-snapshot/

</p></details><hr>

### Question 20:

Which is not a restriction on AWS EBS Snapshots?

- A. Snapshots which are shared cannot be used as a basis for other snapshots
- B. You cannot share a snapshot containing an AWS Access Key ID or AWS Secret Access Key
- C. You cannot share encrypted snapshots 
- D. Snapshot restorations are restricted to the region in which the snapshots are created

<details><summary>Answer:</summary><p>
[A]

Categories:
[EBS]

Explanation:

Question 20@http://jayendrapatil.com/aws-ebs-snapshot/

A: Snapshots shared with other users are usable in full by the recipient, including but limited to the ability to base modified volumes and snapshots

C: NOTE: this has be updated partially where you can share a encrypted snapshot with other accounts

</p></details><hr>

### Question 21:

There is a very serious outage at AWS. EC2 is not affected, but your EC2 instance deployment scripts stopped working in the region with the outage. What might be the issue?

- A. The AWS Console is down, so your CLI commands do not work.
- B. S3 is unavailable, so you can’t create EBS volumes from a snapshot you use to deploy new volumes.
- C. AWS turns off the <code>DeployCode</code> API call when there are major outages, to protect from system floods.
- D. None of the other answers make sense. If EC2 is not affected, it must be some other issue.

<details><summary>Answer:</summary><p>
[B]

Categories:
[S3, EC2, EBS]

Explanation:

Question 21@http://jayendrapatil.com/aws-ebs-snapshot/

B: EBS volume snapshots are stored in S3. If S3 is unavailable, snapshots are unavailable

</p></details><hr>

