# wordpress_deployment_using_docker_compose




## Step 1: Install docker

Install the package, start and enable the service. 

Also, I am adding 'ec2-user' to 'docker' group.
```sh
sudo yum install docker -y 
sudo systemctl start docker.service 
sudo systemctl enable docker.service 
sudo usermod -a -G docker ec2-user
```


## Step 2: Install Compose

Download the necessary files from github and provide execute privileges 
```sh
sudo curl -SL https://github.com/docker/compose/releases/download/v2.6.0/docker-compose-linux-x86_64 -o /usr/bin/docker-compose 
sudo chmod +x /usr/bin/docker-compose
```
![image](https://user-images.githubusercontent.com/120683482/216142950-0e740b9f-9a9d-46c7-9039-54a24c26ac5c.png)

We can then use the following command to display the version information of Docker Compose that is installed on our system.
```sh
docker-compose version
```

## Step 3: Create a project directory and download the project files

```sh
mkdir wp-project; cd wp-project; 
```

Download the project files into your local machine using the below command.
```sh
git clone https://github.com/sreenidhiramachandran/wp_site_deployment_using_docker_compose.git
```

## Step 4: Start the services defined in the Docker Compose file

Using the below command, we can start the services defined the docker compose file in detached mode.
```sh
docker-compose up -d
```
When we run this command, Docker Compose reads the docker-compose.yml file from the current directory and starts the services defined in it. 

The -d option runs the containers in the background and returns control to the terminal. We can use the docker-compose ps command to see the running containers.

![image](https://user-images.githubusercontent.com/120683482/216144687-5ebef4a7-11b9-4219-ad09-37dc03f9b90b.png)


> ## `Screenshot of website create using docker-compose`

![image](https://user-images.githubusercontent.com/120683482/216141018-44a46ea4-ae57-4ee3-9f43-64dd7c898071.png)
