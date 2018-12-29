### Question 1:

You want to pass queue messages that are 1GB each. How should you achieve this?

- A. Use Kinesis as a buffer stream for message bodies. Store the checkpoint id for the placement in the Kinesis Stream in SQS.
- B. Use the Amazon SQS Extended Client Library for Java and Amazon S3 as a storage mechanism for message bodies.
- C. Use SQS’s support for message partitioning and multi-part uploads on Amazon S3.
- D. Use AWS EFS as a shared pool storage medium. Store filesystem pointers to the files on disk in the SQS message bodies.

<details><summary>Answer:</summary><p>
[B]

Categories:
[S3, SQS, Kinesis]

Explanation:

Question 1@http://jayendrapatil.com/aws-storage-options-whitepaper-s3-glacier/

B: http://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/s3-messages.html

B: (Amazon SQS messages with Amazon S3 can be useful for storing and retrieving messages with a message size of up to 2 GB. To manage Amazon SQS messages with Amazon S3, use the Amazon SQS Extended Client Library for Java. Refer )

</p></details><hr>

### Question 2:

Company ABCD has recently launched an online commerce site for bicycles on AWS. They have a “Product” DynamoDB table that stores details for each bicycle, such as, manufacturer, color, price, quantity and size to display in the online store. Due to customer demand, they want to include an image for each bicycle along with the existing details. Which approach below provides the least impact to provisioned throughput on the “Product” table?

- A. Serialize the image and store it in multiple DynamoDB tables
- B. Create an “Images” DynamoDB table to store the Image with a foreign key constraint to the “Product” table
- C. Add an image data type to the “Product” table to store the images in binary format
- D. Store the images in Amazon S3 and add an S3 URL pointer to the “Product” table item for each image

<details><summary>Answer:</summary><p>
[D]

Categories:
[S3, DynamoDB]

Explanation:

Question 2@http://jayendrapatil.com/aws-storage-options-whitepaper-s3-glacier/

</p></details><hr>

