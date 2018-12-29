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

### Question 2:

A customer’s nightly EMR job processes a single 2-TB data file stored on Amazon Simple Storage Service (S3). The Amazon Elastic Map Reduce (EMR) job runs on two On-Demand core nodes and three On-Demand task nodes. Which of the following may help reduce the EMR job completion time? Choose 2 answers

- A. Use three Spot Instances rather than three On-Demand instances for the task nodes.
- B. Change the input split size in the MapReduce job configuration.
- C. Use a bootstrap action to present the S3 bucket as a local filesystem.
- D. Launch the core nodes and task nodes within an Amazon Virtual Cloud.
- E. Adjust the number of simultaneous mapper tasks.
- F. Enable termination protection for the job flow.

<details><summary>Answer:</summary><p>
[B, E]

Categories:
[S3, SES, EMR]

Explanation:

Question 2@http://jayendrapatil.com/aws-emr-certification/

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

