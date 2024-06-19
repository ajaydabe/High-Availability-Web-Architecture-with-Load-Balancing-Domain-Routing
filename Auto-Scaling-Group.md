After creating Launch Templates (apache-LT and nginx-LT), let's create two Auto Scaling Groups having apache-LT in one and nginx-LT in another.

Follow the below steps to create Auto Scaling Groups:

Go to **EC2 ==> Auto Scaling ==> Create Auto Scaling Group**

![image](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/45e3633f-c49e-4a67-8d27-0523d600ea90)

#### Step 1 :- Choose launch template

Give the appropriate name to your Auto Scaling Group

Select the Lauch template and click on Next button

![image](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/a2879fa8-e91a-4529-ad01-38a6acced6b3)

#### Step 2 :- Choose instance launch options

Select VPC, Availability Zones and subnets and click on Next.

#### Step 3 :- Configure advanced options

Click on the option "Attach to an existing Load Balancer"

Then choose option "Choose from your load balancer target groups"

Select the Target Group as shown below

![image](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/7a12fefb-22c7-437e-981b-4d5255b20b20)

#### Step 4 :- Configure group size and scaling

Set
  Desired Capacity = 2
  Min desired capacity = 1
  Max desired capacity = 4

![image](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/54b9a631-e52a-47db-b47b-144b41fad08b)

#### Step 5 :- Add notifications (optional)

This section is optional so we don't need to add anything here.

#### Step 6 :- Add tags (optional)

If required, we can add tags here but for now we are not adding anything here.

#### Step 7 :- Review

Review the all selections and click on "Create Auto Scaling Group"

![image](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/2fb5c613-6389-4454-9210-b8b75c569fb3)

We just created nginx-ASG. Similarly follow the above steps and create apache-ASG having apache-LT Launch Template



Now, both the Auto Scaling Groups are created as shown below

![image](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/3e87fef2-03c2-456d-84d9-ccd8b8d7db65)


After creation, you will see the instances are created exactly equal to the desired capacity (2) given in each Auto Scaling Group.

We can see 4 instances got created (2 of apache-server and 2 of nginx-server)

![1](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/de5227f5-d4d4-4ccd-b574-af98ef0db711)


Now we need to add the Auto scaling Policies in apache-ASG and nginx-ASG so that it will add or remove the instances as per the CPU Utilization

For that follow the below steps

Let's create scale in policy in nginx-ASG for scaling in when CPU utilization is equal to or above 80 %

![image](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/acd01aa6-f70c-4010-a209-f79a32d6c73b)


Follow the above procedure and create the same for the scalling out when CPU utilization is equal to or below 60 %

![image](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/54c80aa3-5c6f-4a2e-9e0f-f8c0b49ed671)

Similarly create the scale in and scale out policies for apache-ASG

![image](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/8d49cb57-bd8c-4922-93ee-0a59f65ce095)
