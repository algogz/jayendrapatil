### Question 1:

Which of the following are valid statements about Amazon S3? Choose 2 answers

- A. S3 provides read-after-write consistency for any type of PUT or DELETE.
- B. Consistency is not guaranteed for any type of PUT or DELETE.
- C. A successful response to a PUT request only occurs when a complete object is saved
- D. Partially saved objects are immediately readable with a GET after an overwrite PUT.
- E. S3 provides eventual consistency for overwrite PUTS and DELETES

<details><summary>Answer:</summary><p>
[C, E]

Categories:
[S3]

Explanation:

Question 1@http://jayendrapatil.com/aws-s3-data-consistency-model/

</p></details><hr>

### Question 2:

A customer is leveraging Amazon Simple Storage Service in eu-west-1 to store static content for web-based property. The customer is storing objects using the Standard Storage class. Where are the customers’ objects replicated?

- A. Single facility in eu-west-1 and a single facility in eu-central-1
- B. Single facility in eu-west-1 and a single facility in us-east-1
- C. Multiple facilities in eu-west-1
- D. A single facility in eu-west-1

<details><summary>Answer:</summary><p>
[]

Categories:
[S3]

Explanation:

Question 2@http://jayendrapatil.com/aws-s3-data-consistency-model/

</p></details><hr>

### Question 3:

A user has an S3 object in the US Standard region with the content “color=red”. The user updates the object with the content as “color=”white”. If the user tries to read the value 1 minute after it was uploaded, what will S3 return?

- A. It will return “color=white”
- B. It will return “color=red”
- C. It will return an error saying that the object was not found
- D. It may return either “color=red” or “color=white” i.e. any of the value

<details><summary>Answer:</summary><p>
[D]

Categories:
[S3]

Explanation:

Question 3@http://jayendrapatil.com/aws-s3-data-consistency-model/

D: Eventual Consistency

</p></details><hr>

