
screenshot of showing path

1) Create alarm to trigger auto scaling policy when CPU Utilization of apache-server goes above or equal to 80 %

Click on "Select metric" option

![image](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/40879c2c-5420-4bdf-b459-510d4f268a52)

Go to EC2 ==> Auto scaling Group ==> Select apache-ASG CPU Utilization

Click on Select Metric

![image](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/82291b79-92dd-4c99-94e7-e6842e9de53c)


![image](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/3323c74e-ea9d-459d-8b33-a45dc4bcac85)


![image](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/37ddffdb-52d2-4c1a-b3e5-d82168f87396)


![image](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/876c0451-a954-4d94-bf8e-f2f4be8025b1)

Give alarm name and click on next

![image](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/904aa3bc-f4a9-41e5-aa47-6e85c4662265)

Preview and click on create Alarm

Follow the above steps to create Alarm to

  To trigger auto scaling policy when CPU Utilization of apache-server is equal to or below 60 %

  To trigger auto scaling policy when CPU Utilization of nginx-server goes above or equal to 80 %

  To trigger auto scaling policy when CPU Utilization of nginx-server is equal to or below 60 %

Our alarms are now created

![image](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/a2998f8a-5dbc-4604-8f34-94f65b48cd1a)
