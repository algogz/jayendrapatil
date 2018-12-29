### Question 1:

A user has configured an HTTPS listener on an ELB. The user has not configured any security policy which can help to negotiate SSL between the client and ELB. What will ELB do in this scenario?

- A. By default ELB will select the first version of the security policy
- B. By default ELB will select the latest version of the policy
- C. ELB creation will fail without a security policy
- D. It is not required to have a security policy since SSL is already installed

<details><summary>Answer:</summary><p>
[B]

Categories:
[ELB]

Explanation:

Question 1@http://jayendrapatil.com/aws-elastic-load-balancing/

</p></details><hr>

### Question 2:

A user has configured ELB with SSL using a security policy for secure negotiation between the client and load balancer. The ELB security policy supports various ciphers. Which of the below mentioned options helps identify the matching cipher at the client side to the ELB cipher list when client is requesting ELB DNS over SSL

- A. Cipher Protocol
- B. Client Configuration Preference
- C. Server Order Preference
- D. Load Balancer Preference

<details><summary>Answer:</summary><p>
[C]

Categories:
[ELB]

Explanation:

Question 2@http://jayendrapatil.com/aws-elastic-load-balancing/

</p></details><hr>

### Question 3:

A user has configured ELB with SSL using a security policy for secure negotiation between the client and load balancer. Which of the below mentioned security policies is supported by ELB?

- A. Dynamic Security Policy
- B. All the other options
- C. Predefined Security Policy
- D. Default Security Policy

<details><summary>Answer:</summary><p>
[C]

Categories:
[ELB]

Explanation:

Question 3@http://jayendrapatil.com/aws-elastic-load-balancing/

</p></details><hr>

### Question 4:

A user has configured ELB with SSL using a security policy for secure negotiation between the client and load balancer. Which of the below mentioned SSL protocols is not supported by the security policy?

- A. TLS 1.3
- B. TLS 1.2
- C. SSL 2.0
- D. SSL 3.0

<details><summary>Answer:</summary><p>
[A]

Categories:
[ELB]

Explanation:

Question 4@http://jayendrapatil.com/aws-elastic-load-balancing/

</p></details><hr>

### Question 5:

A user has configured ELB with a TCP listener at ELB as well as on the back-end instances. The user wants to enable a proxy protocol to capture the source and destination IP information in the header. Which of the below mentioned statements helps the user understand a proxy protocol with TCP configuration?

- A. If the end user is requesting behind a proxy server then the user should not enable a proxy protocol on ELB
- B. ELB does not support a proxy protocol when it is listening on both the load balancer and the back-end instances
- C. Whether the end user is requesting from a proxy server or directly, it does not make a difference for the proxy protocol
- D. If the end user is requesting behind the proxy then the user should add the “isproxy” flag to the ELB Configuration

<details><summary>Answer:</summary><p>
[A]

Categories:
[ELB]

Explanation:

Question 5@http://jayendrapatil.com/aws-elastic-load-balancing/

</p></details><hr>

### Question 6:

A user has enabled session stickiness with ELB. The user does not want ELB to manage the cookie; instead he wants the application to manage the cookie. What will happen when the server instance, which is bound to a cookie, crashes?

- A. The response will have a cookie but stickiness will be deleted
- B. The session will not be sticky until a new cookie is inserted
- C. ELB will throw an error due to cookie unavailability
- D. The session will be sticky and ELB will route requests to another server as ELB keeps replicating the Cookie

<details><summary>Answer:</summary><p>
[B]

Categories:
[SES, ELB]

Explanation:

Question 6@http://jayendrapatil.com/aws-elastic-load-balancing/

</p></details><hr>

### Question 7:

A user has created an ELB with Auto Scaling. Which of the below mentioned offerings from ELB helps the user to stop sending new requests traffic from the load balancer to the EC2 instance when the instance is being deregistered while continuing in-flight requests?

- A. ELB sticky session
- B. ELB deregistration check
- C. ELB connection draining
- D. ELB auto registration Off

<details><summary>Answer:</summary><p>
[C]

Categories:
[SES, EC2, ASG, ELB]

Explanation:

Question 7@http://jayendrapatil.com/aws-elastic-load-balancing/

</p></details><hr>

### Question 8:

When using an Elastic Load Balancer to serve traffic to web servers, which one of the following is true?

- A. Web servers must be publicly accessible
- B. The same security group must be applied to both the ELB and EC2 instances
- C. ELB and EC2 instance must be in the same subnet
- D. ELB and EC2 instances must be in the same VPC

<details><summary>Answer:</summary><p>
[D]

Categories:
[EC2, VPC, ELB]

Explanation:

Question 8@http://jayendrapatil.com/aws-elastic-load-balancing/

</p></details><hr>

### Question 9:

A user has configured Elastic Load Balancing by enabling a Secure Socket Layer (SSL) negotiation configuration known as a Security Policy. Which of the below mentioned options is not part of this secure policy while negotiating the SSL connection between the user and the client?

- A. SSL Protocols
- B. Client Order Preference
- C. SSL Ciphers
- D. Server Order Preference

<details><summary>Answer:</summary><p>
[B]

Categories:
[ELB]

Explanation:

Question 9@http://jayendrapatil.com/aws-elastic-load-balancing/

</p></details><hr>

### Question 10:

A user has created an ELB with the availability zone us-east-1. The user wants to add more zones to ELB to achieve High Availability. How can the user add more zones to the existing ELB?

- A. It is not possible to add more zones to the existing ELB
- B. Only option is to launch instances in different zones and add to ELB
- C. The user should stop the ELB and add zones and instances as required
- D. The user can add zones on the fly from the AWS console

<details><summary>Answer:</summary><p>
[D]

Categories:
[ELB]

Explanation:

Question 10@http://jayendrapatil.com/aws-elastic-load-balancing/

</p></details><hr>

### Question 11:

A user has launched an ELB which has 5 instances registered with it. The user deletes the ELB by mistake. What will happen to the instances?

- A. ELB will ask the user whether to delete the instances or not
- B. Instances will be terminated
- C. ELB cannot be deleted if it has running instances registered with it
- D. Instances will keep running

<details><summary>Answer:</summary><p>
[D]

Categories:
[ELB]

Explanation:

Question 11@http://jayendrapatil.com/aws-elastic-load-balancing/

</p></details><hr>

### Question 12:

A Sys-admin has created a shopping cart application and hosted it on EC2. The EC2 instances are running behind ELB. The admin wants to ensure that the end user request will always go to the EC2 instance where the user session has been created. How can the admin configure this?

- A. Enable ELB cross zone load balancing
- B. Enable ELB cookie setup
- C. Enable ELB sticky session
- D. Enable ELB connection draining

<details><summary>Answer:</summary><p>
[C]

Categories:
[SES, EC2, ELB]

Explanation:

Question 12@http://jayendrapatil.com/aws-elastic-load-balancing/

</p></details><hr>

### Question 13:

A user has setup connection draining with ELB to allow in-flight requests to continue while the instance is being deregistered through Auto Scaling. If the user has not specified the draining time, how long will ELB allow inflight requests traffic to continue?

- A. 600 seconds
- B. 3600 seconds
- C. 300 seconds
- D. 0 seconds

<details><summary>Answer:</summary><p>
[C]

Categories:
[ASG, ELB]

Explanation:

Question 13@http://jayendrapatil.com/aws-elastic-load-balancing/

</p></details><hr>

### Question 14:

A customer has a web application that uses cookie Based sessions to track logged in users. It is deployed on AWS using ELB and Auto Scaling. The customer observes that when load increases Auto Scaling launches new Instances but the load on the existing Instances does not decrease, causing all existing users to have a sluggish experience. Which two answer choices independently describe a behavior that could be the cause of the sluggish user experience?

- A. ELB’s normal behavior sends requests from the same user to the same backend instance 
- B. ELB’s behavior when sticky sessions are enabled causes ELB to send requests in the same session to the same backend
- C. A faulty browser is not honoring the TTL of the ELB DNS name 
- D. The web application uses long polling such as comet or websockets. Thereby keeping a connection open to a web server tor a long time

<details><summary>Answer:</summary><p>
[B, D]

Categories:
[SES, ASG, EBS, ELB]

Explanation:

Question 14@http://jayendrapatil.com/aws-elastic-load-balancing/

A: its not by default

C: DNS TTL would only impact the ELB instances if scaled and not the EC2 instances to which the traffic is routed

</p></details><hr>

### Question 15:

A customer has an online store that uses the cookie-based sessions to track logged-in customers. It is deployed on AWS using ELB and autoscaling. When the load increases, Auto scaling automatically launches new web servers, but the load on the web servers do not decrease. This causes the customers a poor experience. What could be causing the issue ?

- A. ELB DNS records Time to Live is set too high 
- B. ELB is configured to send requests with previously established sessions
- C. Website uses CloudFront which is keeping sessions alive
- D. New Instances are not being added to the ELB during the Auto Scaling cool down period

<details><summary>Answer:</summary><p>
[B]

Categories:
[SES, RDS, CloudFront, ASG, EBS, ELB]

Explanation:

Question 15@http://jayendrapatil.com/aws-elastic-load-balancing/

A: DNS TTL would only impact the ELB instances if scaled and not the EC2 instances to which the traffic is routed

</p></details><hr>

### Question 16:

You are designing a multi-platform web application for AWS. The application will run on EC2 instances and will be accessed from PCs, tablets and smart phones. Supported accessing platforms are Windows, MACOS, IOS and Android. Separate sticky session and SSL certificate setups are required for different platform types. Which of the following describes the most cost effective and performance efficient architecture setup?

- A. Setup a hybrid architecture to handle session state and SSL certificates on-prem and separate EC2 Instance groups running web applications for different platform types running in a VPC.
- B. Set up one ELB for all platforms to distribute load among multiple instance under it. Each EC2 instance implements all functionality for a particular platform.
- C. Set up two ELBs. The first ELB handles SSL certificates for all platforms and the second ELB handles session stickiness for all platforms for each ELB run separate EC2 instance groups to handle the web application for each platform.
- D. Assign multiple ELBs to an EC2 instance or group of EC2 instances running the common components of the web application, one ELB for each platform type. Session stickiness and SSL termination are done at the ELBs.

<details><summary>Answer:</summary><p>
[D]

Categories:
[SES, EC2, VPC, ELB]

Explanation:

Question 16@http://jayendrapatil.com/aws-elastic-load-balancing/

D: Session stickiness requires HTTPS listener with SSL termination on the ELB and ELB does not support multiple SSL certs so one is required for each cert

</p></details><hr>

### Question 17:

You are migrating a legacy client-server application to AWS. The application responds to a specific DNS domain (e.g. www.example.com) and has a 2-tier architecture, with multiple application servers and a database server. Remote clients use TCP to connect to the application servers. The application servers need to know the IP address of the clients in order to function properly and are currently taking that information from the TCP socket. A Multi-AZ RDS MySQL instance will be used for the database. During the migration you can change the application code but you have to file a change request. How would you implement the architecture on AWS in order to maximize scalability and high availability?

- A. File a change request to implement Proxy Protocol support In the application. Use an ELB with a TCP Listener and Proxy Protocol enabled to distribute load on two application servers in different AZs. 
- B. File a change request to Implement Cross-Zone support in the application. Use an ELB with a TCP Listener and Cross-Zone Load Balancing enabled, two application servers in different AZs.
- C. File a change request to implement Latency Based Routing support in the application. Use Route 53 with Latency Based Routing enabled to distribute load on two application servers in different AZs.
- D. File a change request to implement Alias Resource support in the application Use Route 53 Alias Resource Record to distribute load on two application servers in different AZs.

<details><summary>Answer:</summary><p>
[A]

Categories:
[RDS, Route 53, ELB]

Explanation:

Question 17@http://jayendrapatil.com/aws-elastic-load-balancing/

A: (ELB with TCP listener and proxy protocol will allow IP to be passed )

</p></details><hr>

### Question 18:

A user has created an ELB with three instances. How many security groups will ELB create by default?

- A. 3
- B. 5
- C. 2
- D. 1

<details><summary>Answer:</summary><p>
[C]

Categories:
[ELB]

Explanation:

Question 18@http://jayendrapatil.com/aws-elastic-load-balancing/

C: One for ELB to allow inbound and Outbound to listener and health check port of instances and One for the Instances to allow inbound from ELB

</p></details><hr>

### Question 19:

You have a web-style application with a stateless but CPU and memory-intensive web tier running on a cc2 8xlarge EC2 instance inside of a VPC The instance when under load is having problems returning requests within the SLA as defined by your business The application maintains its state in a DynamoDB table, but the data tier is properly provisioned and responses are consistently fast. How can you best resolve the issue of the application responses not meeting your SLA?

- A. Add another cc2 8xlarge application instance, and put both behind an Elastic Load Balancer
- B. Move the cc2 8xlarge to the same Availability Zone as the DynamoDB table 
- C. Cache the database responses in ElastiCache for more rapid access 
- D. Move the database from DynamoDB to RDS MySQL in scale-out read-replica configuration 

<details><summary>Answer:</summary><p>
[A]

Categories:
[SES, RDS, EC2, ElastiCache, VPC, DynamoDB]

Explanation:

Question 19@http://jayendrapatil.com/aws-elastic-load-balancing/

B: Does not improve the response time and performance

C: Data tier is responding fast

D: Data tier is responding fast

</p></details><hr>

### Question 20:

An organization has configured a VPC with an Internet Gateway (IGW). pairs of public and private subnets (each with one subnet per Availability Zone), and an Elastic Load Balancer (ELB) configured to use the public subnets. The applications web tier leverages the ELB, Auto Scaling and a Multi-AZ RDS database instance. The organization would like to eliminate any potential single points of failure in this design. What step should you take to achieve this organization’s objective?

- A. Nothing, there are no single points of failure in this architecture.
- B. Create and attach a second IGW to provide redundant internet connectivity. 
- C. Create and configure a second Elastic Load Balancer to provide a redundant load balancer. 
- D. Create a second multi-AZ RDS instance in another Availability Zone and configure replication to provide a redundant database. 

<details><summary>Answer:</summary><p>
[A]

Categories:
[RDS, ASG, VPC, ELB]

Explanation:

Question 20@http://jayendrapatil.com/aws-elastic-load-balancing/

B: VPC can be attached only 1 IGW

C: ELB scales by itself with multiple availability zones configured with it

D: Multi AZ requires 2 different AZ for setup and already has a standby

</p></details><hr>

### Question 21:

Your application currently leverages AWS Auto Scaling to grow and shrink as load Increases/ decreases and has been performing well. Your marketing team expects a steady ramp up in traffic to follow an upcoming campaign that will result in a 20x growth in traffic over 4 weeks. Your forecast for the approximate number of Amazon EC2 instances necessary to meet the peak demand is 175. What should you do to avoid potential service disruptions during the ramp up in traffic?

- A. Ensure that you have pre-allocated 175 Elastic IP addresses so that each server will be able to obtain one as it launches 
- B. Check the service limits in Trusted Advisor and adjust as necessary so the forecasted count remains within limits.
- C. Change your Auto Scaling configuration to set a desired capacity of 175 prior to the launch of the marketing campaign 
- D. Pre-warm your Elastic Load Balancer to match the requests per second anticipated during peak demand 

<details><summary>Answer:</summary><p>
[B]

Categories:
[SES, Trusted Advisor, EC2, ASG]

Explanation:

Question 21@http://jayendrapatil.com/aws-elastic-load-balancing/

A: max limit 5 EIP and a service request needs to be submitted

C: Will cause 175 instances to be launched and running but not gradually scale

D: Does not need pre warming as the load is increasing steadily

</p></details><hr>

### Question 22:

Which of the following features ensures even distribution of traffic to Amazon EC2 instances in multiple Availability Zones registered with a load balancer?

- A. Elastic Load Balancing request routing
- B. An Amazon Route 53 weighted routing policy 
- C. Elastic Load Balancing cross-zone load balancing
- D. An Amazon Route 53 latency routing policy 

<details><summary>Answer:</summary><p>
[C]

Categories:
[EC2, Route 53, ELB]

Explanation:

Question 22@http://jayendrapatil.com/aws-elastic-load-balancing/

B: does not control traffic to EC2 instance

D: does not control traffic to EC2 instance

</p></details><hr>

### Question 23:

Your web application front end consists of multiple EC2 instances behind an Elastic Load Balancer. You configured ELB to perform health checks on these EC2 instances, if an instance fails to pass health checks, which statement will be true?

- A. The instance gets terminated automatically by the ELB 
- B. The instance gets quarantined by the ELB for root cause analysis.
- C. The instance is replaced automatically by the ELB. 
- D. The ELB stops sending traffic to the instance that failed its health check

<details><summary>Answer:</summary><p>
[D]

Categories:
[EC2, ELB]

Explanation:

Question 23@http://jayendrapatil.com/aws-elastic-load-balancing/

A: it is done by Autoscaling

C: it is done by Autoscaling

</p></details><hr>

### Question 24:

You have a web application running on six Amazon EC2 instances, consuming about 45% of resources on each instance. You are using auto-scaling to make sure that six instances are running at all times. The number of requests this application processes is consistent and does not experience spikes. The application is critical to your business and you want high availability at all times. You want the load to be distributed evenly between all instances. You also want to use the same Amazon Machine Image (AMI) for all instances. Which of the following architectural choices should you make?

- A. Deploy 6 EC2 instances in one availability zone and use Amazon Elastic Load Balancer. 
- B. Deploy 3 EC2 instances in one region and 3 in another region and use Amazon Elastic Load Balancer. 
- C. Deploy 3 EC2 instances in one availability zone and 3 in another availability zone and use Amazon Elastic Load Balancer.
- D. Deploy 2 EC2 instances in three regions and use Amazon Elastic Load Balancer. 

<details><summary>Answer:</summary><p>
[C]

Categories:
[SES, EC2]

Explanation:

Question 24@http://jayendrapatil.com/aws-elastic-load-balancing/

A: Single AZ will not provide High Availability

B: Different region, AMI would not be available unless copied

D: Different region, AMI would not be available unless copied

</p></details><hr>

### Question 25:

You are designing an SSL/TLS solution that requires HTTPS clients to be authenticated by the Web server using client certificate authentication. The solution must be resilient. Which of the following options would you consider for configuring the web server infrastructure? (Choose 2 answers)

- A. Configure ELB with TCP listeners on TCP/443. And place the Web servers behind it.
- B. Configure your Web servers with EIPs. Place the Web servers in a Route53 Record Set and configure health checks against all Web servers.
- C. Configure ELB with HTTPS listeners, and place the Web servers behind it. 
- D. Configure your web servers as the origins for a CloudFront distribution. Use custom SSL certificates on your CloudFront distribution 

<details><summary>Answer:</summary><p>
[A, B]

Categories:
[CloudFront, ELB]

Explanation:

Question 25@http://jayendrapatil.com/aws-elastic-load-balancing/

A: terminate SSL on the instance using client-side certificate

B: Remove ELB and use Web Servers directly with Route 53

C: ELB with HTTPs does not support Client-Side certificates

D: http://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/RequestAndResponseBehaviorCustomOrigin.html#RequestCustomClientSideSslAuth

D: CloudFront Client-Side ssl certificates

</p></details><hr>

### Question 26:

You are designing an application that contains protected health information. Security and compliance requirements for your application mandate that all protected health information in the application use encryption at rest and in transit. The application uses a three-tier architecture where data flows through the load balancer and is stored on Amazon EBS volumes for processing, and the results are stored in Amazon S3 using the AWS SDK. Which of the following two options satisfy the security requirements? Choose 2 answers

- A. Use SSL termination on the load balancer, Amazon EBS encryption on Amazon EC2 instances, and Amazon S3 with server-side encryption. 
- B. Use SSL termination with a SAN SSL certificate on the load balancer, Amazon EC2 with all Amazon EBS volumes using Amazon EBS encryption, and Amazon S3 with server-side encryption with customer-managed keys.
- C. Use TCP load balancing on the load balancer, SSL termination on the Amazon EC2 instances, OS-level disk encryption on the Amazon EBS volumes, and Amazon S3 with server-side encryption.
- D. Use TCP load balancing on the load balancer, SSL termination on the Amazon EC2 instances, and Amazon S3 with server-side encryption. 
- E. Use SSL termination on the load balancer, an SSL listener on the Amazon EC2 instances, Amazon EBS encryption on EBS volumes containing PHI, and Amazon S3 with server-side encryption.

<details><summary>Answer:</summary><p>
[C, E]

Categories:
[S3, SES, EC2, EBS]

Explanation:

Question 26@http://jayendrapatil.com/aws-elastic-load-balancing/

A: connection between ELB and EC2 not encrypted

D: Does not mention EBS encryption

</p></details><hr>

### Question 27:

A startup deploys its photo-sharing site in a VPC. An elastic load balancer distributes web traffic across two subnets. The load balancer session stickiness is configured to use the AWS-generated session cookie, with a session TTL of 5 minutes. The web server Auto Scaling group is configured as min-size=4, max-size=4. The startup is preparing for a public launch, by running load-testing software installed on a single Amazon Elastic Compute Cloud (EC2) instance running in us-west-2a. After 60 minutes of load-testing, the web server logs show the following:WEBSERVER LOGS | # of HTTP requests from load-tester | # of HTTP requests from private beta users || webserver #1 (subnet in us-west-2a): | 19,210 | 434 || webserver #2 (subnet in us-west-2a): | 21,790 | 490 || webserver #3 (subnet in us-west-2b): | 0 | 410 || webserver #4 (subnet in us-west-2b): | 0 | 428 |Which recommendations can help ensure that load-testing HTTP requests are evenly distributed across the four web servers? Choose 2 answers

- A. Launch and run the load-tester Amazon EC2 instance from us-east-1 instead.
- B. Configure Elastic Load Balancing session stickiness to use the app-specific session cookie.
- C. Re-configure the load-testing software to re-resolve DNS for each web request.
- D. Configure Elastic Load Balancing and Auto Scaling to distribute across us-west-2a and us-west-2b.
- E. Use a third-party load-testing service which offers globally distributed test clients.

<details><summary>Answer:</summary><p>
[C, E]

Categories:
[SES, EC2, ASG, EBS, VPC, ELB]

Explanation:

Question 27@http://jayendrapatil.com/aws-elastic-load-balancing/

C: https://aws.amazon.com/articles/1636185810492479

E: https://aws.amazon.com/articles/1636185810492479

</p></details><hr>

### Question 28:

To serve Web traffic for a popular product your chief financial officer and IT director have purchased 10 m1.large heavy utilization Reserved Instances (RIs) evenly spread across two availability zones: Route 53 is used to deliver the traffic to an Elastic Load Balancer (ELB). After several months, the product grows even more popular and you need additional capacity As a result, your company purchases two c3.2xlarge medium utilization RIs You register the two c3.2xlarge instances with your ELB and quickly find that the ml large instances are at 100% of capacity and the c3.2xlarge instances have significant capacity that’s unused Which option is the most cost effective and uses EC2 capacity most effectively?

- A. Use a separate ELB for each instance type and distribute load to ELBs with Route 53 weighted round robin
- B. Configure Autoscaling group and Launch Configuration with ELB to add up to 10 more on-demand mi large instances when triggered by CloudWatch shut off c3.2xlarge instances 
- C. Route traffic to EC2 m1.large and c3.2xlarge instances directly using Route 53 latency based routing and health checks shut off ELB 
- D. Configure ELB with two c3.2xlarge Instances and use on-demand Autoscailng group for up to two additional c3.2xlarge instances Shut on m1.large instances

<details><summary>Answer:</summary><p>
[A]

Categories:
[SES, EC2, CloudWatch, Route 53, ELB]

Explanation:

Question 28@http://jayendrapatil.com/aws-elastic-load-balancing/

B: increase cost as you still pay for the RI

C: will not still use the capacity effectively

D: Increases cost, as you still pay for the 10 m1.large RI

</p></details><hr>

### Question 29:

Which header received at the EC2 instance identifies the port used by the client while requesting ELB?

- A. X-Forwarded-Proto
- B. X-Requested-Proto
- C. X-Forwarded-Port
- D. X-Requested-Port

<details><summary>Answer:</summary><p>
[C]

Categories:
[EC2, ELB]

Explanation:

Question 29@http://jayendrapatil.com/aws-elastic-load-balancing/

</p></details><hr>

### Question 30:

A user has configured ELB with two instances running in separate AZs of the same region? Which of the below mentioned statements is true?

- A. Multi AZ instances will provide HA with ELB
- B. Multi AZ instances are not possible with a single ELB
- C. Multi AZ instances will provide scalability with ELB
- D. The user can achieve both HA and scalability with ELB

<details><summary>Answer:</summary><p>
[A]

Categories:
[ELB]

Explanation:

Question 30@http://jayendrapatil.com/aws-elastic-load-balancing/

A: ELB provides HA to route traffic to healthy instances only it does not provide scalability

</p></details><hr>

### Question 31:

A user is configuring the HTTPS protocol on a front end ELB and the SSL protocol for the back-end listener in ELB. What will ELB do?

- A. It will allow you to create the configuration, but the instance will not pass the health check
- B. Receives requests on HTTPS and sends it to the back end instance on SSL
- C. It will not allow you to create this configuration
- D. It will allow you to create the configuration, but ELB will not work as expected

<details><summary>Answer:</summary><p>
[C]

Categories:
[ELB]

Explanation:

Question 31@http://jayendrapatil.com/aws-elastic-load-balancing/

C: Will give error “Load Balancer protocol is an application layer protocol, but instance protocol is not. Both the Load Balancer protocol and the instance protocol should be at the same layer. Please fix.”

</p></details><hr>

### Question 32:

An ELB is diverting traffic across 5 instances. One of the instances was unhealthy only for 20 minutes. What will happen after 20 minutes when the instance becomes healthy?

- A. ELB will never divert traffic back to the same instance
- B. ELB will not automatically send traffic to the same instance. However, the user can configure to start sending traffic to the same instance
- C. ELB starts sending traffic to the instance once it is healthy
- D. ELB terminates the instance once it is unhealthy. Thus, the instance cannot be healthy after 10 minutes

<details><summary>Answer:</summary><p>
[C]

Categories:
[ELB]

Explanation:

Question 32@http://jayendrapatil.com/aws-elastic-load-balancing/

</p></details><hr>

### Question 33:

A user has hosted a website on AWS and uses ELB to load balance the multiple instances. The user application does not have any cookie management. How can the user bind the session of the requestor with a particular instance?

- A. Bind the IP address with a sticky cookie
- B. Create a cookie at the application level to set at ELB
- C. Use session synchronization with ELB
- D. Let ELB generate a cookie for a specified duration

<details><summary>Answer:</summary><p>
[D]

Categories:
[SES, EBS, ELB]

Explanation:

Question 33@http://jayendrapatil.com/aws-elastic-load-balancing/

</p></details><hr>

### Question 34:

A user has configured a website and launched it using the Apache web server on port 80. The user is using ELB with the EC2 instances for Load Balancing. What should the user do to ensure that the EC2 instances accept requests only from ELB?

- A. Open the port for an ELB static IP in the EC2 security group
- B. Configure the security group of EC2, which allows access to the ELB source security group
- C. Configure the EC2 instance so that it only listens on the ELB port
- D. Configure the security group of EC2, which allows access only to the ELB listener

<details><summary>Answer:</summary><p>
[B]

Categories:
[EC2, EBS, ELB]

Explanation:

Question 34@http://jayendrapatil.com/aws-elastic-load-balancing/

</p></details><hr>

### Question 35:

AWS Elastic Load Balancer supports SSL termination.

- A. For specific availability zones only
- B. False
- C. For specific regions only
- D. For all regions

<details><summary>Answer:</summary><p>
[D]

Categories:
[]

Explanation:

Question 35@http://jayendrapatil.com/aws-elastic-load-balancing/

</p></details><hr>

### Question 36:

User has launched five instances with ELB. How can the user add the sixth EC2 instance to ELB?

- A. The user can add the sixth instance on the fly.
- B. The user must stop the ELB and add the sixth instance.
- C. The user can add the instance and change the ELB config file.
- D. The ELB can only have a maximum of five instances.

<details><summary>Answer:</summary><p>
[A]

Categories:
[EC2, ELB]

Explanation:

Question 36@http://jayendrapatil.com/aws-elastic-load-balancing/

</p></details><hr>

