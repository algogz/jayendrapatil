### Question 1:

You are designing a social media site and are considering how to mitigate distributed denial-of-service (DDoS) attacks. Which of the below are viable mitigation techniques? (Choose 3 answers)

- A. Add multiple elastic network interfaces (ENIs) to each EC2 instance to increase the network bandwidth.
- B. Use dedicated instances to ensure that each instance has the maximum performance possible.
- C. Use an Amazon CloudFront distribution for both static and dynamic content.
- D. Use an Elastic Load Balancer with auto scaling groups at the web app and Amazon Relational Database Service (RDS) tiers
- E. Add alert Amazon CloudWatch to look for high Network in and CPU utilization.
- F. Create processes and capabilities to quickly add and remove rules to the instance OS firewall.

<details><summary>Answer:</summary><p>
[C, D, E]

Categories:
[SES, RDS, CloudFront, EC2, CloudWatch, ASG]

Explanation:

Question 1@http://jayendrapatil.com/aws-ddos-resiliency-best-practices-whitepaper-overview/

</p></details><hr>

### Question 2:

You’ve been hired to enhance the overall security posture for a very large e-commerce site. They have a well architected multi-tier application running in a VPC that uses ELBs in front of both the web and the app tier with static assets served directly from S3. They are using a combination of RDS and DynamoDB for their dynamic data and then archiving nightly into S3 for further processing with EMR. They are concerned because they found questionable log entries and suspect someone is attempting to gain unauthorized access. Which approach provides a cost effective scalable mitigation to this kind of attack?

- A. Recommend that they lease space at a DirectConnect partner location and establish a 1G DirectConnect connection to their VPC they would then establish Internet connectivity into their space, filter the traffic in hardware Web Application Firewall (WAF). And then pass the traffic through the DirectConnect connection into their application running in their VPC. 
- B. Add previously identified hostile source IPs as an explicit INBOUND DENY NACL to the web tier subnet. 
- C. Add a WAF tier by creating a new ELB and an AutoScaling group of EC2 Instances running a host-based WAF. They would redirect Route 53 to resolve to the new WAF tier ELB. The WAF tier would their pass the traffic to the current web tier The web tier Security Groups would be updated to only allow traffic from the WAF tier Security Group
- D. Remove all but TLS 1.2 from the web tier ELB and enable Advanced Protocol Filtering This will enable the ELB itself to perform WAF functionality. 

<details><summary>Answer:</summary><p>
[C]

Categories:
[S3, SES, RDS, EC2, VPC, DynamoDB, Route 53, ELB, EMR, WAF]

Explanation:

Question 2@http://jayendrapatil.com/aws-ddos-resiliency-best-practices-whitepaper-overview/

A: Not cost effective

B: does not protect against new source

D: No advanced protocol filtering in ELB

</p></details><hr>

