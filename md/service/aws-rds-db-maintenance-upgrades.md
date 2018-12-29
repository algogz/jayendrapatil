### Question 1:

A user has launched an RDS MySQL DB with the Multi AZ feature. The user has scheduled the scaling of instance storage during maintenance window. What is the correct order of events during maintenance window? 1. Perform maintenance on standby 2. Promote standby to primary 3. Perform maintenance on original primary 4. Promote original master back as primary

- A. 1, 2, 3, 4
- B. 1, 2, 3
- C. 2, 3, 4, 1

<details><summary>Answer:</summary><p>
[B]

Categories:
[RDS]

Explanation:

Question 1@http://jayendrapatil.com/aws-rds-db-maintenance-upgrades/

</p></details><hr>

### Question 2:

Can I control if and when MySQL based RDS Instance is upgraded to new supported versions?

- A. No
- B. Only in VPC
- C. Yes

<details><summary>Answer:</summary><p>
[C]

Categories:
[RDS, VPC]

Explanation:

Question 2@http://jayendrapatil.com/aws-rds-db-maintenance-upgrades/

</p></details><hr>

### Question 3:

A user has scheduled the maintenance window of an RDS DB on Monday at 3 AM. Which of the below mentioned events may force to take the DB instance offline during the maintenance window?

- A. Enabling Read Replica
- B. Making the DB Multi AZ
- C. DB password change
- D. Security patching

<details><summary>Answer:</summary><p>
[D]

Categories:
[RDS]

Explanation:

Question 3@http://jayendrapatil.com/aws-rds-db-maintenance-upgrades/

</p></details><hr>

### Question 4:

A user has launched an RDS postgreSQL DB with AWS. The user did not specify the maintenance window during creation. The user has configured RDS to update the DB instance type from micro to large. If the user wants to have it during the maintenance window, what will AWS do?

- A. AWS will not allow to update the DB until the maintenance window is configured
- B. AWS will select the default maintenance window if the user has not provided it
- C. AWS will ask the user to specify the maintenance window during the update
- D. It is not possible to change the DB size from micro to large with RDS

<details><summary>Answer:</summary><p>
[B]

Categories:
[RDS]

Explanation:

Question 4@http://jayendrapatil.com/aws-rds-db-maintenance-upgrades/

</p></details><hr>

### Question 5:

Can I test my DB Instance against a new version before upgrading?

- A. No
- B. Yes
- C. Only in VPC

<details><summary>Answer:</summary><p>
[B]

Categories:
[VPC]

Explanation:

Question 5@http://jayendrapatil.com/aws-rds-db-maintenance-upgrades/

</p></details><hr>

