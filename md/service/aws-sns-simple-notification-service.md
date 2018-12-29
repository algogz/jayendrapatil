### Question 1:

Which of the following notification endpoints or clients does Amazon Simple Notification Service support? Choose 2 answers

- A. Email
- B. CloudFront distribution
- C. File Transfer Protocol
- D. Short Message Service
- E. Simple Network Management Protocol

<details><summary>Answer:</summary><p>
[A, D]

Categories:
[CloudFront, SNS]

Explanation:

Question 1@http://jayendrapatil.com/aws-sns-simple-notification-service/

</p></details><hr>

### Question 2:

What happens when you create a topic on Amazon SNS?

- A. The topic is created, and it has the name you specified for it.
- B. An ARN (Amazon Resource Name) is created
- C. You can create a topic on Amazon SQS, not on Amazon SNS.
- D. This question doesn’t make sense.

<details><summary>Answer:</summary><p>
[B]

Categories:
[SQS, SNS]

Explanation:

Question 2@http://jayendrapatil.com/aws-sns-simple-notification-service/

</p></details><hr>

### Question 3:

A user has deployed an application on his private cloud. The user is using his own monitoring tool. He wants to configure that whenever there is an error, the monitoring tool should notify him via SMS. Which of the below mentioned AWS services will help in this scenario?

- A. None because the user infrastructure is in the private cloud/
- B. AWS SNS
- C. AWS SES
- D. AWS SMS

<details><summary>Answer:</summary><p>
[B]

Categories:
[SES, SNS]

Explanation:

Question 3@http://jayendrapatil.com/aws-sns-simple-notification-service/

</p></details><hr>

### Question 4:

A user wants to make so that whenever the CPU utilization of the AWS EC2 instance is above 90%, the redlight of his bedroom turns on. Which of the below mentioned AWS services is helpful for this purpose?

- A. AWS CloudWatch + AWS SES
- B. AWS CloudWatch + AWS SNS
- C. It is not possible to configure the light with the AWS infrastructure services
- D. AWS CloudWatch and a dedicated software turning on the light

<details><summary>Answer:</summary><p>
[B]

Categories:
[SES, EC2, CloudWatch, SNS]

Explanation:

Question 4@http://jayendrapatil.com/aws-sns-simple-notification-service/

</p></details><hr>

### Question 5:

A user is trying to understand AWS SNS. To which of the below mentioned end points is SNS unable to send a notification?

- A. Email JSON
- B. HTTP
- C. AWS SQS
- D. AWS SES

<details><summary>Answer:</summary><p>
[D]

Categories:
[SES, SQS, SNS]

Explanation:

Question 5@http://jayendrapatil.com/aws-sns-simple-notification-service/

</p></details><hr>

### Question 6:

A user is running a webserver on EC2. The user wants to receive the SMS when the EC2 instance utilization is above the threshold limit. Which AWS services should the user configure in this case?

- A. AWS CloudWatch + AWS SES
- B. AWS CloudWatch + AWS SNS
- C. AWS CloudWatch + AWS SQS
- D. AWS EC2 + AWS CloudWatch

<details><summary>Answer:</summary><p>
[B]

Categories:
[SES, SQS, EC2, CloudWatch, EBS, SNS]

Explanation:

Question 6@http://jayendrapatil.com/aws-sns-simple-notification-service/

</p></details><hr>

### Question 7:

A user is planning to host a mobile game on EC2 which sends notifications to active users on either high score or the addition of new features. The user should get this notification when he is online on his mobile device. Which of the below mentioned AWS services can help achieve this functionality?

- A. AWS Simple Notification Service
- B. AWS Simple Queue Service
- C. AWS Mobile Communication Service
- D. AWS Simple Email Service

<details><summary>Answer:</summary><p>
[A]

Categories:
[SES, SQS, EC2, SNS]

Explanation:

Question 7@http://jayendrapatil.com/aws-sns-simple-notification-service/

</p></details><hr>

### Question 8:

You are providing AWS consulting service for a company developing a new mobile application that will be leveraging amazon SNS push for push notifications. In order to send direct notification messages to individual devices each device registration identifier or token needs to be registered with SNS, however the developers are not sure of the best way to do this. You advise them to: –

- A. Bulk upload the device tokens contained in a CSV file via the AWS Management Console
- B. Let the push notification service (e.g. Amazon Device messaging) handle the registration
- C. Implement a token vending service to handle the registration
- D. Call the CreatePlatformEndpoint API function to register multiple device tokens. 

<details><summary>Answer:</summary><p>
[D]

Categories:
[SNS]

Explanation:

Question 8@http://jayendrapatil.com/aws-sns-simple-notification-service/

D: http://docs.aws.amazon.com/sns/latest/dg/mobile-push-send-devicetoken.html

</p></details><hr>

### Question 9:

A company is running a batch analysis every hour on their main transactional DB running on an RDS MySQL instance to populate their central Data Warehouse running on Redshift. During the execution of the batch their transactional applications are very slow. When the batch completes they need to update the top management dashboard with the new data. The dashboard is produced by another system running on-premises that is currently started when a manually-sent email notifies that an update is required The on-premises system cannot be modified because is managed by another team. How would you optimize this scenario to solve performance issues and automate the process as much as possible?

- A. Replace RDS with Redshift for the batch analysis and SNS to notify the on-premises system to update the dashboard
- B. Replace RDS with Redshift for the batch analysis and SQS to send a message to the on-premises system to update the dashboard
- C. Create an RDS Read Replica for the batch analysis and SNS to notify me on-premises system to update the dashboard
- D. Create an RDS Read Replica for the batch analysis and SQS to send a message to the on-premises system to update the dashboard.

<details><summary>Answer:</summary><p>
[C]

Categories:
[SES, RDS, SQS, SNS, Redshift]

Explanation:

Question 9@http://jayendrapatil.com/aws-sns-simple-notification-service/

</p></details><hr>

### Question 10:

Which of the following are valid SNS delivery transports? Choose 2 answers.

- A. HTTP
- B. UDP
- C. SMS
- D. DynamoDB
- E. Named Pipes

<details><summary>Answer:</summary><p>
[A, C]

Categories:
[SNS, DynamoDB]

Explanation:

Question 10@http://jayendrapatil.com/aws-sns-simple-notification-service/

</p></details><hr>

### Question 11:

What is the format of structured notification messages sent by Amazon SNS?

- A. An XML object containing MessageId, UnsubscribeURL, Subject, Message and other values
- B. An JSON object containing MessageId, DuplicateFlag, Message and other values
- C. An XML object containing MessageId, DuplicateFlag, Message and other values
- D. An JSON object containing MessageId, unsubscribeURL, Subject, Message and other values

<details><summary>Answer:</summary><p>
[D]

Categories:
[SNS]

Explanation:

Question 11@http://jayendrapatil.com/aws-sns-simple-notification-service/

</p></details><hr>

### Question 12:

Which of the following are valid arguments for an SNS Publish request? Choose 3 answers.

- A. TopicAm
- B. Subject
- C. Destination
- D. Format
- E. Message
- F. Language

<details><summary>Answer:</summary><p>
[A, B, E]

Categories:
[SNS]

Explanation:

Question 12@http://jayendrapatil.com/aws-sns-simple-notification-service/

</p></details><hr>

