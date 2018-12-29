### Question 1:

If I want my instance to run on a single-tenant hardware, which value do I have to set the instance’s tenancy attribute to?

- A. dedicated
- B. isolated
- C. one
- D. reserved

<details><summary>Answer:</summary><p>
[A]

Categories:
[]

Explanation:

Question 1@http://jayendrapatil.com/aws-ec2-instance-purchasing-option/

</p></details><hr>

### Question 2:

You have a video transcoding application running on Amazon EC2. Each instance polls a queue to find out which video should be transcoded, and then runs a transcoding process. If this process is interrupted, the video will be transcoded by another instance based on the queuing system. You have a large backlog of videos, which need to be transcoded, and would like to reduce this backlog by adding more instances. You will need these instances only until the backlog is reduced. Which type of Amazon EC2 instances should you use to reduce the backlog in the most cost efficient way?

- A. Reserved instances
- B. Spot instances
- C. Dedicated instances
- D. On-demand instances

<details><summary>Answer:</summary><p>
[B]

Categories:
[EC2]

Explanation:

Question 2@http://jayendrapatil.com/aws-ec2-instance-purchasing-option/

</p></details><hr>

### Question 3:

The one-time payment for Reserved Instances is __________ refundable if the reservation is cancelled.

- A. always
- B. in some circumstances
- C. never

<details><summary>Answer:</summary><p>
[C]

Categories:
[]

Explanation:

Question 3@http://jayendrapatil.com/aws-ec2-instance-purchasing-option/

</p></details><hr>

### Question 4:

You run a web application where web servers on EC2 Instances are In an Auto Scaling group Monitoring over the last 6 months shows that 6 web servers are necessary to handle the minimum load. During the day up to 12 servers are needed Five to six days per year, the number of web servers required might go up to 15. What would you recommend to minimize costs while being able to provide hill availability?

- A. 6 Reserved instances (heavy utilization). 6 Reserved instances (medium utilization), rest covered by On-Demand instances
- B. 6 Reserved instances (heavy utilization). 6 On-Demand instances, rest covered by Spot Instances
- C. 6 Reserved instances (heavy utilization) 6 Spot instances, rest covered by On-Demand instances
- D. 6 Reserved instances (heavy utilization) 6 Reserved instances (medium utilization) rest covered by Spot instances

<details><summary>Answer:</summary><p>
[A]

Categories:
[EC2, ASG]

Explanation:

Question 4@http://jayendrapatil.com/aws-ec2-instance-purchasing-option/

B: (don’t go for spot as availability not guaranteed)

C: (don’t go for spot as availability not guaranteed)

D: (don’t go for spot as availability not guaranteed)

</p></details><hr>

### Question 5:

A user is running one instance for only 3 hours every day. The user wants to save some cost with the instance. Which of the below mentioned Reserved Instance categories is advised in this case?

- A. The user should not use RI; instead only go with the on-demand pricing
- B. The user should use the AWS high utilized RI
- C. The user should use the AWS medium utilized RI
- D. The user should use the AWS low utilized RI

<details><summary>Answer:</summary><p>
[A]

Categories:
[]

Explanation:

Question 5@http://jayendrapatil.com/aws-ec2-instance-purchasing-option/

A: (seems question before the introduction of the Scheduled Reserved instances in Jan 2016, which can be used in this case)

</p></details><hr>

### Question 6:

Which of the following are characteristics of a reserved instance? Choose 3 answers (but 4 answers seem correct)

- A. It can be migrated across Availability Zones
- B. It is specific to an Amazon Machine Image (AMI)
- C. It can be applied to instances launched by Auto Scaling
- D. It is specific to an instance Type
- E. It can be used to lower Total Cost of Ownership (TCO) of a system

<details><summary>Answer:</summary><p>
[A, C, E]

Categories:
[ASG]

Explanation:

Question 6@http://jayendrapatil.com/aws-ec2-instance-purchasing-option/

A: (can be modified)

B: (specific to platform)

C: (are allowed)

D: (specific to instance family but instance type can be changed) ( specific to instance family but instance type can be changed )

E: (helps to reduce cost)

</p></details><hr>

### Question 7:

You have a distributed application that periodically processes large volumes of data across multiple Amazon EC2 Instances. The application is designed to recover gracefully from Amazon EC2 instance failures. You are required to accomplish this task in the most cost-effective way. Which of the following will meet your requirements?

- A. Spot Instances
- B. Reserved instances
- C. Dedicated instances
- D. On-Demand instances

<details><summary>Answer:</summary><p>
[A]

Categories:
[SES, EC2]

Explanation:

Question 7@http://jayendrapatil.com/aws-ec2-instance-purchasing-option/

</p></details><hr>

### Question 8:

Can I move a Reserved Instance from one Region to another?

- A. No
- B. Only if they are moving into GovCloud
- C. Yes
- D. Only if they are moving to US East from another region

<details><summary>Answer:</summary><p>
[A]

Categories:
[]

Explanation:

Question 8@http://jayendrapatil.com/aws-ec2-instance-purchasing-option/

</p></details><hr>

### Question 9:

An application you maintain consists of multiple EC2 instances in a default tenancy VPC. This application has undergone an internal audit and has been determined to require dedicated hardware for one instance. Your compliance team has given you a week to move this instance to single-tenant hardware. Which process will have minimal impact on your application while complying with this requirement?

- A. Create a new VPC with tenancy=dedicated and migrate to the new VPC
- B. Use ec2-reboot-instances command line and set the parameter “dedicated=true”
- C. Right click on the instance, select properties and check the box for dedicated tenancy
- D. Stop the instance, create an AMI, launch a new instance with tenancy=dedicated, and terminate the old instance

<details><summary>Answer:</summary><p>
[D]

Categories:
[EC2, VPC]

Explanation:

Question 9@http://jayendrapatil.com/aws-ec2-instance-purchasing-option/

A: (possible but impact not minimal)

</p></details><hr>

### Question 10:

Your department creates regular analytics reports from your company’s log files. All log data is collected in Amazon S3 and processed by daily Amazon Elastic Map Reduce (EMR) jobs that generate daily PDF reports and aggregated tables in CSV format for an Amazon Redshift data warehouse. Your CFO requests that you optimize the cost structure for this system. Which of the following alternatives will lower costs without compromising average performance of the system or data integrity for the raw data? [PROFESSIONAL]

- A. Use reduced redundancy storage (RRS) for PDF and CSV data in Amazon S3. Add Spot instances to Amazon EMR jobs. Use Reserved Instances for Amazon Redshift. 
- B. Use reduced redundancy storage (RRS) for all data in S3. Use a combination of Spot instances and Reserved Instances for Amazon EMR jobs. Use Reserved instances for Amazon Redshift
- C. Use reduced redundancy storage (RRS) for all data in Amazon S3. Add Spot Instances to Amazon EMR jobs. Use Reserved Instances for Amazon Redshift 
- D. Use reduced redundancy storage (RRS) for PDF and CSV data in S3. Add Spot Instances to EMR jobs. Use Spot Instances for Amazon Redshift. 

<details><summary>Answer:</summary><p>
[B]

Categories:
[S3, EMR, Redshift]

Explanation:

Question 10@http://jayendrapatil.com/aws-ec2-instance-purchasing-option/

A: Spot instances impacts performance

B: Combination of the Spot and reserved with guarantee performance and help reduce cost. Also, RRS would reduce cost and guarantee data integrity, which is different from data durability

C: Spot instances impacts performance

D: Spot instances impacts performance

</p></details><hr>

### Question 11:

A research scientist is planning for the one-time launch of an Elastic MapReduce cluster and is encouraged by her manager to minimize the costs. The cluster is designed to ingest 200TB of genomics data with a total of 100 Amazon EC2 instances and is expected to run for around four hours. The resulting data set must be stored temporarily until archived into an Amazon RDS Oracle instance. Which option will help save the most money while meeting requirements? [PROFESSIONAL]

- A. Store ingest and output files in Amazon S3. Deploy on-demand for the master and core nodes and spot for the task nodes.
- B. Optimize by deploying a combination of on-demand, RI and spot-pricing models for the master, core and task nodes. Store ingest and output files in Amazon S3 with a lifecycle policy that archives them to Amazon Glacier. 
- C. Store the ingest files in Amazon S3 RRS and store the output files in S3. Deploy Reserved Instances for the master and core nodes and on-demand for the task nodes. 
- D. Deploy on-demand master, core and task nodes and store ingest and output files in Amazon S3 RRS 

<details><summary>Answer:</summary><p>
[A]

Categories:
[S3, RDS, Glacier, EC2]

Explanation:

Question 11@http://jayendrapatil.com/aws-ec2-instance-purchasing-option/

B: Reserved Instance not cost effective for 4 hour job and data not needed in S3 once moved to RDS

C: Reserved Instance not cost effective

D: RRS provides not much cost benefits for a 4 hour job while the amount of input data would take time to upload and Output data to reproduce

</p></details><hr>

### Question 12:

A company currently has a highly available web application running in production. The application’s web front-end utilizes an Elastic Load Balancer and Auto scaling across 3 availability zones. During peak load, your web servers operate at 90% utilization and leverage a combination of heavy utilization reserved instances for steady state load and on-demand and spot instances for peak load. You are asked with designing a cost effective architecture to allow the application to recover quickly in the event that an availability zone is unavailable during peak load. Which option provides the most cost effective high availability architectural design for this application? [PROFESSIONAL]

- A. Increase auto scaling capacity and scaling thresholds to allow the web-front to cost-effectively scale across all availability zones to lower aggregate utilization levels that will allow an availability zone to fail during peak load without affecting the applications availability.
- B. Continue to run your web front-end at 90% utilization, but purchase an appropriate number of utilization RIs in each availability zone to cover the loss of any of the other availability zones during peak load. 
- C. Continue to run your web front-end at 90% utilization, but leverage a high bid price strategy to cover the loss of any of the other availability zones during peak load. 
- D. Increase use of spot instances to cost effectively to scale the web front-end across all availability zones to lower aggregate utilization levels that will allow an availability zone to fail during peak load without affecting the applications availability. 

<details><summary>Answer:</summary><p>
[A]

Categories:
[ASG]

Explanation:

Question 12@http://jayendrapatil.com/aws-ec2-instance-purchasing-option/

A: Ideal for HA to reduce and distribute load

B: 90% is not recommended as well RIs would increase the cost

C: 90% is not recommended as high bid price would not guarantee instances and would increase cost

D: Availability cannot be guaranteed

</p></details><hr>

### Question 13:

You run accounting software in the AWS cloud. This software needs to be online continuously during the day every day of the week, and has a very static requirement for compute resources. You also have other, unrelated batch jobs that need to run once per day at any time of your choosing. How should you minimize cost? [PROFESSIONAL]

- A. Purchase a Heavy Utilization Reserved Instance to run the accounting software. Turn it off after hours. Run the batch jobs with the same instance class, so the Reserved Instance credits are also applied to the batch jobs.
- B. Purchase a Medium Utilization Reserved Instance to run the accounting software. Turn it off after hours. Run the batch jobs with the same instance class, so the Reserved Instance credits are also applied to the batch jobs.
- C. Purchase a Light Utilization Reserved Instance to run the accounting software. Turn it off after hours. Run the batch jobs with the same instance class, so the Reserved Instance credits are also applied to the batch jobs.
- D. Purchase a Full Utilization Reserved Instance to run the accounting software. Turn it off after hours. Run the batch jobs with the same instance class, so the Reserved Instance credits are also applied to the batch jobs.

<details><summary>Answer:</summary><p>
[A]

Categories:
[]

Explanation:

Question 13@http://jayendrapatil.com/aws-ec2-instance-purchasing-option/

A: Because the instance will always be online during the day, in a predictable manner, and there are sequences of batch jobs to perform at any time, we should run the batch jobs when the account software is off. We can achieve Heavy Utilization by alternating these times, so we should purchase the reservation as such, as this represents the lowest cost. There is no such thing a “Full” level utilization purchases on EC2.

</p></details><hr>

