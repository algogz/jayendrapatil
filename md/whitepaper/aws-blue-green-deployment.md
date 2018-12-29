### Question 1:

What is server immutability?

- A. Not updating a server after creation.
- B. The ability to change server counts.
- C. Updating a server after creation.
- D. The inability to change server counts.

<details><summary>Answer:</summary><p>
[A]

Categories:
[]

Explanation:

Question 1@http://jayendrapatil.com/aws-blue-green-deployment/

A: During the new release, a new set of EC2 instances are rolled out by terminating older instances and are disposable. EC2 instance usage is considered temporary or ephemeral in nature for the period of deployment until the current release is active

</p></details><hr>

### Question 2:

You need to deploy a new application version to production. Because the deployment is high-risk, you need to roll the new version out to users over a number of hours, to make sure everything is working correctly. You need to be able to control the proportion of users seeing the new version of the application down to the percentage point. You use ELB and EC2 with Auto Scaling Groups and custom AMIs with your code pre-installed assigned to Launch Configurations. There are no database-level changes during your deployment. You have been told you cannot spend too much money, so you must not increase the number of EC2 instances much at all during the deployment, but you also need to be able to switch back to the original version of code quickly if something goes wrong. What is the best way to meet these requirements?

- A. Create a second ELB, Auto Scaling Launch Configuration, and Auto Scaling Group using the Launch Configuration. Create AMIs with all code pre-installed. Assign the new AMI to the second Auto Scaling Launch Configuration. Use Route53 Weighted Round Robin Records to adjust the proportion of traffic hitting the two ELBs.
- B. Use the Blue-Green deployment method to enable the fastest possible rollback if needed. Create a full second stack of instances and cut the DNS over to the new stack of instances, and change the DNS back if a rollback is needed. 
- C. Create AMIs with all code pre-installed. Assign the new AMI to the Auto Scaling Launch Configuration, to replace the old one. Gradually terminate instances running the old code (launched with the old Launch Configuration) and allow the new AMIs to boot to adjust the traffic balance to the new code. On rollback, reverse the process by doing the same thing, but changing the AMI on the Launch Config back to the original code. 
- D. Migrate to use AWS Elastic Beanstalk. Use the established and well-tested Rolling Deployment setting AWS provides on the new Application Environment, publishing a zip bundle of the new code and adjusting the wait period to spread the deployment over time. Re-deploy the old code bundle to rollback if needed.

<details><summary>Answer:</summary><p>
[A]

Categories:
[RDS, EC2, ASG, ELB, Elastic Beanstalk]

Explanation:

Question 2@http://jayendrapatil.com/aws-blue-green-deployment/

A: (Use Weighted Round Robin DNS Records and reverse proxies allow such fine-grained tuning of traffic splits. Blue-Green option does not meet the requirement that we mitigate costs and keep overall EC2 fleet size consistent, so we must select the 2 ELB and ASG option with WRR DNS tuning)

B: Full second stack is expensive

C: Cannot modify the existing launch config

</p></details><hr>

### Question 3:

When thinking of AWS Elastic Beanstalk, the ‘Swap Environment URLs’ feature most directly aids in what?

- A. Immutable Rolling Deployments
- B. Mutable Rolling Deployments
- C. Canary Deployments
- D. Blue-Green Deployments

<details><summary>Answer:</summary><p>
[D]

Categories:
[Elastic Beanstalk]

Explanation:

Question 3@http://jayendrapatil.com/aws-blue-green-deployment/

D: Complete switch from one environment to other

</p></details><hr>

### Question 4:

You were just hired as a DevOps Engineer for a startup. Your startup uses AWS for 100% of their infrastructure. They currently have no automation at all for deployment, and they have had many failures while trying to deploy to production. The company has told you deployment process risk mitigation is the most important thing now, and you have a lot of budget for tools and AWS resources. Their stack: 2-tier API Data stored in DynamoDB or S3, depending on type, Compute layer is EC2 in Auto Scaling Groups, They use Route53 for DNS pointing to an ELB, An ELB balances load across the EC2 instances. The scaling group properly varies between 4 and 12 EC2 servers. Which of the following approaches, given this company’s stack and their priorities, best meets the company’s needs?

- A. Model the stack in AWS Elastic Beanstalk as a single Application with multiple Environments. Use Elastic Beanstalk’s Rolling Deploy option to progressively roll out application code changes when promoting across environments. 
- B. Model the stack in 3 CloudFormation templates: Data layer, compute layer, and networking layer. Write stack deployment and integration testing automation following Blue-Green methodologies.
- C. Model the stack in AWS OpsWorks as a single Stack, with 1 compute layer and its associated ELB. Use Chef and App Deployments to automate Rolling Deployment. 
- D. Model the stack in 1 CloudFormation template, to ensure consistency and dependency graph resolution. Write deployment and integration testing automation following Rolling Deployment methodologies. 

<details><summary>Answer:</summary><p>
[B]

Categories:
[S3, SES, OpsWorks, EC2, ASG, CloudFormation, DynamoDB, ELB, Elastic Beanstalk]

Explanation:

Question 4@http://jayendrapatil.com/aws-blue-green-deployment/

A: Does not support DynamoDB also need Blue Green deployment for zero downtime deployment as cost is not a constraint

C: Does not support DynamoDB also need Blue Green deployment for zero downtime deployment as cost is not a constraint

D: Need Blue Green deployment for zero downtime deployment as cost is not a constraint

</p></details><hr>

### Question 5:

You are building out a layer in a software stack on AWS that needs to be able to scale out to react to increased demand as fast as possible. You are running the code on EC2 instances in an Auto Scaling Group behind an ELB. Which application code deployment method should you use?

- A. SSH into new instances those come online, and deploy new code onto the system by pulling it from an S3 bucket, which is populated by code that you refresh from source control on new pushes. 
- B. Bake an AMI when deploying new versions of code, and use that AMI for the Auto Scaling Launch Configuration.
- C. Create a Dockerfile when preparing to deploy a new version to production and publish it to S3. Use UserData in the Auto Scaling Launch configuration to pull down the Dockerfile from S3 and run it when new instances launch. 
- D. Create a new Auto Scaling Launch Configuration with UserData scripts configured to pull the latest code at all times. 

<details><summary>Answer:</summary><p>
[B]

Categories:
[S3, EC2, ASG, ELB]

Explanation:

Question 5@http://jayendrapatil.com/aws-blue-green-deployment/

A: is slow and manual

B: Pre baked AMIs can help to get started quickly

C: is slow

D: is slow

</p></details><hr>

### Question 6:

You company runs a complex customer relations management system that consists of around 10 different software components all backed by the same Amazon Relational Database (RDS) database. You adopted AWS OpsWorks to simplify management and deployment of that application and created an AWS OpsWorks stack with layers for each of the individual components. An internal security policy requires that all instances should run on the latest Amazon Linux AMI and that instances must be replaced within one month after the latest Amazon Linux AMI has been released. AMI replacements should be done without incurring application downtime or capacity problems. You decide to write a script to be run as soon as a new Amazon Linux AMI is released. Which solutions support the security policy and meet your requirements? Choose 2 answers

- A. Assign a custom recipe to each layer, which replaces the underlying AMI. Use AWS OpsWorks life-cycle events to incrementally execute this custom recipe and update the instances with the new AMI.
- B. Create a new stack and layers with identical configuration, add instances with the latest Amazon Linux AMI specified as a custom AMI to the new layer, switch DNS to the new stack, and tear down the old stack.
- C. Identify all Amazon Elastic Compute Cloud (EC2) instances of your AWS OpsWorks stack, stop each instance, replace the AMI ID property with the ID of the latest Amazon Linux AMI ID, and restart the instance. To avoid downtime, make sure not more than one instance is stopped at the same time.
- D. Specify the latest Amazon Linux AMI as a custom AMI at the stack level, terminate instances of the stack and let AWS OpsWorks launch new instances with the new AMI.
- E. Add new instances with the latest Amazon Linux AMI specified as a custom AMI to all AWS OpsWorks layers of your stack, and terminate the old ones.

<details><summary>Answer:</summary><p>
[B, E]

Categories:
[RDS, OpsWorks, EC2]

Explanation:

Question 6@http://jayendrapatil.com/aws-blue-green-deployment/

B: Blue-Green Deployment

</p></details><hr>

### Question 7:

Your company runs an event management SaaS application that uses Amazon EC2, Auto Scaling, Elastic Load Balancing, and Amazon RDS. Your software is installed on instances at first boot, using a tool such as Puppet or Chef, which you also use to deploy small software updates multiple times per week. After a major overhaul of your software, you roll out version 2.0 new, much larger version of the software of your running instances. Some of the instances are terminated during the update process. What actions could you take to prevent instances from being terminated in the future? (Choose two)

- A. Use the zero downtime feature of Elastic Beanstalk to deploy new software releases to your existing instances. 
- B. Use AWS CodeDeploy. Create an application and a deployment targeting the Auto Scaling group. Use CodeDeploy to deploy and update the application in the future.
- C. Run “aws autoscaling suspend-processes” before updating your application.
- D. Use the AWS Console to enable termination protection for the current instances. 
- E. Run “aws autoscaling detach-load-balancers” before updating your application. 

<details><summary>Answer:</summary><p>
[B, C]

Categories:
[SES, RDS, EC2, ASG, ELB, Elastic Beanstalk]

Explanation:

Question 7@http://jayendrapatil.com/aws-blue-green-deployment/

A: No such feature, you can perform environment url swap

B: https://aws.amazon.com/blogs/devops/under-the-hood-aws-codedeploy-and-auto-scaling-integration/

B: (Refer )

C: http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/terminating-instances.html#Using_ChangingDisableAPITermination

C: (Refer )

D: Termination protection does not work with Auto Scaling

E: Does not prevent Auto Scaling to terminate the instances

</p></details><hr>

