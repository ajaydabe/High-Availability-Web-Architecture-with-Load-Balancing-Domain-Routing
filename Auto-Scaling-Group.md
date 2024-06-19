After creating Launch Templates (apache-LT and nginx-LT), let's create two Auto Scaling Groups having apache-LT in one and nginx-LT in another.

Follow the below steps to create Auto Scaling Groups:

**********sceenshot here showing path to create ASG**********

#### Step 1 :- Choose launch template

Give the appropriate name to your Auto Scaling Group

Select the Lauch template and click on Next button

![image](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/a2879fa8-e91a-4529-ad01-38a6acced6b3)

#### Step 2 :- Choose instance launch options

Select VPC, Availability Zones and subnets

#### Step 3 :- Configure advanced options

Click on the option "Attach to an existing Load Balancer"

Then choose option "Choose from your load balancer target groups"

Select the Target Group as shown below

![image](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/de8ea76f-2131-40cf-bf41-4fee37c76a35)

#### Step 4 :- Configure group size and scaling

Set
  Desired Capacity = 2
  Min desired capacity = 1
  Max desired capacity = 4

![image](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/54b9a631-e52a-47db-b47b-144b41fad08b)

#### Step 5 :- Add notifications (optional)

#### Step 6 :- Add tags (optional)

#### Step 7 :- Review

Review the all selections and click on "Create Auto Scaling Group"

![image](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/2fb5c613-6389-4454-9210-b8b75c569fb3)
