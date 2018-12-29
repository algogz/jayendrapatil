### Question 1:

You are working with a customer who is using Chef configuration management in their data center. Which service is designed to let the customer leverage existing Chef recipes in AWS?

- A. Amazon Simple Workflow Service
- B. AWS Elastic Beanstalk
- C. AWS CloudFormation
- D. AWS OpsWorks

<details><summary>Answer:</summary><p>
[D]

Categories:
[OpsWorks, SWF, CloudFormation, Elastic Beanstalk]

Explanation:

Question 1@http://jayendrapatil.com/aws-opsworks/

</p></details><hr>

### Question 2:

Your mission is to create a lights-out datacenter environment, and you plan to use AWS OpsWorks to accomplish this. First you created a stack and added an App Server layer with an instance running in it. Next you added an application to the instance, and now you need to deploy a MySQL RDS database instance. Which of the following answers accurately describe how to add a backend database server to an OpsWorks stack? Choose 3 answers

- A. Add a new database layer and then add recipes to the deploy actions of the database and App Server layers.
- B. Use OpsWorks’ “Clone Stack” feature to create a second RDS stack in another Availability Zone for redundancy in the event of a failure in the Primary AZ. To switch to the secondary RDS instance, set the [:database] attributes to values that are appropriate for your server which you can do by using custom JSON.
- C. The variables that characterize the RDS database connection—host, user, and so on—are set using the corresponding values from the deploy JSON’s [:deploy][:app_name][:database] attributes.
- D. Cookbook attributes are stored in a repository, so OpsWorks requires that the “password”: “your_password” attribute for the RDS instance must be encrypted using at least a 256-bit key.
- E. Set up the connection between the app server and the RDS layer by using a custom recipe. The recipe configures the app server as required, typically by creating a configuration file. The recipe gets the connection data such as the host and database name from a set of attributes in the stack configuration and deployment JSON that AWS OpsWorks installs on every instance.

<details><summary>Answer:</summary><p>
[A, C, E]

Categories:
[RDS, OpsWorks]

Explanation:

Question 2@http://jayendrapatil.com/aws-opsworks/

A: http://docs.aws.amazon.com/opsworks/latest/userguide/customizing-rds.html

C: http://docs.aws.amazon.com/opsworks/latest/userguide/customizing-rds.html

E: http://docs.aws.amazon.com/opsworks/latest/userguide/customizing-rds.html

</p></details><hr>

### Question 3:

You are tasked with the migration of a highly trafficked node.js application to AWS. In order to comply with organizational standards Chef recipes must be used to configure the application servers that host this application and to support application lifecycle events. Which deployment option meets these requirements while minimizing administrative burden?

- A. Create a new stack within Opsworks add the appropriate layers to the stack and deploy the application
- B. Create a new application within Elastic Beanstalk and deploy this application to a new environment 
- C. Launch a Node JS server from a community AMI and manually deploy the application to the launched EC2 instance
- D. Launch and configure Chef Server on an EC2 instance and leverage the AWS CLI to launch application servers and configure those instances using Chef.

<details><summary>Answer:</summary><p>
[A]

Categories:
[RDS, OpsWorks, EC2, Elastic Beanstalk]

Explanation:

Question 3@http://jayendrapatil.com/aws-opsworks/

B: need to comply with chef recipes

</p></details><hr>

### Question 4:

A web-startup runs its very successful social news application on Amazon EC2 with an Elastic Load Balancer, an Auto-Scaling group of Java/Tomcat application-servers, and DynamoDB as data store. The main web application best runs on m2.xlarge instances since it is highly memory- bound. Each new deployment requires semi-automated creation and testing of a new AMI for the application servers which takes quite a while and is therefore only done once per week. Recently, a new chat feature has been implemented in node.js and waits to be integrated in the architecture. First tests show that the new component is CPU bound Because the company has some experience with using Chef, they decided to streamline the deployment process and use AWS OpsWorks as an application life cycle tool to simplify management of the application and reduce the deployment cycles. What configuration in AWS OpsWorks is necessary to integrate the new chat module in the most cost-efficient and flexible way?

- A. Create one AWS Ops Works stack, create one AWS Ops Works layer, create one custom recipe
- B. Create one AWS Ops Works stack, create two AWS Ops Works layers create one custom recipe
- C. Create two AWS Ops Works stacks, create two AWS Ops Works layers create one custom recipe
- D. Create two AWS Ops Works stacks, create two AWS Ops Works layers create two custom recipe

<details><summary>Answer:</summary><p>
[B]

Categories:
[OpsWorks, EC2, DynamoDB]

Explanation:

Question 4@http://jayendrapatil.com/aws-opsworks/

B: http://docs.aws.amazon.com/opsworks/latest/userguide/other-services.html

B: Single environment stack, two layers for java and node.js application using built-in recipes and custom recipe for DynamoDB connectivity only as other configuration. Refer

</p></details><hr>

### Question 5:

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

Question 5@http://jayendrapatil.com/aws-opsworks/

B: Blue-Green Deployment

D: Will lead to downtime

</p></details><hr>

### Question 6:

When thinking of AWS OpsWorks, which of the following is not an instance type you can allocate in a stack layer?

- A. 24/7 instances (24/7 instances are supported and started manually and run until you stop them)
- B. Spot instances
- C. Time-based instances (Time-based instances are run by AWS OpsWorks on a specified daily and weekly schedule)
- D. Load-based instances (Load-based instances are automatically started and stopped by AWS OpsWorks, based on specified load metrics, such as CPU utilization)

<details><summary>Answer:</summary><p>
[B]

Categories:
[OpsWorks]

Explanation:

Question 6@http://jayendrapatil.com/aws-opsworks/

B: https://forums.aws.amazon.com/thread.jspa?threadID=117372

B: (Does not support spot instance directly but can be used with auto scaling Refer )

</p></details><hr>

### Question 7:

Which of the following tools does not directly support AWS OpsWorks, for monitoring your stacks?

- A. AWS Config
- B. Amazon CloudWatch Metrics 
- C. AWS CloudTrail 
- D. Amazon CloudWatch Logs 

<details><summary>Answer:</summary><p>
[A]

Categories:
[OpsWorks, CloudWatch, CloudTrail]

Explanation:

Question 7@http://jayendrapatil.com/aws-opsworks/

A: http://docs.aws.amazon.com/opsworks/latest/userguide/monitoring.html

B: AWS OpsWorks uses CloudWatch to provide thirteen custom metrics with detailed monitoring for each instance in the stack

C: AWS OpsWorks integrates with CloudTrail to log every AWS OpsWorks API call and store the data in an S3 bucket

D: You can use Amazon CloudWatch Logs to monitor your stack’s system, application, and custom logs.

</p></details><hr>

### Question 8:

When thinking of AWS OpsWorks, which of the following is true?

- A. Stacks have many layers, layers have many instances.
- B. Instances have many stacks, stacks have many layers.
- C. Layers have many stacks, stacks have many instances.
- D. Layers have many instances, instances have many stacks.

<details><summary>Answer:</summary><p>
[A]

Categories:
[OpsWorks]

Explanation:

Question 8@http://jayendrapatil.com/aws-opsworks/

</p></details><hr>

