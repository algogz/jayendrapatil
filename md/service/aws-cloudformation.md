### Question 1:

What does Amazon CloudFormation provide?

- A. The ability to setup Autoscaling for Amazon EC2 instances.
- B. A templated resource creation for Amazon Web Services.
- C. A template to map network resources for Amazon Web Services
- D. None of these

<details><summary>Answer:</summary><p>
[B]

Categories:
[EC2, CloudFormation]

Explanation:

Question 1@http://jayendrapatil.com/aws-cloudformation/

</p></details><hr>

### Question 2:

A user is planning to use AWS CloudFormation for his automatic deployment requirements. Which of the below mentioned components are required as a part of the template?

- A. Parameters
- B. Outputs
- C. Template version
- D. Resources

<details><summary>Answer:</summary><p>
[D]

Categories:
[CloudFormation]

Explanation:

Question 2@http://jayendrapatil.com/aws-cloudformation/

</p></details><hr>

### Question 3:

In regard to AWS CloudFormation, what is a stack?

- A. Set of AWS templates that are created and managed as a template
- B. Set of AWS resources that are created and managed as a template
- C. Set of AWS resources that are created and managed as a single unit
- D. Set of AWS templates that are created and managed as a single unit

<details><summary>Answer:</summary><p>
[C]

Categories:
[CloudFormation]

Explanation:

Question 3@http://jayendrapatil.com/aws-cloudformation/

</p></details><hr>

### Question 4:

A large enterprise wants to adopt CloudFormation to automate administrative tasks and implement the security principles of least privilege and separation of duties. They have identified the following roles with the corresponding tasks in the company: (i) network administrators: create, modify and delete VPCs, subnets, NACLs, routing tables, and security groups (ii) application operators: deploy complete application stacks (ELB, Auto -Scaling groups, RDS) whereas all resources must be deployed in the VPCs managed by the network administrators (iii) Both groups must maintain their own CloudFormation templates and should be able to create, update and delete only their own CloudFormation stacks. The company has followed your advice to create two IAM groups, one for applications and one for networks. Both IAM groups are attached to IAM policies that grant rights to perform the necessary task of each group as well as the creation, update and deletion of CloudFormation stacks. Given setup and requirements, which statements represent valid design considerations? Choose 2 answers [PROFESSIONAL]

- A. Network stack updates will fail upon attempts to delete a subnet with EC2 instances
- B. Unless resource level permissions are used on the CloudFormation: DeleteStack action, network administrators could tear down application stacks 
- C. The application stack cannot be deleted before all network stacks are deleted 
- D. Restricting the launch of EC2 instances into VPCs requires resource level permissions in the IAM policy of the application group
- E. Nesting network stacks within application stacks simplifies management and debugging, but requires resource level permissions in the IAM policy of the network group 

<details><summary>Answer:</summary><p>
[A, D]

Categories:
[RDS, IAM, EC2, CloudFormation, VPC, ELB]

Explanation:

Question 4@http://jayendrapatil.com/aws-cloudformation/

A: Subnets cannot be deleted with instances in them

B: Network administrators themselves need permission to delete resources within the application stack & CloudFormation makes calls to create, modify, and delete those resources on their behalf

C: Application stack can be deleted before network stack

D: IAM permissions need to be given explicitly to launch instances

E: Although stacks can be nested, Network group will need to have all the application group permissions

</p></details><hr>

### Question 5:

Your team is excited about the use of AWS because now they have access to programmable infrastructure. You have been asked to manage your AWS infrastructure in a manner similar to the way you might manage application code. You want to be able to deploy exact copies of different versions of your infrastructure, stage changes into different environments, revert back to previous versions, and identify what versions are running at any particular time (development, test, QA, production). Which approach addresses this requirement?

- A. Use cost allocation reports and AWS Opsworks to deploy and manage your infrastructure.
- B. Use AWS CloudWatch metrics and alerts along with resource tagging to deploy and manage your infrastructure.
- C. Use AWS Beanstalk and a version control system like GIT to deploy and manage your infrastructure.
- D. Use AWS CloudFormation and a version control system like GIT to deploy and manage your infrastructure.

<details><summary>Answer:</summary><p>
[D]

Categories:
[SES, OpsWorks, CloudWatch, CloudFormation]

Explanation:

Question 5@http://jayendrapatil.com/aws-cloudformation/

</p></details><hr>

### Question 6:

A user is usingCloudFormation to launch an EC2 instance and then configure an application after the instance is launched. The user wants the stack creation of ELB and AutoScaling to wait until the EC2 instance is launched and configured properly. How can the user configure this?

- A. It is not possible that the stack creation will wait until one service is created and launched
- B. The user can use the HoldCondition resource to wait for the creation of the other dependent resources
- C. The user can use the DependentCondition resource to hold the creation of the other dependent resources
- D. The user can use the WaitCondition resource to hold the creation of the other dependent resources

<details><summary>Answer:</summary><p>
[D]

Categories:
[EC2, CloudFormation, ELB]

Explanation:

Question 6@http://jayendrapatil.com/aws-cloudformation/

</p></details><hr>

### Question 7:

A user has created a CloudFormation stack. The stack creates AWS services, such as EC2 instances, ELB, AutoScaling, and RDS. While creating the stack it created EC2, ELB and AutoScaling but failed to create RDS. What will CloudFormation do in this scenario?

- A. CloudFormation can never throw an error after launching a few services since it verifies all the steps before launching
- B. It will warn the user about the error and ask the user to manually create RDS
- C. Rollback all the changes and terminate all the created services
- D. It will wait for the user’s input about the error and correct the mistake after the input

<details><summary>Answer:</summary><p>
[C]

Categories:
[RDS, EC2, CloudFormation, ELB]

Explanation:

Question 7@http://jayendrapatil.com/aws-cloudformation/

</p></details><hr>

### Question 8:

A user is planning to use AWS CloudFormation. Which of the below mentioned functionalities does not help him to correctly understand CloudFormation?

- A. CloudFormation follows the DevOps model for the creation of Dev & Test
- B. AWS CloudFormation does not charge the user for its service but only charges for the AWS resources created with it
- C. CloudFormation works with a wide variety of AWS services, such as EC2, EBS, VPC, IAM, S3, RDS, ELB, etc
- D. CloudFormation provides a set of application bootstrapping scripts which enables the user to install Software

<details><summary>Answer:</summary><p>
[A]

Categories:
[S3, RDS, IAM, EC2, EBS, CloudFormation, VPC, ELB]

Explanation:

Question 8@http://jayendrapatil.com/aws-cloudformation/

</p></details><hr>

### Question 9:

A customer is using AWS for Dev and Test. The customer wants to setup the Dev environment with CloudFormation. Which of the below mentioned steps are not required while using CloudFormation?

- A. Create a stack
- B. Configure a service
- C. Create and upload the template
- D. Provide the parameters configured as part of the template

<details><summary>Answer:</summary><p>
[B]

Categories:
[CloudFormation]

Explanation:

Question 9@http://jayendrapatil.com/aws-cloudformation/

</p></details><hr>

### Question 10:

A marketing research company has developed a tracking system that collects user behavior during web marketing campaigns on behalf of their customers all over the world. The tracking system consists of an auto-scaled group of Amazon Elastic Compute Cloud (EC2) instances behind an elastic load balancer (ELB), and the collected data is stored in Amazon DynamoDB. After the campaign is terminated, the tracking system is torn down and the data is moved to Amazon Redshift, where it is aggregated, analyzed and used to generate detailed reports. The company wants to be able to instantiate new tracking systems in any region without any manual intervention and therefore adopted AWS CloudFormation. What needs to be done to make sure that the AWS CloudFormation template works in every AWS region? Choose 2 answers [PROFESSIONAL]

- A. IAM users with the right to start AWS CloudFormation stacks must be defined for every target region. 
- B. The names of the Amazon DynamoDB tables must be different in every target region. 
- C. Use the built-in function of AWS CloudFormation to set the AvailabilityZone attribute of the ELB resource.
- D. Avoid using DeletionPolicies for EBS snapshots. 
- E. Use the built-in Mappings and FindInMap functions of AWS CloudFormation to refer to the AMI ID set in the ImageId attribute of the Auto Scaling::LaunchConfiguration resource.

<details><summary>Answer:</summary><p>
[C, E]

Categories:
[IAM, EC2, ASG, EBS, CloudFormation, DynamoDB, ELB, Redshift]

Explanation:

Question 10@http://jayendrapatil.com/aws-cloudformation/

A: IAM users are global

B: DynamoDB names should be unique only within a region

D: Don’t want the data to be retained

</p></details><hr>

### Question 11:

A gaming company adopted AWS CloudFormation to automate load -testing of their games. They have created an AWS CloudFormation template for each gaming environment and one for the load -testing stack. The load – testing stack creates an Amazon Relational Database Service (RDS) Postgres database and two web servers running on Amazon Elastic Compute Cloud (EC2) that send HTTP requests, measure response times, and write the results into the database. A test run usually takes between 15 and 30 minutes. Once the tests are done, the AWS CloudFormation stacks are torn down immediately. The test results written to the Amazon RDS database must remain accessible for visualization and analysis. Select possible solutions that allow access to the test results after the AWS CloudFormation load -testing stack is deleted. Choose 2 answers. [PROFESSIONAL]

- A. Define a deletion policy of type Retain for the Amazon QDS resource to assure that the RDS database is not deleted with the AWS CloudFormation stack.
- B. Define a deletion policy of type Snapshot for the Amazon RDS resource to assure that the RDS database can be restored after the AWS CloudFormation stack is deleted.
- C. Define automated backups with a backup retention period of 30 days for the Amazon RDS database and perform point -in -time recovery of the database after the AWS CloudFormation stack is deleted. 
- D. Define an Amazon RDS Read-Replica in the load-testing AWS CloudFormation stack and define a dependency relation between master and replica via the DependsOn attribute. 
- E. Define an update policy to prevent deletion of the Amazon RDS database after the AWS CloudFormation stack is deleted. 

<details><summary>Answer:</summary><p>
[A, B]

Categories:
[RDS, EC2, CloudFormation]

Explanation:

Question 11@http://jayendrapatil.com/aws-cloudformation/

C: as the environment is required for limited time the automated backup will not serve the purpose

D: read replica not needed and will be deleted when the stack is deleted

E: UpdatePolicy does not apply to RDS

</p></details><hr>

### Question 12:

When working with AWS CloudFormation Templates what is the maximum number of stacks that you can create?

- A. 500
- B. 50
- C. 200
- D. 10

<details><summary>Answer:</summary><p>
[C]

Categories:
[CloudFormation]

Explanation:

Question 12@http://jayendrapatil.com/aws-cloudformation/

C: https://aws.amazon.com/cloudformation/faqs/

C: (Refer – The limit keeps on changing to check for the latest)

</p></details><hr>

### Question 13:

What happens, by default, when one of the resources in a CloudFormation stack cannot be created?

- A. Previously created resources are kept but the stack creation terminates
- B. Previously created resources are deleted and the stack creation terminates
- C. Stack creation continues, and the final results indicate which steps failed
- D. CloudFormation templates are parsed in advance so stack creation is guaranteed to succeed.

<details><summary>Answer:</summary><p>
[B]

Categories:
[CloudFormation]

Explanation:

Question 13@http://jayendrapatil.com/aws-cloudformation/

</p></details><hr>

### Question 14:

You need to deploy an AWS stack in a repeatable manner across multiple environments. You have selected CloudFormation as the right tool to accomplish this, but have found that there is a resource type you need to create and model, but is unsupported by CloudFormation. How should you overcome this challenge? [PROFESSIONAL]

- A. Use a CloudFormation Custom Resource Template by selecting an API call to proxy for create, update, and delete actions. CloudFormation will use the AWS SDK, CLI, or API method of your choosing as the state transition function for the resource type you are modeling.
- B. Submit a ticket to the AWS Forums. AWS extends CloudFormation Resource Types by releasing tooling to the AWS Labs organization on GitHub. Their response time is usually 1 day, and they complete requests within a week or two.
- C. Instead of depending on CloudFormation, use Chef, Puppet, or Ansible to author Heat templates, which are declarative stack resource definitions that operate over the OpenStack hypervisor and cloud environment.
- D. Create a CloudFormation Custom Resource Type by implementing create, update, and delete functionality, either by subscribing a Custom Resource Provider to an SNS topic, or by implementing the logic in AWS Lambda.

<details><summary>Answer:</summary><p>
[D]

Categories:
[CloudFormation, SNS, Lambda]

Explanation:

Question 14@http://jayendrapatil.com/aws-cloudformation/

D: http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-custom-resources.html

D: (Refer )

</p></details><hr>

### Question 15:

What is a circular dependency in AWS CloudFormation?

- A. When a Template references an earlier version of itself.
- B. When Nested Stacks depend on each other.
- C. When Resources form a DependOn loop.
- D. When a Template references a region, which references the original Template.

<details><summary>Answer:</summary><p>
[C]

Categories:
[CloudFormation]

Explanation:

Question 15@http://jayendrapatil.com/aws-cloudformation/

C: http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/troubleshooting.html#troubleshooting-errors-dependence-error

C: to resolve a dependency error, add a DependsOn attribute to resources that depend on other resources in the template. Some cases for e.g. EIP and VPC with IGW where EIP depends on IGW need explicitly declaration for the resources to be created in correct order

</p></details><hr>

### Question 16:

You need to run a very large batch data processing job one time per day. The source data exists entirely in S3, and the output of the processing job should also be written to S3 when finished. If you need to version control this processing job and all setup and teardown logic for the system, what approach should you use?

- A. Model an AWS EMR job in AWS Elastic Beanstalk. 
- B. Model an AWS EMR job in AWS CloudFormation.
- C. Model an AWS EMR job in AWS OpsWorks. 
- D. Model an AWS EMR job in AWS CLI Composer. 

<details><summary>Answer:</summary><p>
[B]

Categories:
[S3, OpsWorks, CloudFormation, EMR, Elastic Beanstalk]

Explanation:

Question 16@http://jayendrapatil.com/aws-cloudformation/

A: cannot directly model EMR Clusters

B: http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-emr-cluster.html

B: (EMR cluster can be modeled using CloudFormation. Refer )

C: cannot directly model EMR Clusters

D: does not exist

</p></details><hr>

### Question 17:

Your company needs to automate 3 layers of a large cloud deployment. You want to be able to track this deployment’s evolution as it changes over time, and carefully control any alterations. What is a good way to automate a stack to meet these requirements? [PROFESSIONAL]

- A. Use OpsWorks Stacks with three layers to model the layering in your stack.
- B. Use CloudFormation Nested Stack Templates, with three child stacks to represent the three logical layers of your cloud.
- C. Use AWS Config to declare a configuration set that AWS should roll out to your cloud.
- D. Use Elastic Beanstalk Linked Applications, passing the important DNS entries between layers using the metadata interface.

<details><summary>Answer:</summary><p>
[B]

Categories:
[OpsWorks, CloudFormation, Elastic Beanstalk]

Explanation:

Question 17@http://jayendrapatil.com/aws-cloudformation/

B: CloudFormation allows source controlled, declarative templates as the basis for stack automation and Nested Stacks help achieve clean separation of layers while simultaneously providing a method to control all layers at once when needed

</p></details><hr>

### Question 18:

You have been asked to de-risk deployments at your company. Specifically, the CEO is concerned about outages that occur because of accidental inconsistencies between Staging and Production, which sometimes cause unexpected behaviors in Production even when Staging tests pass. You already use Docker to get high consistency between Staging and Production for the application environment on your EC2 instances. How do you further de-risk the rest of the execution environment, since in AWS, there are many service components you may use beyond EC2 virtual machines? [PROFESSIONAL]

- A. Develop models of your entire cloud system in CloudFormation. Use this model in Staging and Production to achieve greater parity.
- B. Use AWS Config to force the Staging and Production stacks to have configuration parity. Any differences will be detected for you so you are aware of risks.
- C. Use AMIs to ensure the whole machine, including the kernel of the virual machines, is consistent, since Docker uses Linux Container (LXC) technology, and we need to make sure the container environment is consistent.
- D. Use AWS ECS and Docker clustering. This will make sure that the AMIs and machine sizes are the same across both environments.

<details><summary>Answer:</summary><p>
[A]

Categories:
[SES, ECS, EC2, CloudFormation]

Explanation:

Question 18@http://jayendrapatil.com/aws-cloudformation/

A: https://blogs.aws.amazon.com/application-management/blog/category/Best+practices

A: Only CloudFormation’s JSON Templates allow declarative version control of repeatedly deployable models of entire AWS clouds

</p></details><hr>

### Question 19:

Which code snippet below returns the URL of a load balanced web site created in CloudFormation with an AWS::ElasticLoadBalancing::LoadBalancer resource name “ElasticLoad Balancer”? [Developer]

- A. “Fn::Join” : [“”, [ “http://”, {“Fn::GetAtt” : [ “ElasticLoadBalancer”,”DNSName”]}]]
- B. “Fn::Join” : [“”,[ “http://”, {“Fn::GetAtt” : [ “ElasticLoadBalancer”,”Url”]}]]
- C. “Fn::Join” : [“”, [ “http://”, {“Ref” : “ElasticLoadBalancerUrl”}]]
- D. “Fn::Join” : [“”, [ “http://”, {“Ref” : “ElasticLoadBalancerDNSName”}]]

<details><summary>Answer:</summary><p>
[A]

Categories:
[CloudFormation]

Explanation:

Question 19@http://jayendrapatil.com/aws-cloudformation/

A: http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html

</p></details><hr>

### Question 20:

For AWS CloudFormation, which stack state refuses UpdateStack calls? [Developer]

- A. <code>UPDATE_ROLLBACK_FAILED</code>
- B. <code>UPDATE_ROLLBACK_COMPLETE</code>
- C. <code>UPDATE_COMPLETE</code>
- D. <code>CREATE_COMPLETE</code>

<details><summary>Answer:</summary><p>
[A]

Categories:
[SES, CloudFormation]

Explanation:

Question 20@http://jayendrapatil.com/aws-cloudformation/

A: http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-continueupdaterollback.html

</p></details><hr>

### Question 21:

Which of these is not a Pseudo Parameter in AWS CloudFormation? [Developer]

- A. AWS::StackName
- B. AWS::AccountId
- C. AWS::StackArn
- D. AWS::NotificationARNs

<details><summary>Answer:</summary><p>
[C]

Categories:
[CloudFormation]

Explanation:

Question 21@http://jayendrapatil.com/aws-cloudformation/

C: http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/pseudo-parameter-reference.html

</p></details><hr>

### Question 22:

Which of these is not an intrinsic function in AWS CloudFormation? [Developer]

- A. Fn::SplitValue
- B. Fn::FindInMap
- C. Fn::Select
- D. Fn::GetAZs

<details><summary>Answer:</summary><p>
[A]

Categories:
[CloudFormation]

Explanation:

Question 22@http://jayendrapatil.com/aws-cloudformation/

A: http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference.html

</p></details><hr>

### Question 23:

Which of these is not a CloudFormation Helper Script? [Developer]

- A. cfn-signal
- B. cfn-hup
- C. cfn-request
- D. cfn-get-metadata

<details><summary>Answer:</summary><p>
[C]

Categories:
[CloudFormation]

Explanation:

Question 23@http://jayendrapatil.com/aws-cloudformation/

C: http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-helper-scripts-reference.html

</p></details><hr>

### Question 24:

What method should I use to author automation if I want to wait for a CloudFormation stack to finish completing in a script? [Developer]

- A. Event subscription using SQS.
- B. Event subscription using SNS.
- C. Poll using <code>ListStacks</code> / <code>list-stacks</code>.
- D. Poll using <code>GetStackStatus</code> / <code>get-stack-status</code>. 

<details><summary>Answer:</summary><p>
[C]

Categories:
[SQS, CloudFormation, SNS]

Explanation:

Question 24@http://jayendrapatil.com/aws-cloudformation/

C: http://docs.aws.amazon.com/cli/latest/reference/cloudformation/list-stacks.html

C: Only polling will make a script wait to complete. ListStacks / list-stacks is a real method. Refer

D: GetStackStatus / get-stack-status does not exist

</p></details><hr>

### Question 25:

Which status represents a failure state in AWS CloudFormation? [Developer]

- A. <code>UPDATE_COMPLETE_CLEANUP_IN_PROGRESS</code> 
- B. <code>DELETE_COMPLETE_WITH_ARTIFACTS</code> 
- C. <code>ROLLBACK_IN_PROGRESS</code>
- D. <code>ROLLBACK_FAILED</code> 

<details><summary>Answer:</summary><p>
[C]

Categories:
[CloudFormation]

Explanation:

Question 25@http://jayendrapatil.com/aws-cloudformation/

A: UPDATE_COMPLETE_CLEANUP_IN_PROGRESS means an update was successful, and CloudFormation is deleting any replaced, no longer used resources

B: DELETE_COMPLETE_WITH_ARTIFACTS does not exist

C: http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks.html

C: ROLLBACK_IN_PROGRESS means an UpdateStack operation failed and the stack is in the process of trying to return to the valid, pre-update state Refer

D: ROLLBACK_FAILED is not a CloudFormation state but UPDATE_ROLLBACK_FAILED is

</p></details><hr>

### Question 26:

Which of these is not an intrinsic function in AWS CloudFormation? [Developer]

- A. Fn::Equals
- B. Fn::If
- C. Fn::Not
- D. Fn::Parse

<details><summary>Answer:</summary><p>
[D]

Categories:
[CloudFormation]

Explanation:

Question 26@http://jayendrapatil.com/aws-cloudformation/

D: http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference.html

D: Complete list of Intrinsic Functions: Fn::Base64, Fn::And, Fn::Equals, Fn::If, Fn::Not, Fn::Or, Fn::FindInMap, Fn::GetAtt, Fn::GetAZs, Fn::Join, Fn::Select, Refer

</p></details><hr>

### Question 27:

You need to create a Route53 record automatically in CloudFormation when not running in production during all launches of a Template. How should you implement this? [Developer]

- A. Use a <code>Parameter</code> for <code>environment</code>, and add a <code>Condition</code> on the Route53 <code>Resource</code> in the template to create the record only when <code>environment</code> is not <code>production</code>.
- B. Create two templates, one with the Route53 record value and one with a null value for the record. Use the one without it when deploying to production.
- C. Use a <code>Parameter</code> for <code>environment</code>, and add a <code>Condition</code> on the Route53 <code>Resource</code> in the template to create the record with a null string when <code>environment</code> is <code>production</code>.
- D. Create two templates, one with the Route53 record and one without it. Use the one without it when deploying to production.

<details><summary>Answer:</summary><p>
[A]

Categories:
[CloudFormation]

Explanation:

Question 27@http://jayendrapatil.com/aws-cloudformation/

A: http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/conditions-section-structure.html

A: Best way to do this is with one template, and a Condition on the resource. Route53 does not allow null strings for Refer

</p></details><hr>

