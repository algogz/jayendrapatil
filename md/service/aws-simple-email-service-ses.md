### Question 1:

What does Amazon SES stand for?

- A. Simple Elastic Server
- B. Simple Email Service
- C. Software Email Solution
- D. Software Enabled Server

<details><summary>Answer:</summary><p>
[B]

Categories:
[SES]

Explanation:

Question 1@http://jayendrapatil.com/aws-simple-email-service-ses/

</p></details><hr>

### Question 2:

Your startup wants to implement an order fulfillment process for selling a personalized gadget that needs an average of 3-4 days to produce with some orders taking up to 6 months you expect 10 orders per day on your first day. 1000 orders per day after 6 months and 10,000 orders after 12 months. Orders coming in are checked for consistency men dispatched to your manufacturing plant for production quality control packaging shipment and payment processing If the product does not meet the quality standards at any stage of the process employees may force the process to repeat a step Customers are notified via email about order status and any critical issues with their orders such as payment failure. Your case architecture includes AWS Elastic Beanstalk for your website with an RDS MySQL instance for customer data and orders. How can you implement the order fulfillment process while making sure that the emails are delivered reliably? [PROFESSIONAL]

- A. Add a business process management application to your Elastic Beanstalk app servers and re-use the ROS database for tracking order status use one of the Elastic Beanstalk instances to send emails to customers.
- B. Use SWF with an Auto Scaling group of activity workers and a decider instance in another Auto Scaling group with min/max=1 Use the decider instance to send emails to customers.
- C. Use SWF with an Auto Scaling group of activity workers and a decider instance in another Auto Scaling group with min/max=1 use SES to send emails to customers.
- D. Use an SQS queue to manage all process tasks Use an Auto Scaling group of EC2 Instances that poll the tasks and execute them. Use SES to send emails to customers.

<details><summary>Answer:</summary><p>
[C]

Categories:
[SES, RDS, SWF, SQS, EC2, ASG, EBS, Elastic Beanstalk]

Explanation:

Question 2@http://jayendrapatil.com/aws-simple-email-service-ses/

</p></details><hr>

