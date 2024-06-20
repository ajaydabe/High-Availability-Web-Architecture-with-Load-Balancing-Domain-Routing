First task of our project is to create 2 EC2 Insances having Apache and Nginx servers respectively and then create images from those instances.

## Steps to create EC2 Instance:

* Login to AWS account
* Search EC2 on search-bar
* Click on **Launch Instance**
* Give name as **nginx-server**
* Select AMI as **Ubuntu 22.04**
* Select Instance type as **t2.micro**
* Select Key Pair (recommonded)
* Select Security Group
* select EBS Volume
* And last click on **Launch Instance**.

Create another instance with the same configurations and give the name as **apache-server**

![2instances](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/5a2b67cd-ce19-4ec3-9dc9-ee532544e5a0)

Install apache webserver and nginx webserver on apache-server and nginx-server respectively using the below commands

 * **On apache-server :-**

        sudo apt update -y

        sudo apt install apache2 -y

 * **On nginx-server :-**

        sudo apt update -y

        sudo apt install nginx -y

Further we need to create Image of both the servers. Later on we are going to use these images in Launch Templates.

#### **To roceed with the image creation, follow the below given steps :-**

Select one instance (apache-server) and follow the path **Action ==> Image and Template ==> Create Image**

![AMI-creation-step](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/258b608c-8168-4c65-bc4b-871c1155fdfb)

Give name to your image. Scroll down and click on **Create Image** button.

![image](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/e3d39f13-06c6-426d-b7f8-d6c5f00e41fb)

Follow the same steps to create the image from **nginx-server**.

You can see below both the images are created.

![image](https://github.com/ajaydabe/Automated-Cloud-Web-Server-Scaling-with-Load-Balancing-Domain-Routing/assets/160045230/bb8fd94c-a816-4c27-9d87-a90181abb3ed)
