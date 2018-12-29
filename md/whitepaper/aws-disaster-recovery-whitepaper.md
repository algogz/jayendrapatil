### Question 1:

Which of these Disaster Recovery options costs the least?

- A. Pilot Light
- B. Fully Working Low capacity Warm standby
- C. Multi site Active-Active

<details><summary>Answer:</summary><p>
[A]

Categories:
[]

Explanation:

Question 1@http://jayendrapatil.com/aws-disaster-recovery-whitepaper/

A: most systems are down and brought up only after disaster

</p></details><hr>

### Question 2:

Your company currently has a 2-tier web application running in an on-premises data center. You have experienced several infrastructure failures in the past two months resulting in significant financial losses. Your CIO is strongly agreeing to move the application to AWS. While working on achieving buy-in from the other company executives, he asks you to develop a disaster recovery plan to help improve Business continuity in the short term. He specifies a target Recovery Time Objective (RTO) of 4 hours and a Recovery Point Objective (RPO) of 1 hour or less. He also asks you to implement the solution within 2 weeks. Your database is 200GB in size and you have a 20Mbps Internet connection. How would you do this while minimizing costs?

- A. Create an EBS backed private AMI which includes a fresh install or your application. Setup a script in your data center to backup the local database every 1 hour and to encrypt and copy the resulting file to an S3 bucket using multi-part upload 
- B. Install your application on a compute-optimized EC2 instance capable of supporting the application’s average load synchronously replicate transactions from your on-premises database to a database instance in AWS across a secure Direct Connect connection.
- C. Deploy your application on EC2 instances within an Auto Scaling group across multiple availability zones asynchronously replicate transactions from your on-premises database to a database instance in AWS across a secure VPN connection. 
- D. Create an EBS backed private AMI that includes a fresh install of your application. Develop a Cloud Formation template which includes your AMI and the required EC2. Auto-Scaling and ELB resources to support deploying the application across Multiple Availability Zones. Asynchronously replicate transactions from your on-premises database to a database instance in AWS across a secure VPN connection. ( )

<details><summary>Answer:</summary><p>
[D]

Categories:
[S3, SES, EC2, ASG, EBS, ELB, Direct Connect]

Explanation:

Question 2@http://jayendrapatil.com/aws-disaster-recovery-whitepaper/

A: while AMI is a right approach to keep cost down, Upload to S3 very Slow

B: (EC2 running in Compute Optimized as well as Direct Connect is expensive to start with also Direct Connect cannot be implemented in 2 weeks)

C: While VPN can be setup quickly asynchronous replication using VPN would work, running instances in DR is expensive

D: Pilot Light approach with only DB running and replicate while you have preconfigured AMI and autoscaling config

</p></details><hr>

### Question 3:

You are designing an architecture that can recover from a disaster very quickly with minimum down time to the end users. Which of the following approaches is best?

- A. Leverage Route 53 health checks to automatically fail over to backup site when the primary site becomes unreachable
- B. Implement the Pilot Light DR architecture so that traffic can be processed seamlessly in case the primary site becomes unreachable
- C. Implement either Fully Working Low Capacity Standby or Multi-site Active-Active architecture so that the end users will not experience any delay even if the primary site becomes unreachable
- D. Implement multi-region architecture to ensure high availability

<details><summary>Answer:</summary><p>
[C]

Categories:
[Route 53]

Explanation:

Question 3@http://jayendrapatil.com/aws-disaster-recovery-whitepaper/

</p></details><hr>

### Question 4:

Your customer wishes to deploy an enterprise application to AWS that will consist of several web servers, several application servers and a small (50GB) Oracle database. Information is stored, both in the database and the file systems of the various servers. The backup system must support database recovery, whole server and whole disk restores, and individual file restores with a recovery time of no more than two hours. They have chosen to use RDS Oracle as the database. Which backup architecture will meet these requirements?

- A. Backup RDS using automated daily DB backups. Backup the EC2 instances using AMIs and supplement with file-level backup to S3 using traditional enterprise backup software to provide file level restore 
- B. Backup RDS using a Multi-AZ Deployment Backup the EC2 instances using AMIs, and supplement by copying file system data to S3 to provide file level restore 
- C. Backup RDS using automated daily DB backups. Backup the EC2 instances using EBS snapshots and supplement with file-level backups to Amazon Glacier using traditional enterprise backup software to provide file level restore 
- D. Backup RDS database to S3 using Oracle RMAN. Backup the EC2 instances using AMIs, and supplement with EBS snapshots for individual volume restore. 

<details><summary>Answer:</summary><p>
[]

Categories:
[S3, RDS, Glacier, EC2, EBS]

Explanation:

Question 4@http://jayendrapatil.com/aws-disaster-recovery-whitepaper/

A: RDS automated backups with file-level backups can be used

B: Multi-AZ is more of an Disaster recovery solution

C: Glacier not an option with the 2 hours RTO

D: Will use RMAN only if Database hosted on EC2 and not when using RDS

</p></details><hr>

### Question 5:

Which statements are true about the Pilot Light Disaster recovery architecture pattern?

- A. Pilot Light is a hot standby 
- B. Enables replication of all critical data to AWS
- C. Very cost-effective DR pattern
- D. Can scale the system as needed to handle current production load

<details><summary>Answer:</summary><p>
[B, C, D]

Categories:
[]

Explanation:

Question 5@http://jayendrapatil.com/aws-disaster-recovery-whitepaper/

A: Cold Standby

</p></details><hr>

### Question 6:

An ERP application is deployed across multiple AZs in a single region. In the event of failure, the Recovery Time Objective (RTO) must be less than 3 hours, and the Recovery Point Objective (RPO) must be 15 minutes. The customer realizes that data corruption occurred roughly 1.5 hours ago. What DR strategy could be used to achieve this RTO and RPO in the event of this kind of failure?

- A. Take hourly DB backups to S3, with transaction logs stored in S3 every 5 minutes
- B. Use synchronous database master-slave replication between two availability zones. 
- C. Take hourly DB backups to EC2 Instance store volumes with transaction logs stored In S3 every 5 minutes. 
- D. Take 15 minute DB backups stored in Glacier with transaction logs stored in S3 every 5 minutes. 

<details><summary>Answer:</summary><p>
[A]

Categories:
[S3, Glacier, EC2, Instance Store]

Explanation:

Question 6@http://jayendrapatil.com/aws-disaster-recovery-whitepaper/

B: Replication won’t help to backtrack and would be sync always

C: Instance store not a preferred storage

D: Glacier does not meet the RTO

</p></details><hr>

### Question 7:

Your company’s on-premises content management system has the following architecture: – Application Tier – Java code on a JBoss application server – Database Tier – Oracle database regularly backed up to Amazon Simple Storage Service (S3) using the Oracle RMAN backup utility – Static Content – stored on a 512GB gateway stored Storage Gateway volume attached to the application server via the iSCSI interfaceWhich AWS based disaster recovery strategy will give you the best RTO?

- A. Deploy the Oracle database and the JBoss app server on EC2. Restore the RMAN Oracle backups from Amazon S3. Generate an EBS volume of static content from the Storage Gateway and attach it to the JBoss EC2 server.
- B. Deploy the Oracle database on RDS. Deploy the JBoss app server on EC2. Restore the RMAN Oracle backups from Amazon Glacier. Generate an EBS volume of static content from the Storage Gateway and attach it to the JBoss EC2 server. 
- C. Deploy the Oracle database and the JBoss app server on EC2. Restore the RMAN Oracle backups from Amazon S3. Restore the static content by attaching an AWS Storage Gateway running on Amazon EC2 as an iSCSI volume to the JBoss EC2 server. 
- D. Deploy the Oracle database and the JBoss app server on EC2. Restore the RMAN Oracle backups from Amazon S3. Restore the static content from an AWS Storage Gateway-VTL running on Amazon EC2 

<details><summary>Answer:</summary><p>
[A]

Categories:
[S3, SES, RDS, Glacier, EC2, Storage Gateway, EBS]

Explanation:

Question 7@http://jayendrapatil.com/aws-disaster-recovery-whitepaper/

B: Glacier does help to give best RTO

C: No need to attach the Storage Gateway as an iSCSI volume can just create a EBS volume

D: VTL is Virtual Tape library and doesn’t fit the RTO

</p></details><hr>

