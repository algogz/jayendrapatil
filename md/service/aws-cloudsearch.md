### Question 1:

A newspaper organization has an on-premises application which allows the public to search its back catalogue and retrieve individual newspaper pages via a website written in Java. They have scanned the old newspapers into JPEGs (approx. 17TB) and used Optical Character Recognition (OCR) to populate a commercial search product. The hosting platform and software is now end of life and the organization wants to migrate its archive to AWS and produce a cost efficient architecture and still be designed for availability and durability. Which is the most appropriate?

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

Question 1@http://jayendrapatil.com/aws-cloudsearch/

A: Reusing Commercial search application which is nearing end of life not a good option for cost

B: storing JPEGs on EBS volumes not cost effective also answer does not address Open source solution availability

C: Cost effective S3 storage, CloudSearch for Search and Highly available and durable web application

D: MySQL not an ideal solution to sore index and JPEG images for cost and performance

E: Web Application not scalable, whats the source for JPEGs files through CloudFront

</p></details><hr>

