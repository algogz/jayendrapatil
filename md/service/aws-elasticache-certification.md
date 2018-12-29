### Question 1:

What does Amazon ElastiCache provide?

- A. A service by this name doesn’t exist. Perhaps you mean Amazon CloudCache.
- B. A virtual server with a huge amount of memory.
- C. A managed In-memory cache service
- D. An Amazon EC2 instance with the Memcached software already pre-installed.

<details><summary>Answer:</summary><p>
[C]

Categories:
[EC2, ElastiCache]

Explanation:

Question 1@http://jayendrapatil.com/aws-elasticache-certification/

</p></details><hr>

### Question 2:

You are developing a highly available web application using stateless web servers. Which services are suitable for storing session state data? Choose 3 answers.

- A. Elastic Load Balancing
- B. Amazon Relational Database Service (RDS)
- C. Amazon CloudWatch
- D. Amazon ElastiCache
- E. Amazon DynamoDB
- F. AWS Storage Gateway

<details><summary>Answer:</summary><p>
[B, D, E]

Categories:
[SES, RDS, Storage Gateway, CloudWatch, ElastiCache, DynamoDB, ELB]

Explanation:

Question 2@http://jayendrapatil.com/aws-elasticache-certification/

</p></details><hr>

### Question 3:

Which statement best describes ElastiCache?

- A. Reduces the latency by splitting the workload across multiple AZs
- B. A simple web services interface to create and store multiple data sets, query your data easily, and return the results
- C. Offload the read traffic from your database in order to reduce latency caused by read-heavy workload
- D. Managed service that makes it easy to set up, operate and scale a relational database in the cloud

<details><summary>Answer:</summary><p>
[C]

Categories:
[ElastiCache]

Explanation:

Question 3@http://jayendrapatil.com/aws-elasticache-certification/

</p></details><hr>

### Question 4:

Our company is getting ready to do a major public announcement of a social media site on AWS. The website is running on EC2 instances deployed across multiple Availability Zones with a Multi-AZ RDS MySQL Extra Large DB Instance. The site performs a high number of small reads and writes per second and relies on an eventual consistency model. After comprehensive tests you discover that there is read contention on RDS MySQL. Which are the best approaches to meet these requirements? (Choose 2 answers)

- A. Deploy ElastiCache in-memory cache running in each availability zone
- B. Implement sharding to distribute load to multiple RDS MySQL instances
- C. Increase the RDS MySQL Instance size and Implement provisioned IOPS
- D. Add an RDS MySQL read replica in each availability zone

<details><summary>Answer:</summary><p>
[A, D]

Categories:
[RDS, EC2, ElastiCache, EBS]

Explanation:

Question 4@http://jayendrapatil.com/aws-elasticache-certification/

</p></details><hr>

### Question 5:

You are using ElastiCache Memcached to store session state and cache database queries in your infrastructure. You notice in CloudWatch that Evictions and Get Misses are both very high. What two actions could you take to rectify this? Choose 2 answers

- A. Increase the number of nodes in your cluster
- B. Tweak the max_item_size parameter
- C. Shrink the number of nodes in your cluster
- D. Increase the size of the nodes in the cluster

<details><summary>Answer:</summary><p>
[A, D]

Categories:
[SES, CloudWatch, ElastiCache]

Explanation:

Question 5@http://jayendrapatil.com/aws-elasticache-certification/

</p></details><hr>

### Question 6:

You have been tasked with moving an ecommerce web application from a customer’s datacenter into a VPC. The application must be fault tolerant and well as highly scalable. Moreover, the customer is adamant that service interruptions not affect the user experience. As you near launch, you discover that the application currently uses multicast to share session state between web servers, In order to handle session state within the VPC, you choose to:

- A. Store session state in Amazon ElastiCache for Redis
- B. Create a mesh VPN between instances and allow multicast on it
- C. Store session state in Amazon Relational Database Service 
- D. Enable session stickiness via Elastic Load Balancing 

<details><summary>Answer:</summary><p>
[A]

Categories:
[SES, RDS, ElastiCache, VPC, ELB]

Explanation:

Question 6@http://jayendrapatil.com/aws-elasticache-certification/

A: scalable and makes the web applications stateless

C: RDS solution not highly scalable

D: affects user experience if the instance goes down

</p></details><hr>

### Question 7:

When you are designing to support a 24-hour flash sale, which one of the following methods best describes a strategy to lower the latency while keeping up with unusually heavy traffic?

- A. Launch enhanced networking instances in a placement group to support the heavy traffic 
- B. Apply Service Oriented Architecture (SOA) principles instead of a 3-tier architecture 
- C. Use Elastic Beanstalk to enable blue-green deployment 
- D. Use ElastiCache as in-memory storage on top of DynamoDB to store user sessions

<details><summary>Answer:</summary><p>
[D]

Categories:
[SES, ElastiCache, DynamoDB, Elastic Beanstalk]

Explanation:

Question 7@http://jayendrapatil.com/aws-elasticache-certification/

A: only improves internal communication

B: just simplifies architecture

C: only minimizes download for applications and ease of rollback

D: scalable, faster read/writes and in memory storage

</p></details><hr>

### Question 8:

You are configuring your company’s application to use Auto Scaling and need to move user state information. Which of the following AWS services provides a shared data store with durability and low latency?

- A. AWS ElastiCache Memcached 
- B. Amazon Simple Storage Service
- C. Amazon EC2 instance storage
- D. Amazon DynamoDB

<details><summary>Answer:</summary><p>
[D]

Categories:
[S3, EC2, ASG, ElastiCache, DynamoDB]

Explanation:

Question 8@http://jayendrapatil.com/aws-elasticache-certification/

A: does not provide durability as if the node is gone the data is gone

</p></details><hr>

### Question 9:

Your application is using an ELB in front of an Auto Scaling group of web/application servers deployed across two AZs and a Multi-AZ RDS Instance for data persistence. The database CPU is often above 80% usage and 90% of I/O operations on the database are reads. To improve performance you recently added a single-node Memcached ElastiCache Cluster to cache frequent DB query results. In the next weeks the overall workload is expected to grow by 30%. Do you need to change anything in the architecture to maintain the high availability for the application with the anticipated additional load and Why?

- A. You should deploy two Memcached ElastiCache Clusters in different AZs because the RDS Instance will not be able to handle the load if the cache node fails.
- B. If the cache node fails the automated ElastiCache node recovery feature will prevent any availability impact. 
- C. Yes you should deploy the Memcached ElastiCache Cluster with two nodes in the same AZ as the RDS DB master instance to handle the load if one cache node fails. 
- D. No if the cache node fails you can always get the same data from the DB without having any availability impact. 

<details><summary>Answer:</summary><p>
[A]

Categories:
[RDS, ASG, ElastiCache, ELB]

Explanation:

Question 9@http://jayendrapatil.com/aws-elasticache-certification/

B: does not provide high availability, as data is lost if the node is lost

C: Single AZ affects availability as DB is Multi AZ and would be overloaded is the AZ goes down

D: Will overload the database affecting availability

</p></details><hr>

### Question 10:

A read only news reporting site with a combined web and application tier and a database tier that receives large and unpredictable traffic demands must be able to respond to these traffic fluctuations automatically. What AWS services should be used meet these requirements?

- A. Stateless instances for the web and application tier synchronized using ElastiCache Memcached in an autoscaling group monitored with CloudWatch and RDS with read replicas.
- B. Stateful instances for the web and application tier in an autoscaling group monitored with CloudWatch and RDS with read replicas 
- C. Stateful instances for the web and application tier in an autoscaling group monitored with CloudWatch and multi-AZ RDS (
- D. Stateless instances for the web and application tier synchronized using ElastiCache Memcached in an autoscaling group monitored with CloudWatch and multi-AZ RDS 

<details><summary>Answer:</summary><p>
[A]

Categories:
[RDS, CloudWatch, ElastiCache]

Explanation:

Question 10@http://jayendrapatil.com/aws-elasticache-certification/

B: Stateful instances will not allow for scaling

C: Stateful instances will allow not for scaling & multi-AZ is for high availability and not scaling)

D: multi-AZ is for high availability and not scaling

</p></details><hr>

### Question 11:

You have written an application that uses the Elastic Load Balancing service to spread traffic to several web servers. Your users complain that they are sometimes forced to login again in the middle of using your application, after they have already logged in. This is not behavior you have designed. What is a possible solution to prevent this happening?

- A. Use instance memory to save session state.
- B. Use instance storage to save session state.
- C. Use EBS to save session state.
- D. Use ElastiCache to save session state.
- E. Use Glacier to save session slate.

<details><summary>Answer:</summary><p>
[D]

Categories:
[SES, Glacier, ElastiCache, EBS, ELB]

Explanation:

Question 11@http://jayendrapatil.com/aws-elasticache-certification/

</p></details><hr>

