## Let's see a demo of how our resources will work

Using DNS Name created by Load Balancer, we will try to generate traffic on our servers

For that, copy DNS and paste on browser and search multiple times.

![image](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/ad69083d-6063-4333-8994-5d1eb1079a0b)

If that not helps to increase CPU Utilization, we can connect to instance and use below command multiple times to increate stress on servers

    yes > /dev/null &

As shown below, we can see incresed CPU Utilization using **CloudWatch Dashboard**

![cpu80](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/43c0e988-b886-49b7-abee-16f2a5cf01df)

When it goes above 80 %, the **Nginx_CPU_Utilization_>=80%** and/or **Apache_CPU_Utilization_>=80%** alarm state will change to **In Alarm**.

It will send you an email as shown below

![image](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/645fd076-48db-4257-a22b-519b26d8e3a3)

This action will add the number of instances given in auto scaling policy, which is 2 in each ASG in our case.

![image](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/b0885ac6-92d0-48f0-8e85-5678e2c221b4)

Also similarly, when CPU Utilization goes below 60 %, **Apache_CPU_Utilization_<=60%** and/or **Nginx_CPU_Utilization_<=60%**
alarm state will change to **In Alarm** as shown below.

![image](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/b603549b-16c4-4288-a9d1-3970647435f1)

Again it will send you an email for CPU Utilization below 60 %

![image](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/e8436785-f257-4311-b258-be613723de90)

And also, it will remove the number of instances given in auto scaling policy, which is 2 in each ASG in our case.

![image](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/8714fad1-9fd9-4722-8849-0dd52603a121)

Last but not least, we created hosted zone.

Let's try if our domain is working or not.

We don't have purchased domain so we have to try it from our instance.

We can use below command to reach out to our servers

    curl <domain_name>    # our domain name is "aws.project2.com"

At first it took me to the apache-server

![image](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/175011ed-bbda-4410-9bdd-f641486188c2)

After using the same command, this time it took me to the nginx-server

![image](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/946d9e0d-5a53-4577-9d03-a1cd28c2885c)

### This is how we successfully completed the demo.
