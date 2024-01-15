# Shazia-Implement-ASG-on-EC2-ELB-.
step1. Create an Amazon Machine Image (AMI):
Launch an EC2 instance and configure it with the necessary software and configurations for your web application.
Create an AMI from the configured EC2 instance. This AMI will be used to provision new instances quickly.

step2. Set Up an Elastic classic Load Balancer (ELB):
Create an Elastic Load Balancer in the AWS Management Console. Select any one AZ other than the instance subnet.
Configure listeners and routing rules based on your application requirements (e.g., HTTP on port 80).
Add the instances (from the AMI created) to the ELB.

step3: Create alerts:
SNS alert for e-mails -Create a topic and give subscription 
In SNS section give Topic name and protocal-Gmail.ID and confirm

step-4 : Create launch configuration
Go to launch config-Name
                    Select AMI name, instance type, select key pair and launch wizard and create

step5:Create an Auto Scaling Group:
-Create launch configuration 
Set up an Auto Scaling group using the AWS Management Console.
Configure the desired capacity, minimum and maximum instances, and network settings.
Link the Auto Scaling group to the ELB to distribute traffic across instances.

step6 : Configure Auto Scaling Policies:
Define scaling policies for scaling out and scaling in based on metrics like CPU utilization, network 
traffic, or custom CloudWatch metrics.
For example, you might set a policy to add instances when average CPU utilization exceeds a certain threshold and remove instances when it drops below another threshold.
7. Implement Health Checks:
Configure health checks to monitor the instances' health within the Auto Scaling group.
Set up CloudWatch Alarms to trigger Auto Scaling actions based on health check results.
8. Test the Auto-Scaling Setup:
Monitor the scaling activities in the Auto Scaling group and check the ELB to confirm new instances are added and traffic is distributed.Check the metrics.
9. Optimize :
Continuously monitor and analyse the performance and costs of your auto-scaling setup.
Adjust Auto Scaling policies, instance types, and other configurations as needed to optimize the environment.

DNS  -shaz-LB-964136400.eu-west-2.elb.amazonaws.com
