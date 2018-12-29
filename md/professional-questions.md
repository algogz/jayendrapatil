### Question 7:

You are designing a file-sharing service. This service will have millions of files in it. Revenue for the service will come from fees based on how much storage a user is using. You also want to store metadata on each file, such as title, description and whether the object is public or private. How do you achieve all of these goals in a way that is economical and can scale to millions of users? [PROFESSIONAL]

- A. Store all files in Amazon Simple Storage Service (S3). Create a bucket for each user. Store metadata in the filename of each object, and access it with LIST commands against the S3 API. 
- B. Store all files in Amazon S3. Create Amazon DynamoDB tables for the corresponding key-value pairs on the associated metadata, when objects are uploaded.
- C. Create a striped set of 4000 IOPS Elastic Load Balancing volumes to store the data. Use a database running in Amazon Relational Database Service (RDS) to store the metadata.
- D. Create a striped set of 4000 IOPS Elastic Load Balancing volumes to store the data. Create Amazon DynamoDB tables for the corresponding key-value pairs on the associated metadata, when objects are uploaded. 

<details><summary>Answer:</summary><p>
[B]

Categories:
[S3, RDS, DynamoDB, ELB]

Explanation:

Question 7@http://jayendrapatil.com/aws-dynamodb/

A: expensive and slow as it returns only 1000 items at a time

C: not economical with volumes

D: not economical with volumes

</p></details><hr>

### Question 8:

A utility company is building an application that stores data coming from more than 10,000 sensors. Each sensor has a unique ID and will send a datapoint (approximately 1KB) every 10 minutes throughout the day. Each datapoint contains the information coming from the sensor as well as a timestamp. This company would like to query information coming from a particular sensor for the past week very rapidly and want to delete all the data that is older than 4 weeks. Using Amazon DynamoDB for its scalability and rapidity, how do you implement this in the most cost effective way? [PROFESSIONAL]

- A. One table, with a primary key that is the sensor ID and a hash key that is the timestamp 
- B. One table, with a primary key that is the concatenation of the sensor ID and timestamp 
- C. One table for each week, with a primary key that is the concatenation of the sensor ID and timestamp 
- D. One table for each week, with a primary key that is the sensor ID and a hash key that is the timestamp

<details><summary>Answer:</summary><p>
[D]

Categories:
[DynamoDB]

Explanation:

Question 8@http://jayendrapatil.com/aws-dynamodb/

A: Single table impacts performance

B: Single table and concatenation impacts performance

C: Concatenation will cause queries would be slower, if at all

D: Composite key with Sensor ID and timestamp would help for faster queries

</p></details><hr>

### Question 9:

You have recently joined a startup company building sensors to measure street noise and air quality in urban areas. The company has been running a pilot deployment of around 100 sensors for 3 months. Each sensor uploads 1KB of sensor data every minute to a backend hosted on AWS. During the pilot, you measured a peak of 10 IOPS on the database, and you stored an average of 3GB of sensor data per month in the database. The current deployment consists of a load-balanced auto scaled Ingestion layer using EC2 instances and a PostgreSQL RDS database with 500GB standard storage. The pilot is considered a success and your CEO has managed to get the attention or some potential investors. The business plan requires a deployment of at least 100K sensors, which needs to be supported by the backend. You also need to store sensor data for at least two years to be able to compare year over year Improvements. To secure funding, you have to make sure that the platform meets these requirements and leaves room for further scaling. Which setup will meet the requirements? [PROFESSIONAL]

- A. Add an SQS queue to the ingestion layer to buffer writes to the RDS instance 
- B. Ingest data into a DynamoDB table and move old data to a Redshift cluster
- C. Replace the RDS instance with a 6 node Redshift cluster with 96TB of storage 
- D. Keep the current architecture but upgrade RDS storage to 3TB and 10K provisioned IOPS 

<details><summary>Answer:</summary><p>
[B]

Categories:
[RDS, SQS, EC2, DynamoDB, Redshift]

Explanation:

Question 9@http://jayendrapatil.com/aws-dynamodb/

A: RDS instance will not support data for 2 years

B: Handle 10K IOPS ingestion and store data into Redshift for analysis

C: Does not handle the ingestion issue

D: RDS instance will not support data for 2 years

</p></details><hr>

### Question 21:

An application stores payroll information nightly in DynamoDB for a large number of employees across hundreds of offices. Item attributes consist of individual name, office identifier, and cumulative daily hours. Managers run reports for ranges of names working in their office. One query is. “Return all Items in this office for names starting with A through E”. Which table configuration will result in the lowest impact on provisioned throughput for this query? [PROFESSIONAL]

- A. Configure the table to have a hash index on the name attribute, and a range index on the office identifier
- B. Configure the table to have a range index on the name attribute, and a hash index on the office identifier
- C. Configure a hash index on the name attribute and no range index
- D. Configure a hash index on the office Identifier attribute and no range index

<details><summary>Answer:</summary><p>
[B]

Categories:
[DynamoDB]

Explanation:

Question 21@http://jayendrapatil.com/aws-dynamodb/

</p></details><hr>

### Question 27:

Your company sells consumer devices and needs to record the first activation of all sold devices. Devices are not activated until the information is written on a persistent database. Activation data is very important for your company and must be analyzed daily with a MapReduce job. The execution time of the data analysis process must be less than three hours per day. Devices are usually sold evenly during the year, but when a new device model is out, there is a predictable peak in activation’s, that is, for a few days there are 10 times or even 100 times more activation’s than in average day. Which of the following databases and analysis framework would you implement to better optimize costs and performance for this workload? [PROFESSIONAL]

- A. Amazon RDS and Amazon Elastic MapReduce with Spot instances.
- B. Amazon DynamoDB and Amazon Elastic MapReduce with Spot instances.
- C. Amazon RDS and Amazon Elastic MapReduce with Reserved instances.
- D. Amazon DynamoDB and Amazon Elastic MapReduce with Reserved instances

<details><summary>Answer:</summary><p>
[B]

Categories:
[SES, RDS, DynamoDB]

Explanation:

Question 27@http://jayendrapatil.com/aws-dynamodb/

</p></details><hr>

### Question 2:

You deployed your company website using Elastic Beanstalk and you enabled log file rotation to S3. An Elastic Map Reduce job is periodically analyzing the logs on S3 to build a usage dashboard that you share with your CIO. You recently improved overall performance of the website using Cloud Front for dynamic content delivery and your website as the origin. After this architectural change, the usage dashboard shows that the traffic on your website dropped by an order of magnitude. How do you fix your usage dashboard’? [PROFESSIONAL]

- A. Enable CloudFront to deliver access logs to S3 and use them as input of the Elastic Map Reduce job
- B. Turn on Cloud Trail and use trail log tiles on S3 as input of the Elastic Map Reduce job
- C. Change your log collection process to use Cloud Watch ELB metrics as input of the Elastic Map Reduce job
- D. Use Elastic Beanstalk “Rebuild Environment” option to update log delivery to the Elastic Map Reduce job.
- E. Use Elastic Beanstalk ‘Restart App server(s)” option to update log delivery to the Elastic Map Reduce job.

<details><summary>Answer:</summary><p>
[A]

Categories:
[S3, CloudFront, EBS, ELB, EMR, Elastic Beanstalk]

Explanation:

Question 2@http://jayendrapatil.com/aws-cloudfront/

</p></details><hr>

### Question 3:

An AWS customer runs a public blogging website. The site users upload two million blog entries a month. The average blog entry size is 200 KB. The access rate to blog entries drops to negligible 6 months after publication and users rarely access a blog entry 1 year after publication. Additionally, blog entries have a high update rate during the first 3 months following publication; this drops to no updates after 6 months. The customer wants to use CloudFront to improve his user’s load times. Which of the following recommendations would you make to the customer? [PROFESSIONAL]

- A. Duplicate entries into two different buckets and create two separate CloudFront distributions where S3 access is restricted only to Cloud Front identity
- B. Create a CloudFront distribution with “US & Europe” price class for US/Europe users and a different CloudFront distribution with All Edge Locations for the remaining users.
- C. Create a CloudFront distribution with S3 access restricted only to the CloudFront identity and partition the blog entry’s location in S3 according to the month it was uploaded to be used with CloudFront behaviors
- D. Create a CloudFront distribution with Restrict Viewer Access Forward Query string set to true and minimum TTL of 0.

<details><summary>Answer:</summary><p>
[C]

Categories:
[S3, CloudFront, EBS]

Explanation:

Question 3@http://jayendrapatil.com/aws-cloudfront/

</p></details><hr>

### Question 4:

Your company has on-premises multi-tier PHP web application, which recently experienced downtime due to a large burst in web traffic due to a company announcement. Over the coming days, you are expecting similar announcements to drive similar unpredictable bursts, and are looking to find ways to quickly improve your infrastructures ability to handle unexpected increases in traffic. The application currently consists of 2 tiers a web tier, which consists of a load balancer, and several Linux Apache web servers as well as a database tier which hosts a Linux server hosting a MySQL database. Which scenario below will provide full site functionality, while helping to improve the ability of your application in the short timeframe required? [PROFESSIONAL]

- A. Offload traffic from on-premises environment Setup a CloudFront distribution and configure CloudFront to cache objects from a custom origin Choose to customize your object cache behavior, and select a TTL that objects should exist in cache.
- B. Migrate to AWS Use VM Import/Export to quickly convert an on-premises web server to an AMI create an Auto Scaling group, which uses the imported AMI to scale the web tier based on incoming traffic Create an RDS read replica and setup replication between the RDS instance and on-premises MySQL server to migrate the database.
- C. Failover environment: Create an S3 bucket and configure it tor website hosting Migrate your DNS to Route53 using zone (lie import and leverage Route53 DNS failover to failover to the S3 hosted website.
- D. Hybrid environment Create an AMI which can be used of launch web serfers in EC2 Create an Auto Scaling group which uses the * AMI to scale the web tier based on incoming traffic Leverage Elastic Load Balancing to balance traffic between on-premises web servers and those hosted in AWS.

<details><summary>Answer:</summary><p>
[A]

Categories:
[S3, SES, RDS, CloudFront, EC2, ASG, EBS, ELB]

Explanation:

Question 4@http://jayendrapatil.com/aws-cloudfront/

</p></details><hr>

### Question 6:

A media production company wants to deliver high-definition raw video for preproduction and dubbing to customer all around the world. They would like to use Amazon CloudFront for their scenario, and they require the ability to limit downloads per customer and video file to a configurable number. A CloudFront download distribution with TTL=0 was already setup to make sure all client HTTP requests hit an authentication backend on Amazon Elastic Compute Cloud (EC2)/Amazon RDS first, which is responsible for restricting the number of downloads. Content is stored in S3 and configured to be accessible only via CloudFront. What else needs to be done to achieve an architecture that meets the requirements? Choose 2 answers [PROFESSIONAL]

- A. Enable URL parameter forwarding, let the authentication backend count the number of downloads per customer in RDS, and return the content S3 URL unless the download limit is reached.
- B. Enable CloudFront logging into an S3 bucket, leverage EMR to analyze CloudFront logs to determine the number of downloads per customer, and return the content S3 URL unless the download limit is reached. 
- C. Enable URL parameter forwarding, let the authentication backend count the number of downloads per customer in RDS, and invalidate the CloudFront distribution as soon as the download limit is reached. 
- D. Enable CloudFront logging into the S3 bucket, let the authentication backend determine the number of downloads per customer by parsing those logs, and return the content S3 URL unless the download limit is reached. 
- E. Configure a list of trusted signers, let the authentication backend count the number of download requests per customer in RDS, and return a dynamically signed URL unless the download limit is reached.

<details><summary>Answer:</summary><p>
[A, E]

Categories:
[S3, RDS, CloudFront, EC2, EMR]

Explanation:

Question 6@http://jayendrapatil.com/aws-cloudfront/

B: CloudFront logs are logged periodically and EMR not being real time, hence not suitable

C: Distribution are not invalidated but Objects

D: CloudFront logs are logged periodically and EMR not being real time, hence not suitable

</p></details><hr>

### Question 7:

Your customer is implementing a video on-demand streaming platform on AWS. The requirements are to support for multiple devices such as iOS, Android, and PC as client devices, using a standard client player, using streaming technology (not download) and scalable architecture with cost effectiveness [PROFESSIONAL]

- A. Store the video contents to Amazon Simple Storage Service (S3) as an origin server. Configure the Amazon CloudFront distribution with a streaming option to stream the video contents
- B. Store the video contents to Amazon S3 as an origin server. Configure the Amazon CloudFront distribution with a download option to stream the video contents
- C. Launch a streaming server on Amazon Elastic Compute Cloud (EC2) (for example, Adobe Media Server), and store the video contents as an origin server. Configure the Amazon CloudFront distribution with a download option to stream the video contents
- D. Launch a streaming server on Amazon Elastic Compute Cloud (EC2) (for example, Adobe Media Server), and store the video contents as an origin server. Launch and configure the required amount of streaming servers on Amazon EC2 as an edge server to stream the video contents

<details><summary>Answer:</summary><p>
[B]

Categories:
[S3, CloudFront, EC2]

Explanation:

Question 7@http://jayendrapatil.com/aws-cloudfront/

B: http://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/distribution-web.html

</p></details><hr>

### Question 8:

You are an architect for a news -sharing mobile application. Anywhere in the world, your users can see local news on of topics they choose. They can post pictures and videos from inside the application. Since the application is being used on a mobile phone, connection stability is required for uploading content, and delivery should be quick. Content is accessed a lot in the first minutes after it has been posted, but is quickly replaced by new content before disappearing. The local nature of the news means that 90 percent of the uploaded content is then read locally (less than a hundred kilometers from where it was posted). What solution will optimize the user experience when users upload and view content (by minimizing page load times and minimizing upload times)? [PROFESSIONAL]

- A. Upload and store the content in a central Amazon Simple Storage Service (S3) bucket, and use an Amazon Cloud Front Distribution for content delivery.
- B. Upload and store the content in an Amazon Simple Storage Service (S3) bucket in the region closest to the user, and use multiple Amazon Cloud Front distributions for content delivery.
- C. Upload the content to an Amazon Elastic Compute Cloud (EC2) instance in the region closest to the user, send the content to a central Amazon Simple Storage Service (S3) bucket, and use an Amazon Cloud Front distribution for content delivery.
- D. Use an Amazon Cloud Front distribution for uploading the content to a central Amazon Simple Storage Service (S3) bucket and for content delivery.

<details><summary>Answer:</summary><p>
[D]

Categories:
[S3, SES, EC2]

Explanation:

Question 8@http://jayendrapatil.com/aws-cloudfront/

</p></details><hr>

### Question 9:

To enable end-to-end HTTPS connections from the user‘s browser to the origin via CloudFront, which of the following options are valid? Choose 2 answers [PROFESSIONAL]

- A. Use self signed certificate in the origin and CloudFront default certificate in CloudFront. 
- B. Use the CloudFront default certificate in both origin and CloudFront 
- C. Use 3rd-party CA certificate in the origin and CloudFront default certificate in CloudFront
- D. Use 3rd-party CA certificate in both origin and CloudFront
- E. Use a self signed certificate in both the origin and CloudFront 

<details><summary>Answer:</summary><p>
[C, D]

Categories:
[CloudFront]

Explanation:

Question 9@http://jayendrapatil.com/aws-cloudfront/

A: Origin cannot be self signed

B: CloudFront cert cannot be applied to origin

E: Origin cannot be self signed

</p></details><hr>

### Question 10:

Your application consists of 10% writes and 90% reads. You currently service all requests through a Route53 Alias Record directed towards an AWS ELB, which sits in front of an EC2 Auto Scaling Group. Your system is getting very expensive when there are large traffic spikes during certain news events, during which many more people request to read similar data all at the same time. What is the simplest and cheapest way to reduce costs and scale with spikes like this? [PROFESSIONAL]

- A. Create an S3 bucket and asynchronously replicate common requests responses into S3 objects. When a request comes in for a precomputed response, redirect to AWS S3
- B. Create another ELB and Auto Scaling Group layer mounted on top of the other system, adding a tier to the system. Serve most read requests out of the top layer
- C. Create a CloudFront Distribution and direct Route53 to the Distribution. Use the ELB as an Origin and specify Cache Behaviors to proxy cache requests, which can be served late.
- D. Create a Memcached cluster in AWS ElastiCache. Create cache logic to serve requests, which can be served late from the in-memory cache for increased performance.

<details><summary>Answer:</summary><p>
[C]

Categories:
[S3, SES, RDS, CloudFront, EC2, ASG, ElastiCache, ELB]

Explanation:

Question 10@http://jayendrapatil.com/aws-cloudfront/

C: CloudFront can server request from cache and multiple cache behavior can be defined based on rules for a given URL pattern based on file extensions, file names, or any portion of a URL. Each cache behavior can include the CloudFront configuration values: origin server name, viewer connection protocol, minimum expiration period, query string parameters, cookies, and trusted signers for private content.

</p></details><hr>

### Question 12:

Your website is serving on-demand training videos to your workforce. Videos are uploaded monthly in high resolution MP4 format. Your workforce is distributed globally often on the move and using company-provided tablets that require the HTTP Live Streaming (HLS) protocol to watch a video. Your company has no video transcoding expertise and it required you might need to pay for a consultant. How do you implement the most cost-efficient architecture without compromising high availability and quality of video delivery? [PROFESSIONAL]

- A. Elastic Transcoder to transcode original high-resolution MP4 videos to HLS. S3 to host videos with lifecycle Management to archive original flies to Glacier after a few days. CloudFront to serve HLS transcoded videos from S3
- B. A video transcoding pipeline running on EC2 using SQS to distribute tasks and Auto Scaling to adjust the number or nodes depending on the length of the queue S3 to host videos with Lifecycle Management to archive all files to Glacier after a few days CloudFront to serve HLS transcoding videos from Glacier
- C. Elastic Transcoder to transcode original high-resolution MP4 videos to HLS EBS volumes to host videos and EBS snapshots to incrementally backup original rues after a few days. CloudFront to serve HLS transcoded videos from EC2.
- D. A video transcoding pipeline running on EC2 using SQS to distribute tasks and Auto Scaling to adjust the number of nodes depending on the length of the queue. EBS volumes to host videos and EBS snapshots to incrementally backup original files after a few days. CloudFront to serve HLS transcoded videos from EC2

<details><summary>Answer:</summary><p>
[A]

Categories:
[S3, CloudFront, SQS, Glacier, EC2, ASG, Elastic Transcoder, EBS]

Explanation:

Question 12@http://jayendrapatil.com/aws-cloudfront/

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

### Question 35:

You have deployed a three-tier web application in a VPC with a CIDR block of 10.0.0.0/28. You initially deploy two web servers, two application servers, two database servers and one NAT instance tor a total of seven EC2 instances The web. Application and database servers are deployed across two availability zones (AZs). You also deploy an ELB in front of the two web servers, and use Route53 for DNS Web (raffle gradually increases in the first few days following the deployment, so you attempt to double the number of instances in each tier of the application to handle the new load unfortunately some of these new instances fail to launch. Which of the following could the root caused? (Choose 2 answers) [PROFESSIONAL]

- A. The Internet Gateway (IGW) of your VPC has scaled-up adding more instances to handle the traffic spike, reducing the number of available private IP addresses for new instance launches.
- B. AWS reserves one IP address in each subnet’s CIDR block for Route53 so you do not have enough addresses left to launch all of the new EC2 instances.
- C. AWS reserves the first and the last private IP address in each subnet’s CIDR block so you do not have enough addresses left to launch all of the new EC2 instances.
- D. The ELB has scaled-up. Adding more instances to handle the traffic reducing the number of available private IP addresses for new instance launches
- E. AWS reserves the first four and the last IP address in each subnet’s CIDR block so you do not have enough addresses left to launch all of the new EC2 instances.

<details><summary>Answer:</summary><p>
[D, E]

Categories:
[SES, EC2, VPC, ELB]

Explanation:

Question 35@http://jayendrapatil.com/aws-virtual-private-cloud-vpc/

</p></details><hr>

### Question 4:

You are designing network connectivity for your fat client application. The application is designed for business travelers who must be able to connect to it from their hotel rooms, cafes, public Wi-Fi hotspots, and elsewhere on the Internet. You do not want to publish the application on the Internet. Which network design meets the above requirements while minimizing deployment and operational costs? [PROFESSIONAL]

- A. Implement AWS Direct Connect, and create a private interface to your VPC. Create a public subnet and place your application servers in it. 
- B. Implement Elastic Load Balancing with an SSL listener that terminates the back-end connection to the application. 
- C. Configure an IPsec VPN connection, and provide the users with the configuration details. Create a public subnet in your VPC, and place your application servers in it. 
- D. Configure an SSL VPN solution in a public subnet of your VPC, then install and configure SSL VPN client software on all user computers. Create a private subnet in your VPC and place your application servers in it.

<details><summary>Answer:</summary><p>
[D]

Categories:
[VPC, ELB, Direct Connect]

Explanation:

Question 4@http://jayendrapatil.com/aws-vpc-vpn-cloudhub/

A: High Cost and does not minimize deployment

B: Needs to be published to internet

C: Instances still in public subnet are internet accessible

D: Cost effective and can be in private subnet as well

</p></details><hr>

### Question 5:

You are designing a connectivity solution between on-premises infrastructure and Amazon VPC Your server’s on-premises will De communicating with your VPC instances You will De establishing IPSec tunnels over the internet You will be using VPN gateways and terminating the IPsec tunnels on AWS-supported customer gateways. Which of the following objectives would you achieve by implementing an IPSec tunnel as outlined above? (Choose 4 answers) [PROFESSIONAL]

- A. End-to-end protection of data in transit
- B. End-to-end Identity authentication
- C. Data encryption across the Internet
- D. Protection of data in transit over the Internet
- E. Peer identity authentication between VPN gateway and customer gateway
- F. Data integrity protection across the Internet

<details><summary>Answer:</summary><p>
[C, D, E, F]

Categories:
[SES, VPC]

Explanation:

Question 5@http://jayendrapatil.com/aws-vpc-vpn-cloudhub/

</p></details><hr>

### Question 6:

A development team that is currently doing a nightly six-hour build which is lengthening over time on-premises with a large and mostly under utilized server would like to transition to a continuous integration model of development on AWS with multiple builds triggered within the same day. However, they are concerned about cost, security and how to integrate with existing on-premises applications such as their LDAP and email servers, which cannot move off-premises. The development environment needs a source code repository; a project management system with a MySQL database resources for performing the builds and a storage location for QA to pick up builds from. What AWS services combination would you recommend to meet the development team’s requirements? [PROFESSIONAL]

- A. A Bastion host Amazon EC2 instance running a VPN server for access from on-premises, Amazon EC2 for the source code repository with attached Amazon EBS volumes, Amazon EC2 and Amazon RDS MySQL for the project management system, EIP for the source code repository and project management system, Amazon SQL for a build queue, An Amazon Auto Scaling group of Amazon EC2 instances for performing builds and Amazon Simple Email Service for sending the build output. 
- B. An AWS Storage Gateway for connecting on-premises software applications with cloud-based storage securely, Amazon EC2 for the resource code repository with attached Amazon EBS volumes, Amazon EC2 and Amazon RDS MySQL for the project management system, EIPs for the source code repository and project management system, Amazon Simple Notification Service for a notification initiated build, An Auto Scaling group of Amazon EC2 instances for performing builds and Amazon S3 for the build output. 
- C. An AWS Storage Gateway for connecting on-premises software applications with cloud-based storage securely, Amazon EC2 for the resource code repository with attached Amazon EBS volumes, Amazon EC2 and Amazon RDS MySQL for the project management system, EIPs for the source code repository and project management system, Amazon SQS for a build queue, An Amazon Elastic Map Reduce (EMR) cluster of Amazon EC2 instances for performing builds and Amazon CloudFront for the build output. 
- D. A VPC with a VPN Gateway back to their on-premises servers, Amazon EC2 for the source-code repository with attached Amazon EBS volumes, Amazon EC2 and Amazon RDS MySQL for the project management system, EIPs for the source code repository and project management system, SQS for a build queue, An Auto Scaling group of EC2 instances for performing builds and S3 for the build output.

<details><summary>Answer:</summary><p>
[D]

Categories:
[S3, SES, RDS, CloudFront, SQS, EC2, Storage Gateway, ASG, EBS, VPC, SNS, EMR]

Explanation:

Question 6@http://jayendrapatil.com/aws-vpc-vpn-cloudhub/

A: Bastion is not for VPN connectivity also SES should not be used

B: Storage Gateway does provide secure connectivity but still needs VPN. SNS alone cannot handle builds

C: Storage Gateway does not provide secure connectivity, still needs VPN. EMR is not ideal for performing builds as it needs normal EC2 instances

D: VPN gateway is required for secure connectivity. SQS for build queue and EC2 for builds

</p></details><hr>

### Question 14:

An application that you are managing has EC2 instances and DynamoDB tables deployed to several AWS Regions. In order to monitor the performance of the application globally, you would like to see two graphs 1) Avg CPU Utilization across all EC2 instances and 2) Number of Throttled Requests for all DynamoDB tables. How can you accomplish this? [PROFESSIONAL]

- A. Tag your resources with the application name, and select the tag name as the dimension in the CloudWatch Management console to view the respective graphs 
- B. Use the CloudWatch CLI tools to pull the respective metrics from each regional endpoint. Aggregate the data offline & store it for graphing in CloudWatch.
- C. Add SNMP traps to each instance and DynamoDB table. Leverage a central monitoring server to capture data from each instance and table. Put the aggregate data into CloudWatch for graphing 
- D. Add a CloudWatch agent to each instance and attach one to each DynamoDB table. When configuring the agent set the appropriate application name & view the graphs in CloudWatch. 

<details><summary>Answer:</summary><p>
[B]

Categories:
[EC2, CloudWatch, DynamoDB]

Explanation:

Question 14@http://jayendrapatil.com/aws-cloudwatch-overview/

A: CloudWatch metrics are regional

C: Can’t add SNMP traps to DynamoDB as it is a managed service

D: Can’t add agents to DynamoDB as it is a managed service

</p></details><hr>

### Question 15:

You have set up Individual AWS accounts for each project. You have been asked to make sure your AWS Infrastructure costs do not exceed the budget set per project for each month. Which of the following approaches can help ensure that you do not exceed the budget each month? [PROFESSIONAL]

- A. Consolidate your accounts so you have a single bill for all accounts and projects 
- B. Set up auto scaling with CloudWatch alarms using SNS to notify you when you are running too many Instances in a given account 
- C. Set up CloudWatch billing alerts for all AWS resources used by each project, with a notification occurring when the amount for each resource tagged to a particular project matches the budget allocated to the project. 
- D. Set up CloudWatch billing alerts for all AWS resources used by each account, with email notifications when it hits 50%. 80% and 90% of its budgeted monthly spend

<details><summary>Answer:</summary><p>
[D]

Categories:
[CloudWatch, ASG, SNS]

Explanation:

Question 15@http://jayendrapatil.com/aws-cloudwatch-overview/

A: Consolidation will not help limit per account

B: many instances do not directly map to cost and would not give exact cost

C: as each project already has a account, no need for resource tagging

</p></details><hr>

### Question 19:

You are hired as the new head of operations for a SaaS company. Your CTO has asked you to make debugging any part of your entire operation simpler and as fast as possible. She complains that she has no idea what is going on in the complex, service-oriented architecture, because the developers just log to disk, and it’s very hard to find errors in logs on so many services. How can you best meet this requirement and satisfy your CTO? [PROFESSIONAL]

- A. Copy all log files into AWS S3 using a cron job on each instance. Use an S3 Notification Configuration on the <code>PutBucket</code> event and publish events to AWS Lambda. Use the Lambda to analyze logs as soon as they come in and flag issues. 
- B. Begin using CloudWatch Logs on every service. Stream all Log Groups into S3 objects. Use AWS EMR cluster jobs to perform adhoc MapReduce analysis and write new queries when needed. 
- C. Copy all log files into AWS S3 using a cron job on each instance. Use an S3 Notification Configuration on the <code>PutBucket</code> event and publish events to AWS Kinesis. Use Apache Spark on AWS EMR to perform at-scale stream processing queries on the log chunks and flag issues. 
- D. Begin using CloudWatch Logs on every service. Stream all Log Groups into an AWS Elasticsearch Service Domain running Kibana 4 and perform log analysis on a search cluster.

<details><summary>Answer:</summary><p>
[D]

Categories:
[S3, Elasticsearch, CloudWatch, Kinesis, EMR, Lambda]

Explanation:

Question 19@http://jayendrapatil.com/aws-cloudwatch-overview/

A: is not fast in search and introduces delay

B: is not fast in search and introduces delay

C: is not fast in search and introduces delay

D: ELK – Elasticsearch, Kibana stack is designed specifically for real-time, ad-hoc log analysis and aggregation

</p></details><hr>

### Question 20:

Your EC2-Based Multi-tier application includes a monitoring instance that periodically makes application -level read only requests of various application components and if any of those fail more than three times 30 seconds calls CloudWatch to fire an alarm, and the alarm notifies your operations team by email and SMS of a possible application health problem. However, you also need to watch the watcher -the monitoring instance itself – and be notified if it becomes unhealthy. Which of the following is a simple way to achieve that goal? [PROFESSIONAL]

- A. Run another monitoring instance that pings the monitoring instance and fires a could watch alarm mat notifies your operations team should the primary monitoring instance become unhealthy.
- B. Set a CloudWatch alarm based on EC2 system and instance status checks and have the alarm notify your operations team of any detected problem with the monitoring instance.
- C. Set a CloudWatch alarm based on the CPU utilization of the monitoring instance and nave the alarm notify your operations team if C r the CPU usage exceeds 50% few more than one minute: then have your monitoring application go into a CPU-bound loop should it Detect any application problems.
- D. Have the monitoring instances post messages to an SOS queue and then dequeue those messages on another instance should the queue cease to have new messages, the second instance should first terminate the original monitoring instance start another backup monitoring instance and assume (the role of the previous monitoring instance and beginning adding messages to the SQS queue.

<details><summary>Answer:</summary><p>
[B]

Categories:
[SQS, EC2, CloudWatch]

Explanation:

Question 20@http://jayendrapatil.com/aws-cloudwatch-overview/

</p></details><hr>

### Question 5:

You are looking to migrate your Development (Dev) and Test environments to AWS. You have decided to use separate AWS accounts to host each environment. You plan to link each accounts bill to a Master AWS account using Consolidated Billing. To make sure you Keep within budget you would like to implement a way for administrators in the Master account to have access to stop, delete and/or terminate resources in both the Dev and Test accounts. Identify which option will allow you to achieve this goal. [PROFESSIONAL]

- A. Create IAM users in the Master account with full Admin permissions. Create cross-account roles in the Dev and Test accounts that grant the Master account access to the resources in the account by inheriting permissions from the Master account.
- B. Create IAM users and a cross-account role in the Master account that grants full Admin permissions to the Dev and Test accounts.
- C. Create IAM users in the Master account Create cross-account roles in the Dev and Test accounts that have full Admin permissions and grant the Master account access
- D. Link the accounts using Consolidated Billing. This will give IAM users in the Master account access to resources in the Dev and Test accounts

<details><summary>Answer:</summary><p>
[C]

Categories:
[IAM]

Explanation:

Question 5@http://jayendrapatil.com/aws-iam-role/

</p></details><hr>

### Question 6:

You have an application running on an EC2 Instance which will allow users to download flies from a private S3 bucket using a pre-assigned URL. Before generating the URL the application should verify the existence of the file in S3. How should the application use AWS credentials to access the S3 bucket securely? [PROFESSIONAL]

- A. Use the AWS account access Keys the application retrieves the credentials from the source code of the application.
- B. Create a IAM user for the application with permissions that allow list access to the S3 bucket launch the instance as the IAM user and retrieve the IAM user’s credentials from the EC2 instance user data.
- C. Create an IAM role for EC2 that allows list access to objects in the S3 bucket. Launch the instance with the role, and retrieve the role’s credentials from the EC2 Instance metadata
- D. Create an IAM user for the application with permissions that allow list access to the S3 bucket. The application retrieves the IAM user credentials from a temporary directory with permissions that allow read access only to the application user.

<details><summary>Answer:</summary><p>
[C]

Categories:
[S3, IAM, EC2]

Explanation:

Question 6@http://jayendrapatil.com/aws-iam-role/

</p></details><hr>

### Question 7:

An administrator is using Amazon CloudFormation to deploy a three tier web application that consists of a web tier and application tier that will utilize Amazon DynamoDB for storage when creating the CloudFormation template which of the following would allow the application instance access to the DynamoDB tables without exposing API credentials? [PROFESSIONAL]

- A. Create an Identity and Access Management Role that has the required permissions to read and write from the required DynamoDB table and associate the Role to the application instances by referencing an instance profile.
- B. Use the Parameter section in the Cloud Formation template to nave the user input Access and Secret Keys from an already created IAM user that has me permissions required to read and write from the required DynamoDB table.
- C. Create an Identity and Access Management Role that has the required permissions to read and write from the required DynamoDB table and reference the Role in the instance profile property of the application instance.
- D. Create an identity and Access Management user in the CloudFormation template that has permissions to read and write from the required DynamoDB table, use the GetAtt function to retrieve the Access and secret keys and pass them to the application instance through user-data.

<details><summary>Answer:</summary><p>
[C]

Categories:
[IAM, CloudFormation, DynamoDB]

Explanation:

Question 7@http://jayendrapatil.com/aws-iam-role/

</p></details><hr>

### Question 8:

An enterprise wants to use a third-party SaaS application. The SaaS application needs to have access to issue several API commands to discover Amazon EC2 resources running within the enterprise’s account. The enterprise has internal security policies that require any outside access to their environment must conform to the principles of least privilege and there must be controls in place to ensure that the credentials used by the SaaS vendor cannot be used by any other third party. Which of the following would meet all of these conditions? [PROFESSIONAL]

- A. From the AWS Management Console, navigate to the Security Credentials page and retrieve the access and secret key for your account.
- B. Create an IAM user within the enterprise account assign a user policy to the IAM user that allows only the actions required by the SaaS application create a new access and secret key for the user and provide these credentials to the SaaS provider.
- C. Create an IAM role for cross-account access allows the SaaS provider’s account to assume the role and assign it a policy that allows only the actions required by the SaaS application.
- D. Create an IAM role for EC2 instances, assign it a policy mat allows only the actions required tor the SaaS application to work, provide the role ARM to the SaaS provider to use when launching their application instances.

<details><summary>Answer:</summary><p>
[C]

Categories:
[IAM, EC2]

Explanation:

Question 8@http://jayendrapatil.com/aws-iam-role/

</p></details><hr>

### Question 10:

A customer is in the process of deploying multiple applications to AWS that are owned and operated by different development teams. Each development team maintains the authorization of its users independently from other teams. The customer’s information security team would like to be able to delegate user authorization to the individual development teams but independently apply restrictions to the users permissions based on factors such as the users device and location. For example, the information security team would like to grant read-only permissions to a user who is defined by the development team as read/write whenever the user is authenticating from outside the corporate network. What steps can the information security team take to implement this capability? [PROFESSIONAL]

- A. Operate an authentication service that generates AWS STS tokens with IAM policies from application-defined IAM roles. 
- B. Add additional IAM policies to the application IAM roles that deny user privileges based on information security policy.
- C. Configure IAM policies that restrict modification of the application IAM roles only to the information security team. 
- D. Enable federation with the internal LDAP directory and grant the application teams permissions to modify users.

<details><summary>Answer:</summary><p>
[B]

Categories:
[IAM]

Explanation:

Question 10@http://jayendrapatil.com/aws-iam-role/

A: no user separation, will just help generate temporary tokens

B: Different policy with deny rules based on location, device and more restrictive wins

C: Authorization should still be in developers control

</p></details><hr>

### Question 10:

A web design company currently runs several FTP servers that their 250 customers use to upload and download large graphic files. They wish to move this system to AWS to make it more scalable, but they wish to maintain customer privacy and keep costs to a minimum. What AWS architecture would you recommend? [PROFESSIONAL]

- A. Ask their customers to use an S3 client instead of an FTP client. Create a single S3 bucket. Create an IAM user for each customer. Put the IAM Users in a Group that has an IAM policy that permits access to subdirectories within the bucket via use of the ‘username’ Policy variable.
- B. Create a single S3 bucket with Reduced Redundancy Storage turned on and ask their customers to use an S3 client instead of an FTP client. Create a bucket for each customer with a Bucket Policy that permits access only to that one customer. 
- C. Create an auto-scaling group of FTP servers with a scaling policy to automatically scale-in when minimum network traffic on the auto-scaling group is below a given threshold. Load a central list of ftp users from S3 as part of the user Data startup script on each Instance 
- D. Create a single S3 bucket with Requester Pays turned on and ask their customers to use an S3 client instead of an FTP client. Create a bucket tor each customer with a Bucket Policy that permits access only to that one customer. 

<details><summary>Answer:</summary><p>
[A]

Categories:
[S3, IAM]

Explanation:

Question 10@http://jayendrapatil.com/aws-iam-access-management/

B: https://aws.amazon.com/about-aws/whats-new/2015/08/amazon-s3-introduces-new-usability-enhancements/

B: Creating bucket for each user is not a scalable model, also 100 buckets are a limit earlier without extending which has since changed

C: Expensive

D: https://aws.amazon.com/about-aws/whats-new/2015/08/amazon-s3-introduces-new-usability-enhancements/

D: Creating bucket for each user is not a scalable model, also 100 buckets are a limit earlier without extending which has since changed

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

### Question 6:

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

Question 6@http://jayendrapatil.com/aws-s3-storage-classes/

A: Spot instances impacts performance

B: Combination of the Spot and reserved with guarantee performance and help reduce cost. Also, RRS would reduce cost and guarantee data integrity, which is different from data durability

C: Spot instances impacts performance

D: Spot instances impacts performance

</p></details><hr>

### Question 8:

A newspaper organization has an on-premises application which allows the public to search its back catalogue and retrieve individual newspaper pages via a website written in Java. They have scanned the old newspapers into JPEGs (approx. 17TB) and used Optical Character Recognition (OCR) to populate a commercial search product. The hosting platform and software is now end of life and the organization wants to migrate its archive to AWS and produce a cost efficient architecture and still be designed for availability and durability. Which is the most appropriate? [PROFESSIONAL]

- A. Use S3 with reduced redundancy to store and serve the scanned files, install the commercial search application on EC2 Instances and configure with auto-scaling and an Elastic Load Balancer. 
- B. Model the environment using CloudFormation. Use an EC2 instance running Apache webserver and an open source search application, stripe multiple standard EBS volumes together to store the JPEGs and search index. 
- C. Use S3 with standard redundancy to store and serve the scanned files, use CloudSearch for query processing, and use Elastic Beanstalk to host the website across multiple availability zones.
- D. Use a single-AZ RDS MySQL instance to store the search index and the JPEG images use an EC2 instance to serve the website and translate user queries into SQL. 
- E. Use a CloudFront download distribution to serve the JPEGs to the end users and Install the current commercial search product, along with a Java Container for the website on EC2 instances and use Route53 with DNS round-robin. 

<details><summary>Answer:</summary><p>
[C]

Categories:
[S3, SES, RDS, CloudFront, EC2, EBS, CloudFormation, CloudSearch, Elastic Beanstalk]

Explanation:

Question 8@http://jayendrapatil.com/aws-s3-storage-classes/

A: RRS impacts durability and commercial search would add to cost

B: Using EBS is not cost effective for storing files

C: Standard S3 and Elastic Beanstalk provides availability and durability, Standard S3 and CloudSearch provides cost effective storage and search

D: RDS is not ideal and cost effective to store files, Single AZ impacts availability

E: CloudFront needs a source and using commercial search product is not cost effective

</p></details><hr>

### Question 9:

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

Question 9@http://jayendrapatil.com/aws-s3-storage-classes/

B: Master and Core must be RI or On Demand. Cannot be Spot

C: Need better durability for ingest file. Spot instances can be used for task nodes for cost saving.

D: Input must be in S3 standard

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

### Question 2:

Your startup wants to implement an order fulfillment process for selling a personalized gadget that needs an average of 3-4 days to produce with some orders taking up to 6 months you expect 10 orders per day on your first day. 1000 orders per day after 6 months and 10,000 orders after 12 months. Orders coming in are checked for consistency men dispatched to your manufacturing plant for production quality control packaging shipment and payment processing If the product does not meet the quality standards at any stage of the process employees may force the process to repeat a step Customers are notified via email about order status and any critical issues with their orders such as payment failure. Your case architecture includes AWS Elastic Beanstalk for your website with an RDS MySQL instance for customer data and orders. How can you implement the order fulfillment process while making sure that the emails are delivered reliably? [PROFESSIONAL]

- A. Add a business process management application to your Elastic Beanstalk app servers and re-use the ROS database for tracking order status use one of the Elastic Beanstalk instances to send emails to customers.
- B. Use SWF with an Auto Scaling group of activity workers and a decider instance in another Auto Scaling group with min/max=1 Use the decider instance to send emails to customers.
- C. Use SWF with an Auto Scaling group of activity workers and a decider instance in another Auto Scaling group with min/max=1 use SES to send emails to customers.
- D. Use an SQS queue to manage all process tasks Use an Auto Scaling group of EC2 Instances that poll the tasks and execute them. Use SES to send emails to customers.

<details><summary>Answer:</summary><p>
[C]

Categories:
[SES, RDS, SWF, SQS, EC2, ASG, EBS, Elastic Beanstalk]

Explanation:

Question 2@http://jayendrapatil.com/aws-simple-email-service-ses/

</p></details><hr>

### Question 6:

You are implementing a URL whitelisting system for a company that wants to restrict outbound HTTP’S connections to specific domains from their EC2-hosted applications you deploy a single EC2 instance running proxy software and configure It to accept traffic from all subnets and EC2 instances in the VPC. You configure the proxy to only pass through traffic to domains that you define in its whitelist configuration You have a nightly maintenance window or 10 minutes where ail instances fetch new software updates. Each update Is about 200MB In size and there are 500 instances In the VPC that routinely fetch updates After a few days you notice that some machines are failing to successfully download some, but not all of their updates within the maintenance window The download URLs used for these updates are correctly listed in the proxy’s whitelist configuration and you are able to access them manually using a web browser on the instances What might be happening? (Choose 2 answers) [PROFESSIONAL]

- A. You are running the proxy on an undersized EC2 instance type so network throughput is not sufficient for all instances to download their updates in time.
- B. You have not allocated enough storage to the EC2 instance running me proxy so the network buffer is filling up causing some requests to fall
- C. You are running the proxy in a public subnet but have not allocated enough EIPs to support the needed network throughput through the Internet Gateway (IGW)
- D. You are running the proxy on a affluently-sized EC2 instance in a private subnet and its network throughput is being throttled by a NAT running on an undersized EC2 instance
- E. The route table for the subnets containing the affected EC2 instances is not configured to direct network traffic for the software update locations to the proxy.

<details><summary>Answer:</summary><p>
[A, D]

Categories:
[EC2, VPC]

Explanation:

Question 6@http://jayendrapatil.com/aws-ec2-instance-types/

</p></details><hr>

### Question 7:

You have been asked to design the storage layer for an application. The application requires disk performance of at least 100,000 IOPS in addition; the storage layer must be able to survive the loss of an individual disk, EC2 instance, or Availability Zone without any data loss. The volume you provide must have a capacity of at least 3TB. Which of the following designs will meet these objectives? [PROFESSIONAL]

- A. Instantiate an i2.8xlarge instance in us-east-1a. Create a RAID 0 volume using the four 800GB SSD ephemeral disks provided with the instance. Provision 3×1 TB EBS volumes attach them to the instance and configure them as a second RAID 0 volume. Configure synchronous, block-level replication from the ephemeral backed volume to the EBS-backed volume. 
- B. Instantiate an i2.8xlarge instance in us-east-1a. Create a RAID 0 volume using the four 800GB SSD ephemeral disks provided with the Instance Configure synchronous block-level replication to an identically configured Instance in us-east-1b.
- C. Instantiate a c3.8xlarge Instance in us-east-1. Provision an AWS Storage Gateway and configure it for 3 TB of storage and 100,000 IOPS. Attach the volume to the instance. 
- D. Instantiate a c3.8xlarge instance in us-east-1 provision 4x1TB EBS volumes, attach them to the instance, and configure them as a single RAID 5 volume Ensure that EBS snapshots are performed every 15 minutes. 
- E. Instantiate a c3 8xlarge Instance in us-east-1 Provision 3x1TB EBS volumes attach them to the instance, and configure them as a single RAID 0 volume Ensure that EBS snapshots are performed every 15 minutes. 

<details><summary>Answer:</summary><p>
[B]

Categories:
[EC2, Storage Gateway, EBS]

Explanation:

Question 7@http://jayendrapatil.com/aws-ec2-instance-types/

A: Same AZ will not survive the AZ loss

C: Need synchronous replication to prevent any data loss

D: RAID 5 not recommended by AWS and Need synchronous replication to prevent any data loss

E: Need synchronous replication to prevent any data loss

</p></details><hr>

### Question 3:

You are designing a photo sharing mobile app the application will store all pictures in a single Amazon S3 bucket. Users will upload pictures from their mobile device directly to Amazon S3 and will be able to view and download their own pictures directly from Amazon S3. You want to configure security to handle potentially millions of users in the most secure manner possible. What should your server-side application do when a new user registers on the photo-sharing mobile application? [PROFESSIONAL]

- A. Create a set of long-term credentials using AWS Security Token Service with appropriate permissions Store these credentials in the mobile app and use them to access Amazon S3.
- B. Record the user’s Information in Amazon RDS and create a role in IAM with appropriate permissions. When the user uses their mobile app create temporary credentials using the AWS Security Token Service ‘AssumeRole’ function. Store these credentials in the mobile app’s memory and use them to access Amazon S3. Generate new credentials the next time the user runs the mobile app.
- C. Record the user’s Information in Amazon DynamoDB. When the user uses their mobile app create temporary credentials using AWS Security Token Service with appropriate permissions. Store these credentials in the mobile app’s memory and use them to access Amazon S3 Generate new credentials the next time the user runs the mobile app.
- D. Create IAM user. Assign appropriate permissions to the IAM user Generate an access key and secret key for the IAM user, store them in the mobile app and use these credentials to access Amazon S3.
- E. Create an IAM user. Update the bucket policy with appropriate permissions for the IAM user Generate an access Key and secret Key for the IAM user, store them In the mobile app and use these credentials to access Amazon S3.

<details><summary>Answer:</summary><p>
[B]

Categories:
[S3, SES, RDS, IAM, DynamoDB]

Explanation:

Question 3@http://jayendrapatil.com/iam-role-identity-providers-federation/

</p></details><hr>

### Question 4:

Your company has recently extended its datacenter into a VPC on AWS to add burst computing capacity as needed Members of your Network Operations Center need to be able to go to the AWS Management Console and administer Amazon EC2 instances as necessary. You don’t want to create new IAM users for each NOC member and make those users sign in again to the AWS Management Console. Which option below will meet the needs for your NOC members? [PROFESSIONAL]

- A. Use OAuth 2.0 to retrieve temporary AWS security credentials to enable your NOC members to sign in to the AWS Management Console.
- B. Use Web Identity Federation to retrieve AWS temporary security credentials to enable your NOC members to sign in to the AWS Management Console.
- C. Use your on-premises SAML 2.O-compliant identity provider (IDP) to grant the NOC members federated access to the AWS Management Console via the AWS single sign-on (SSO) endpoint.
- D. Use your on-premises SAML 2.0-compliant identity provider (IDP) to retrieve temporary security credentials to enable NOC members to sign in to the AWS Management Console

<details><summary>Answer:</summary><p>
[C]

Categories:
[SES, IAM, EC2, VPC]

Explanation:

Question 4@http://jayendrapatil.com/iam-role-identity-providers-federation/

</p></details><hr>

### Question 5:

A corporate web application is deployed within an Amazon Virtual Private Cloud (VPC) and is connected to the corporate data center via an iPsec VPN. The application must authenticate against the on-premises LDAP server. After authentication, each logged-in user can only access an Amazon Simple Storage Space (S3) keyspace specific to that user. Which two approaches can satisfy these objectives? (Choose 2 answers) [PROFESSIONAL]

- A. Develop an identity broker that authenticates against IAM security Token service to assume a IAM role in order to get temporary AWS security credentials. The application calls the identity broker to get AWS temporary security credentials with access to the appropriate S3 bucket. 
- B. The application authenticates against LDAP and retrieves the name of an IAM role associated with the user. The application then calls the IAM Security Token Service to assume that IAM role. The application can use the temporary credentials to access the appropriate S3 bucket.
- C. Develop an identity broker that authenticates against LDAP and then calls IAM Security Token Service to get IAM federated user credentials The application calls the identity broker to get IAM federated user credentials with access to the appropriate S3 bucket.
- D. The application authenticates against LDAP the application then calls the AWS identity and Access Management (IAM) Security Token service to log in to IAM using the LDAP credentials the application can use the IAM temporary credentials to access the appropriate S3 bucket. 
- E. The application authenticates against IAM Security Token Service using the LDAP credentials the application uses those temporary AWS security credentials to access the appropriate S3 bucket. 

<details><summary>Answer:</summary><p>
[B, C]

Categories:
[S3, SES, IAM, VPC]

Explanation:

Question 5@http://jayendrapatil.com/iam-role-identity-providers-federation/

A: Needs to authenticate against LDAP and not IAM

B: Authenticates with LDAP and calls the AssumeRole

C: Custom Identity broker implementation, with authentication with LDAP and using federated token

D: Can’t login to IAM using LDAP credentials

E: Need to authenticate with LDAP

</p></details><hr>

### Question 6:

Company B is launching a new game app for mobile devices. Users will log into the game using their existing social media account to streamline data capture. Company B would like to directly save player data and scoring information from the mobile app to a DynamoDB table named Score Data When a user saves their game the progress data will be stored to the Game state S3 bucket. what is the best approach for storing data to DynamoDB and S3? [PROFESSIONAL]

- A. Use an EC2 Instance that is launched with an EC2 role providing access to the Score Data DynamoDB table and the GameState S3 bucket that communicates with the mobile app via web services.
- B. Use temporary security credentials that assume a role providing access to the Score Data DynamoDB table and the Game State S3 bucket using web identity federation
- C. Use Login with Amazon allowing users to sign in with an Amazon account providing the mobile app with access to the Score Data DynamoDB table and the Game State S3 bucket.
- D. Use an IAM user with access credentials assigned a role providing access to the Score Data DynamoDB table and the Game State S3 bucket for distribution with the mobile app.

<details><summary>Answer:</summary><p>
[B]

Categories:
[S3, IAM, EC2, DynamoDB]

Explanation:

Question 6@http://jayendrapatil.com/iam-role-identity-providers-federation/

</p></details><hr>

### Question 9:

Your fortune 500 company has under taken a TCO analysis evaluating the use of Amazon S3 versus acquiring more hardware The outcome was that all employees would be granted access to use Amazon S3 for storage of their personal documents. Which of the following will you need to consider so you can set up a solution that incorporates single sign-on from your corporate AD or LDAP directory and restricts access for each user to a designated user folder in a bucket? (Choose 3 Answers) [PROFESSIONAL]

- A. Setting up a federation proxy or identity provider
- B. Using AWS Security Token Service to generate temporary tokens
- C. Tagging each folder in the bucket
- D. Configuring IAM role
- E. Setting up a matching IAM user for every user in your corporate directory that needs access to a folder in the bucket

<details><summary>Answer:</summary><p>
[A, B, D]

Categories:
[S3, IAM]

Explanation:

Question 9@http://jayendrapatil.com/iam-role-identity-providers-federation/

</p></details><hr>

### Question 10:

An AWS customer is deploying a web application that is composed of a front-end running on Amazon EC2 and of confidential data that is stored on Amazon S3. The customer security policy that all access operations to this sensitive data must be authenticated and authorized by a centralized access management system that is operated by a separate security team. In addition, the web application team that owns and administers the EC2 web front-end instances is prohibited from having any ability to access the data that circumvents this centralized access management system. Which of the following configurations will support these requirements? [PROFESSIONAL]

- A. Encrypt the data on Amazon S3 using a CloudHSM that is operated by the separate security team. Configure the web application to integrate with the CloudHSM for decrypting approved data access operations for trusted end-users. 
- B. Configure the web application to authenticate end-users against the centralized access management system. Have the web application provision trusted users STS tokens entitling the download of approved data directly from Amazon S3
- C. Have the separate security team create and IAM role that is entitled to access the data on Amazon S3. Have the web application team provision their instances with this role while denying their IAM users access to the data on Amazon S3 
- D. Configure the web application to authenticate end-users against the centralized access management system using SAML. Have the end-users authenticate to IAM using their SAML token and download the approved data directly from S3. 

<details><summary>Answer:</summary><p>
[B]

Categories:
[S3, IAM, EC2]

Explanation:

Question 10@http://jayendrapatil.com/iam-role-identity-providers-federation/

A: S3 doesn’t integrate directly with CloudHSM, also there is no centralized access management system control

B: (Controlled access and admins cannot access the data as it needs authentication)

C: Web team would have access to the data

D: not the way SAML auth works and not sure if the centralized access management system is SAML complaint

</p></details><hr>

### Question 14:

The Marketing Director in your company asked you to create a mobile app that lets users post sightings of good deeds known as random acts of kindness in 80-character summaries. You decided to write the application in JavaScript so that it would run on the broadest range of phones, browsers, and tablets. Your application should provide access to Amazon DynamoDB to store the good deed summaries. Initial testing of a prototype shows that there aren’t large spikes in usage. Which option provides the most cost-effective and scalable architecture for this application? [PROFESSIONAL]

- A. Provide the JavaScript client with temporary credentials from the Security Token Service using a Token Vending Machine (TVM) on an EC2 instance to provide signed credentials mapped to an Amazon Identity and Access Management (IAM) user allowing DynamoDB puts and S3 gets. You serve your mobile application out of an S3 bucket enabled as a web site. Your client updates DynamoDB. (Single EC2 instance not a scalable architecture)
- B. Register the application with a Web Identity Provider like Amazon, Google, or Facebook, create an IAM role for that provider, and set up permissions for the IAM role to allow S3 gets and DynamoDB puts. You serve your mobile application out of an S3 bucket enabled as a web site. Your client updates DynamoDB.
- C. Provide the JavaScript client with temporary credentials from the Security Token Service using a Token Vending Machine (TVM) to provide signed credentials mapped to an IAM user allowing DynamoDB puts. You serve your mobile application out of Apache EC2 instances that are load-balanced and autoscaled. Your EC2 instances are configured with an IAM role that allows DynamoDB puts. Your server updates DynamoDB. (Is Scalable but Not cost effective)
- D. Register the JavaScript application with a Web Identity Provider like Amazon, Google, or Facebook, create an IAM role for that provider, and set up permissions for the IAM role to allow DynamoDB puts. You serve your mobile application out of Apache EC2 instances that are load-balanced and autoscaled. Your EC2 instances are configured with an IAM role that allows DynamoDB puts. Your server updates DynamoDB. (Is Scalable but Not cost effective)

<details><summary>Answer:</summary><p>
[B]

Categories:
[S3, IAM, EC2, DynamoDB]

Explanation:

Question 14@http://jayendrapatil.com/iam-role-identity-providers-federation/

B: (Can work with JavaScript SDK, is scalable and cost effective)

</p></details><hr>

### Question 1:

You require the ability to analyze a large amount of data, which is stored on Amazon S3 using Amazon Elastic Map Reduce. You are using the cc2.8xlarge instance type, who’s CPUs are mostly idle during processing. Which of the below would be the most cost efficient way to reduce the runtime of the job? [PROFESSIONAL]

- A. Create smaller files on Amazon S3.
- B. Add additional cc2.8xlarge instances by introducing a task group.
- C. Use smaller instances that have higher aggregate I/O performance.
- D. Create fewer, larger files on Amazon S3.

<details><summary>Answer:</summary><p>
[C]

Categories:
[S3, EMR]

Explanation:

Question 1@http://jayendrapatil.com/aws-emr-certification/

</p></details><hr>

### Question 3:

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

Question 3@http://jayendrapatil.com/aws-emr-certification/

A: Only Spot instances impacts performance

B: Combination of the Spot and reserved with guarantee performance and help reduce cost. Also, RRS would reduce cost and guarantee data integrity, which is different from data durability

C: Only Spot instances impacts performance

D: Spot instances impacts performance and Spot instance not available for Redshift

</p></details><hr>

### Question 4:

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

Question 4@http://jayendrapatil.com/aws-emr-certification/

B: Master and Core must be RI or On Demand. Cannot be Spot

C: Need better durability for ingest file. Spot instances can be used for task nodes for cost saving. RI will not provide cost saving in this case

D: Input should be in S3 standard, as re-ingesting the input data might end up being more costly then holding the data for limited time in standard S3

</p></details><hr>

### Question 5:

Your company sells consumer devices and needs to record the first activation of all sold devices. Devices are not activated until the information is written on a persistent database. Activation data is very important for your company and must be analyzed daily with a MapReduce job. The execution time of the data analysis process must be less than three hours per day. Devices are usually sold evenly during the year, but when a new device model is out, there is a predictable peak in activation’s, that is, for a few days there are 10 times or even 100 times more activation’s than in average day. Which of the following databases and analysis framework would you implement to better optimize costs and performance for this workload? [PROFESSIONAL]

- A. Amazon RDS and Amazon Elastic MapReduce with Spot instances.
- B. Amazon DynamoDB and Amazon Elastic MapReduce with Spot instances.
- C. Amazon RDS and Amazon Elastic MapReduce with Reserved instances.
- D. Amazon DynamoDB and Amazon Elastic MapReduce with Reserved instances

<details><summary>Answer:</summary><p>
[B]

Categories:
[SES, RDS, DynamoDB]

Explanation:

Question 5@http://jayendrapatil.com/aws-emr-certification/

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

### Question 2:

Your firm has uploaded a large amount of aerial image data to S3. In the past, in your on-premises environment, you used a dedicated group of servers to oaten process this data and used Rabbit MQ, an open source messaging system, to get job information to the servers. Once processed the data would go to tape and be shipped offsite. Your manager told you to stay with the current design, and leverage AWS archival storage and messaging services to minimize cost. Which is correct? [PROFESSIONAL]

- A. Use SQS for passing job messages, use Cloud Watch alarms to terminate EC2 worker instances when they become idle. Once data is processed, change the storage class of the S3 objects to Reduced Redundancy Storage.
- B. Setup Auto-Scaled workers triggered by queue depth that use spot instances to process messages in SQS. Once data is processed, change the storage class of the S3 objects to Reduced Redundancy Storage.
- C. Setup Auto-Scaled workers triggered by queue depth that use spot instances to process messages in SQS. Once data is processed, change the storage class of the S3 objects to Glacier.
- D. Use SNS to pass job messages use Cloud Watch alarms to terminate spot worker instances when they become idle. Once data is processed, change the storage class of the S3 object to Glacier.

<details><summary>Answer:</summary><p>
[C]

Categories:
[S3, SES, SQS, Glacier, EC2, SNS]

Explanation:

Question 2@http://jayendrapatil.com/aws-storage-options-whitepaper/

</p></details><hr>

### Question 3:

You are developing a new mobile application and are considering storing user preferences in AWS, which would provide a more uniform cross-device experience to users using multiple mobile devices to access the application. The preference data for each user is estimated to be 50KB in size. Additionally 5 million customers are expected to use the application on a regular basis. The solution needs to be cost-effective, highly available, scalable and secure, how would you design a solution to meet the above requirements? [PROFESSIONAL]

- A. Setup an RDS MySQL instance in 2 availability zones to store the user preference data. Deploy a public facing application on a server in front of the database to manage security and access credentials
- B. Setup a DynamoDB table with an item for each user having the necessary attributes to hold the user preferences. The mobile application will query the user preferences directly from the DynamoDB table. Utilize STS. Web Identity Federation, and DynamoDB Fine Grained Access Control to authenticate and authorize access
- C. Setup an RDS MySQL instance with multiple read replicas in 2 availability zones to store the user preference data .The mobile application will query the user preferences from the read replicas. Leverage the MySQL user management and access privilege system to manage security and access credentials.
- D. Store the user preference data in S3 Setup a DynamoDB table with an item for each user and an item attribute pointing to the user’ S3 object. The mobile application will retrieve the S3 URL from DynamoDB and then access the S3 object directly utilize STS, Web identity Federation, and S3 ACLs to authenticate and authorize access.

<details><summary>Answer:</summary><p>
[B]

Categories:
[S3, RDS, DynamoDB]

Explanation:

Question 3@http://jayendrapatil.com/aws-storage-options-whitepaper/

</p></details><hr>

### Question 4:

A company is building a voting system for a popular TV show, viewers would watch the performances then visit the show’s website to vote for their favorite performer. It is expected that in a short period of time after the show has finished the site will receive millions of visitors. The visitors will first login to the site using their Amazon.com credentials and then submit their vote. After the voting is completed the page will display the vote totals. The company needs to build the site such that can handle the rapid influx of traffic while maintaining good performance but also wants to keep costs to a minimum. Which of the design patterns below should they use? [PROFESSIONAL]

- A. Use CloudFront and an Elastic Load balancer in front of an auto-scaled set of web servers, the web servers will first can the Login With Amazon service to authenticate the user then process the users vote and store the result into a multi-AZ Relational Database Service instance.
- B. Use CloudFront and the static website hosting feature of S3 with the Javascript SDK to call the Login With Amazon service to authenticate the user, use IAM Roles to gain permissions to a DynamoDB table to store the users vote.
- C. Use CloudFront and an Elastic Load Balancer in front of an auto-scaled set of web servers, the web servers will first call the Login with Amazon service to authenticate the user, the web servers will process the users vote and store the result into a DynamoDB table using IAM Roles for EC2 instances to gain permissions to the DynamoDB table.
- D. Use CloudFront and an Elastic Load Balancer in front of an auto-scaled set of web servers, the web servers will first call the Login. With Amazon service to authenticate the user, the web servers would process the users vote and store the result into an SQS queue using IAM Roles for EC2 Instances to gain permissions to the SQS queue. A set of application servers will then retrieve the items from the queue and store the result into a DynamoDB table

<details><summary>Answer:</summary><p>
[D]

Categories:
[S3, RDS, CloudFront, IAM, SQS, EC2, EBS, DynamoDB]

Explanation:

Question 4@http://jayendrapatil.com/aws-storage-options-whitepaper/

</p></details><hr>

### Question 5:

A large real-estate brokerage is exploring the option to adding a cost-effective location-based alert to their existing mobile application. The application backend infrastructure currently runs on AWS. Users who opt in to this service will receive alerts on their mobile device regarding real-estate offers in proximity to their location. For the alerts to be relevant delivery time needs to be in the low minute count. The existing mobile app has 5 million users across the US. Which one of the following architectural suggestions would you make to the customer? [PROFESSIONAL]

- A. Mobile application will submit its location to a web service endpoint utilizing Elastic Load Balancing and EC2 instances. DynamoDB will be used to store and retrieve relevant offers. EC2 instances will communicate with mobile earners/device providers to push alerts back to mobile application. —
- B. Use AWS Direct Connect or VPN to establish connectivity with mobile carriers EC2 instances will receive the mobile applications location through carrier connection: RDS will be used to store and relevant offers. EC2 instances will communicate with mobile carriers to push alerts back to the mobile application
- C. Mobile application will send device location using SQS. EC2 instances will retrieve the relevant offers from DynamoDB. AWS Mobile Push will be used to send offers to the mobile application
- D. Mobile application will send device location using AWS Mobile Push. EC2 instances will retrieve the relevant offers from DynamoDB. EC2 instances will communicate with mobile carriers/device providers to push alerts back to the mobile application.

<details><summary>Answer:</summary><p>
[C]

Categories:
[RDS, SQS, EC2, DynamoDB, ELB, Direct Connect]

Explanation:

Question 5@http://jayendrapatil.com/aws-storage-options-whitepaper/

</p></details><hr>

### Question 6:

You are running a news website in the eu-west-1 region that updates every 15 minutes. The website has a worldwide audience and it uses an Auto Scaling group behind an Elastic Load Balancer and an Amazon RDS database. Static content resides on Amazon S3, and is distributed through Amazon CloudFront. Your Auto Scaling group is set to trigger a scale up event at 60% CPU utilization; you use an Amazon RDS extra-large DB instance with 10.000 Provisioned IOPS its CPU utilization is around 80%. While freeable memory is in the 2 GB range. Web analytics reports show that the average load time of your web pages is around 1.5 to 2 seconds, but your SEO consultant wants to bring down the average load time to under 0.5 seconds. How would you improve page load times for your users? (Choose 3 answers) [PROFESSIONAL]

- A. Lower the scale up trigger of your Auto Scaling group to 30% so it scales more aggressively.
- B. Add an Amazon ElastiCache caching layer to your application for storing sessions and frequent DB queries
- C. Configure Amazon CloudFront dynamic content support to enable caching of re-usable content from your site
- D. Switch Amazon RDS database to the high memory extra-large Instance type
- E. Set up a second installation in another region, and use the Amazon Route 53 latency-based routing feature to select the right region.

<details><summary>Answer:</summary><p>
[B, C, D]

Categories:
[S3, SES, RDS, CloudFront, ASG, ElastiCache, EBS, Route 53]

Explanation:

Question 6@http://jayendrapatil.com/aws-storage-options-whitepaper/

</p></details><hr>

### Question 7:

A read only news reporting site with a combined web and application tier and a database tier that receives large and unpredictable traffic demands must be able to respond to these traffic fluctuations automatically. What AWS services should be used meet these requirements? [PROFESSIONAL]

- A. Stateless instances for the web and application tier synchronized using ElastiCache Memcached in an autoscaling group monitored with CloudWatch. And RDS with read replicas.
- B. Stateful instances for the web and application tier in an autoscaling group monitored with CloudWatch and RDS with read replicas
- C. Stateful instances for the web and application tier in an autoscaling group monitored with CloudWatch. And multi-AZ RDS
- D. Stateless instances for the web and application tier synchronized using ElastiCache Memcached in an autoscaling group monitored with CloudWatch and multi-AZ RDS

<details><summary>Answer:</summary><p>
[A]

Categories:
[RDS, CloudWatch, ElastiCache]

Explanation:

Question 7@http://jayendrapatil.com/aws-storage-options-whitepaper/

</p></details><hr>

### Question 8:

You have a periodic Image analysis application that gets some files as input, analyzes them and for each file writes some data in output to a ten file. The number of files in input per day is high and concentrated in a few hours of the day. Currently you have a server on EC2 with a large EBS volume that hosts the input data and the results it takes almost 20 hours per day to complete the process. What services could be used to reduce the elaboration time and improve the availability of the solution? [PROFESSIONAL]

- A. S3 to store I/O files. SQS to distribute elaboration commands to a group of hosts working in parallel. Auto scaling to dynamically size the group of hosts depending on the length of the SQS queue
- B. EBS with Provisioned IOPS (PIOPS) to store I/O files. SNS to distribute elaboration commands to a group of hosts working in parallel Auto Scaling to dynamically size the group of hosts depending on the number of SNS notifications
- C. S3 to store I/O files, SNS to distribute evaporation commands to a group of hosts working in parallel. Auto scaling to dynamically size the group of hosts depending on the number of SNS notifications
- D. EBS with Provisioned IOPS (PIOPS) to store I/O files SOS to distribute elaboration commands to a group of hosts working in parallel Auto Scaling to dynamically size the group to hosts depending on the length of the SQS queue.

<details><summary>Answer:</summary><p>
[A]

Categories:
[S3, SQS, EC2, ASG, EBS, SNS]

Explanation:

Question 8@http://jayendrapatil.com/aws-storage-options-whitepaper/

</p></details><hr>

### Question 9:

A 3-tier e-commerce web application is current deployed on-premises and will be migrated to AWS for greater scalability and elasticity. The web server currently shares read-only data using a network distributed file system The app server tier uses a clustering mechanism for discovery and shared session state that depends on IP multicast The database tier uses shared-storage clustering to provide database fail over capability, and uses several read slaves for scaling. Data on all servers and the distributed file system directory is backed up weekly to off-site tapes. Which AWS storage and database architecture meets the requirements of the application? [PROFESSIONAL]

- A. Web servers store read-only data in S3, and copy from S3 to root volume at boot time. App servers share state using a combination of DynamoDB and IP unicast. Database use RDS with multi-AZ deployment and one or more Read Replicas. Backup web and app servers backed up weekly via AMIs, database backed up via DB snapshots.
- B. Web servers store read-only data in S3, and copy from S3 to root volume at boot time. App servers share state using a combination of DynamoDB and IP unicast. Database use RDS with multi-AZ deployment and one or more Read replicas. Backup web servers app servers, and database backed up weekly to Glacier using snapshots 
- C. Web servers store read-only data in S3 and copy from S3 to root volume at boot time. App servers share state using a combination of DynamoDB and IP unicast. Database use RDS with multi-AZ deployment. Backup web and app servers backed up weekly via AMIs. Database backed up via DB snapshots 
- D. Web servers, store read-only data in an EC2 NFS server, mount to each web server at boot time App servers share state using a combination of DynamoDB and IP multicast Database use RDS with multi-AZ deployment and one or more Read Replicas Backup web and app servers backed up weekly via AMIs database backed up via DB snapshots 

<details><summary>Answer:</summary><p>
[]

Categories:
[S3, SES, RDS, Glacier, EC2, DynamoDB]

Explanation:

Question 9@http://jayendrapatil.com/aws-storage-options-whitepaper/

B: Snapshots to Glacier don’t work directly with EBS snapshots

C: Need Read replicas for scalability and elasticity

D: IP multicast not available in AWS

</p></details><hr>

### Question 10:

Our company is getting ready to do a major public announcement of a social media site on AWS. The website is running on EC2 instances deployed across multiple Availability Zones with a Multi-AZ RDS MySQL Extra Large DB Instance. The site performs a high number of small reads and writes per second and relies on an eventual consistency model. After comprehensive tests you discover that there is read contention on RDS MySQL. Which are the best approaches to meet these requirements? (Choose 2 answers) [PROFESSIONAL]

- A. Deploy ElasticCache in-memory cache running in each availability zone
- B. Implement sharding to distribute load to multiple RDS MySQL instances 
- C. Increase the RDS MySQL Instance size and Implement provisioned IOPS 
- D. Add an RDS MySQL read replica in each availability zone

<details><summary>Answer:</summary><p>
[A, D]

Categories:
[RDS, EC2, EBS]

Explanation:

Question 10@http://jayendrapatil.com/aws-storage-options-whitepaper/

B: Would distributed read write both, focus is on read contention

C: Would distributed read write both, focus is on read contention

</p></details><hr>

### Question 11:

Run 2-tier app with the following: an ELB, three web app server on EC2, and 1 MySQL RDS db. With grown load, db queries take longer and longer and slow down the overall response time for user request. What Options could speed up performance? (Choose 3) [PROFESSIONAL]

- A. Create an RDS read-replica and redirect half of the database read request to it
- B. Cache database queries in amazon ElastiCache
- C. Setup RDS in multi-availability zone mode.
- D. Shard the database and distribute loads between shards.
- E. Use amazon CloudFront to cache database queries.

<details><summary>Answer:</summary><p>
[A, B, D]

Categories:
[RDS, CloudFront, EC2, ElastiCache, ELB]

Explanation:

Question 11@http://jayendrapatil.com/aws-storage-options-whitepaper/

</p></details><hr>

### Question 12:

You have a web application leveraging an Elastic Load Balancer (ELB) In front of the web servers deployed using an Auto Scaling Group Your database is running on Relational Database Service (RDS) The application serves out technical articles and responses to them in general there are more views of an article than there are responses to the article. On occasion, an article on the site becomes extremely popular resulting in significant traffic Increases that causes the site to go down. What could you do to help alleviate the pressure on the infrastructure while maintaining availability during these events? Choose 3 answers [PROFESSIONAL]

- A. Leverage CloudFront for the delivery of the articles.
- B. Add RDS read-replicas for the read traffic going to your relational database
- C. Leverage Elastic Cache for caching the most frequently used data.
- D. Use SQS to queue up the requests for the technical posts and deliver them out of the queue 
- E. Use Route53 health checks to fail over to an S3 bucket for an error page 

<details><summary>Answer:</summary><p>
[A, B, C]

Categories:
[S3, SES, RDS, CloudFront, SQS, ASG, ELB]

Explanation:

Question 12@http://jayendrapatil.com/aws-storage-options-whitepaper/

D: does not process and would not be real time

E: more of an error handling then availability

</p></details><hr>

### Question 13:

Your website is serving on-demand training videos to your workforce. Videos are uploaded monthly in high resolution MP4 format. Your workforce is distributed globally often on the move and using company-provided tablets that require the HTTP Live Streaming (HLS) protocol to watch a video. Your company has no video transcoding expertise and it required you might need to pay for a consultant. How do you implement the most cost-efficient architecture without compromising high availability and quality of video delivery? [PROFESSIONAL]

- A. Elastic Transcoder to transcode original high-resolution MP4 videos to HLS. S3 to host videos with lifecycle Management to archive original flies to Glacier after a few days. CloudFront to serve HLS transcoded videos from S3
- B. A video transcoding pipeline running on EC2 using SQS to distribute tasks and Auto Scaling to adjust the number or nodes depending on the length of the queue S3 to host videos with Lifecycle Management to archive all files to Glacier after a few days CloudFront to serve HLS transcoding videos from Glacier
- C. Elastic Transcoder to transcode original high-resolution MP4 videos to HLS EBS volumes to host videos and EBS snapshots to incrementally backup original rues after a few days. CloudFront to serve HLS transcoded videos from EC2.
- D. A video transcoding pipeline running on EC2 using SQS to distribute tasks and Auto Scaling to adjust the number of nodes depending on the length of the queue. EBS volumes to host videos and EBS snapshots to incrementally backup original files after a few days. CloudFront to serve HLS transcoded videos from EC2

<details><summary>Answer:</summary><p>
[A]

Categories:
[S3, CloudFront, SQS, Glacier, EC2, ASG, Elastic Transcoder, EBS]

Explanation:

Question 13@http://jayendrapatil.com/aws-storage-options-whitepaper/

A: Elastic Transcoder for High quality, S3 to host videos cheaply, Glacier for archives and CloudFront for high availability

</p></details><hr>

### Question 14:

To meet regulatory requirements, a pharmaceuticals company needs to archive data after a drug trial test is concluded. Each drug trial test may generate up to several thousands of files, with compressed file sizes ranging from 1 byte to 100MB. Once archived, data rarely needs to be restored, and on the rare occasion when restoration is needed, the company has 24 hours to restore specific files that match certain metadata. Searches must be possible by numeric file ID, drug name, participant names, date ranges, and other metadata. Which is the most cost-effective architectural approach that can meet the requirements? [PROFESSIONAL]

- A. Store individual files in Amazon Glacier, using the file ID as the archive name. When restoring data, query the Amazon Glacier vault for files matching the search criteria. 
- B. Store individual files in Amazon S3, and store search metadata in an Amazon Relational Database Service (RDS) multi-AZ database. Create a lifecycle rule to move the data to Amazon Glacier after a certain number of days. When restoring data, query the Amazon RDS database for files matching the search criteria, and move the files matching the search criteria back to S3 Standard class. 
- C. Store individual files in Amazon Glacier, and store the search metadata in an Amazon RDS multi-AZ database. When restoring data, query the Amazon RDS database for files matching the search criteria, and retrieve the archive name that matches the file ID returned from the database query. 
- D. First, compress and then concatenate all files for a completed drug trial test into a single Amazon Glacier archive. Store the associated byte ranges for the compressed files along with other search metadata in an Amazon RDS database with regular snapshotting. When restoring data, query the database for files that match the search criteria, and create restored files from the retrieved byte ranges.
- E. Store individual compressed files and search metadata in Amazon Simple Storage Service (S3). Create a lifecycle rule to move the data to Amazon Glacier, after a certain number of days. When restoring data, query the Amazon S3 bucket for files matching the search criteria, and retrieve the file to S3 reduced redundancy in order to move it back to S3 Standard class. 

<details><summary>Answer:</summary><p>
[D]

Categories:
[S3, RDS, Glacier]

Explanation:

Question 14@http://jayendrapatil.com/aws-storage-options-whitepaper/

A: Individual files are expensive and does not allow searching by participant names etc

B: As the data is not needed can be stored to Glacier directly and the data need not be moved back to S3 standard

C: Individual files and Multi-AZ is expensive

E: Once the data is moved from S3 to Glacier the metadata is lost, as Glacier does not have metadata and must be maintained externally

</p></details><hr>

### Question 15:

A document storage company is deploying their application to AWS and changing their business model to support both free tier and premium tier users. The premium tier users will be allowed to store up to 200GB of data and free tier customers will be allowed to store only 5GB. The customer expects that billions of files will be stored. All users need to be alerted when approaching 75 percent quota utilization and again at 90 percent quota use. To support the free tier and premium tier users, how should they architect their application? [PROFESSIONAL]

- A. The company should utilize an amazon simple work flow service activity worker that updates the users data counter in amazon dynamo DB. The activity worker will use simple email service to send an email if the counter increases above the appropriate thresholds.
- B. The company should deploy an amazon relational data base service relational database with a store objects table that has a row for each stored object along with size of each object. The upload server will query the aggregate consumption of the user in questions by first determining the files store by the user, and then querying the stored objects table for respective file sizes) and send an email via amazon simple email service if the thresholds are breached.
- C. The company should write both the content length and the username of the files owner as S3 metadata for the object. They should then create a file watcher to iterate over each object and aggregate the size for each user and send a notification via amazon simple queue service to an emailing service if the storage threshold is exceeded.
- D. The company should create two separated amazon simple storage service buckets one for data storage for free tier users and another for data storage for premium tier users. An amazon simple workflow service activity worker will query all objects for a given user based on the bucket the data is stored

<details><summary>Answer:</summary><p>
[A]

Categories:
[S3, SES, SWF, SQS]

Explanation:

Question 15@http://jayendrapatil.com/aws-storage-options-whitepaper/

</p></details><hr>

### Question 16:

Your company has been contracted to develop and operate a website that tracks NBA basketball statistics. Statistical data to derive reports like “best game-winning shots from the regular season” and more frequently built reports like “top shots of the game” need to be stored durably for repeated lookup. Leveraging social media techniques, NBA fans submit and vote on new report types from the existing data set so the system needs to accommodate variability in data queries and new static reports must be generated and posted daily. Initial research in the design phase indicates that there will be over 3 million report queries on game day by end users and other applications that use this application as a data source. It is expected that this system will gain in popularity over time and reach peaks of 10-15 million report queries of the system on game days. Select the answer that will allow your application to best meet these requirements while minimizing costs. [PROFESSIONAL]

- A. Launch a multi-AZ MySQL Amazon Relational Database Service (RDS) Read Replica connected to your multi AZ master database and generate reports by querying the Read Replica. Perform a daily table cleanup.
- B. Implement a multi-AZ MySQL RDS deployment and have the application generate reports from Amazon ElastiCache for in-memory performance results. Utilize the default expire parameter for items in the cache.
- C. Generate reports from a multi-AZ MySQL Amazon RDS deployment and have an offline task put reports in Amazon Simple Storage Service (S3) and use CloudFront to cache the content. Use a TTL to expire objects daily.
- D. Query a multi-AZ MySQL RDS instance and store the results in a DynamoDB table. Generate reports from the DynamoDB table. Remove stale tables daily.

<details><summary>Answer:</summary><p>
[C]

Categories:
[S3, RDS, CloudFront, ElastiCache, EBS, DynamoDB]

Explanation:

Question 16@http://jayendrapatil.com/aws-storage-options-whitepaper/

C: Offline task with S3 storage and CloudFront cache

</p></details><hr>

### Question 1:

You are moving an existing traditional system to AWS, and during the migration discover that there is a master server which is a single point of failure. Having examined the implementation of the master server you realize there is not enough time during migration to re-engineer it to be highly available, though you do discover that it stores its state in a local MySQL database. In order to minimize down-time you select RDS to replace the local database and configure master to use it, what steps would best allow you to create a self-healing architecture[PROFESSIONAL]

- A. Migrate the local database into multi-AWS RDS database. Place master node into a multi-AZ auto-scaling group with a minimum of one and maximum of one with health checks.
- B. Replicate the local database into a RDS read replica. Place master node into a Cross-Zone ELB with a minimum of one and maximum of one with health checks. 
- C. Migrate the local database into multi-AWS RDS database. Place master node into a Cross-Zone ELB with a minimum of one and maximum of one with health checks. 
- D. Replicate the local database into a RDS read replica. Place master node into a multi-AZ auto-scaling group with a minimum of one and maximum of one with health checks. 

<details><summary>Answer:</summary><p>
[A]

Categories:
[RDS, ELB]

Explanation:

Question 1@http://jayendrapatil.com/aws-high-availability-fault-tolerance-architecture-certification/

B: Read Replica does not provide HA and write capability and ELB does not have feature for Min and Max 1 and Cross Zone allows just the equal distribution of load across instances

C: ELB does not have feature for Min and Max 1 and Cross Zone allows just the equal distribution of load across instances

D: Read Replica does not provide HA and write capability

</p></details><hr>

### Question 3:

When deploying a highly available 2-tier web application on AWS, which combination of AWS services meets the requirements? 1. AWS Direct Connect 2. Amazon Route 53 3. AWS Storage Gateway 4. Elastic Load Balancing 4. Amazon EC2 5. Auto scaling 6. Amazon VPC 7. AWS Cloud Trail [PROFESSIONAL]

- A. 2,4,5 and 6
- B. 3,4,5 and 8
- C. 1 through 8
- D. 1,3,5 and 7
- E. 1,2,5 and 6

<details><summary>Answer:</summary><p>
[A]

Categories:
[EC2, Storage Gateway, ASG, VPC, Route 53, ELB, Direct Connect]

Explanation:

Question 3@http://jayendrapatil.com/aws-high-availability-fault-tolerance-architecture-certification/

</p></details><hr>

### Question 4:

Company A has hired you to assist with the migration of an interactive website that allows registered users to rate local restaurants. Updates to the ratings are displayed on the home page, and ratings are updated in real time. Although the website is not very popular today, the company anticipates that It will grow rapidly over the next few weeks. They want the site to be highly available. The current architecture consists of a single Windows Server 2008 R2 web server and a MySQL database running on Linux. Both reside inside an on -premises hypervisor. What would be the most efficient way to transfer the application to AWS, ensuring performance and high-availability? [PROFESSIONAL]

- A. Export web files to an Amazon S3 bucket in us-west-1. Run the website directly out of Amazon S3. Launch a multi-AZ MySQL Amazon RDS instance in us-west-1a. Import the data into Amazon RDS from the latest MySQL backup. Use Route 53 and create an alias record pointing to the elastic load balancer. 
- B. Launch two Windows Server 2008 R2 instances in us-west-1b and two in us-west-1a. Copy the web files from on premises web server to each Amazon EC2 web server, using Amazon S3 as the repository. Launch a multi-AZ MySQL Amazon RDS instance in us-west-2a. Import the data into Amazon RDS from the latest MySQL backup. Create an elastic load balancer to front your web servers. Use Route 53 and create an alias record pointing to the elastic load balancer.
- C. Use AWS VM Import/Export to create an Amazon Elastic Compute Cloud (EC2) Amazon Machine Image (AMI) of the web server. Configure Auto Scaling to launch two web servers in us-west-1a and two in us-west-1b. Launch a Multi-AZ MySQL Amazon Relational Database Service (RDS) instance in us-west-1b. Import the data into Amazon RDS from the latest MySQL backup. Use Amazon Route 53 to create a hosted zone and point an A record to the elastic load balancer. 
- D. Use AWS VM Import/Export to create an Amazon EC2 AMI of the web server. Configure auto-scaling to launch two web servers in us-west-1a and two in us-west-1b. Launch a multi-AZ MySQL Amazon RDS instance in us-west-1a. Import the data into Amazon RDS from the latest MySQL backup. Create an elastic load balancer to front your web servers. Use Amazon Route 53 and create an A record pointing to the elastic load balancer. 

<details><summary>Answer:</summary><p>
[B]

Categories:
[S3, SES, RDS, EC2, ASG, EBS, Route 53]

Explanation:

Question 4@http://jayendrapatil.com/aws-high-availability-fault-tolerance-architecture-certification/

A: Its an Interactive website, although it can be implemented using Javascript SDK, its a migration and the application would need changes. Also no use of ELB if hosted on S3 Its an Interactive website, although it can be implemented using Javascript SDK, its a migration and the application would need changes. Also no use of ELB if hosted on S3

B: Although RDS instance is in a different region which will impact performance, this is the only option that works.

C: does not create a load balancer

D: Need to create a aliased record without which the Route 53 pointing to ELB would not work

</p></details><hr>

### Question 5:

Your company runs a customer facing event registration site. This site is built with a 3-tier architecture with web and application tier servers and a MySQL database. The application requires 6 web tier servers and 6 application tier servers for normal operation, but can run on a minimum of 65% server capacity and a single MySQL database. When deploying this application in a region with three availability zones (AZs) which architecture provides high availability? [PROFESSIONAL]

- A. A web tier deployed across 2 AZs with 3 EC2 (Elastic Compute Cloud) instances in each AZ inside an Auto Scaling Group behind an ELB (elastic load balancer), and an application tier deployed across 2 AZs with 3 EC2 instances in each AZ inside an Auto Scaling Group behind an ELB. and one RDS (Relational Database Service) instance deployed with read replicas in the other AZ.
- B. A web tier deployed across 3 AZs with 2 EC2 (Elastic Compute Cloud) instances in each AZ inside an Auto Scaling Group behind an ELB (elastic load balancer) and an application tier deployed across 3 AZs with 2 EC2 instances in each AZ inside an Auto Scaling Group behind an ELB and one RDS (Relational Database Service) Instance deployed with read replicas in the two other AZs.
- C. A web tier deployed across 2 AZs with 3 EC2 (Elastic Compute Cloud) instances in each AZ inside an Auto Scaling Group behind an ELB (elastic load balancer) and an application tier deployed across 2 AZs with 3 EC2 instances m each AZ inside an Auto Scaling Group behind an ELS and a Multi-AZ RDS (Relational Database Service) deployment.
- D. A web tier deployed across 3 AZs with 2 EC2 (Elastic Compute Cloud) instances in each AZ Inside an Auto Scaling Group behind an ELB (elastic load balancer). And an application tier deployed across 3 AZs with 2 EC2 instances in each AZ inside an Auto Scaling Group behind an ELB. And a Multi-AZ RDS (Relational Database services) deployment.

<details><summary>Answer:</summary><p>
[D]

Categories:
[RDS, EC2, ASG, ELB]

Explanation:

Question 5@http://jayendrapatil.com/aws-high-availability-fault-tolerance-architecture-certification/

</p></details><hr>

### Question 6:

For a 3-tier, customer facing, inclement weather site utilizing a MySQL database running in a Region which has two AZs which architecture provides fault tolerance within the region for the application that minimally requires 6 web tier servers and 6 application tier servers running in the web and application tiers and one MySQL database? [PROFESSIONAL]

- A. A web tier deployed across 2 AZs with 6 EC2 (Elastic Compute Cloud) instances in each AZ inside an Auto Scaling Group behind an ELB (elastic load balancer), and an application tier deployed across 2 AZs with 6 EC2 instances in each AZ inside an Auto Scaling Group behind an ELB. and a Multi-AZ RDS (Relational Database Service) deployment.
- B. A web tier deployed across 2 AZs with 3 EC2 (Elastic Compute Cloud) instances in each A2 inside an Auto Scaling Group behind an ELB (elastic load balancer) and an application tier deployed across 2 AZs with 3 EC2 instances in each AZ inside an Auto Scaling Group behind an ELB and a Multi-AZ RDS (Relational Database Service) deployment.
- C. A web tier deployed across 2 AZs with 3 EC2 (Elastic Compute Cloud) instances in each AZ inside an Auto Scaling Group behind an ELB (elastic load balancer) and an application tier deployed across 2 AZs with 6 EC2 instances in each AZ inside an Auto Scaling Group behind an ELB and one RDS (Relational Database Service) Instance deployed with read replicas in the other AZs.
- D. A web tier deployed across 1 AZs with 6 EC2 (Elastic Compute Cloud) instances in each AZ Inside an Auto Scaling Group behind an ELB (elastic load balancer). And an application tier deployed in the same AZs with 6 EC2 instances inside an Auto scaling group behind an ELB and a Multi-AZ RDS (Relational Database services) deployment, with 6 stopped web tier EC2 instances and 6 stopped application tier EC2 instances all in the other AZ ready to be started if any of the running instances in the first AZ fails.

<details><summary>Answer:</summary><p>
[A]

Categories:
[RDS, EC2, ASG, ELB]

Explanation:

Question 6@http://jayendrapatil.com/aws-high-availability-fault-tolerance-architecture-certification/

A: As it needs Fault Tolerance with minimal 6 servers always available

</p></details><hr>

### Question 8:

You need your API backed by DynamoDB to stay online during a total regional AWS failure. You can tolerate a couple minutes of lag or slowness during a large failure event, but the system should recover with normal operation after those few minutes. What is a good approach? [PROFESSIONAL]

- A. Set up DynamoDB cross-region replication in a master-standby configuration, with a single standby in another region. Create an Auto Scaling Group behind an ELB in each of the two regions DynamoDB is running in. Add a Route53 Latency DNS Record with DNS Failover, using the ELBs in the two regions as the resource records.
- B. Set up a DynamoDB Multi-Region table. Create an Auto Scaling Group behind an ELB in each of the two regions DynamoDB is running in. Add a Route53 Latency DNS Record with DNS Failover, using the ELBs in the two regions as the resource records. 
- C. Set up a DynamoDB Multi-Region table. Create a cross-region ELB pointing to a cross-region Auto Scaling Group, and direct a Route53 Latency DNS Record with DNS Failover to the cross-region ELB. 
- D. Set up DynamoDB cross-region replication in a master-standby configuration, with a single standby in another region. Create a cross-region ELB pointing to a cross-region Auto Scaling Group, and direct a Route53 Latency DNS Record with DNS Failover to the cross-region ELB. 

<details><summary>Answer:</summary><p>
[A]

Categories:
[RDS, ASG, DynamoDB, ELB]

Explanation:

Question 8@http://jayendrapatil.com/aws-high-availability-fault-tolerance-architecture-certification/

A: http://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Streams.CrossRegionRepl.html

A: Use DynamoDB cross-regional replication version with two ELBs and ASGs with Route53 Failover and Latency DNS

B: No such thing as DynamoDB Multi-Region table before. However, global tables have been now introduced.

C: No such thing as Cross Region ELB or cross-region ASG

D: No such thing as DynamoDB cross-region table or cross-region ELB

</p></details><hr>

### Question 10:

A development team that is currently doing a nightly six-hour build which is lengthening over time on-premises with a large and mostly under utilized server would like to transition to a continuous integration model of development on AWS with multiple builds triggered within the same day. However, they are concerned about cost, security and how to integrate with existing on-premises applications such as their LDAP and email servers, which cannot move off-premises. The development environment needs a source code repository; a project management system with a MySQL database resources for performing the builds and a storage location for QA to pick up builds from. What AWS services combination would you recommend to meet the development team’s requirements? [PROFESSIONAL]

- A. A Bastion host Amazon EC2 instance running a VPN server for access from on-premises, Amazon EC2 for the source code repository with attached Amazon EBS volumes, Amazon EC2 and Amazon RDS MySQL for the project management system, EIP for the source code repository and project management system, Amazon SQL for a build queue, An Amazon Auto Scaling group of Amazon EC2 instances for performing builds and Amazon Simple Email Service for sending the build output. (Bastion is not for VPN connectivity also SES should not be used)
- B. An AWS Storage Gateway for connecting on-premises software applications with cloud-based storage securely, Amazon EC2 for the resource code repository with attached Amazon EBS volumes, Amazon EC2 and Amazon RDS MySQL for the project management system, EIPs for the source code repository and project management system, Amazon Simple Notification Service for a notification initiated build, An Auto Scaling group of Amazon EC2 instances for performing builds and Amazon S3 for the build output. (Storage Gateway does not provide secure connectivity, still needs VPN. SNS alone cannot handle builds)
- C. An AWS Storage Gateway for connecting on-premises software applications with cloud-based storage securely, Amazon EC2 for the resource code repository with attached Amazon EBS volumes, Amazon EC2 and Amazon RDS MySQL for the project management system, EIPs for the source code repository and project management system, Amazon SQS for a build queue, An Amazon Elastic Map Reduce (EMR) cluster of Amazon EC2 instances for performing builds and Amazon CloudFront for the build output. (Storage Gateway does not provide secure connectivity, still needs VPN. EMR is not ideal for performing builds as it needs normal EC2 instances)
- D. A VPC with a VPN Gateway back to their on-premises servers, Amazon EC2 for the source-code repository with attached Amazon EBS volumes, Amazon EC2 and Amazon RDS MySQL for the project management system, EIPs for the source code repository and project management system, SQS for a build queue, An Auto Scaling group of EC2 instances for performing builds and S3 for the build output.

<details><summary>Answer:</summary><p>
[D]

Categories:
[S3, SES, RDS, CloudFront, SQS, EC2, Storage Gateway, ASG, EBS, VPC, SNS, EMR]

Explanation:

Question 10@http://jayendrapatil.com/aws-high-availability-fault-tolerance-architecture-certification/

D: (VPN gateway is required for secure connectivity. SQS for build queue and EC2 for builds)

</p></details><hr>

