After image creation, let's proceed with the Launch Template creation.

Here, we are creating 2 Launch Templates, 1 using apache-image and 1 using nginx-image,
as we will be creating 2 separate Auto scaling Groups for apache-server and nginx-server respectively.

Follow the path **Launch Template ==> Create Launch Template**

screenshot

Give specific name to your template

![image](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/1de2cd1e-46d0-4b23-a1a7-b631858eb821)

Give version as V 1.0

![image](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/ea108196-1b89-471a-84fd-fc74b23bee54)

Select the AMI from **My AMIs ==> Owned by me ==> AMI (apache-image)

![image](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/c47f9ab0-2230-476b-a1e2-ae021e3d05ec)

Select instance type as t2.micro

![image](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/c48cc5bb-b676-4417-8c70-2ea3d8b55104)

