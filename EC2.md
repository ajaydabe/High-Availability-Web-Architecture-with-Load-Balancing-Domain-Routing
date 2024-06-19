
## Steps to create EC2 Instance:

* Login to AWS account
* Search EC2 on search-bar
* Click on launch-instance
* Give name as "nginx-server"
* Select AMI as "Ubuntu 22.04 LTS"
* Select Instance type as "t2.micro"
* Select key pair (its recommonded)
* Select security group
* select EBS volume
* And last click on launch instance.

  create another instance with same configuration and give name as "apache-server"

  ![2instances](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/5a2b67cd-ce19-4ec3-9dc9-ee532544e5a0)

Install apache webserver and nginx webserver on apache-server and nginx-server respectively using the below commands

  On apache-server :-

    sudo apt update -y

    sudo apt install apache2 -y

  On nginx-server :-

    sudo apt update -y

    sudo apt install nginx -y

Further we need to create Image of both the servers. Later on we are going to use these images in Launch Template.

To proceed with image creation, follow the below given steps:

Select one instance and follow the path **Action ==> Image and Template ==> Create Image**

![AMI-creation-step](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/258b608c-8168-4c65-bc4b-871c1155fdfb)
