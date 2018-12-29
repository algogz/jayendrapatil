### Question 1:

You have deployed a web application targeting a global audience across multiple AWS Regions under the domain name example.com. You decide to use Route 53 Latency-Based Routing to serve web requests to users from the region closest to the user. To provide business continuity in the event of server downtime you configure weighted record sets associated with two web servers in separate Availability Zones per region. During a DR test you notice that when you disable all web servers in one of the regions Route 53 does not automatically direct all users to the other region. What could be happening? (Choose 2 answers)

- A. Latency resource record sets cannot be used in combination with weighted resource record sets.
- B. You did not setup an http health check for one or more of the weighted resource record sets associated with the disabled web servers
- C. The value of the weight associated with the latency alias resource record set in the region with the disabled servers is higher than the weight for the other region.
- D. One of the two working web servers in the other region did not pass its HTTP health check
- E. You did not set “Evaluate Target Health” to “Yes” on the latency alias resource record set associated with example.com in the region where you disabled the servers.

<details><summary>Answer:</summary><p>
[B, E]

Categories:
[SES, Route 53]

Explanation:

Question 1@http://jayendrapatil.com/aws-route-53-routing-policy/

</p></details><hr>

### Question 2:

The compliance department within your multi-national organization requires that all data for your customers that reside in the European Union (EU) must not leave the EU and also data for customers that reside in the US must not leave the US without explicit authorization. What must you do to comply with this requirement for a web based profile management application running on EC2?

- A. Run EC2 instances in multiple AWS Availability Zones in single Region and leverage an Elastic Load Balancer with session stickiness to route traffic to the appropriate zone to create their profile 
- B. Run EC2 instances in multiple Regions and leverage Route 53’s Latency Based Routing capabilities to route traffic to the appropriate region to create their profile 
- C. Run EC2 instances in multiple Regions and leverage a third party data provider to determine if a user needs to be redirect to the appropriate region to create their profile
- D. Run EC2 instances in multiple AWS Availability Zones in a single Region and leverage a third party data provider to determine if a user needs to be redirect to the appropriate zone to create their profile

<details><summary>Answer:</summary><p>
[C]

Categories:
[SES, EC2, Route 53]

Explanation:

Question 2@http://jayendrapatil.com/aws-route-53-routing-policy/

A: should be in 2 different regions – US and Europe

B: Latency based routing policy would not guarantee the compliance requirement

D: should be in 2 different regions – US and Europe

</p></details><hr>

### Question 3:

A US-based company is expanding their web presence into Europe. The company wants to extend their AWS infrastructure from Northern Virginia (us-east-1) into the Dublin (eu-west-1) region. Which of the following options would enable an equivalent experience for users on both continents?

- A. Use a public-facing load balancer per region to load-balance web traffic, and enable HTTP health checks.
- B. Use a public-facing load balancer per region to load-balance web traffic, and enable sticky sessions.
- C. Use Amazon Route 53, and apply a geolocation routing policy to distribute traffic across both regions
- D. Use Amazon Route 53, and apply a weighted routing policy to distribute traffic across both regions.

<details><summary>Answer:</summary><p>
[C]

Categories:
[SES, Route 53]

Explanation:

Question 3@http://jayendrapatil.com/aws-route-53-routing-policy/

</p></details><hr>

### Question 4:

You have been asked to propose a multi-region deployment of a web-facing application where a controlled portion of your traffic is being processed by an alternate region. Which configuration would achieve that goal?

- A. Route 53 record sets with weighted routing policy
- B. Route 53 record sets with latency based routing policy
- C. Auto Scaling with scheduled scaling actions set
- D. Elastic Load Balancing with health checks enabled

<details><summary>Answer:</summary><p>
[A]

Categories:
[ASG, Route 53, ELB]

Explanation:

Question 4@http://jayendrapatil.com/aws-route-53-routing-policy/

</p></details><hr>

### Question 5:

Your company is moving towards tracking web page users with a small tracking image loaded on each page. Currently you are serving this image out of us-east, but are starting to get concerned about the time it takes to load the image for users on the west coast. What are the two best ways to speed up serving this image? Choose 2 answers

- A. Use Route 53’s Latency Based Routing and serve the image out of us-west-2 as well as us-east-1
- B. Serve the image out through CloudFront
- C. Serve the image out of S3 so that it isn’t being served of your web application tier
- D. Use EBS PIOPs to serve the image faster out of your EC2 instances

<details><summary>Answer:</summary><p>
[A, B]

Categories:
[S3, RDS, CloudFront, EC2, EBS, Route 53]

Explanation:

Question 5@http://jayendrapatil.com/aws-route-53-routing-policy/

</p></details><hr>

### Question 6:

Your API requires the ability to stay online during AWS regional failures. Your API does not store any state, it only aggregates data from other sources – you do not have a database. What is a simple but effective way to achieve this uptime goal?

- A. Use a CloudFront distribution to serve up your API. Even if the region your API is in goes down, the edge locations CloudFront uses will be fine.
- B. Use an ELB and a cross-zone ELB deployment to create redundancy across datacenters. Even if a region fails, the other AZ will stay online.
- C. Create a Route53 Weighted Round Robin record, and if one region goes down, have that region redirect to the other region.
- D. Create a Route53 Latency Based Routing Record with Failover and point it to two identical deployments of your stateless API in two different regions. Make sure both regions use Auto Scaling Groups behind ELBs.

<details><summary>Answer:</summary><p>
[D]

Categories:
[SES, CloudFront, ASG, ELB]

Explanation:

Question 6@http://jayendrapatil.com/aws-route-53-routing-policy/

D: http://docs.aws.amazon.com/Route53/latest/DeveloperGuide/dns-failover.html

D: Refer

</p></details><hr>

