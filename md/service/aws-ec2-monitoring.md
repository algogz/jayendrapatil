### Question 1:

In the basic monitoring package for EC2, Amazon CloudWatch provides the following metrics:

- A. Web server visible metrics such as number failed transaction requests
- B. Operating system visible metrics such as memory utilization
- C. Database visible metrics such as number of connections
- D. Hypervisor visible metrics such as CPU utilization

<details><summary>Answer:</summary><p>
[D]

Categories:
[EC2, CloudWatch]

Explanation:

Question 1@http://jayendrapatil.com/aws-ec2-monitoring/

</p></details><hr>

### Question 2:

Which of the following requires a custom CloudWatch metric to monitor?

- A. Memory Utilization of an EC2 instance
- B. CPU Utilization of an EC2 instance
- C. Disk usage activity of an EC2 instance
- D. Data transfer of an EC2 instance

<details><summary>Answer:</summary><p>
[A]

Categories:
[EC2, CloudWatch]

Explanation:

Question 2@http://jayendrapatil.com/aws-ec2-monitoring/

</p></details><hr>

### Question 3:

A user has configured CloudWatch monitoring on an EBS backed EC2 instance. If the user has not attached any additional device, which of the below mentioned metrics will always show a 0 value?

- A. DiskReadBytes
- B. NetworkIn
- C. NetworkOut
- D. CPUUtilization

<details><summary>Answer:</summary><p>
[A]

Categories:
[EC2, CloudWatch, EBS]

Explanation:

Question 3@http://jayendrapatil.com/aws-ec2-monitoring/

</p></details><hr>

### Question 4:

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

Question 4@http://jayendrapatil.com/aws-ec2-monitoring/

</p></details><hr>

### Question 5:

An AWS account owner has setup multiple IAM users. One IAM user only has CloudWatch access. He has setup the alarm action, which stops the EC2 instances when the CPU utilization is below the threshold limit. What will happen in this case?

- A. It is not possible to stop the instance using the CloudWatch alarm
- B. CloudWatch will stop the instance when the action is executed
- C. The user cannot set an alarm on EC2 since he does not have the permission
- D. The user can setup the action but it will not be executed if the user does not have EC2 rights

<details><summary>Answer:</summary><p>
[D]

Categories:
[IAM, EC2, CloudWatch]

Explanation:

Question 5@http://jayendrapatil.com/aws-ec2-monitoring/

</p></details><hr>

### Question 6:

A user has launched 10 instances from the same AMI ID using Auto Scaling. The user is trying to see the average CPU utilization across all instances of the last 2 weeks under the CloudWatch console. How can the user achieve this?

- A. View the Auto Scaling CPU metrics
- B. Aggregate the data over the instance AMI ID 
- C. The user has to use the CloudWatchanalyser to find the average data across instances
- D. It is not possible to see the average CPU utilization of the same AMI ID since the instance ID is different

<details><summary>Answer:</summary><p>
[A]

Categories:
[CloudWatch, ASG]

Explanation:

Question 6@http://jayendrapatil.com/aws-ec2-monitoring/

A: https://docs.aws.amazon.com/autoscaling/latest/userguide/as-instance-monitoring.html

B: Works but needs detailed monitoring enabled

</p></details><hr>

