DAY 8 AWS

Assignment 1
Create an infrastructure that would scale as per load: Create cloudwatch alarms for scaling up and scaling down along with sns topic to notify you during any scaling operation.
Put fake load on the stack 
scale up if av. cpu threashold > 70 
scale down if av. cpu threashold < 40 
First do it via console and then via aws cli 

SOLUTIONS
Completed this assignment in 3 parts :-

Created an AMI Image of an Instance
- Created an Ubuntu t2.micro Instance.
- Clicked on Action and selected Image and Create Image.
- An AMI is been created.

![Snapshot]()



Created Launch Configuration.
- Enabled Cloud Watch Monitoring
![Launch Configuration]()

Created Auto Scaling Group
- Used scaling policies to adjust capacity of the group.
- Used simple scaling policy
- Created 2 simple policy i.e. Increase group size & Decrease group size.
- Created alarm in both for load>=70 and load<=40 and provided warm up time of 300 seconds.
- Added Notification by creating a topic and provided SNS and email ID  lovedeeps789@gmail.com.
- This Notification Topic sends a subscription mail to email ID which was been subscribed.
![subscribe]()
- Provided minimum, desired and maximum state.
![Auto scaling]()
![Auto scaling]()
![Auto scaling]()
![Auto scaling]()



Created fake load
- Created ssh connection to one Instance which is been created by autoscaling desired state.
- Created a fake load by giving command yes > /dev/null
![load]()
- Waited for 300 seconds and now autoscaling created an Alarm for load more than 70 and send it to my email ID
![Alarm]()
![Alarm]()
![Alarm]()
![Alarm]()
- Launched Instances one by one.
![Launch]()
![Launch]()
![Launch]()
![Launch]()
- Stopped the fake load by giving command killall yes.
- Auto scaling again created an alarm for load less than 40.
![Alarm]()
![Alarm]()
![Alarm]()
![Alarm]()
- Terminated Instance one by one.
![Terminate]()
![Terminate]()
![Terminate]()
![Terminate]()