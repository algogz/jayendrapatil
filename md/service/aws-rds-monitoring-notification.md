### Question 1:

You run a web application with the following components Elastic Load Balancer (ELB), 3 Web/Application servers, 1 MySQL RDS database with read replicas, and Amazon Simple Storage Service (Amazon S3) for static content. Average response time for users is increasing slowly. What three CloudWatch RDS metrics will allow you to identify if the database is the bottleneck? Choose 3 answers

- A. The number of outstanding IOs waiting to access the disk
- B. The amount of write latency
- C. The amount of disk space occupied by binary logs on the master.
- D. The amount of time a Read Replica DB Instance lags behind the source DB Instance
- E. The average number of disk I/O operations per second.

<details><summary>Answer:</summary><p>
[A, B, D]

Categories:
[S3, RDS, CloudWatch, ELB]

Explanation:

Question 1@http://jayendrapatil.com/aws-rds-monitoring-notification/

</p></details><hr>

### Question 2:

Typically, you want your application to check whether a request generated an error before you spend any time processing results. The easiest way to find out if an error occurred is to look for an __________ node in the response from the Amazon RDS API.

- A. Incorrect
- B. Error
- C. FALSE

<details><summary>Answer:</summary><p>
[B]

Categories:
[RDS]

Explanation:

Question 2@http://jayendrapatil.com/aws-rds-monitoring-notification/

</p></details><hr>

### Question 3:

In the Amazon CloudWatch, which metric should I be checking to ensure that your DB Instance has enough free storage space?

- A. FreeStorage
- B. FreeStorageSpace
- C. FreeStorageVolume
- D. FreeDBStorageSpace

<details><summary>Answer:</summary><p>
[B]

Categories:
[CloudWatch]

Explanation:

Question 3@http://jayendrapatil.com/aws-rds-monitoring-notification/

</p></details><hr>

### Question 4:

A user is receiving a notification from the RDS DB whenever there is a change in the DB security group. The user does not want to receive these notifications for only a month. Thus, he does not want to delete the notification. How can the user configure this?

- A. Change the Disable button for notification to “Yes” in the RDS console
- B. Set the send mail flag to false in the DB event notification console
- C. The only option is to delete the notification from the console
- D. Change the Enable button for notification to “No” in the RDS console

<details><summary>Answer:</summary><p>
[D]

Categories:
[RDS]

Explanation:

Question 4@http://jayendrapatil.com/aws-rds-monitoring-notification/

</p></details><hr>

### Question 5:

A sys admin is planning to subscribe to the RDS event notifications. For which of the below mentioned source categories the subscription cannot be configured?

- A. DB security group
- B. DB snapshot
- C. DB options group
- D. DB parameter group

<details><summary>Answer:</summary><p>
[C]

Categories:
[RDS]

Explanation:

Question 5@http://jayendrapatil.com/aws-rds-monitoring-notification/

</p></details><hr>

### Question 6:

A user is planning to setup notifications on the RDS DB for a snapshot. Which of the below mentioned event categories is not supported by RDS for this snapshot source type?

- A. Backup
- B. Creation
- C. Deletion
- D. Restoration

<details><summary>Answer:</summary><p>
[A]

Categories:
[RDS]

Explanation:

Question 6@http://jayendrapatil.com/aws-rds-monitoring-notification/

A: http://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_Events.html#USER_Events.Messages

</p></details><hr>

### Question 7:

A system admin is planning to setup event notifications on RDS. Which of the below mentioned services will help the admin setup notifications?

- A. AWS SES
- B. AWS Cloudtrail
- C. AWS CloudWatch
- D. AWS SNS

<details><summary>Answer:</summary><p>
[D]

Categories:
[SES, RDS, CloudWatch, SNS, CloudTrail]

Explanation:

Question 7@http://jayendrapatil.com/aws-rds-monitoring-notification/

</p></details><hr>

### Question 8:

A user has setup an RDS DB with Oracle. The user wants to get notifications when someone modifies the security group of that DB. How can the user configure that?

- A. It is not possible to get the notifications on a change in the security group
- B. Configure SNS to monitor security group changes
- C. Configure event notification on the DB security group
- D. Configure the CloudWatch alarm on the DB for a change in the security group

<details><summary>Answer:</summary><p>
[C]

Categories:
[RDS, CloudWatch, SNS]

Explanation:

Question 8@http://jayendrapatil.com/aws-rds-monitoring-notification/

</p></details><hr>

### Question 9:

It is advised that you watch the Amazon CloudWatch “_____” metric (available via the AWS Management Console or Amazon Cloud Watch APIs) carefully and recreate the Read Replica should it fall behind due to replication errors.

- A. Write Lag
- B. Read Replica
- C. Replica Lag
- D. Single Replica

<details><summary>Answer:</summary><p>
[C]

Categories:
[CloudWatch]

Explanation:

Question 9@http://jayendrapatil.com/aws-rds-monitoring-notification/

</p></details><hr>

