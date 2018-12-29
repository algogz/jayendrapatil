### Question 1:

Can I encrypt connections between my application and my DB Instance using SSL?

- A. No
- B. Yes
- C. Only in VPC
- D. Only in certain regions

<details><summary>Answer:</summary><p>
[B]

Categories:
[VPC]

Explanation:

Question 1@http://jayendrapatil.com/aws-rds-security/

</p></details><hr>

### Question 2:

Which of these configuration or deployment practices is a security risk for RDS?

- A. Storing SQL function code in plaintext
- B. Non-Multi-AZ RDS instance
- C. Having RDS and EC2 instances exist in the same subnet
- D. RDS in a public subnet

<details><summary>Answer:</summary><p>
[D]

Categories:
[RDS, EC2]

Explanation:

Question 2@http://jayendrapatil.com/aws-rds-security/

D: http://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Overview.RDSSecurityGroups.html

D: (Making RDS accessible to the public internet in a public subnet poses a security risk, by making your database directly addressable and spammable. DB instances deployed within a VPC can be configured to be accessible from the Internet or from EC2 instances outside the VPC. If a VPC security group specifies a port access such as TCP port 22, you would not be able to access the DB instance because the firewall for the DB instance provides access only via the IP addresses specified by the DB security groups the instance is a member of and the port defined when the DB instance was created. Refer )

</p></details><hr>

