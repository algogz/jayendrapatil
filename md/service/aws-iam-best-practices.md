### Question 1:

Your organization is preparing for a security assessment of your use of AWS. In preparation for this assessment, which two IAM best practices should you consider implementing? Choose 2 answers

- A. Create individual IAM users for everyone in your organization
- B. Configure MFA on the root account and for privileged IAM users
- C. Assign IAM users and groups configured with policies granting least privilege access
- D. Ensure all users have been assigned and are frequently rotating a password, access ID/secret key, and X.509 certificate

<details><summary>Answer:</summary><p>
[]

Categories:
[SES, IAM]

Explanation:

Question 1@http://jayendrapatil.com/aws-iam-best-practices/

A: (May not be needed as can use Roles as well)

D: (Must be assigned only if using console or through command line)

</p></details><hr>

### Question 2:

What are the recommended best practices for IAM? (Choose 3 answers)

- A. Grant least privilege
- B. User the AWS account(root) for regular user
- C. Use Mutli-Factor Authentication (MFA)
- D. Store access key/private key in git
- E. Rotate credentials regularly

<details><summary>Answer:</summary><p>
[A, C, E]

Categories:
[IAM]

Explanation:

Question 2@http://jayendrapatil.com/aws-iam-best-practices/

</p></details><hr>

### Question 3:

Which of the below mentioned options is not a best practice to securely manage the AWS access credentials?

- A. Enable MFA for privileged users
- B. Create individual IAM users
- C. Keep rotating your secure access credentials at regular intervals
- D. Create strong access key and secret access key and attach to the root account

<details><summary>Answer:</summary><p>
[D]

Categories:
[IAM]

Explanation:

Question 3@http://jayendrapatil.com/aws-iam-best-practices/

</p></details><hr>

### Question 4:

Your CTO is very worried about the security of your AWS account. How best can you prevent hackers from completely hijacking your account?

- A. Use short but complex password on the root account and any administrators.
- B. Use AWS IAM Geo-Lock and disallow anyone from logging in except for in your city.
- C. Use MFA on all users and accounts, especially on the root account.
- D. Don’t write down or remember the root account password after creating the AWS account.

<details><summary>Answer:</summary><p>
[C]

Categories:
[IAM]

Explanation:

Question 4@http://jayendrapatil.com/aws-iam-best-practices/

C: For increased security, it is recommend to configure MFA to help protect AWS resources

</p></details><hr>

### Question 5:

Fill the blanks: ____ helps us track AWS API calls and transitions, ____ helps to understand what resources we have now, and ____ allows auditing credentials and logins.

- A. AWS Config, CloudTrail, IAM Credential Reports
- B. CloudTrail, IAM Credential Reports, AWS Config
- C. CloudTrail, AWS Config, IAM Credential Reports
- D. AWS Config, IAM Credential Reports, CloudTrail

<details><summary>Answer:</summary><p>
[C]

Categories:
[IAM, CloudTrail]

Explanation:

Question 5@http://jayendrapatil.com/aws-iam-best-practices/

</p></details><hr>

