### Question 1:

A company is building a two-tier web application to serve dynamic transaction-based content. The data tier is leveraging an Online Transactional Processing (OLTP) database. What services should you leverage to enable an elastic and scalable web tier?

- A. Elastic Load Balancing, Amazon EC2, and Auto Scaling
- B. Elastic Load Balancing, Amazon RDS with Multi-AZ, and Amazon S3
- C. Amazon RDS with Multi-AZ and Auto Scaling
- D. Amazon EC2, Amazon DynamoDB, and Amazon S3

<details><summary>Answer:</summary><p>
[A]

Categories:
[S3, RDS, EC2, ASG, DynamoDB, ELB]

Explanation:

Question 1@http://jayendrapatil.com/aws-auto-scaling-elb/

</p></details><hr>

### Question 2:

You have been given a scope to deploy some AWS infrastructure for a large organization. The requirements are that you will have a lot of EC2 instances but may need to add more when the average utilization of your Amazon EC2 fleet is high and conversely remove them when CPU utilization is low. Which AWS services would be best to use to accomplish this?

- A. Amazon CloudFront, Amazon CloudWatch and Elastic Load Balancing
- B. Auto Scaling, Amazon CloudWatch and AWS CloudTrail
- C. Auto Scaling, Amazon CloudWatch and Elastic Load Balancing
- D. Auto Scaling, Amazon CloudWatch and AWS Elastic Beanstalk

<details><summary>Answer:</summary><p>
[C]

Categories:
[CloudFront, EC2, CloudWatch, ASG, ELB, Elastic Beanstalk, CloudTrail]

Explanation:

Question 2@http://jayendrapatil.com/aws-auto-scaling-elb/

</p></details><hr>

### Question 3:

A user has configured ELB with Auto Scaling. The user suspended the Auto Scaling AddToLoadBalancer, which adds instances to the load balancer. process for a while. What will happen to the instances launched during the suspension period?

- A. The instances will not be registered with ELB and the user has to manually register when the process is resumed
- B. The instances will be registered with ELB only once the process has resumed
- C. Auto Scaling will not launch the instance during this period due to process suspension
- D. It is not possible to suspend only the AddToLoadBalancer process

<details><summary>Answer:</summary><p>
[A]

Categories:
[ASG, ELB]

Explanation:

Question 3@http://jayendrapatil.com/aws-auto-scaling-elb/

</p></details><hr>

### Question 4:

You have an Auto Scaling group associated with an Elastic Load Balancer (ELB). You have noticed that instances launched via the Auto Scaling group are being marked unhealthy due to an ELB health check, but these unhealthy instances are not being terminated. What do you need to do to ensure trial instances marked unhealthy by the ELB will be terminated and replaced?

- A. Change the thresholds set on the Auto Scaling group health check
- B. Add an Elastic Load Balancing health check to your Auto Scaling group
- C. Increase the value for the Health check interval set on the Elastic Load Balancer
- D. Change the health check set on the Elastic Load Balancer to use TCP rather than HTTP checks

<details><summary>Answer:</summary><p>
[B]

Categories:
[ASG, ELB]

Explanation:

Question 4@http://jayendrapatil.com/aws-auto-scaling-elb/

</p></details><hr>

### Question 5:

You are responsible for a web application that consists of an Elastic Load Balancing (ELB) load balancer in front of an Auto Scaling group of Amazon Elastic Compute Cloud (EC2) instances. For a recent deployment of a new version of the application, a new Amazon Machine Image (AMI) was created, and the Auto Scaling group was updated with a new launch configuration that refers to this new AMI. During the deployment, you received complaints from users that the website was responding with errors. All instances passed the ELB health checks. What should you do in order to avoid errors for future deployments? (Choose 2 answer) [PROFESSIONAL]

- A. Add an Elastic Load Balancing health check to the Auto Scaling group. Set a short period for the health checks to operate as soon as possible in order to prevent premature registration of the instance to the load balancer.
- B. Enable EC2 instance CloudWatch alerts to change the launch configuration’s AMI to the previous one. Gradually terminate instances that are using the new AMI.
- C. Set the Elastic Load Balancing health check configuration to target a part of the application that fully tests application health and returns an error if the tests fail.
- D. Create a new launch configuration that refers to the new AMI, and associate it with the group. Double the size of the group, wait for the new instances to become healthy, and reduce back to the original size. If new instances do not become healthy, associate the previous launch configuration.
- E. Increase the Elastic Load Balancing Unhealthy Threshold to a higher value to prevent an unhealthy instance from going into service behind the load balancer.

<details><summary>Answer:</summary><p>
[C, D]

Categories:
[EC2, CloudWatch, ASG, EBS, ELB]

Explanation:

Question 5@http://jayendrapatil.com/aws-auto-scaling-elb/

</p></details><hr>

### Question 6:

What is the order of most-to-least rapidly-scaling (fastest to scale first)? A) EC2 + ELB + Auto Scaling B) Lambda C) RDS

- A. B, A, C
- B. C, B, A
- C. C, A, B
- D. A, C, B

<details><summary>Answer:</summary><p>
[A]

Categories:
[RDS, EC2, ASG, ELB, Lambda]

Explanation:

Question 6@http://jayendrapatil.com/aws-auto-scaling-elb/

A: (Lambda is designed to scale instantly. EC2 + ELB + Auto Scaling require single-digit minutes to scale out. RDS will take at least 15 minutes, and will apply OS patches or any other updates when applied.)

</p></details><hr>

### Question 7:

A user has hosted an application on EC2 instances. The EC2 instances are configured with ELB and Auto Scaling. The application server session time out is 2 hours. The user wants to configure connection draining to ensure that all in-flight requests are supported by ELB even though the instance is being deregistered. What time out period should the user specify for connection draining?

- A. 5 minutes
- B. 1 hour
- C. 30 minutes
- D. 2 hours

<details><summary>Answer:</summary><p>
[B]

Categories:
[SES, EC2, ASG, ELB]

Explanation:

Question 7@http://jayendrapatil.com/aws-auto-scaling-elb/

B: max allowed is 3600 secs that is close to 2 hours to keep the in flight requests alive

</p></details><hr>

