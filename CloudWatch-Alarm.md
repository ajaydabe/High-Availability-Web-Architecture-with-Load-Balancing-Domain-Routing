### Now, we will create CloudWatch Alarms with SNS Topic so we can use them in our Scaling Policy

Let's create below CloudWatch Alarms to trigger the Auto Scaling event

  1) When CPU Utilization of apache-server is >=80 %
  2) When CPU Utilization of apache-server is <=60 %
  3) When CPU Utilization of nginx-server is >=80 %
  4) When CPU Utilization of nginx-server is <=60 %

### Steps are as follows

Go to **CloudWatch ==> All Alarms ==> Create Alarm**

![image](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/0af22c1e-e4f2-46bc-ac8c-92e310c6676d)

First let's create alarm to trigger auto scaling policy when CPU Utilization of apache-server is equal to or above 80 %

Click on **Select metric** option

![image](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/40879c2c-5420-4bdf-b459-510d4f268a52)

Go to **EC2 ==> Auto scaling Group ==> Select apache-ASG CPU Utilization**

#### Specify metric and conditions

Click on Select Metric

![image](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/82291b79-92dd-4c99-94e7-e6842e9de53c)

We will select conditions as per our requirements

i.e when for given Statistic **(maximum)** CPU Utilization within given Period **(1 minute)** is equal to or above **(Greater / Equal >= threshold)** our threshold value **(80)** 

![image](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/3323c74e-ea9d-459d-8b33-a45dc4bcac85)


![image](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/37ddffdb-52d2-4c1a-b3e5-d82168f87396)


![image](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/a39f02aa-62db-45c8-a429-17191d4edb3a)


Give alarm name and click on next

![image](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/904aa3bc-f4a9-41e5-aa47-6e85c4662265)

Preview and click on create Alarm

Follow the above steps to create Alarm to

  To trigger auto scaling policy when CPU Utilization of apache-server is equal to or below 60 % (Create SNS topic in this for CloudWatch_Alarms_below_60% CPU Utilization)

  To trigger auto scaling policy when CPU Utilization of nginx-server goes above or equal to 80 % (use "CloudWatch_Alarms_above_80" SNS topic)

  To trigger auto scaling policy when CPU Utilization of nginx-server is equal to or below 60 % (use "CloudWatch_Alarms_below_60" SNS topic)

Our alarms are now created

![image](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/a2998f8a-5dbc-4604-8f34-94f65b48cd1a)


We can create a dashboard so that we can see the CPU Utilization of both servers on the graph

Follow below steps to create Custom Dashboard



Give a meaningful name to your dashboard.

![image](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/e582d4ab-a039-435c-baff-0b345e533250)


![image](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/c8c467aa-b9ce-4344-ad65-056fb82623f3)

Go to EC2 ==> by Auto Scaling Group and search for CPUUtilization in search box.

You will see apache-ASG and nginx-ASG. Select both and click on Create Widget

![image](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/31756834-d98b-4536-9e38-fcb32afb7a9a)

Make the changes on the next screen as you want and click on Save button

![image](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/4326842f-e4e2-40f4-a020-002692855e13)

We can see in SNS (Simple Notification Service) service that our SNS Topics are now created

![image](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/6774a9fe-affb-4116-a895-e61f11dfbef2)

You will receive the email similar to shown below

Click on Confirm Subscription to receive the notifications when your alarm triggers

![image](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/ab076eed-c7c2-4b59-94ed-2d4f85015313)

Now you can see subscription status is "Confirmed" now

![image](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/f29c3071-661c-44e1-87d2-19a27cb4911b)
