### Question 1:

A company needs to monitor the read and write IOPs metrics for their AWS MySQL RDS instance and send real-time alerts to their operations team. Which AWS services can accomplish this? Choose 2 answers

- A. Amazon Simple Email Service 
- B. Amazon CloudWatch
- C. Amazon Simple Queue Service
- D. Amazon Route 53
- E. Amazon Simple Notification Service

<details><summary>Answer:</summary><p>
[B, E]

Categories:
[SES, RDS, SQS, CloudWatch, SNS, Route 53]

Explanation:

Question 1@http://jayendrapatil.com/aws-cloudwatch-overview/

A: Cannot be integrated with CloudWatch directly

</p></details><hr>

### Question 2:

A customer needs to capture all client connection information from their load balancer every five minutes. The company wants to use this data for analyzing traffic patterns and troubleshooting their applications. Which of the following options meets the customer requirements?

- A. Enable AWS CloudTrail for the load balancer.
- B. Enable access logs on the load balancer. 
- C. Install the Amazon CloudWatch Logs agent on the load balancer.
- D. Enable Amazon CloudWatch metrics on the load balancer 

<details><summary>Answer:</summary><p>
[B]

Categories:
[CloudWatch, CloudTrail]

Explanation:

Question 2@http://jayendrapatil.com/aws-cloudwatch-overview/

B: https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/access-log-collection.html

D: does not provide Client connection information

</p></details><hr>

### Question 3:

A user is running a batch process on EBS backed EC2 instances. The batch process starts a few instances to process Hadoop Map reduce jobs, which can run between 50 – 600 minutes or sometimes for more time. The user wants to configure that the instance gets terminated only when the process is completed. How can the user configure this with CloudWatch?

- A. Setup the CloudWatch action to terminate the instance when the CPU utilization is less than 5%
- B. Setup the CloudWatch with Auto Scaling to terminate all the instances
- C. Setup a job which terminates all instances after 600 minutes
- D. It is not possible to terminate instances automatically

<details><summary>Answer:</summary><p>
[A]

Categories:
[EC2, CloudWatch, ASG, EBS]

Explanation:

Question 3@http://jayendrapatil.com/aws-cloudwatch-overview/

</p></details><hr>

### Question 4:

A user has two EC2 instances running in two separate regions. The user is running an internal memory management tool, which captures the data and sends it to CloudWatch in US East, using a CLI with the same namespace and metric. Which of the below mentioned options is true with respect to the above statement?

- A. The setup will not work as CloudWatch cannot receive data across regions
- B. CloudWatch will receive and aggregate the data based on the namespace and metric
- C. CloudWatch will give an error since the data will conflict due to two sources
- D. CloudWatch will take the data of the server, which sends the data first

<details><summary>Answer:</summary><p>
[B]

Categories:
[EC2, CloudWatch]

Explanation:

Question 4@http://jayendrapatil.com/aws-cloudwatch-overview/

</p></details><hr>

### Question 5:

A user is sending the data to CloudWatch using the CloudWatch API. The user is sending data 90 minutes in the future. What will CloudWatch do in this case?

- A. CloudWatch will accept the data
- B. It is not possible to send data of the future
- C. It is not possible to send the data manually to CloudWatch
- D. The user cannot send data for more than 60 minutes in the future

<details><summary>Answer:</summary><p>
[A]

Categories:
[CloudWatch]

Explanation:

Question 5@http://jayendrapatil.com/aws-cloudwatch-overview/

</p></details><hr>

### Question 6:

A user is having data generated randomly based on a certain event. The user wants to upload that data to CloudWatch. It may happen that event may not have data generated for some period due to randomness. Which of the below mentioned options is a recommended option for this case?

- A. For the period when there is no data, the user should not send the data at all
- B. For the period when there is no data the user should send a blank value
- C. For the period when there is no data the user should send the value as 0
- D. The user must upload the data to CloudWatch as having no data for some period will cause an error at CloudWatch monitoring

<details><summary>Answer:</summary><p>
[C]

Categories:
[CloudWatch]

Explanation:

Question 6@http://jayendrapatil.com/aws-cloudwatch-overview/

C: https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/publishingMetrics.html#publishingZero

C: (Refer

</p></details><hr>

### Question 7:

A user has a weighing plant. The user measures the weight of some goods every 5 minutes and sends data to AWS CloudWatch for monitoring and tracking. Which of the below mentioned parameters is mandatory for the user to include in the request list?

- A. Value
- B. Namespace ( )
- C. Metric Name
- D. Timezone

<details><summary>Answer:</summary><p>
[B]

Categories:
[CloudWatch]

Explanation:

Question 7@http://jayendrapatil.com/aws-cloudwatch-overview/

B: http://docs.aws.amazon.com/cli/latest/reference/cloudwatch/put-metric-data.html

B: refer

</p></details><hr>

### Question 8:

A user has a refrigerator plant. The user is measuring the temperature of the plant every 15 minutes. If the user wants to send the data to CloudWatch to view the data visually, which of the below mentioned statements is true with respect to the information given above?

- A. The user needs to use AWS CLI or API to upload the data
- B. The user can use the AWS Import Export facility to import data to CloudWatch
- C. The user will upload data from the AWS console
- D. The user cannot upload data to CloudWatch since it is not an AWS service metric

<details><summary>Answer:</summary><p>
[A]

Categories:
[CloudWatch]

Explanation:

Question 8@http://jayendrapatil.com/aws-cloudwatch-overview/

</p></details><hr>

### Question 9:

A user has launched an EC2 instance. The user is planning to setup the CloudWatch alarm. Which of the below mentioned actions is not supported by the CloudWatch alarm?

- A. Notify the Auto Scaling launch config to scale up
- B. Send an SMS using SNS
- C. Notify the Auto Scaling group to scale down
- D. Stop the EC2 instance

<details><summary>Answer:</summary><p>
[A]

Categories:
[EC2, CloudWatch, ASG, SNS]

Explanation:

Question 9@http://jayendrapatil.com/aws-cloudwatch-overview/

</p></details><hr>

### Question 10:

A user has a refrigerator plant. The user is measuring the temperature of the plant every 15 minutes. If the user wants to send the data to CloudWatch to view the data visually, which of the below mentioned statements is true with respect to the information given above?

- A. The user needs to use AWS CLI or API to upload the data
- B. The user can use the AWS Import Export facility to import data to CloudWatch
- C. The user will upload data from the AWS console
- D. The user cannot upload data to CloudWatch since it is not an AWS service metric

<details><summary>Answer:</summary><p>
[A]

Categories:
[CloudWatch]

Explanation:

Question 10@http://jayendrapatil.com/aws-cloudwatch-overview/

</p></details><hr>

### Question 11:

A user is trying to aggregate all the CloudWatch metric data of the last 1 week. Which of the below mentioned statistics is not available for the user as a part of data aggregation?

- A. Aggregate
- B. Sum
- C. Sample data
- D. Average

<details><summary>Answer:</summary><p>
[A]

Categories:
[CloudWatch]

Explanation:

Question 11@http://jayendrapatil.com/aws-cloudwatch-overview/

</p></details><hr>

### Question 12:

A user has setup a CloudWatch alarm on an EC2 action when the CPU utilization is above 75%. The alarm sends a notification to SNS on the alarm state. If the user wants to simulate the alarm action how can he achieve this?

- A. Run activities on the CPU such that its utilization reaches above 75%
- B. From the AWS console change the state to ‘Alarm’
- C. The user can set the alarm state to ‘Alarm’ using CLI
- D. Run the SNS action manually

<details><summary>Answer:</summary><p>
[C]

Categories:
[EC2, CloudWatch, SNS]

Explanation:

Question 12@http://jayendrapatil.com/aws-cloudwatch-overview/

</p></details><hr>

### Question 13:

A user is publishing custom metrics to CloudWatch. Which of the below mentioned statements will help the user understand the functionality better?

- A. The user can use the CloudWatch Import tool
- B. The user should be able to see the data in the console after around 15 minutes
- C. If the user is uploading the custom data, the user must supply the namespace, timezone, and metric name as part of the command
- D. The user can view as well as upload data using the console, CLI and APIs

<details><summary>Answer:</summary><p>
[B]

Categories:
[CloudWatch]

Explanation:

Question 13@http://jayendrapatil.com/aws-cloudwatch-overview/

</p></details><hr>

### Question 14:

An application that you are managing has EC2 instances and DynamoDB tables deployed to several AWS Regions. In order to monitor the performance of the application globally, you would like to see two graphs 1) Avg CPU Utilization across all EC2 instances and 2) Number of Throttled Requests for all DynamoDB tables. How can you accomplish this? [PROFESSIONAL]

- A. Tag your resources with the application name, and select the tag name as the dimension in the CloudWatch Management console to view the respective graphs 
- B. Use the CloudWatch CLI tools to pull the respective metrics from each regional endpoint. Aggregate the data offline & store it for graphing in CloudWatch.
- C. Add SNMP traps to each instance and DynamoDB table. Leverage a central monitoring server to capture data from each instance and table. Put the aggregate data into CloudWatch for graphing 
- D. Add a CloudWatch agent to each instance and attach one to each DynamoDB table. When configuring the agent set the appropriate application name & view the graphs in CloudWatch. 

<details><summary>Answer:</summary><p>
[B]

Categories:
[EC2, CloudWatch, DynamoDB]

Explanation:

Question 14@http://jayendrapatil.com/aws-cloudwatch-overview/

A: CloudWatch metrics are regional

C: Can’t add SNMP traps to DynamoDB as it is a managed service

D: Can’t add agents to DynamoDB as it is a managed service

</p></details><hr>

### Question 15:

You have set up Individual AWS accounts for each project. You have been asked to make sure your AWS Infrastructure costs do not exceed the budget set per project for each month. Which of the following approaches can help ensure that you do not exceed the budget each month? [PROFESSIONAL]

- A. Consolidate your accounts so you have a single bill for all accounts and projects 
- B. Set up auto scaling with CloudWatch alarms using SNS to notify you when you are running too many Instances in a given account 
- C. Set up CloudWatch billing alerts for all AWS resources used by each project, with a notification occurring when the amount for each resource tagged to a particular project matches the budget allocated to the project. 
- D. Set up CloudWatch billing alerts for all AWS resources used by each account, with email notifications when it hits 50%. 80% and 90% of its budgeted monthly spend

<details><summary>Answer:</summary><p>
[D]

Categories:
[CloudWatch, ASG, SNS]

Explanation:

Question 15@http://jayendrapatil.com/aws-cloudwatch-overview/

A: Consolidation will not help limit per account

B: many instances do not directly map to cost and would not give exact cost

C: as each project already has a account, no need for resource tagging

</p></details><hr>

### Question 16:

You meet once per month with your operations team to review the past month’s data. During the meeting, you realize that 3 weeks ago, your monitoring system which pings over HTTP from outside AWS recorded a large spike in latency on your 3-tier web service API. You use DynamoDB for the database layer, ELB, EBS, and EC2 for the business logic tier, and SQS, ELB, and EC2 for the presentation layer. Which of the following techniques will NOT help you figure out what happened?

- A. Check your CloudTrail log history around the spike’s time for any API calls that caused slowness.
- B. Review CloudWatch Metrics graphs to determine which component(s) slowed the system down.
- C. Review your ELB access logs in S3 to see if any ELBs in your system saw the latency.
- D. Analyze your logs to detect bursts in traffic at that time.

<details><summary>Answer:</summary><p>
[B]

Categories:
[S3, SQS, EC2, CloudWatch, EBS, DynamoDB, ELB, CloudTrail]

Explanation:

Question 16@http://jayendrapatil.com/aws-cloudwatch-overview/

B: Metrics data was available for 2 weeks before, however it has been extended now before, however it has been extended now

</p></details><hr>

### Question 17:

You have a high security requirement for your AWS accounts. What is the most rapid and sophisticated setup you can use to react to AWS API calls to your account?

- A. Subscription to AWS Config via an SNS Topic. Use a Lambda Function to perform in-flight analysis and reactivity to changes as they occur.
- B. Global AWS CloudTrail setup delivering to S3 with an SNS subscription to the deliver notifications, pushing into a Lambda, which inserts records into an ELK stack for analysis.
- C. Use a CloudWatch Rule ScheduleExpression to periodically analyze IAM credential logs. Push the deltas for events into an ELK stack and perform ad-hoc analysis there.
- D. CloudWatch Events Rules, which trigger based on all AWS API calls, submitting all events to an AWS Kinesis Stream for arbitrary downstream analysis.

<details><summary>Answer:</summary><p>
[D]

Categories:
[S3, RDS, IAM, CloudWatch, Kinesis, SNS, Lambda, CloudTrail]

Explanation:

Question 17@http://jayendrapatil.com/aws-cloudwatch-overview/

D: http://docs.aws.amazon.com/AmazonCloudWatch/latest/DeveloperGuide/EventTypes.html#api_event_type

D: CloudWatch Events allow subscription to AWS API calls, and direction of these events into Kinesis Streams. This allows a unified, near real-time stream for all API calls, which can be analyzed with any tool(s). Refer

</p></details><hr>

### Question 18:

To monitor API calls against our AWS account by different users and entities, we can use ____ to create a history of calls in bulk for later review, and use ____ for reacting to AWS API calls in real-time.

- A. AWS Config; AWS Inspector
- B. AWS CloudTrail; AWS Config
- C. AWS CloudTrail; CloudWatch Events
- D. AWS Config; AWS Lambda

<details><summary>Answer:</summary><p>
[C]

Categories:
[CloudWatch, Lambda, CloudTrail]

Explanation:

Question 18@http://jayendrapatil.com/aws-cloudwatch-overview/

C: https://aws.amazon.com/whitepapers/security-at-scale-governance-in-aws/

C: CloudTrail is a batch API call collection service, CloudWatch Events enables real-time monitoring of calls through the Rules object interface. Refer

</p></details><hr>

### Question 19:

You are hired as the new head of operations for a SaaS company. Your CTO has asked you to make debugging any part of your entire operation simpler and as fast as possible. She complains that she has no idea what is going on in the complex, service-oriented architecture, because the developers just log to disk, and it’s very hard to find errors in logs on so many services. How can you best meet this requirement and satisfy your CTO? [PROFESSIONAL]

- A. Copy all log files into AWS S3 using a cron job on each instance. Use an S3 Notification Configuration on the <code>PutBucket</code> event and publish events to AWS Lambda. Use the Lambda to analyze logs as soon as they come in and flag issues. 
- B. Begin using CloudWatch Logs on every service. Stream all Log Groups into S3 objects. Use AWS EMR cluster jobs to perform adhoc MapReduce analysis and write new queries when needed. 
- C. Copy all log files into AWS S3 using a cron job on each instance. Use an S3 Notification Configuration on the <code>PutBucket</code> event and publish events to AWS Kinesis. Use Apache Spark on AWS EMR to perform at-scale stream processing queries on the log chunks and flag issues. 
- D. Begin using CloudWatch Logs on every service. Stream all Log Groups into an AWS Elasticsearch Service Domain running Kibana 4 and perform log analysis on a search cluster.

<details><summary>Answer:</summary><p>
[D]

Categories:
[S3, Elasticsearch, CloudWatch, Kinesis, EMR, Lambda]

Explanation:

Question 19@http://jayendrapatil.com/aws-cloudwatch-overview/

A: is not fast in search and introduces delay

B: is not fast in search and introduces delay

C: is not fast in search and introduces delay

D: ELK – Elasticsearch, Kibana stack is designed specifically for real-time, ad-hoc log analysis and aggregation

</p></details><hr>

### Question 20:

Your EC2-Based Multi-tier application includes a monitoring instance that periodically makes application -level read only requests of various application components and if any of those fail more than three times 30 seconds calls CloudWatch to fire an alarm, and the alarm notifies your operations team by email and SMS of a possible application health problem. However, you also need to watch the watcher -the monitoring instance itself – and be notified if it becomes unhealthy. Which of the following is a simple way to achieve that goal? [PROFESSIONAL]

- A. Run another monitoring instance that pings the monitoring instance and fires a could watch alarm mat notifies your operations team should the primary monitoring instance become unhealthy.
- B. Set a CloudWatch alarm based on EC2 system and instance status checks and have the alarm notify your operations team of any detected problem with the monitoring instance.
- C. Set a CloudWatch alarm based on the CPU utilization of the monitoring instance and nave the alarm notify your operations team if C r the CPU usage exceeds 50% few more than one minute: then have your monitoring application go into a CPU-bound loop should it Detect any application problems.
- D. Have the monitoring instances post messages to an SOS queue and then dequeue those messages on another instance should the queue cease to have new messages, the second instance should first terminate the original monitoring instance start another backup monitoring instance and assume (the role of the previous monitoring instance and beginning adding messages to the SQS queue.

<details><summary>Answer:</summary><p>
[B]

Categories:
[SQS, EC2, CloudWatch]

Explanation:

Question 20@http://jayendrapatil.com/aws-cloudwatch-overview/

</p></details><hr>

