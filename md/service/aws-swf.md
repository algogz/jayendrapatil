### Question 1:

What does Amazon SWF stand for?

- A. Simple Web Flow
- B. Simple Work Flow
- C. Simple Wireless Forms
- D. Simple Web Form

<details><summary>Answer:</summary><p>
[B]

Categories:
[SWF]

Explanation:

Question 1@http://jayendrapatil.com/aws-swf/

</p></details><hr>

### Question 2:

Regarding Amazon SWF, the coordination logic in a workflow is contained in a software program called a ____.

- A. Handler
- B. Decider
- C. Coordinator
- D. Worker

<details><summary>Answer:</summary><p>
[B]

Categories:
[SWF]

Explanation:

Question 2@http://jayendrapatil.com/aws-swf/

</p></details><hr>

### Question 3:

For which of the following use cases are Simple Workflow Service (SWF) and Amazon EC2 an appropriate solution? Choose 2 answers

- A. Using as an endpoint to collect thousands of data points per hour from a distributed fleet of sensors
- B. Managing a multi-step and multi-decision checkout process of an e-commerce website
- C. Orchestrating the execution of distributed and auditable business processes
- D. Using as an SNS (Simple Notification Service) endpoint to trigger execution of video transcoding jobs
- E. Using as a distributed session store for your web application

<details><summary>Answer:</summary><p>
[B, C]

Categories:
[SES, SWF, EC2, EBS, SNS]

Explanation:

Question 3@http://jayendrapatil.com/aws-swf/

</p></details><hr>

### Question 4:

Amazon SWF is designed to help users…

- A. … Design graphical user interface interactions
- B. … Manage user identification and authorization
- C. … Store Web content
- D. … Coordinate synchronous and asynchronous tasks which are distributed and fault tolerant.

<details><summary>Answer:</summary><p>
[D]

Categories:
[SWF]

Explanation:

Question 4@http://jayendrapatil.com/aws-swf/

</p></details><hr>

### Question 5:

What does a “Domain” refer to in Amazon SWF?

- A. A security group in which only tasks inside can communicate with each other
- B. A special type of worker
- C. A collection of related Workflows
- D. The DNS record for the Amazon SWF service

<details><summary>Answer:</summary><p>
[C]

Categories:
[SWF]

Explanation:

Question 5@http://jayendrapatil.com/aws-swf/

</p></details><hr>

### Question 6:

Your company produces customer commissioned one-of-a-kind skiing helmets combining nigh fashion with custom technical enhancements Customers can show oft their Individuality on the ski slopes and have access to head-up-displays. GPS rear-view cams and any other technical innovation they wish to embed in the helmet. The current manufacturing process is data rich and complex including assessments to ensure that the custom electronics and materials used to assemble the helmets are to the highest standards Assessments are a mixture of human and automated assessments you need to add a new set of assessment to model the failure modes of the custom electronics using GPUs with CUD across a cluster of servers with low latency networking. What architecture would allow you to automate the existing process using a hybrid approach and ensure that the architecture can support the evolution of processes over time? [PROFESSIONAL]

- A. Use AWS Data Pipeline to manage movement of data & meta-data and assessments. Use an auto-scaling group of G2 instances in a placement group. 
- B. Use Amazon Simple Workflow (SWF) to manage assessments, movement of data & meta-data. Use an autoscaling group of G2 instances in a placement group. 
- C. Use Amazon Simple Workflow (SWF) to manage assessments movement of data & meta-data. Use an autoscaling group of C3 instances with SR-IOV (Single Root I/O Virtualization). 
- D. Use AWS data Pipeline to manage movement of data & meta-data and assessments use auto-scaling group of C3 with SR-IOV (Single Root I/O virtualization). 

<details><summary>Answer:</summary><p>
[]

Categories:
[SES, RDS, SWF]

Explanation:

Question 6@http://jayendrapatil.com/aws-swf/

A: Involves mixture of human assessments

B: Human and automated assessments with GPU and low latency networking

C: C3 and SR-IOV won’t provide GPU as well as Enhanced networking needs to be enabled

D: Involves mixture of human assessments

</p></details><hr>

### Question 7:

Your startup wants to implement an order fulfillment process for selling a personalized gadget that needs an average of 3-4 days to produce with some orders taking up to 6 months you expect 10 orders per day on your first day. 1000 orders per day after 6 months and 10,000 orders after 12 months. Orders coming in are checked for consistency men dispatched to your manufacturing plant for production quality control packaging shipment and payment processing. If the product does not meet the quality standards at any stage of the process employees may force the process to repeat a step Customers are notified via email about order status and any critical issues with their orders such as payment failure. Your case architecture includes AWS Elastic Beanstalk for your website with an RDS MySQL instance for customer data and orders. How can you implement the order fulfillment process while making sure that the emails are delivered reliably? [PROFESSIONAL]

- A. Add a business process management application to your Elastic Beanstalk app servers and re-use the ROS database for tracking order status use one of the Elastic Beanstalk instances to send emails to customers. 
- B. Use SWF with an Auto Scaling group of activity workers and a decider instance in another Auto Scaling group with min/max=1. Use the decider instance to send emails to customers. 
- C. Use SWF with an Auto Scaling group of activity workers and a decider instance in another Auto Scaling group with min/max=1. Use SES to send emails to customers.
- D. Use an SQS queue to manage all process tasks. Use an Auto Scaling group of EC2 Instances that poll the tasks and execute them. Use SES to send emails to customers. 

<details><summary>Answer:</summary><p>
[C]

Categories:
[SES, RDS, SWF, SQS, EC2, ASG, EBS, Elastic Beanstalk]

Explanation:

Question 7@http://jayendrapatil.com/aws-swf/

A: Would use a SWF instead of BPM

B: Decider sending emails might not be reliable

D: Does not provide an ability to repeat a step

</p></details><hr>

### Question 8:

Select appropriate use cases for SWF with Amazon EC2? (Choose 2)

- A. Video encoding using Amazon S3 and Amazon EC2. In this use case, large videos are uploaded to Amazon S3 in chunks. Application is built as a workflow where each video file is handled as one workflow execution.
- B. Processing large product catalogs using Amazon Mechanical Turk. While validating data in large catalogs, the products in the catalog are processed in batches. Different batches can be processed concurrently.
- C. Order processing system with Amazon EC2, SQS, and SimpleDB. Use SWF notifications to orchestrate an order processing system running on EC2, where notifications sent over HTTP can trigger real-time processing in related components such as an inventory system or a shipping service.
- D. Using as an SQS (Simple Queue Service) endpoint to trigger execution of video transcoding jobs.

<details><summary>Answer:</summary><p>
[A, B]

Categories:
[S3, SES, SWF, SQS, EC2]

Explanation:

Question 8@http://jayendrapatil.com/aws-swf/

</p></details><hr>

### Question 9:

When you register an activity in Amazon SWF, you provide the following information, except:

- A. a name
- B. timeout values
- C. a domain
- D. version

<details><summary>Answer:</summary><p>
[C]

Categories:
[SWF]

Explanation:

Question 9@http://jayendrapatil.com/aws-swf/

</p></details><hr>

### Question 10:

Regarding Amazon SWF, at times you might want to record information in the workflow history of a workflow execution that is specific to your use case. ____ enable you to record information in the workflow execution history that you can use for any custom or scenario-specific purpose.

- A. Markers
- B. Tags
- C. Hash keys
- D. Events

<details><summary>Answer:</summary><p>
[A]

Categories:
[SWF]

Explanation:

Question 10@http://jayendrapatil.com/aws-swf/

</p></details><hr>

### Question 11:

Which of the following statements about SWF are true? Choose 3 answers.

- A. SWF tasks are assigned once and never duplicated
- B. SWF requires an S3 bucket for workflow storage
- C. SWF workflow executions can last up to a year
- D. SWF triggers SNS notifications on task assignment
- E. SWF uses deciders and workers to complete tasks
- F. SWF requires at least 1 EC2 instance per domain

<details><summary>Answer:</summary><p>
[A, C, E]

Categories:
[S3, SES, SWF, EC2, SNS]

Explanation:

Question 11@http://jayendrapatil.com/aws-swf/

</p></details><hr>

