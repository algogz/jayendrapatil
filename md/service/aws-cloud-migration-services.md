### Question 1:

Your must architect the migration of a web application to AWS. The application consists of Linux web servers running a custom web server. You are required to save the logs generated from the application to a durable location. What options could you select to migrate the application to AWS? (Choose 2)

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

Question 1@http://jayendrapatil.com/aws-cloud-migration-services/

A: EB does not work with Custom server executable

B: although this is one of the option, the last sentence mentions configure the application to push the logs to S3, which would need changes to application as it needs to use SDK or CLI

C: Kinesis not needed

D: Use Docker configuration with awslogs and EB with Docker

E: Use VM Import/Export to create AMI and CloudWatch logs agent to log

</p></details><hr>

### Question 2:

Your company hosts an on-premises legacy engineering application with 900GB of data shared via a central file server. The engineering data consists of thousands of individual files ranging in size from megabytes to multiple gigabytes. Engineers typically modify 5-10 percent of the files a day. Your CTO would like to migrate this application to AWS, but only if the application can be migrated over the weekend to minimize user downtime. You calculate that it will take a minimum of 48 hours to transfer 900GB of data using your company’s existing 45-Mbps Internet connection. After replicating the application’s environment in AWS, which option will allow you to move the application’s data to AWS without losing any data and within the given timeframe?

- A. Copy the data to Amazon S3 using multiple threads and multi-part upload for large files over the weekend, and work in parallel with your developers to reconfigure the replicated application environment to leverage Amazon S3 to serve the engineering files. 
- B. Sync the application data to Amazon S3 starting a week before the migration, on Friday morning perform a final sync, and copy the entire data set to your AWS file server after the sync completes. 
- C. Copy the application data to a 1-TB USB drive on Friday and immediately send overnight, with Saturday delivery, the USB drive to AWS Import/Export to be imported as an EBS volume, mount the resulting EBS volume to your AWS file server on Sunday. 
- D. Leverage the AWS Storage Gateway to create a Gateway-Stored volume. On Friday copy the application data to the Storage Gateway volume. After the data has been copied, perform a snapshot of the volume and restore the volume as an EBS volume to be attached to your AWS file server on Sunday. 

<details><summary>Answer:</summary><p>
[]

Categories:
[S3, SES, Storage Gateway, EBS]

Explanation:

Question 2@http://jayendrapatil.com/aws-cloud-migration-services/

A: Still limited by 45 Mbps speed with minimum 48 hours when utilized to max

B: Works best as the data changes can be propagated over the week and are fractional and downtime would be know

C: Downtime is not known when the data upload would be done, although Amazon says the same day the package is received

D: Still uses the internet

</p></details><hr>

### Question 3:

You are tasked with moving a legacy application from a virtual machine running inside your datacenter to an Amazon VPC. Unfortunately this app requires access to a number of on-premises services and no one who configured the app still works for your company. Even worse there’s no documentation for it. What will allow the application running inside the VPC to reach back and access its internal dependencies without being reconfigured? (Choose 3 answers)

- A. An AWS Direct Connect link between the VPC and the network housing the internal services
- B. An Internet Gateway to allow a VPN connection. 
- C. An Elastic IP address on the VPC instance
- D. An IP address space that does not conflict with the one on-premises
- E. Entries in Amazon Route 53 that allow the Instance to resolve its dependencies’ IP addresses
- F. A VM Import of the current virtual machine

<details><summary>Answer:</summary><p>
[A, D, F]

Categories:
[SES, VPC, Route 53, Direct Connect]

Explanation:

Question 3@http://jayendrapatil.com/aws-cloud-migration-services/

B: Virtual and Customer gateway is needed

</p></details><hr>

