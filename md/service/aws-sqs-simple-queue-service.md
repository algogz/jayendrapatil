### Question 1:

Which AWS service can help design architecture to persist in-flight transactions?

- A. Elastic IP Address
- B. SQS
- C. Amazon CloudWatch
- D. Amazon ElastiCache

<details><summary>Answer:</summary><p>
[B]

Categories:
[SQS, CloudWatch, ElastiCache]

Explanation:

Question 1@http://jayendrapatil.com/aws-sqs-simple-queue-service/

</p></details><hr>

### Question 2:

A company has a workflow that sends video files from their on-premise system to AWS for transcoding. They use EC2 worker instances that pull transcoding jobs from SQS. Why is SQS an appropriate service for this scenario?

- A. SQS guarantees the order of the messages.
- B. SQS synchronously provides transcoding output.
- C. SQS checks the health of the worker instances.
- D. SQS helps to facilitate horizontal scaling of encoding tasks

<details><summary>Answer:</summary><p>
[D]

Categories:
[SQS, EC2]

Explanation:

Question 2@http://jayendrapatil.com/aws-sqs-simple-queue-service/

</p></details><hr>

### Question 3:

Which statement best describes an Amazon SQS use case?

- A. Automate the process of sending an email notification to administrators when the CPU utilization reaches 70% on production servers (Amazon EC2 instances) 
- B. Create a video transcoding website where multiple components need to communicate with each other, but can’t all process the same amount of work simultaneously
- C. Coordinate work across distributed web services to process employee’s expense reports 
- D. Distribute static web content to end users with low latency across multiple countries 

<details><summary>Answer:</summary><p>
[B]

Categories:
[SQS, EC2, EBS]

Explanation:

Question 3@http://jayendrapatil.com/aws-sqs-simple-queue-service/

A: CloudWatch + SNS + SES

B: SQS provides loose coupling

C: SWF – Steps in order and might need manual steps

D: CloudFront + S3

</p></details><hr>

### Question 4:

Your application provides data transformation services. Files containing data to be transformed are first uploaded to Amazon S3 and then transformed by a fleet of spot EC2 instances. Files submitted by your premium customers must be transformed with the highest priority. How should you implement such a system?

- A. Use a DynamoDB table with an attribute defining the priority level. Transformation instances will scan the table for tasks, sorting the results by priority level.
- B. Use Route 53 latency based-routing to send high priority tasks to the closest transformation instances.
- C. Use two SQS queues, one for high priority messages, and the other for default priority. Transformation instances first poll the high priority queue; if there is no message, they poll the default priority queue
- D. Use a single SQS queue. Each message contains the priority level. Transformation instances poll high-priority messages first.

<details><summary>Answer:</summary><p>
[C]

Categories:
[S3, SES, SQS, EC2, DynamoDB, Route 53]

Explanation:

Question 4@http://jayendrapatil.com/aws-sqs-simple-queue-service/

</p></details><hr>

### Question 5:

Your company plans to host a large donation website on Amazon Web Services (AWS). You anticipate a large and undetermined amount of traffic that will create many database writes. To be certain that you do not drop any writes to a database hosted on AWS. Which service should you use?

- A. Amazon RDS with provisioned IOPS up to the anticipated peak write throughput.
- B. Amazon Simple Queue Service (SQS) for capturing the writes and draining the queue to write to the database
- C. Amazon ElastiCache to store the writes until the writes are committed to the database.
- D. Amazon DynamoDB with provisioned write throughput up to the anticipated peak write throughput.

<details><summary>Answer:</summary><p>
[B]

Categories:
[RDS, SQS, ElastiCache, EBS, DynamoDB]

Explanation:

Question 5@http://jayendrapatil.com/aws-sqs-simple-queue-service/

</p></details><hr>

### Question 6:

A customer has a 10 GB AWS Direct Connect connection to an AWS region where they have a web application hosted on Amazon Elastic Computer Cloud (EC2). The application has dependencies on an on-premises mainframe database that uses a BASE (Basic Available, Soft state, Eventual consistency) rather than an ACID (Atomicity, Consistency, Isolation, Durability) consistency model. The application is exhibiting undesirable behavior because the database is not able to handle the volume of writes. How can you reduce the load on your on-premises database resources in the most cost-effective way?

- A. Use an Amazon Elastic Map Reduce (EMR) S3DistCp as a synchronization mechanism between the onpremises database and a Hadoop cluster on AWS.
- B. Modify the application to write to an Amazon SQS queue and develop a worker process to flush the queue to the on-premises database
- C. Modify the application to use DynamoDB to feed an EMR cluster which uses a map function to write to the on-premises database.
- D. Provision an RDS read-replica database on AWS to handle the writes and synchronize the two databases using Data Pipeline.

<details><summary>Answer:</summary><p>
[B]

Categories:
[S3, SES, RDS, SQS, EC2, DynamoDB, Direct Connect, EMR]

Explanation:

Question 6@http://jayendrapatil.com/aws-sqs-simple-queue-service/

</p></details><hr>

### Question 7:

An organization has created a Queue named “modularqueue” with SQS. The organization is not performing any operations such as SendMessage, ReceiveMessage, DeleteMessage, GetQueueAttributes, SetQueueAttributes, AddPermission, and RemovePermission on the queue. What can happen in this scenario?

- A. AWS SQS sends notification after 15 days for inactivity on queue
- B. AWS SQS can delete queue after 30 days without notification
- C. AWS SQS marks queue inactive after 30 days
- D. AWS SQS notifies the user after 2 weeks and deletes the queue after 3 weeks.

<details><summary>Answer:</summary><p>
[B]

Categories:
[SQS]

Explanation:

Question 7@http://jayendrapatil.com/aws-sqs-simple-queue-service/

</p></details><hr>

### Question 8:

A user is using the AWS SQS to decouple the services. Which of the below mentioned operations is not supported by SQS?

- A. SendMessageBatch
- B. DeleteMessageBatch
- C. CreateQueue
- D. DeleteMessageQueue

<details><summary>Answer:</summary><p>
[D]

Categories:
[SQS]

Explanation:

Question 8@http://jayendrapatil.com/aws-sqs-simple-queue-service/

</p></details><hr>

### Question 9:

A user has created a queue named “awsmodule” with SQS. One of the consumers of queue is down for 3 days and then becomes available. Will that component receive message from queue?

- A. Yes, since SQS by default stores message for 4 days
- B. No, since SQS by default stores message for 1 day only
- C. No, since SQS sends message to consumers who are available that time
- D. Yes, since SQS will not delete message until it is delivered to all consumers

<details><summary>Answer:</summary><p>
[A]

Categories:
[SQS]

Explanation:

Question 9@http://jayendrapatil.com/aws-sqs-simple-queue-service/

</p></details><hr>

### Question 10:

A user has created a queue named “queue2” in US-East region with AWS SQS. The user’s AWS account ID is 123456789012. If the user wants to perform some action on this queue, which of the below Queue URL should he use?

- A. http://sqs.us-east-1.amazonaws.com/123456789012/queue2
- B. http://sqs.amazonaws.com/123456789012/queue2
- C. http://sqs. 123456789012.us-east-1.amazonaws.com/queue2
- D. http://123456789012.sqs.us-east-1.amazonaws.com/queue2

<details><summary>Answer:</summary><p>
[A]

Categories:
[SQS]

Explanation:

Question 10@http://jayendrapatil.com/aws-sqs-simple-queue-service/

</p></details><hr>

### Question 11:

A user has created a queue named “myqueue” with SQS. There are four messages published to queue, which are not received by the consumer yet. If the user tries to delete the queue, what will happen?

- A. A user can never delete a queue manually. AWS deletes it after 30 days of inactivity on queue
- B. It will delete the queue
- C. It will initiate the delete but wait for four days before deleting until all messages are deleted automatically.
- D. I t will ask user to delete the messages first

<details><summary>Answer:</summary><p>
[B]

Categories:
[SQS]

Explanation:

Question 11@http://jayendrapatil.com/aws-sqs-simple-queue-service/

</p></details><hr>

### Question 12:

A user has developed an application, which is required to send the data to a NoSQL database. The user wants to decouple the data sending such that the application keeps processing and sending data but does not wait for an acknowledgement of DB. Which of the below mentioned applications helps in this scenario?

- A. AWS Simple Notification Service
- B. AWS Simple Workflow
- C. AWS Simple Queue Service
- D. AWS Simple Query Service

<details><summary>Answer:</summary><p>
[C]

Categories:
[SWF, SQS, SNS]

Explanation:

Question 12@http://jayendrapatil.com/aws-sqs-simple-queue-service/

</p></details><hr>

### Question 13:

You are building an online store on AWS that uses SQS to process your customer orders. Your backend system needs those messages in the same sequence the customer orders have been put in. How can you achieve that?

- A. It is not possible to do this with SQS
- B. You can use sequencing information on each message
- C. You can do this with SQS but you also need to use SWF
- D. Messages will arrive in the same order by default

<details><summary>Answer:</summary><p>
[B]

Categories:
[SES, SWF, SQS]

Explanation:

Question 13@http://jayendrapatil.com/aws-sqs-simple-queue-service/

</p></details><hr>

### Question 14:

A user has created a photo editing software and hosted it on EC2. The software accepts requests from the user about the photo format and resolution and sends a message to S3 to enhance the picture accordingly. Which of the below mentioned AWS services will help make a scalable software with the AWS infrastructure in this scenario?

- A. AWS Glacier
- B. AWS Elastic Transcoder
- C. AWS Simple Notification Service
- D. AWS Simple Queue Service

<details><summary>Answer:</summary><p>
[D]

Categories:
[S3, SQS, Glacier, EC2, Elastic Transcoder, SNS]

Explanation:

Question 14@http://jayendrapatil.com/aws-sqs-simple-queue-service/

</p></details><hr>

### Question 15:

Refer to the architecture diagram of a batch processing solution using Simple Queue Service (SQS) to set up a message queue between EC2 instances, which are used as batch processors. Cloud Watch monitors the number of Job requests (queued messages) and an Auto Scaling group adds or deletes batch servers automatically based on parameters set in Cloud Watch alarms. You can use this architecture to implement which of the following features in a cost effective and efficient manner?

- A. Reduce the overall time for executing jobs through parallel processing by allowing a busy EC2 instance that receives a message to pass it to the next instance in a daisy-chain setup.
- B. Implement fault tolerance against EC2 instance failure since messages would remain in SQS and worn can continue with recovery of EC2 instances implement fault tolerance against SQS failure by backing up messages to S3.
- C. Implement message passing between EC2 instances within a batch by exchanging messages through SOS.
- D. Coordinate number of EC2 instances with number of job requests automatically thus Improving cost effectiveness
- E. Handle high priority jobs before lower priority jobs by assigning a priority metadata field to SQS messages.

<details><summary>Answer:</summary><p>
[D]

Categories:
[S3, SQS, EC2, ASG]

Explanation:

Question 15@http://jayendrapatil.com/aws-sqs-simple-queue-service/

</p></details><hr>

### Question 16:

How does Amazon SQS allow multiple readers to access the same message queue without losing messages or processing them many times?

- A. By identifying a user by his unique id
- B. By using unique cryptography
- C. Amazon SQS queue has a configurable visibility timeout
- D. Multiple readers can’t access the same message queue

<details><summary>Answer:</summary><p>
[C]

Categories:
[SQS]

Explanation:

Question 16@http://jayendrapatil.com/aws-sqs-simple-queue-service/

</p></details><hr>

### Question 17:

A user has created photo editing software and hosted it on EC2. The software accepts requests from the user about the photo format and resolution and sends a message to S3 to enhance the picture accordingly. Which of the below mentioned AWS services will help make a scalable software with the AWS infrastructure in this scenario?

- A. AWS Elastic Transcoder
- B. AWS Simple Notification Service
- C. AWS Simple Queue Service
- D. AWS Glacier

<details><summary>Answer:</summary><p>
[C]

Categories:
[S3, SQS, Glacier, EC2, Elastic Transcoder, SNS]

Explanation:

Question 17@http://jayendrapatil.com/aws-sqs-simple-queue-service/

</p></details><hr>

### Question 18:

How do you configure SQS to support longer message retention?

- A. Set the MessageRetentionPeriod attribute using the SetQueueAttributes method
- B. Using a Lambda function
- C. You can’t. It is set to 14 days and cannot be changed
- D. You need to request it from AWS

<details><summary>Answer:</summary><p>
[A]

Categories:
[SQS, Lambda]

Explanation:

Question 18@http://jayendrapatil.com/aws-sqs-simple-queue-service/

</p></details><hr>

### Question 19:

A user has developed an application, which is required to send the data to a NoSQL database. The user wants to decouple the data sending such that the application keeps processing and sending data but does not wait for an acknowledgement of DB. Which of the below mentioned applications helps in this scenario?

- A. AWS Simple Notification Service
- B. AWS Simple Workflow
- C. AWS Simple Query Service
- D. AWS Simple Queue Service

<details><summary>Answer:</summary><p>
[D]

Categories:
[SWF, SQS, SNS]

Explanation:

Question 19@http://jayendrapatil.com/aws-sqs-simple-queue-service/

</p></details><hr>

### Question 20:

If a message is retrieved from a queue in Amazon SQS, how long is the message inaccessible to other users by default?

- A. 0 seconds
- B. 1 hour
- C. 1 day
- D. forever
- E. 30 seconds

<details><summary>Answer:</summary><p>
[E]

Categories:
[SQS]

Explanation:

Question 20@http://jayendrapatil.com/aws-sqs-simple-queue-service/

</p></details><hr>

### Question 21:

Which of the following statements about SQS is true?

- A. Messages will be delivered exactly once and messages will be delivered in First in, First out order
- B. Messages will be delivered exactly once and message delivery order is indeterminate
- C. Messages will be delivered one or more times and messages will be delivered in First in, First out order
- D. Messages will be delivered one or more times and message delivery order is indeterminate

<details><summary>Answer:</summary><p>
[D]

Categories:
[SQS]

Explanation:

Question 21@http://jayendrapatil.com/aws-sqs-simple-queue-service/

D: Before the introduction of FIFO queues

</p></details><hr>

### Question 22:

How long can you keep your Amazon SQS messages in Amazon SQS queues?

- A. From 120 secs up to 4 weeks
- B. From 10 secs up to 7 days
- C. From 60 secs up to 2 weeks
- D. From 30 secs up to 1 week

<details><summary>Answer:</summary><p>
[C]

Categories:
[SQS, ECS]

Explanation:

Question 22@http://jayendrapatil.com/aws-sqs-simple-queue-service/

</p></details><hr>

### Question 23:

When a Simple Queue Service message triggers a task that takes 5 minutes to complete, which process below will result in successful processing of the message and remove it from the queue while minimizing the chances of duplicate processing?

- A. Retrieve the message with an increased visibility timeout, process the message, delete the message from the queue
- B. Retrieve the message with an increased visibility timeout, delete the message from the queue, process the message
- C. Retrieve the message with increased DelaySeconds, process the message, delete the message from the queue
- D. Retrieve the message with increased DelaySeconds, delete the message from the queue, process the message

<details><summary>Answer:</summary><p>
[A]

Categories:
[SQS]

Explanation:

Question 23@http://jayendrapatil.com/aws-sqs-simple-queue-service/

</p></details><hr>

### Question 24:

You need to process long-running jobs once and only once. How might you do this?

- A. Use an SNS queue and set the visibility timeout to long enough for jobs to process.
- B. Use an SQS queue and set the reprocessing timeout to long enough for jobs to process.
- C. Use an SQS queue and set the visibility timeout to long enough for jobs to process.
- D. Use an SNS queue and set the reprocessing timeout to long enough for jobs to process.

<details><summary>Answer:</summary><p>
[C]

Categories:
[SQS, SNS]

Explanation:

Question 24@http://jayendrapatil.com/aws-sqs-simple-queue-service/

</p></details><hr>

### Question 25:

You are getting a lot of empty receive requests when using Amazon SQS. This is making a lot of unnecessary network load on your instances. What can you do to reduce this load?

- A. Subscribe your queue to an SNS topic instead.
- B. Use as long of a poll as possible, instead of short polls.
- C. Alter your visibility timeout to be shorter.
- D. Use <code>sqsd</code> on your EC2 instances.

<details><summary>Answer:</summary><p>
[B]

Categories:
[SQS, EC2, SNS]

Explanation:

Question 25@http://jayendrapatil.com/aws-sqs-simple-queue-service/

B: http://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-long-polling.html

</p></details><hr>

### Question 26:

You have an asynchronous processing application using an Auto Scaling Group and an SQS Queue. The Auto Scaling Group scales according to the depth of the job queue. The completion velocity of the jobs has gone down, the Auto Scaling Group size has maxed out, but the inbound job velocity did not increase. What is a possible issue?

- A. Some of the new jobs coming in are malformed and unprocessable.
- B. The routing tables changed and none of the workers can process events anymore. 
- C. Someone changed the IAM Role Policy on the instances in the worker group and broke permissions to access the queue. 
- D. The scaling metric is not functioning correctly. 

<details><summary>Answer:</summary><p>
[A]

Categories:
[IAM, SQS, ASG]

Explanation:

Question 26@http://jayendrapatil.com/aws-sqs-simple-queue-service/

A: As other options would cause the job to stop processing completely, the only reasonable option seems that some of the recent messages must be malformed and unprocessable

B: If changed, none of the jobs would be processed

C: If IAM role changed no jobs would be processed

D: scaling metric did work fine as the autoscaling caused the instances to increase

</p></details><hr>

### Question 27:

Company B provides an online image recognition service and utilizes SQS to decouple system components for scalability. The SQS consumers poll the imaging queue as often as possible to keep end-to-end throughput as high as possible. However, Company B is realizing that polling in tight loops is burning CPU cycles and increasing costs with empty responses. How can Company B reduce the number of empty responses?

- A. Set the imaging queue visibility Timeout attribute to 20 seconds
- B. Set the Imaging queue ReceiveMessageWaitTimeSeconds attribute to 20 seconds
- C. Set the imaging queue MessageRetentionPeriod attribute to 20 seconds
- D. Set the DelaySeconds parameter of a message to 20 seconds

<details><summary>Answer:</summary><p>
[B]

Categories:
[SES, SQS]

Explanation:

Question 27@http://jayendrapatil.com/aws-sqs-simple-queue-service/

B: http://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-long-polling.html

B: Refer

B: (Long polling. )

</p></details><hr>

