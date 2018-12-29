### Question 1:

An organization’s security policy requires multiple copies of all critical data to be replicated across at least a primary and backup data center. The organization has decided to store some critical data on Amazon S3. Which option should you implement to ensure this requirement is met?

- A. Use the S3 copy API to replicate data between two S3 buckets in different regions
- B. You do not need to implement anything since S3 data is automatically replicated between regions
- C. Use the S3 copy API to replicate data between two S3 buckets in different facilities within an AWS Region
- D. You do not need to implement anything since S3 data is automatically replicated between multiple facilities within an AWS Region

<details><summary>Answer:</summary><p>
[D]

Categories:
[S3]

Explanation:

Question 1@http://jayendrapatil.com/aws-s3-subresources/

</p></details><hr>

### Question 2:

A customer wants to track access to their Amazon Simple Storage Service (S3) buckets and also use this information for their internal security and access audits. Which of the following will meet the Customer requirement?

- A. Enable AWS CloudTrail to audit all Amazon S3 bucket access.
- B. Enable server access logging for all required Amazon S3 buckets
- C. Enable the Requester Pays option to track access via AWS Billing
- D. Enable Amazon S3 event notifications for Put and Post.

<details><summary>Answer:</summary><p>
[B]

Categories:
[S3, CloudTrail]

Explanation:

Question 2@http://jayendrapatil.com/aws-s3-subresources/

</p></details><hr>

### Question 3:

A user is enabling a static website hosting on an S3 bucket. Which of the below mentioned parameters cannot be configured by the user?

- A. Error document
- B. Conditional error on object name
- C. Index document
- D. Conditional redirection on object name

<details><summary>Answer:</summary><p>
[B]

Categories:
[S3, EBS]

Explanation:

Question 3@http://jayendrapatil.com/aws-s3-subresources/

</p></details><hr>

### Question 4:

Company ABCD is running their corporate website on Amazon S3 accessed from http//www.companyabcd.com. Their marketing team has published new web fonts to a separate S3 bucket accessed by the S3 endpoint: https://s3-us-west1.amazonaws.com/abcdfonts. While testing the new web fonts, Company ABCD recognized the web fonts are being blocked by the browser. What should Company ABCD do to prevent the web fonts from being blocked by the browser?

- A. Enable versioning on the abcdfonts bucket for each web font
- B. Create a policy on the abcdfonts bucket to enable access to everyone
- C. Add the Content-MD5 header to the request for webfonts in the abcdfonts bucket from the website
- D. Configure the abcdfonts bucket to allow cross-origin requests by creating a CORS configuration

<details><summary>Answer:</summary><p>
[D]

Categories:
[S3, EBS]

Explanation:

Question 4@http://jayendrapatil.com/aws-s3-subresources/

</p></details><hr>

### Question 5:

Company ABCD is currently hosting their corporate site in an Amazon S3 bucket with Static Website Hosting enabled. Currently, when visitors go to http://www.companyabcd.com the index.html page is returned. Company C now would like a new page welcome.html to be returned when a visitor enters http://www.companyabcd.com in the browser. Which of the following steps will allow Company ABCD to meet this requirement? Choose 2 answers.

- A. Upload an html page named welcome.html to their S3 bucket
- B. Create a welcome subfolder in their S3 bucket
- C. Set the Index Document property to welcome.html
- D. Move the index.html page to a welcome subfolder
- E. Set the Error Document property to welcome.html

<details><summary>Answer:</summary><p>
[A, C]

Categories:
[S3, EBS]

Explanation:

Question 5@http://jayendrapatil.com/aws-s3-subresources/

</p></details><hr>

