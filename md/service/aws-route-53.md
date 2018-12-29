### Question 1:

What does Amazon Route53 provide?

- A. A global Content Delivery Network.
- B. None of these.
- C. A scalable Domain Name System
- D. An SSH endpoint for Amazon EC2.

<details><summary>Answer:</summary><p>
[C]

Categories:
[EC2]

Explanation:

Question 1@http://jayendrapatil.com/aws-route-53/

</p></details><hr>

### Question 2:

Does Amazon Route 53 support NS Records?

- A. Yes, it supports Name Service records.
- B. No
- C. It supports only MX records.
- D. Yes, it supports Name Server records. 

<details><summary>Answer:</summary><p>
[D]

Categories:
[RDS, Route 53]

Explanation:

Question 2@http://jayendrapatil.com/aws-route-53/

</p></details><hr>

### Question 3:

Does Route 53 support MX Records?

- A. Yes
- B. It supports CNAME records, but not MX records.
- C. No
- D. Only Primary MX records. Secondary MX records are not supported.

<details><summary>Answer:</summary><p>
[A]

Categories:
[RDS, Route 53]

Explanation:

Question 3@http://jayendrapatil.com/aws-route-53/

</p></details><hr>

### Question 4:

Which of the following statements are true about Amazon Route 53 resource records? Choose 2 answers

- A. An Alias record can map one DNS name to another Amazon Route 53 DNS name.
- B. A CNAME record can be created for your zone apex.
- C. An Amazon Route 53 CNAME record can point to any DNS record hosted anywhere.
- D. TTL can be set for an Alias record in Amazon Route 53.
- E. An Amazon Route 53 Alias record can point to any DNS record hosted anywhere.

<details><summary>Answer:</summary><p>
[A, C]

Categories:
[RDS, Route 53]

Explanation:

Question 4@http://jayendrapatil.com/aws-route-53/

</p></details><hr>

### Question 5:

Which statements are true about Amazon Route 53? (Choose 2 answers)

- A. Amazon Route 53 is a region-level service
- B. You can register your domain name
- C. Amazon Route 53 can perform health checks and failovers to a backup site in the even of the primary site failure
- D. Amazon Route 53 only supports Latency-based routing

<details><summary>Answer:</summary><p>
[B, C]

Categories:
[Route 53]

Explanation:

Question 5@http://jayendrapatil.com/aws-route-53/

</p></details><hr>

### Question 6:

A customer is hosting their company website on a cluster of web servers that are behind a public-facing load balancer. The customer also uses Amazon Route 53 to manage their public DNS. How should the customer configure the DNS zone apex record to point to the load balancer?

- A. Create an A record pointing to the IP address of the load balancer
- B. Create a CNAME record pointing to the load balancer DNS name.
- C. Create a CNAME record aliased to the load balancer DNS name.
- D. Create an A record aliased to the load balancer DNS name

<details><summary>Answer:</summary><p>
[D]

Categories:
[SES, EBS, Route 53]

Explanation:

Question 6@http://jayendrapatil.com/aws-route-53/

</p></details><hr>

### Question 7:

A user has configured ELB with three instances. The user wants to achieve High Availability as well as redundancy with ELB. Which of the below mentioned AWS services helps the user achieve this for ELB?

- A. Route 53
- B. AWS Mechanical Turk
- C. Auto Scaling
- D. AWS EMR

<details><summary>Answer:</summary><p>
[A]

Categories:
[ASG, Route 53, ELB, EMR]

Explanation:

Question 7@http://jayendrapatil.com/aws-route-53/

</p></details><hr>

### Question 8:

How can the domain’s zone apex for example “myzoneapexdomain com” be pointed towards an Elastic Load Balancer?

- A. By using an AAAA record
- B. By using an A record
- C. By using an Amazon Route 53 CNAME record
- D. By using an Amazon Route 53 Alias record

<details><summary>Answer:</summary><p>
[D]

Categories:
[RDS, Route 53]

Explanation:

Question 8@http://jayendrapatil.com/aws-route-53/

</p></details><hr>

### Question 9:

You need to create a simple, holistic check for your system’s general availability and uptime. Your system presents itself as an HTTP-speaking API. What is the simplest tool on AWS to achieve this with?

- A. Route53 Health Checks
- B. CloudWatch Health Checks
- C. AWS ELB Health Checks
- D. EC2 Health Checks

<details><summary>Answer:</summary><p>
[A]

Categories:
[EC2, CloudWatch, ELB]

Explanation:

Question 9@http://jayendrapatil.com/aws-route-53/

A: http://docs.aws.amazon.com/Route53/latest/DeveloperGuide/dns-failover-determining-health-of-endpoints.html

</p></details><hr>

