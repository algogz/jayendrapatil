### Question 1:

You’ve been hired to enhance the overall security posture for a very large e-commerce site. They have a well architected multi-tier application running in a VPC that uses ELBs in front of both the web and the app tier with static assets served directly from S3. They are using a combination of RDS and DynamoDB for their dynamic data and then archiving nightly into S3 for further processing with EMR. They are concerned because they found questionable log entries and suspect someone is attempting to gain unauthorized access. Which approach provides a cost effective scalable mitigation to this kind of attack?

- A. Recommend mat they lease space at a DirectConnect partner location and establish a 1G DirectConnect connection to tneirvPC they would then establish Internet connectivity into their space, filter the traffic in hardware Web Application Firewall (WAF). And then pass the traffic through the DirectConnect connection into their application running in their VPC. 
- B. Add previously identified hostile source IPs as an explicit INBOUND DENY NACL to the web tier subnet. 
- C. Add a WAF tier by creating a new ELB and an AutoScaling group of EC2 Instances running a host-based WAF. They would redirect Route 53 to resolve to the new WAF tier ELB. The WAF tier would then pass the traffic to the current web tier. Web tier Security Groups would be updated to only allow traffic from the WAF tier Security Group
- D. Remove all but TLS 1.2 from the web tier ELB and enable Advanced Protocol Filtering This will enable the ELB itself to perform WAF functionality. 

<details><summary>Answer:</summary><p>
[C]

Categories:
[S3, SES, RDS, EC2, VPC, DynamoDB, Route 53, ELB, EMR, WAF]

Explanation:

Question 1@http://jayendrapatil.com/aws-waf/

A: Not cost effective

B: does not protect against new source

D: No advanced protocol filtering in ELB

</p></details><hr>

