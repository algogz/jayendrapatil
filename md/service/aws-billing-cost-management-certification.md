### Question 2:

Your company wants to understand where cost is coming from in the company’s production AWS account. There are a number of applications and services running at any given time. Without expending too much initial development time, how best can you give the business a good understanding of which applications cost the most per month to operate?

- A. Create an automation script, which periodically creates AWS Support tickets requesting detailed intra-month information about your bill.
- B. Use custom CloudWatch Metrics in your system, and put a metric data point whenever cost is incurred.
- C. Use AWS Cost Allocation Tagging for all resources, which support it. Use the Cost Explorer to analyze costs throughout the month.
- D. Use the AWS Price API and constantly running resource inventory scripts to calculate total price based on multiplication of consumed resources over time.

<details><summary>Answer:</summary><p>
[C]

Categories:
[CloudWatch]

Explanation:

Question 2@http://jayendrapatil.com/aws-billing-cost-management-certification/

C: http://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/cost-alloc-tags.html

</p></details><hr>

### Question 3:

You need to know when you spend $1000 or more on AWS. What’s the easy way for you to see that notification?

- A. AWS CloudWatch Events tied to API calls, when certain thresholds are exceeded, publish to SNS.
- B. Scrape the billing page periodically and pump into Kinesis.
- C. AWS CloudWatch Metrics + Billing Alarm + Lambda event subscription. When a threshold is exceeded, email the manager.
- D. Scrape the billing page periodically and publish to SNS.

<details><summary>Answer:</summary><p>
[C]

Categories:
[CloudWatch, Kinesis, SNS, Lambda]

Explanation:

Question 3@http://jayendrapatil.com/aws-billing-cost-management-certification/

</p></details><hr>

### Question 4:

A user is planning to use AWS services for his web application. If the user is trying to set up his own billing management system for AWS, how can he configure it?

- A. Set up programmatic billing access. Download and parse the bill as per the requirement
- B. It is not possible for the user to create his own billing management service with AWS
- C. Enable the AWS CloudWatch alarm which will provide APIs to download the alarm data
- D. Use AWS billing APIs to download the usage report of each service from the AWS billing console

<details><summary>Answer:</summary><p>
[A]

Categories:
[CloudWatch]

Explanation:

Question 4@http://jayendrapatil.com/aws-billing-cost-management-certification/

</p></details><hr>

### Question 5:

An organization is setting up programmatic billing access for their AWS account. Which of the below mentioned services is not required or enabled when the organization wants to use programmatic access?

- A. Programmatic access
- B. AWS bucket to hold the billing report
- C. AWS billing alerts
- D. Monthly Billing report

<details><summary>Answer:</summary><p>
[C]

Categories:
[]

Explanation:

Question 5@http://jayendrapatil.com/aws-billing-cost-management-certification/

</p></details><hr>

### Question 6:

A user has setup a billing alarm using CloudWatch for $200. The usage of AWS exceeded $200 after some days. The user wants to increase the limit from $200 to $400? What should the user do?

- A. Create a new alarm of $400 and link it with the first alarm
- B. It is not possible to modify the alarm once it has crossed the usage limit
- C. Update the alarm to set the limit at $400 instead of $200
- D. Create a new alarm for the additional $200 amount

<details><summary>Answer:</summary><p>
[C]

Categories:
[CloudWatch]

Explanation:

Question 6@http://jayendrapatil.com/aws-billing-cost-management-certification/

C: http://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/monitor_estimated_charges_with_cloudwatch.html#editing_billing_alarm

</p></details><hr>

### Question 7:

A user is trying to configure the CloudWatch billing alarm. Which of the below mentioned steps should be performed by the user for the first time alarm creation in the AWS Account Management section?

- A. Enable Receiving Billing Reports
- B. Enable Receiving Billing Alerts
- C. Enable AWS billing utility
- D. Enable CloudWatch Billing Threshold

<details><summary>Answer:</summary><p>
[B]

Categories:
[CloudWatch]

Explanation:

Question 7@http://jayendrapatil.com/aws-billing-cost-management-certification/

</p></details><hr>

