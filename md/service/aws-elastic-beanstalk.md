### Question 1:

An organization is planning to use AWS for their production roll out. The organization wants to implement automation for deployment such that it will automatically create a LAMP stack, download the latest PHP installable from S3 and setup the ELB. Which of the below mentioned AWS services meets the requirement for making an orderly deployment of the software?

- A. AWS Elastic Beanstalk
- B. AWS CloudFront
- C. AWS CloudFormation
- D. AWS DevOps

<details><summary>Answer:</summary><p>
[A]

Categories:
[S3, CloudFront, CloudFormation, ELB, Elastic Beanstalk]

Explanation:

Question 1@http://jayendrapatil.com/aws-elastic-beanstalk/

</p></details><hr>

### Question 2:

What does Amazon Elastic Beanstalk provide?

- A. A scalable storage appliance on top of Amazon Web Services.
- B. An application container on top of Amazon Web Services
- C. A service by this name doesn’t exist.
- D. A scalable cluster of EC2 instances

<details><summary>Answer:</summary><p>
[B]

Categories:
[EC2, Elastic Beanstalk]

Explanation:

Question 2@http://jayendrapatil.com/aws-elastic-beanstalk/

</p></details><hr>

### Question 3:

You want to have multiple versions of your application running at the same time, with all versions launched via AWS Elastic Beanstalk. Is this possible?

- A. However if you have 2 AWS accounts this can be done
- B. AWS Elastic Beanstalk is not designed to support multiple running environments
- C. AWS Elastic Beanstalk is designed to support a number of multiple running environments
- D. However AWS Elastic Beanstalk is designed to support only 2 multiple running environments

<details><summary>Answer:</summary><p>
[C]

Categories:
[Elastic Beanstalk]

Explanation:

Question 3@http://jayendrapatil.com/aws-elastic-beanstalk/

</p></details><hr>

### Question 4:

A .NET application that you manage is running in Elastic Beanstalk. Your developers tell you they will need access to application log files to debug issues that arise. The infrastructure will scale up and down. How can you ensure the developers will be able to access only the log files?

- A. Access the log files directly from Elastic Beanstalk
- B. Enable log file rotation to S3 within the Elastic Beanstalk configuration
- C. Ask your developers to enable log file rotation in the applications web.config file
- D. Connect to each Instance launched by Elastic Beanstalk and create a Windows Scheduled task to rotate the log files to S3

<details><summary>Answer:</summary><p>
[B]

Categories:
[S3, Elastic Beanstalk]

Explanation:

Question 4@http://jayendrapatil.com/aws-elastic-beanstalk/

</p></details><hr>

### Question 5:

Your team has a tomcat-based Java application you need to deploy into development, test and production environments. After some research, you opt to use Elastic Beanstalk due to its tight integration with your developer tools and RDS due to its ease of management. Your QA team lead points out that you need to roll a sanitized set of production data into your environment on a nightly basis. Similarly, other software teams in your org want access to that same restored data via their EC2 instances in your VPC .The optimal setup for persistence and security that meets the above requirements would be the following. [PROFESSIONAL]

- A. Create your RDS instance as part of your Elastic Beanstalk definition and alter its security group to allow access to it from hosts in your application subnets. 
- B. Create your RDS instance separately and add its IP address to your application’s DB connection strings in your code. Alter its security group to allow access to it from hosts within your VPC’s IP address block. 
- C. Create your RDS instance separately and pass its DNS name to your app’s DB connection string as an environment variable. Create a security group for client machines and add it as a valid source for DB traffic to the security group of the RDS instance itself.
- D. Create your RDS instance separately and pass its DNS name to your DB connection string as an environment variable. Alter its security group to allow access to it from hosts in your application subnets. 

<details><summary>Answer:</summary><p>
[C]

Categories:
[RDS, EC2, VPC, Elastic Beanstalk]

Explanation:

Question 5@http://jayendrapatil.com/aws-elastic-beanstalk/

A: Not optimal for persistence as the RDS is associated with the Elastic Beanstalk lifecycle and would not live independently

B: RDS is connected using DNS endpoint only

C: Security group allows instances to access the RDS with new instances launched without any changes

D: Not optimal for security adding individual hosts

</p></details><hr>

### Question 6:

Your must architect the migration of a web application to AWS. The application consists of Linux web servers running a custom web server. You are required to save the logs generated from the application to a durable location. What options could you select to migrate the application to AWS? (Choose 2) [PROFESSIONAL]

- A. Create an AWS Elastic Beanstalk application using the custom web server platform. Specify the web server executable and the application project and source files. Enable log file rotation to Amazon Simple Storage Service (S3). 
- B. Create Dockerfile for the application. Create an AWS OpsWorks stack consisting of a custom layer. Create custom recipes to install Docker and to deploy your Docker container using the Dockerfile. Create custom recipes to install and configure the application to publish the logs to Amazon CloudWatch Logs 
- C. Create Dockerfile for the application. Create an AWS OpsWorks stack consisting of a Docker layer that uses the Dockerfile. Create custom recipes to install and configure Amazon Kinesis to publish the logs into Amazon CloudWatch. 
- D. Create a Dockerfile for the application. Create an AWS Elastic Beanstalk application using the Docker platform and the Dockerfile. Enable logging the Docker configuration to automatically publish the application logs. Enable log file rotation to Amazon S3.
- E. Use VM import/Export to import a virtual machine image of the server into AWS as an AMI. Create an Amazon Elastic Compute Cloud (EC2) instance from AMI, and install and configure the Amazon CloudWatch Logs agent. Create a new AMI from the instance. Create an AWS Elastic Beanstalk application using the AMI platform and the new AMI.

<details><summary>Answer:</summary><p>
[D, E]

Categories:
[S3, SES, OpsWorks, EC2, CloudWatch, Kinesis, Elastic Beanstalk]

Explanation:

Question 6@http://jayendrapatil.com/aws-elastic-beanstalk/

A: EB does not work with Custom server executable

B: although this is one of the option, the last sentence mentions configure the application to push the logs to S3, which would need changes to application as it needs to use SDK or CLI

C: Kinesis not needed

D: Use Docker configuration with awslogs and EB with Docker

E: Use VM Import/Export to create AMI and CloudWatch logs agent to log

</p></details><hr>

### Question 7:

Which of the following groups is AWS Elastic Beanstalk best suited for?

- A. Those who want to deploy and manage their applications within minutes in the AWS cloud.
- B. Those who want to privately store and manage Git repositories in the AWS cloud.
- C. Those who want to automate the deployment of applications to instances and to update the applications as required.
- D. Those who want to model, visualize, and automate the steps required to release software.

<details><summary>Answer:</summary><p>
[A]

Categories:
[Elastic Beanstalk]

Explanation:

Question 7@http://jayendrapatil.com/aws-elastic-beanstalk/

</p></details><hr>

### Question 8:

When thinking of AWS Elastic Beanstalk’s model, which is true?

- A. Applications have many deployments, deployments have many environments.
- B. Environments have many applications, applications have many deployments.
- C. Applications have many environments, environments have many deployments.
- D. Deployments have many environments, environments have many applications.

<details><summary>Answer:</summary><p>
[C]

Categories:
[Elastic Beanstalk]

Explanation:

Question 8@http://jayendrapatil.com/aws-elastic-beanstalk/

C: (Applications group logical services. Environments belong to Applications, and typically represent different deployment levels (dev, stage, prod, forth). Deployments belong to environments, and are pushes of bundles of code for the environments to run.)

</p></details><hr>

### Question 9:

If you’re trying to configure an AWS Elastic Beanstalk worker tier for easy debugging if there are problems finishing queue jobs, what should you configure?

- A. Configure Rolling Deployments.
- B. Configure Enhanced Health Reporting
- C. Configure Blue-Green Deployments.
- D. Configure a Dead Letter Queue

<details><summary>Answer:</summary><p>
[D]

Categories:
[Elastic Beanstalk]

Explanation:

Question 9@http://jayendrapatil.com/aws-elastic-beanstalk/

D: http://docs.aws.amazon.com/elasticbeanstalk/latest/dg/using-features-managing-env-tiers.html#worker-deadletter

D: (Elastic Beanstalk worker environments support SQS dead letter queues, where worker can send messages that for some reason could not be successfully processed. Dead letter queue provides the ability to sideline, isolate and analyze the unsuccessfully processed messages. Refer )

</p></details><hr>

### Question 10:

When thinking of AWS Elastic Beanstalk, which statement is true?

- A. Worker tiers pull jobs from SNS.
- B. Worker tiers pull jobs from HTTP.
- C. Worker tiers pull jobs from JSON.
- D. Worker tiers pull jobs from SQS.

<details><summary>Answer:</summary><p>
[D]

Categories:
[SQS, SNS, Elastic Beanstalk]

Explanation:

Question 10@http://jayendrapatil.com/aws-elastic-beanstalk/

D: http://docs.aws.amazon.com/elasticbeanstalk/latest/dg/using-features-managing-env-tiers.html

D: (Elastic Beanstalk installs a daemon on each EC2 instance in the Auto Scaling group to process SQS messages in the worker environment. Refer )

</p></details><hr>

### Question 11:

You are building a Ruby on Rails application for internal, non-production use, which uses MySQL as a database. You want developers without very much AWS experience to be able to deploy new code with a single command line push. You also want to set this up as simply as possible. Which tool is ideal for this setup?

- A. AWS CloudFormation
- B. AWS OpsWorks
- C. AWS ELB + EC2 with CLI Push
- D. AWS Elastic Beanstalk

<details><summary>Answer:</summary><p>
[D]

Categories:
[SES, OpsWorks, EC2, CloudFormation, ELB, Elastic Beanstalk]

Explanation:

Question 11@http://jayendrapatil.com/aws-elastic-beanstalk/

</p></details><hr>

### Question 12:

What AWS products and features can be deployed by Elastic Beanstalk? Choose 3 answers.

- A. Auto scaling groups
- B. Route 53 hosted zones
- C. Elastic Load Balancers
- D. RDS Instances
- E. Elastic IP addresses
- F. SQS Queues

<details><summary>Answer:</summary><p>
[A, C, D]

Categories:
[SES, RDS, SQS, ASG, Route 53, Elastic Beanstalk]

Explanation:

Question 12@http://jayendrapatil.com/aws-elastic-beanstalk/

</p></details><hr>

### Question 13:

AWS Elastic Beanstalk stores your application files and optionally server log files in ____.

- A. Amazon Storage Gateway
- B. Amazon Glacier
- C. Amazon EC2
- D. Amazon S3

<details><summary>Answer:</summary><p>
[D]

Categories:
[S3, Glacier, EC2, Storage Gateway, Elastic Beanstalk]

Explanation:

Question 13@http://jayendrapatil.com/aws-elastic-beanstalk/

</p></details><hr>

### Question 14:

When you use the AWS Elastic Beanstalk console to deploy a new application ____.

- A. Need to upload each file separately
- B. Need to create each file and path
- C. Need to upload a source bundle
- D. Need to create each file

<details><summary>Answer:</summary><p>
[C]

Categories:
[Elastic Beanstalk]

Explanation:

Question 14@http://jayendrapatil.com/aws-elastic-beanstalk/

</p></details><hr>

