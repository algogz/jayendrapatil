### Question 1:

George has launched three EC2 instances inside the US-East-1a zone with his AWS account. Ray has launched two EC2 instances in the US-East-1a zone with his AWS account. Which of the below entioned statements will help George and Ray understand the availability zone (AZ) concept better?

- A. The instances of George and Ray will be running in the same data centre
- B. All the instances of George and Ray can communicate over a private IP with a minimal cost
- C. All the instances of George and Ray can communicate over a private IP without any cost
- D. us-east-1a region of George and Ray can be different availability zones

<details><summary>Answer:</summary><p>
[D]

Categories:
[EC2]

Explanation:

Question 1@http://jayendrapatil.com/aws-regions-availability-zones-and-edge-locations/

D: http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-regions-availability-zones.html

D: An Availability Zone is represented by a region code followed by a letter identifier; for example, us-east-1a. To ensure that resources are distributed across the Availability Zones for a region, we independently map Availability Zones to identifiers for each account. For example, your Availability Zone us-east-1a might not be the same location as us-east-1a for another account. There’s no way for you to coordinate Availability Zones between accounts.

</p></details><hr>

