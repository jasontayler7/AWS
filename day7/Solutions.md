DAY 3 AWS

Assignment 1

Rajat is the devops guy in 'abc' organization and he is responsible for creating 't2.micro' and all the 'm' family of instances as per requirement but he can't terminate 'm' family of instances but that's not the case with t2.micro. Tejasvi Rana has got root access to the account but he isn't a technical guy. He is always suspicious about Rajat's actions in company's aws account. Luckily Tejasvi has got a friend, Priyanka jugran, she is amazon certified and knows everything about aws. Tejasvi wants Priyanka to cross check rajat's IAM permissions. In order to do that, he gave priyanaka full access. Now priyanka needs s3 storage for one of her friend, priyanka sharama to run athena queries for data analysis,they don't want to pay for that from their own aws account. Jugran has created a bucket with name 'abc-data' with a policy that sharma will only be able to access this bucket from a particular ec2 instance that she created & provided the user details to sharma. Rajat referenced his friends kavit and vishwas to his organization and now all of then share the same permission level. Kushgra is also one of the team memebers from operations team but recently he has got a task to create and run lambda function that is going to access rds database.






SOLUTIONS

Created the whole scenario in 3 steps :-

1. DevOps group

Created users Anshul , Kavit and Vishwas and added them into DevOps Group with 2 policies i.e. allowed policy for t2.micro and m*.* and denied policy for m*.* (Termination)

![User](https://github.com/lovedeepsh/AWS/blob/master/AWS-day7-images/IAM-USER1234.png)

![allowed policy](https://github.com/lovedeepsh/AWS/blob/master/AWS-day7-images/allowed-policy-VisualEditor.png)

![allowed policy](https://github.com/lovedeepsh/AWS/blob/master/AWS-day7-images/allowed-policy-json.png)

![denied policy](https://github.com/lovedeepsh/AWS/blob/master/AWS-day7-images/Denied-Policy-VisualEditor.png)

![denied policy](https://github.com/lovedeepsh/AWS/blob/master/AWS-day7-images/Denied-policy-json.png)

![Instance Terminate Denied](https://github.com/lovedeepsh/AWS/blob/master/AWS-day7-images/Instance-Terminate-denied.png)

![Instance Terminated](https://github.com/lovedeepsh/AWS/blob/master/AWS-day7-images/not-authorized-insstance-type.png)

![Not Authorised Instance](https://github.com/lovedeepsh/AWS/blob/master/AWS-day7-images/Terminate-Instance.png)

![Policies](https://github.com/lovedeepsh/AWS/blob/master/AWS-day7-images/policies.png)





2. Created a bucket in S3 and created a policy for allowing access on that bucket and inside bucket and attached that policy to an ec2 instance. 

Created a user and allowed access to that instance for that user.

![Bucket](https://github.com/lovedeepsh/AWS/blob/master/AWS-day7-images/buckets.png)

![Bucket](https://github.com/lovedeepsh/AWS/blob/master/AWS-day7-images/bucket-role-json.png)

![Bucket](https://github.com/lovedeepsh/AWS/blob/master/AWS-day7-images/bucket-role-policy-visual-editor.png)

![Bucket](https://github.com/lovedeepsh/AWS/blob/master/AWS-day7-images/access-denied-bucket.png)

![Bucket](https://github.com/lovedeepsh/AWS/blob/master/AWS-day7-images/access-done.png)

3. Created a user kushgra and attached a policy to it allowing all lambda access and created a role for lambda service to access RDS.

![lambda](https://github.com/lovedeepsh/AWS/blob/master/AWS-day7-images/khushagra.png)

![lambda](https://github.com/lovedeepsh/AWS/blob/master/AWS-day7-images/khushagra-lambda.png)

![lambda](https://github.com/lovedeepsh/AWS/blob/master/AWS-day7-images/lambdarole.png)

![lambda](https://github.com/lovedeepsh/AWS/blob/master/AWS-day7-images/kushgra-ec2-denied.png)

![lambda](https://github.com/lovedeepsh/AWS/blob/master/AWS-day7-images/kushgra-lambda-access.png)

![lambda](https://github.com/lovedeepsh/AWS/blob/master/AWS-day7-images/kushgra-RDS-allowed.png)

