### Question 1:

A user is trying to setup a scheduled scaling activity using Auto Scaling. The user wants to setup the recurring schedule. Which of the below mentioned parameters is not required in this case?

- A. Maximum size
- B. Auto Scaling group name
- C. End time
- D. Recurrence value

<details><summary>Answer:</summary><p>
[A]

Categories:
[ASG]

Explanation:

Question 1@http://jayendrapatil.com/aws-auto-scaling/

</p></details><hr>

### Question 2:

A user has configured Auto Scaling with 3 instances. The user had created a new AMI after updating one of the instances. If the user wants to terminate two specific instances to ensure that Auto Scaling launches an instances with the new launch configuration, which command should he run?

- A. as-delete-instance-in-auto-scaling-group <Instance ID> –no-decrement-desired-capacity
- B. as-terminate-instance-in-auto-scaling-group <Instance ID> –update-desired-capacity
- C. as-terminate-instance-in-auto-scaling-group <Instance ID> –decrement-desired-capacity
- D. as-terminate-instance-in-auto-scaling-group <Instance ID> –no-decrement-desired-capacity

<details><summary>Answer:</summary><p>
[D]

Categories:
[ASG]

Explanation:

Question 2@http://jayendrapatil.com/aws-auto-scaling/

</p></details><hr>

### Question 3:

A user is planning to scale up an application by 8 AM and scale down by 7 PM daily using Auto Scaling. What should the user do in this case?

- A. Setup the scaling policy to scale up and down based on the CloudWatch alarms
- B. User should increase the desired capacity at 8 AM and decrease it by 7 PM manually
- C. User should setup a batch process which launches the EC2 instance at a specific time
- D. Setup scheduled actions to scale up or down at a specific time

<details><summary>Answer:</summary><p>
[D]

Categories:
[EC2, CloudWatch, ASG]

Explanation:

Question 3@http://jayendrapatil.com/aws-auto-scaling/

</p></details><hr>

### Question 4:

An organization has setup Auto Scaling with ELB. Due to some manual error, one of the instances got rebooted. Thus, it failed the Auto Scaling health check. Auto Scaling has marked it for replacement. How can the system admin ensure that the instance does not get terminated?

- A. Update the Auto Scaling group to ignore the instance reboot event
- B. It is not possible to change the status once it is marked for replacement
- C. Manually add that instance to the Auto Scaling group after reboot to avoid replacement
- D. Change the health of the instance to healthy using the Auto Scaling commands

<details><summary>Answer:</summary><p>
[D]

Categories:
[ASG, ELB]

Explanation:

Question 4@http://jayendrapatil.com/aws-auto-scaling/

</p></details><hr>

### Question 5:

A user has configured Auto Scaling with the minimum capacity as 2 and the desired capacity as 2. The user is trying to terminate one of the existing instance with the command: as-terminate-instance-in-auto-scaling-group<Instance ID> –decrement-desired-capacity. What will Auto Scaling do in this scenario?

- A. Terminates the instance and does not launch a new instance
- B. Terminates the instance and updates the desired capacity to 1
- C. Terminates the instance and updates the desired capacity & minimum size to 1
- D. Throws an error

<details><summary>Answer:</summary><p>
[D]

Categories:
[ASG]

Explanation:

Question 5@http://jayendrapatil.com/aws-auto-scaling/

</p></details><hr>

### Question 6:

An organization has configured Auto Scaling for hosting their application. The system admin wants to understand the Auto Scaling health check process. If the instance is unhealthy, Auto Scaling launches an instance and terminates the unhealthy instance. What is the order execution?

- A. Auto Scaling launches a new instance first and then terminates the unhealthy instance
- B. Auto Scaling performs the launch and terminate processes in a random order
- C. Auto Scaling launches and terminates the instances simultaneously
- D. Auto Scaling terminates the instance first and then launches a new instance

<details><summary>Answer:</summary><p>
[D]

Categories:
[SES, ASG]

Explanation:

Question 6@http://jayendrapatil.com/aws-auto-scaling/

</p></details><hr>

### Question 7:

A user has configured ELB with Auto Scaling. The user suspended the Auto Scaling terminate process only for a while. What will happen to the availability zone rebalancing process (AZRebalance) during this period?

- A. Auto Scaling will not launch or terminate any instances
- B. Auto Scaling will allow the instances to grow more than the maximum size
- C. Auto Scaling will keep launching instances till the maximum instance size
- D. It is not possible to suspend the terminate process while keeping the launch active

<details><summary>Answer:</summary><p>
[B]

Categories:
[ASG, ELB]

Explanation:

Question 7@http://jayendrapatil.com/aws-auto-scaling/

</p></details><hr>

### Question 8:

An organization has configured Auto Scaling with ELB. There is a memory issue in the application which is causing CPU utilization to go above 90%. The higher CPU usage triggers an event for Auto Scaling as per the scaling policy. If the user wants to find the root cause inside the application without triggering a scaling activity, how can he achieve this?

- A. Stop the scaling process until research is completed
- B. It is not possible to find the root cause from that instance without triggering scaling
- C. Delete Auto Scaling until research is completed
- D. Suspend the scaling process until research is completed

<details><summary>Answer:</summary><p>
[D]

Categories:
[ASG, ELB]

Explanation:

Question 8@http://jayendrapatil.com/aws-auto-scaling/

</p></details><hr>

### Question 9:

A user has configured ELB with Auto Scaling. The user suspended the Auto Scaling Alarm Notification (which notifies Auto Scaling for CloudWatch alarms) process for a while. What will Auto Scaling do during this period?

- A. AWS will not receive the alarms from CloudWatch
- B. AWS will receive the alarms but will not execute the Auto Scaling policy
- C. Auto Scaling will execute the policy but it will not launch the instances until the process is resumed
- D. It is not possible to suspend the AlarmNotification process

<details><summary>Answer:</summary><p>
[B]

Categories:
[CloudWatch, ASG, ELB]

Explanation:

Question 9@http://jayendrapatil.com/aws-auto-scaling/

</p></details><hr>

### Question 10:

An organization has configured two single availability zones. The Auto Scaling groups are configured in separate zones. The user wants to merge the groups such that one group spans across multiple zones. How can the user configure this?

- A. Run the command as-join-auto-scaling-group to join the two groups
- B. Run the command as-update-auto-scaling-group to configure one group to span across zones and delete the other group
- C. Run the command as-copy-auto-scaling-group to join the two groups
- D. Run the command as-merge-auto-scaling-group to merge the groups

<details><summary>Answer:</summary><p>
[B]

Categories:
[ASG]

Explanation:

Question 10@http://jayendrapatil.com/aws-auto-scaling/

</p></details><hr>

### Question 11:

An organization has configured Auto Scaling with ELB. One of the instance health check returns the status as Impaired to Auto Scaling. What will Auto Scaling do in this scenario?

- A. Perform a health check until cool down before declaring that the instance has failed
- B. Terminate the instance and launch a new instance
- C. Notify the user using SNS for the failed state
- D. Notify ELB to stop sending traffic to the impaired instance

<details><summary>Answer:</summary><p>
[B]

Categories:
[ASG, SNS, ELB]

Explanation:

Question 11@http://jayendrapatil.com/aws-auto-scaling/

</p></details><hr>

### Question 12:

A user has setup an Auto Scaling group. The group has failed to launch a single instance for more than 24 hours. What will happen to Auto Scaling in this condition

- A. Auto Scaling will keep trying to launch the instance for 72 hours
- B. Auto Scaling will suspend the scaling process
- C. Auto Scaling will start an instance in a separate region
- D. The Auto Scaling group will be terminated automatically

<details><summary>Answer:</summary><p>
[B]

Categories:
[ASG]

Explanation:

Question 12@http://jayendrapatil.com/aws-auto-scaling/

</p></details><hr>

### Question 13:

A user is planning to setup infrastructure on AWS for the Christmas sales. The user is planning to use Auto Scaling based on the schedule for proactive scaling. What advise would you give to the user?

- A. It is good to schedule now because if the user forgets later on it will not scale up
- B. The scaling should be setup only one week before Christmas
- C. Wait till end of November before scheduling the activity
- D. It is not advisable to use scheduled based scaling

<details><summary>Answer:</summary><p>
[C]

Categories:
[ASG]

Explanation:

Question 13@http://jayendrapatil.com/aws-auto-scaling/

</p></details><hr>

### Question 14:

A user is trying to setup a recurring Auto Scaling process. The user has setup one process to scale up every day at 8 am and scale down at 7 PM. The user is trying to setup another recurring process which scales up on the 1st of every month at 8 AM and scales down the same day at 7 PM. What will Auto Scaling do in this scenario

- A. Auto Scaling will execute both processes but will add just one instance on the 1st
- B. Auto Scaling will add two instances on the 1st of the month
- C. Auto Scaling will schedule both the processes but execute only one process randomly
- D. Auto Scaling will throw an error since there is a conflict in the schedule of two separate Auto Scaling Processes

<details><summary>Answer:</summary><p>
[D]

Categories:
[SES, ASG]

Explanation:

Question 14@http://jayendrapatil.com/aws-auto-scaling/

</p></details><hr>

### Question 15:

A sys admin is trying to understand the Auto Scaling activities. Which of the below mentioned processes is not performed by Auto Scaling?

- A. Reboot Instance
- B. Schedule Actions
- C. Replace Unhealthy
- D. Availability Zone Re-Balancing

<details><summary>Answer:</summary><p>
[A]

Categories:
[SES, ASG]

Explanation:

Question 15@http://jayendrapatil.com/aws-auto-scaling/

</p></details><hr>

### Question 16:

You have started a new job and are reviewing your company’s infrastructure on AWS. You notice one web application where they have an Elastic Load Balancer in front of web instances in an Auto Scaling Group. When you check the metrics for the ELB in CloudWatch you see four healthy instances in Availability Zone (AZ) A and zero in AZ B. There are zero unhealthy instances. What do you need to fix to balance the instances across AZs?

- A. Set the ELB to only be attached to another AZ
- B. Make sure Auto Scaling is configured to launch in both AZs
- C. Make sure your AMI is available in both AZs
- D. Make sure the maximum size of the Auto Scaling Group is greater than 4

<details><summary>Answer:</summary><p>
[B]

Categories:
[CloudWatch, ASG, ELB]

Explanation:

Question 16@http://jayendrapatil.com/aws-auto-scaling/

</p></details><hr>

### Question 17:

You have been asked to leverage Amazon VPC EC2 and SQS to implement an application that submits and receives millions of messages per second to a message queue. You want to ensure your application has sufficient bandwidth between your EC2 instances and SQS. Which option will provide the most scalable solution for communicating between the application and SQS?

- A. Ensure the application instances are properly configured with an Elastic Load Balancer
- B. Ensure the application instances are launched in private subnets with the EBS-optimized option enabled
- C. Ensure the application instances are launched in public subnets with the associate-public-IP-address=trueoption enabled
- D. Launch application instances in private subnets with an Auto Scaling group and Auto Scaling triggers configured to watch the SQS queue size

<details><summary>Answer:</summary><p>
[D]

Categories:
[SQS, EC2, ASG, EBS, VPC]

Explanation:

Question 17@http://jayendrapatil.com/aws-auto-scaling/

</p></details><hr>

### Question 18:

You have decided to change the Instance type for instances running in your application tier that are using Auto Scaling. In which area below would you change the instance type definition?

- A. Auto Scaling launch configuration
- B. Auto Scaling group
- C. Auto Scaling policy
- D. Auto Scaling tags

<details><summary>Answer:</summary><p>
[A]

Categories:
[ASG]

Explanation:

Question 18@http://jayendrapatil.com/aws-auto-scaling/

</p></details><hr>

### Question 19:

A user is trying to delete an Auto Scaling group from CLI. Which of the below mentioned steps are to be performed by the user?

- A. Terminate the instances with the ec2-terminate-instance command
- B. Terminate the Auto Scaling instances with the as-terminate-instance command
- C. Set the minimum size and desired capacity to 0
- D. There is no need to change the capacity. Run the as-delete-group command and it will reset all values to 0

<details><summary>Answer:</summary><p>
[C]

Categories:
[EC2, ASG]

Explanation:

Question 19@http://jayendrapatil.com/aws-auto-scaling/

</p></details><hr>

### Question 20:

A user has created a web application with Auto Scaling. The user is regularly monitoring the application and he observed that the traffic is highest on Thursday and Friday between 8 AM to 6 PM. What is the best solution to handle scaling in this case?

- A. Add a new instance manually by 8 AM Thursday and terminate the same by 6 PM Friday
- B. Schedule Auto Scaling to scale up by 8 AM Thursday and scale down after 6 PM on Friday
- C. Schedule a policy which may scale up every day at 8 AM and scales down by 6 PM
- D. Configure a batch process to add a instance by 8 AM and remove it by Friday 6 PM

<details><summary>Answer:</summary><p>
[B]

Categories:
[ASG]

Explanation:

Question 20@http://jayendrapatil.com/aws-auto-scaling/

</p></details><hr>

### Question 21:

A user has configured the Auto Scaling group with the minimum capacity as 3 and the maximum capacity as 5. When the user configures the AS group, how many instances will Auto Scaling launch?

- A. 3
- B. 0
- C. 5
- D. 2

<details><summary>Answer:</summary><p>
[A]

Categories:
[ASG]

Explanation:

Question 21@http://jayendrapatil.com/aws-auto-scaling/

</p></details><hr>

### Question 22:

A sys admin is maintaining an application on AWS. The application is installed on EC2 and user has configured ELB and Auto Scaling. Considering future load increase, the user is planning to launch new servers proactively so that they get registered with ELB. How can the user add these instances with Auto Scaling?

- A. Increase the desired capacity of the Auto Scaling group
- B. Increase the maximum limit of the Auto Scaling group
- C. Launch an instance manually and register it with ELB on the fly
- D. Decrease the minimum limit of the Auto Scaling group

<details><summary>Answer:</summary><p>
[A]

Categories:
[EC2, ASG, ELB]

Explanation:

Question 22@http://jayendrapatil.com/aws-auto-scaling/

</p></details><hr>

### Question 23:

In reviewing the auto scaling events for your application you notice that your application is scaling up and down multiple times in the same hour. What design choice could you make to optimize for the cost while preserving elasticity? Choose 2 answers.

- A. Modify the Amazon CloudWatch alarm period that triggers your auto scaling scale down policy.
- B. Modify the Auto scaling group termination policy to terminate the oldest instance first.
- C. Modify the Auto scaling policy to use scheduled scaling actions.
- D. Modify the Auto scaling group cool down timers.
- E. Modify the Auto scaling group termination policy to terminate newest instance first.

<details><summary>Answer:</summary><p>
[A, D]

Categories:
[CloudWatch, ASG]

Explanation:

Question 23@http://jayendrapatil.com/aws-auto-scaling/

</p></details><hr>

### Question 24:

You have a business critical two tier web app currently deployed in two availability zones in a single region, using Elastic Load Balancing and Auto Scaling. The app depends on synchronous replication (very low latency connectivity) at the database layer. The application needs to remain fully available even if one application Availability Zone goes off-line, and Auto scaling cannot launch new instances in the remaining Availability Zones. How can the current architecture be enhanced to ensure this? [PROFESSIONAL]

- A. Deploy in two regions using Weighted Round Robin (WRR), with Auto Scaling minimums set for 100% peak load per region.
- B. Deploy in three AZs, with Auto Scaling minimum set to handle 50% peak load per zone.
- C. Deploy in three AZs, with Auto Scaling minimum set to handle 33% peak load per zone. 
- D. Deploy in two regions using Weighted Round Robin (WRR), with Auto Scaling minimums set for 50% peak load per region.

<details><summary>Answer:</summary><p>
[B]

Categories:
[ASG, ELB]

Explanation:

Question 24@http://jayendrapatil.com/aws-auto-scaling/

C: Loss of one AZ will handle only 66% if the autoscaling also fails

</p></details><hr>

### Question 25:

A user has created a launch configuration for Auto Scaling where CloudWatch detailed monitoring is disabled. The user wants to now enable detailed monitoring. How can the user achieve this?

- A. Update the Launch config with CLI to set InstanceMonitoringDisabled = false
- B. The user should change the Auto Scaling group from the AWS console to enable detailed monitoring
- C. Update the Launch config with CLI to set InstanceMonitoring.Enabled = true
- D. Create a new Launch Config with detail monitoring enabled and update the Auto Scaling group

<details><summary>Answer:</summary><p>
[D]

Categories:
[CloudWatch, ASG]

Explanation:

Question 25@http://jayendrapatil.com/aws-auto-scaling/

</p></details><hr>

### Question 26:

A user has created an Auto Scaling group with default configurations from CLI. The user wants to setup the CloudWatch alarm on the EC2 instances, which are launched by the Auto Scaling group. The user has setup an alarm to monitor the CPU utilization every minute. Which of the below mentioned statements is true?

- A. It will fetch the data at every minute but the four data points [corresponding to 4 minutes] will not have value since the EC2 basic monitoring metrics are collected every five minutes
- B. It will fetch the data at every minute as detailed monitoring on EC2 will be enabled by the default launch configuration of Auto Scaling
- C. The alarm creation will fail since the user has not enabled detailed monitoring on the EC2 instances
- D. The user has to first enable detailed monitoring on the EC2 instances to support alarm monitoring at every minute

<details><summary>Answer:</summary><p>
[B]

Categories:
[EC2, CloudWatch, ASG]

Explanation:

Question 26@http://jayendrapatil.com/aws-auto-scaling/

</p></details><hr>

### Question 27:

A customer has a website which shows all the deals available across the market. The site experiences a load of 5 large EC2 instances generally. However, a week before Thanksgiving vacation they encounter a load of almost 20 large instances. The load during that period varies over the day based on the office timings. Which of the below mentioned solutions is cost effective as well as help the website achieve better performance?

- A. Keep only 10 instances running and manually launch 10 instances every day during office hours.
- B. Setup to run 10 instances during the pre-vacation period and only scale up during the office time by launching 10 more instances using the AutoScaling schedule.
- C. During the pre-vacation period setup a scenario where the organization has 15 instances running and 5 instances to scale up and down using Auto Scaling based on the network I/O policy.
- D. During the pre-vacation period setup 20 instances to run continuously.

<details><summary>Answer:</summary><p>
[B]

Categories:
[EC2, ASG, EBS]

Explanation:

Question 27@http://jayendrapatil.com/aws-auto-scaling/

</p></details><hr>

### Question 28:

When Auto Scaling is launching a new instance based on condition, which of the below mentioned policies will it follow?

- A. Based on the criteria defined with cross zone Load balancing
- B. Launch an instance which has the highest load distribution
- C. Launch an instance in the AZ with the fewest instances
- D. Launch an instance in the AZ which has the highest instances

<details><summary>Answer:</summary><p>
[C]

Categories:
[ASG]

Explanation:

Question 28@http://jayendrapatil.com/aws-auto-scaling/

</p></details><hr>

### Question 29:

The user has created multiple AutoScaling groups. The user is trying to create a new AS group but it fails. How can the user know that he has reached the AS group limit specified by AutoScaling in that region?

- A. Run the command: as-describe-account-limits
- B. Run the command: as-describe-group-limits
- C. Run the command: as-max-account-limits
- D. Run the command: as-list-account-limits

<details><summary>Answer:</summary><p>
[A]

Categories:
[]

Explanation:

Question 29@http://jayendrapatil.com/aws-auto-scaling/

</p></details><hr>

### Question 30:

A user is trying to save some cost on the AWS services. Which of the below mentioned options will not help him save cost?

- A. Delete the unutilized EBS volumes once the instance is terminated
- B. Delete the Auto Scaling launch configuration after the instances are terminated 
- C. Release the elastic IP if not required once the instance is terminated
- D. Delete the AWS ELB after the instances are terminated

<details><summary>Answer:</summary><p>
[]

Categories:
[ASG, EBS, ELB]

Explanation:

Question 30@http://jayendrapatil.com/aws-auto-scaling/

B: Auto Scaling Launch config does not cost anything

</p></details><hr>

### Question 31:

To scale up the AWS resources using manual Auto Scaling, which of the below mentioned parameters should the user change?

- A. Maximum capacity
- B. Desired capacity
- C. Preferred capacity
- D. Current capacity

<details><summary>Answer:</summary><p>
[B]

Categories:
[ASG]

Explanation:

Question 31@http://jayendrapatil.com/aws-auto-scaling/

</p></details><hr>

### Question 32:

For AWS Auto Scaling, what is the first transition state an existing instance enters after leaving steady state in Standby mode?

- A. Detaching
- B. Terminating:Wait
- C. Pending
- D. EnteringStandby

<details><summary>Answer:</summary><p>
[C]

Categories:
[ASG]

Explanation:

Question 32@http://jayendrapatil.com/aws-auto-scaling/

C: http://docs.aws.amazon.com/AutoScaling/latest/DeveloperGuide/AutoScalingGroupLifecycle.html

C: (You can put any instance that is in an InService state into a Standby state. This enables you to remove the instance from service, troubleshoot or make changes to it, and then put it back into service. Instances in a Standby state continue to be managed by the Auto Scaling group. However, they are not an active part of your application until you put them back into service. Refer )

</p></details><hr>

### Question 33:

For AWS Auto Scaling, what is the first transition state an instance enters after leaving steady state when scaling in due to health check failure or decreased load?

- A. Terminating
- B. Detaching
- C. Terminating:Wait
- D. EnteringStandby

<details><summary>Answer:</summary><p>
[A]

Categories:
[ASG]

Explanation:

Question 33@http://jayendrapatil.com/aws-auto-scaling/

A: http://docs.aws.amazon.com/AutoScaling/latest/DeveloperGuide/AutoScalingGroupLifecycle.html

A: (When Auto Scaling responds to a scale in event, it terminates one or more instances. These instances are detached from the Auto Scaling group and enter the Terminating state. Refer )

</p></details><hr>

### Question 34:

A user has setup Auto Scaling with ELB on the EC2 instances. The user wants to configure that whenever the CPU utilization is below 10%, Auto Scaling should remove one instance. How can the user configure this?

- A. The user can get an email using SNS when the CPU utilization is less than 10%. The user can use the desired capacity of Auto Scaling to remove the instance
- B. Use CloudWatch to monitor the data and Auto Scaling to remove the instances using scheduled actions
- C. Configure CloudWatch to send a notification to Auto Scaling Launch configuration when the CPU utilization is less than 10% and configure the Auto Scaling policy to remove the instance
- D. Configure CloudWatch to send a notification to the Auto Scaling group when the CPU Utilization is less than 10% and configure the Auto Scaling policy to remove the instance

<details><summary>Answer:</summary><p>
[D]

Categories:
[EC2, CloudWatch, ASG, SNS, ELB]

Explanation:

Question 34@http://jayendrapatil.com/aws-auto-scaling/

</p></details><hr>

### Question 35:

A user has enabled detailed CloudWatch metric monitoring on an Auto Scaling group. Which of the below mentioned metrics will help the user identify the total number of instances in an Auto Scaling group including pending, terminating and running instances?

- A. GroupTotalInstances
- B. GroupSumInstances
- C. It is not possible to get a count of all the three metrics together. The user has to find the individual number of running, terminating and pending instances and sum it
- D. GroupInstancesCount

<details><summary>Answer:</summary><p>
[A]

Categories:
[CloudWatch, ASG]

Explanation:

Question 35@http://jayendrapatil.com/aws-auto-scaling/

A: http://docs.aws.amazon.com/autoscaling/latest/userguide/as-instance-monitoring.html#as-group-metrics

</p></details><hr>

### Question 36:

Your startup wants to implement an order fulfillment process for selling a personalized gadget that needs an average of 3-4 days to produce with some orders taking up to 6 months you expect 10 orders per day on your first day. 1000 orders per day after 6 months and 10,000 orders after 12 months. Orders coming in are checked for consistency then dispatched to your manufacturing plant for production quality control packaging shipment and payment processing. If the product does not meet the quality standards at any stage of the process employees may force the process to repeat a step. Customers are notified via email about order status and any critical issues with their orders such as payment failure. Your case architecture includes AWS Elastic Beanstalk for your website with an RDS MySQL instance for customer data and orders. How can you implement the order fulfillment process while making sure that the emails are delivered reliably? [PROFESSIONAL]

- A. Add a business process management application to your Elastic Beanstalk app servers and re-use the ROS database for tracking order status use one of the Elastic Beanstalk instances to send emails to customers.
- B. Use SWF with an Auto Scaling group of activity workers and a decider instance in another Auto Scaling group with min/max=1 Use the decider instance to send emails to customers.
- C. Use SWF with an Auto Scaling group of activity workers and a decider instance in another Auto Scaling group with min/max=1 use SES to send emails to customers.
- D. Use an SQS queue to manage all process tasks Use an Auto Scaling group of EC2 Instances that poll the tasks and execute them. Use SES to send emails to customers.

<details><summary>Answer:</summary><p>
[C]

Categories:
[SES, RDS, SWF, SQS, EC2, ASG, EBS, Elastic Beanstalk]

Explanation:

Question 36@http://jayendrapatil.com/aws-auto-scaling/

</p></details><hr>

