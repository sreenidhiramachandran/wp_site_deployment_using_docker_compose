# wordpress_deployment_using_docker_compose


Step 1: 

## Install docker

sudo yum install docker -y sudo systemctl restart docker.service sudo systemctl enable docker.service sudo usermod -a -G docker ec2-user

Step 2:

## Install Compose

Download the necessary files from github and provide execute privileges sudo curl -SL https://github.com/docker/compose/releases/download/v2.6.0/docker-compose-linux-x86_64 -o /usr/bin/docker-compose sudo chmod +x /usr/bin/docker-compose

![image](https://user-images.githubusercontent.com/120683482/216142950-0e740b9f-9a9d-46c7-9039-54a24c26ac5c.png)

We can then use the following command to see the compose version. 

docker-compose version

## Create a project directory.
mkdir wp-project; cd wp-project; 

Download the project files into your local machine using the below command.
git clone https://github.com/sreenidhiramachandran/wordpress_deployment_using_docker_compose.git

## Using the below command, we can create and start all the services from your configuration.

docker-compose up -d

![image](https://user-images.githubusercontent.com/120683482/216144687-5ebef4a7-11b9-4219-ad09-37dc03f9b90b.png)



![image](https://user-images.githubusercontent.com/120683482/216141018-44a46ea4-ae57-4ee3-9f43-64dd7c898071.png)
