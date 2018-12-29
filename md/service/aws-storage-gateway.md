### Question 1:

Which of the following services natively encrypts data at rest within an AWS region?Choose 2 answers

- A. AWS Storage Gateway
- B. Amazon DynamoDB
- C. Amazon CloudFront
- D. Amazon Glacier
- E. Amazon Simple Queue Service

<details><summary>Answer:</summary><p>
[A, D]

Categories:
[CloudFront, SQS, Glacier, Storage Gateway, DynamoDB]

Explanation:

Question 1@http://jayendrapatil.com/aws-storage-gateway/

</p></details><hr>

### Question 2:

What does the AWS Storage Gateway provide?

- A. It allows to integrate on-premises IT environments with Cloud Storage
- B. A direct encrypted connection to Amazon S3.
- C. It’s a backup solution that provides an on-premises Cloud storage.
- D. It provides an encrypted SSL endpoint for backups in the Cloud.

<details><summary>Answer:</summary><p>
[A]

Categories:
[S3, SES, Storage Gateway]

Explanation:

Question 2@http://jayendrapatil.com/aws-storage-gateway/

</p></details><hr>

### Question 3:

You’re running an application on-premises due to its dependency on non-x86 hardware and want to use AWS for data backup. Your backup application is only able to write to POSIX-compatible block-based storage. You have 140TB of data and would like to mount it as a single folder on your file server. Users must be able to access portions of this data while the backups are taking place. What backup solution would be most appropriate for this use case?

- A. Use Storage Gateway and configure it to use Gateway Cached volumes.
- B. Configure your backup software to use S3 as the target for your data backups.
- C. Configure your backup software to use Glacier as the target for your data backups
- D. Use Storage Gateway and configure it to use Gateway Stored volumes

<details><summary>Answer:</summary><p>
[D]

Categories:
[S3, SES, Glacier, Storage Gateway]

Explanation:

Question 3@http://jayendrapatil.com/aws-storage-gateway/

D: Data is hosted on the On-premise server as well. The requirement for 140TB is for file server On-Premise more to confuse and not in AWS. Just need a backup solution hence stored instead of cached volumes

</p></details><hr>

### Question 4:

A customer has a single 3-TB volume on-premises that is used to hold a large repository of images and print layout files. This repository is growing at 500 GB a year and must be presented as a single logical volume. The customer is becoming increasingly constrained with their local storage capacity and wants an off-site backup of this data, while maintaining low-latency access to their frequently accessed data. Which AWS Storage Gateway configuration meets the customer requirements?

- A. Gateway-Cached volumes with snapshots scheduled to Amazon S3
- B. Gateway-Stored volumes with snapshots scheduled to Amazon S3
- C. Gateway-Virtual Tape Library with snapshots to Amazon S3
- D. Gateway-Virtual Tape Library with snapshots to Amazon Glacier

<details><summary>Answer:</summary><p>
[A]

Categories:
[S3, SES, Glacier, Storage Gateway]

Explanation:

Question 4@http://jayendrapatil.com/aws-storage-gateway/

</p></details><hr>

### Question 5:

You have a proprietary data store on-premises that must be backed up daily by dumping the data store contents to a single compressed 50GB file and sending the file to AWS. Your SLAs state that any dump file backed up within the past 7 days can be retrieved within 2 hours. Your compliance department has stated that all data must be held indefinitely. The time required to restore the data store from a backup is approximately 1 hour. Your on-premise network connection is capable of sustaining 1gbps to AWS. Which backup methods to AWS would be most cost-effective while still meeting all of your requirements?

- A. Send the daily backup files to Glacier immediately after being generated 
- B. Transfer the daily backup files to an EBS volume in AWS and take daily snapshots of the volume 
- C. Transfer the daily backup files to S3 and use appropriate bucket lifecycle policies to send to Glacier 
- D. Host the backup files on a Storage Gateway with Gateway-Cached Volumes and take daily snapshots 

<details><summary>Answer:</summary><p>
[]

Categories:
[S3, SES, Glacier, Storage Gateway, EBS]

Explanation:

Question 5@http://jayendrapatil.com/aws-storage-gateway/

A: will not meet the RTO

B: Not cost effective

C: Store in S3 for seven days and then archive to Glacier

D: Not Cost effective as local storage as well as S3 storage

</p></details><hr>

### Question 6:

A customer implemented AWS Storage Gateway with a gateway-cached volume at their main office. An event takes the link between the main and branch office offline. Which methods will enable the branch office to access their data? Choose 3 answers

- A. Use a HTTPS GET to the Amazon S3 bucket where the files are located 
- B. Restore by implementing a lifecycle policy on the Amazon S3 bucket.
- C. Make an Amazon Glacier Restore API call to load the files into another Amazon S3 bucket within four to six hours.
- D. Launch a new AWS Storage Gateway instance AMI in Amazon EC2, and restore from a gateway snapshot
- E. Create an Amazon EBS volume from a gateway snapshot, and mount it to an Amazon EC2 instance.
- F. Launch an AWS Storage Gateway virtual iSCSI device at the branch office, and restore from a gateway snapshot

<details><summary>Answer:</summary><p>
[D, E, F]

Categories:
[S3, Glacier, EC2, Storage Gateway, EBS]

Explanation:

Question 6@http://jayendrapatil.com/aws-storage-gateway/

A: gateway volumes are only accessible from the AWS Storage Gateway and cannot be directly accessed using Amazon S3 APIs

</p></details><hr>

