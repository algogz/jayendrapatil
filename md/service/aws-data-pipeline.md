### Question 1:

An International company has deployed a multi-tier web application that relies on DynamoDB in a single region. For regulatory reasons they need disaster recovery capability in a separate region with a Recovery Time Objective of 2 hours and a Recovery Point Objective of 24 hours. They should synchronize their data on a regular basis and be able to provision the web application rapidly using CloudFormation. The objective is to minimize changes to the existing web application, control the throughput of DynamoDB used for the synchronization of data and synchronize only the modified elements. Which design would you choose to meet these requirements?

- A. Use AWS data Pipeline to schedule a DynamoDB cross region copy once a day. Create a ‘Lastupdated’ attribute in your DynamoDB table that would represent the timestamp of the last update and use it as a filter.
- B. Use EMR and write a custom script to retrieve data from DynamoDB in the current region using a SCAN operation and push it to DynamoDB in the second region. 
- C. Use AWS data Pipeline to schedule an export of the DynamoDB table to S3 in the current region once a day then schedule another task immediately after it that will import data from S3 to DynamoDB in the other region. 
- D. Send each item into an SQS queue in the second region; use an auto-scaling group behind the SQS queue to replay the write in the second region. 

<details><summary>Answer:</summary><p>
[A]

Categories:
[S3, SQS, CloudFormation, DynamoDB, EMR]

Explanation:

Question 1@http://jayendrapatil.com/aws-data-pipeline/

A: https://aws.amazon.com/blogs/aws/copy-dynamodb-data-between-regions-using-the-aws-data-pipeline/

A: Refer 

B: No Schedule and throughput control

C: With AWS Data pipeline the data can be copied directly to other DynamoDB table

D: Not Automated to replay the write

</p></details><hr>

### Question 2:

Your company produces customer commissioned one-of-a-kind skiing helmets combining nigh fashion with custom technical enhancements. Customers can show off their Individuality on the ski slopes and have access to head-up-displays, GPS rear-view cams and any other technical innovation they wish to embed in the helmet. The current manufacturing process is data rich and complex including assessments to ensure that the custom electronics and materials used to assemble the helmets are to the highest standards. Assessments are a mixture of human and automated assessments you need to add a new set of assessment to model the failure modes of the custom electronics using GPUs with CUD across a cluster of servers with low latency networking. What architecture would allow you to automate the existing process using a hybrid approach and ensure that the architecture can support the evolution of processes over time?

- A. Use AWS Data Pipeline to manage movement of data & meta-data and assessments. Use an auto-scaling group of G2 instances in a placement group. 
- B. Use Amazon Simple Workflow (SWF) to manage assessments, movement of data & meta-data. Use an autoscaling group of G2 instances in a placement group. 
- C. Use Amazon Simple Workflow (SWF) to manage assessments movement of data & meta-data. Use an autoscaling group of C3 instances with SR-IOV (Single Root I/O Virtualization). 
- D. Use AWS data Pipeline to manage movement of data & meta-data and assessments use auto-scaling group of C3 with SR-IOV (Single Root I/O virtualization). 

<details><summary>Answer:</summary><p>
[]

Categories:
[SES, RDS, SWF]

Explanation:

Question 2@http://jayendrapatil.com/aws-data-pipeline/

A: Involves mixture of human assessments

B: Human and automated assessments with GPU and low latency networking

C: C3 and SR-IOV won’t provide GPU as well as Enhanced networking needs to be enabled

D: Involves mixture of human assessments

</p></details><hr>

