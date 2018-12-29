### Question 1:

A user has launched an EC2 instance from an instance store backed AMI. The infrastructure team wants to create an AMI from the running instance. Which of the below mentioned credentials is not required while creating the AMI?

- A. AWS account ID
- B. 509 certificate and private key
- C. AWS login ID to login to the console
- D. Access key and secret access key

<details><summary>Answer:</summary><p>
[C]

Categories:
[EC2, Instance Store]

Explanation:

Question 1@http://jayendrapatil.com/aws-ec2-amazon-machine-image-ami/

</p></details><hr>

### Question 2:

A user has launched an EC2 Windows instance from an instance store backed AMI. The user wants to convert the AMI to an EBS backed AMI. How can the user convert it?

- A. Attach an EBS volume to the instance and unbundle all the AMI bundled data inside the EBS
- B. A Windows based instance store backed AMI cannot be converted to an EBS backed AMI
- C. It is not possible to convert an instance store backed AMI to an EBS backed AMI
- D. Attach an EBS volume and use the copy command to copy all the ephemeral content to the EBS Volume

<details><summary>Answer:</summary><p>
[B]

Categories:
[EC2, EBS, Instance Store]

Explanation:

Question 2@http://jayendrapatil.com/aws-ec2-amazon-machine-image-ami/

</p></details><hr>

### Question 3:

A user has launched two EBS backed EC2 instances in the US-East-1a region. The user wants to change the zone of one of the instances. How can the user change it?

- A. Stop one of the instances and change the availability zone
- B. The zone can only be modified using the AWS CLI
- C. From the AWS EC2 console, select the Actions – > Change zones and specify new zone
- D. Create an AMI of the running instance and launch the instance in a separate AZ

<details><summary>Answer:</summary><p>
[D]

Categories:
[EC2, EBS]

Explanation:

Question 3@http://jayendrapatil.com/aws-ec2-amazon-machine-image-ami/

</p></details><hr>

### Question 4:

A user has launched a large EBS backed EC2 instance in the US-East-1a region. The user wants to achieve Disaster Recovery (DR) for that instance by creating another small instance in Europe. How can the user achieve DR?

- A. Copy the running instance using the “Instance Copy” command to the EU region
- B. Create an AMI of the instance and copy the AMI to the EU region. Then launch the instance from the EU AMI
- C. Copy the instance from the US East region to the EU region
- D. Use the “Launch more like this” option to copy the instance from one region to another

<details><summary>Answer:</summary><p>
[B]

Categories:
[EC2, EBS]

Explanation:

Question 4@http://jayendrapatil.com/aws-ec2-amazon-machine-image-ami/

</p></details><hr>

### Question 5:

A user has launched an EC2 instance store backed instance in the US-East-1a zone. The user created AMI #1 and copied it to the Europe region. After that, the user made a few updates to the application running in the US-East-1a zone. The user makes an AMI#2 after the changes. If the user launches a new instance in Europe from the AMI #1 copy, which of the below mentioned statements is true?

- A. The new instance will have the changes made after the AMI copy as AWS just copies the reference of the original AMI during the copying. Thus, the copied AMI will have all the updated data
- B. The new instance will have the changes made after the AMI copy since AWS keeps updating the AMI
- C. It is not possible to copy the instance store backed AMI from one region to another
- D. The new instance in the EU region will not have the changes made after the AMI copy

<details><summary>Answer:</summary><p>
[D]

Categories:
[EC2, Instance Store]

Explanation:

Question 5@http://jayendrapatil.com/aws-ec2-amazon-machine-image-ami/

</p></details><hr>

### Question 6:

George has shared an EC2 AMI created in the US East region from his AWS account with Stefano. George copies the same AMI to the US West region. Can Stefano access the copied AMI of George’s account from the US West region?

- A. No, copy AMI does not copy the permission
- B. It is not possible to share the AMI with a specific account
- C. Yes, since copy AMI copies all private account sharing permissions
- D. Yes, since copy AMI copies all the permissions attached with the AMI

<details><summary>Answer:</summary><p>
[A]

Categories:
[EC2]

Explanation:

Question 6@http://jayendrapatil.com/aws-ec2-amazon-machine-image-ami/

</p></details><hr>

### Question 7:

EC2 instances are launched from Amazon Machine images (AMIS). A given public AMI can:

- A. be used to launch EC2 Instances in any AWS region.
- B. only be used to launch EC2 instances in the same country as the AMI is stored.
- C. only be used to launch EC2 instances in the same AWS region as the AMI is stored.
- D. only be used to launch EC2 instances in the same AWS availability zone as the AMI is stored.

<details><summary>Answer:</summary><p>
[C]

Categories:
[EC2]

Explanation:

Question 7@http://jayendrapatil.com/aws-ec2-amazon-machine-image-ami/

C: (An AMI is tied to the region where its files are located within Amazon S3)

</p></details><hr>

