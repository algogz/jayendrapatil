### Question 1:

If an object is stored in the Standard S3 storage class and you want to move it to Glacier, what must you do in order to properly migrate it?

- A. Change the storage class directly on the object.
- B. Delete the object and re-upload it, selecting Glacier as the storage class.
- C. None of the above.
- D. Create a lifecycle policy that will migrate it after a minimum of 30 days.

<details><summary>Answer:</summary><p>
[D]

Categories:
[S3, Glacier]

Explanation:

Question 1@http://jayendrapatil.com/aws-s3-object-lifecycle-management/

D: Any object uploaded to S3 must first be placed into either the Standard, Reduced Redundancy, or Infrequent Access storage class. Once in S3 the only way to move the object to glacier is through a lifecycle policy

</p></details><hr>

### Question 2:

A company wants to store their documents in AWS. Initially, these documents will be used frequently, and after a duration of 6 months, they would not be needed anymore. How would you architect this requirement?

- A. Store the files in Amazon EBS and create a Lifecycle Policy to remove the files after 6 months.
- B. Store the files in Amazon S3 and create a Lifecycle Policy to remove the files after 6 months.
- C. Store the files in Amazon Glacier and create a Lifecycle Policy to remove the files after 6 months.
- D. Store the files in Amazon EFS and create a Lifecycle Policy to remove the files after 6 months.

<details><summary>Answer:</summary><p>
[B]

Categories:
[S3, Glacier, EBS]

Explanation:

Question 2@http://jayendrapatil.com/aws-s3-object-lifecycle-management/

</p></details><hr>

### Question 3:

Your firm has uploaded a large amount of aerial image data to S3. In the past, in your on-premises environment, you used a dedicated group of servers to oaten process this data and used Rabbit MQ, an open source messaging system, to get job information to the servers. Once processed the data would go to tape and be shipped offsite. Your manager told you to stay with the current design, and leverage AWS archival storage and messaging services to minimize cost. Which is correct?

- A. Use SQS for passing job messages, use Cloud Watch alarms to terminate EC2 worker instances when they become idle. Once data is processed, change the storage class of the S3 objects to Reduced Redundancy Storage 
- B. Setup Auto-Scaled workers triggered by queue depth that use spot instances to process messages in SQS. Once data is processed, change the storage class of the S3 objects to Reduced Redundancy Storage 
- C. Setup Auto-Scaled workers triggered by queue depth that use spot instances to process messages in SQS. Once data is processed, change the storage class of the S3 objects to Glacier
- D. Use SNS to pass job messages use Cloud Watch alarms to terminate spot worker instances when they become idle. Once data is processed, change the storage class of the S3 object to Glacier.

<details><summary>Answer:</summary><p>
[C]

Categories:
[S3, SES, SQS, Glacier, EC2, SNS]

Explanation:

Question 3@http://jayendrapatil.com/aws-s3-object-lifecycle-management/

A: Need to replace On-Premises Tape functionality

B: Need to replace On-Premises Tape functionality

C: Glacier suitable for Tape backup

</p></details><hr>

### Question 4:

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

Question 4@http://jayendrapatil.com/aws-s3-object-lifecycle-management/

A: will not meet the RTO

B: Not cost effective

C: Store in S3 for seven days and then archive to Glacier

D: Not Cost effective as local storage as well as S3 storage

</p></details><hr>

