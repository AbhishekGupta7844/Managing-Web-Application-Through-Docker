# Managing-Web-Application-Through-Docker
Here I will explain that how we can solve storage and networking problems through docker. 


## Installation
* First we have to install the docker, I installed the docker on top of Linux os.
* There are so many websites are available to install and setup docker, so there is no any difficulty in installing.
* After installation we have to start docker by command- *systemctl start docker*, in such a way- 

![screenshot docker](https://user-images.githubusercontent.com/64313278/80433023-69c31d00-8913-11ea-87b3-c26a5120271e.png)
* By above command docker will not work permanent, when we give *systemctl stop docker* command or when we switch off our system, docker will stop working and we have to restart when require.

![screenshot stop docker](https://user-images.githubusercontent.com/64313278/80468099-60aa6e00-895c-11ea-818d-ade2db18b5b6.png)

*So for this we run following command for permanent work- *systemctl  enable docker*.

![screenshot enable docker permanent](https://user-images.githubusercontent.com/64313278/80468379-b8e17000-895c-11ea-91ba-2f5a84a0d8be.png)



## Storage Problem Solution
* We can use any database server but I will use mysql database server.
* There are so many versions of mysql but I prefer mysql 5.7.
* So we can install mysql 5.7 by giving command *docker pull mysql:5.7*  

![screenshot mysql](https://user-images.githubusercontent.com/64313278/80432966-439d7d00-8913-11ea-87a1-ac21b2e69577.png)

or we can also download from https://hub.docker.com/_/mysqlimage.
* There is one advantage of using docker for storage purpose that is also mentioned on Google -  


![screenshot google](https://user-images.githubusercontent.com/64313278/80381920-440c2880-88bf-11ea-9e46-dd4c7aab515e.jpg)

* Data that we store is not permanent by default so there might be chances of data lost, to overcome this problem we use docker volume to make data permanent or persistent.
* We can create volume in following manner- 

![screenshot volume](https://user-images.githubusercontent.com/64313278/80381586-c516f000-88be-11ea-9b69-5ad9616598d9.png)

## Internet Connectivity Problem

* The great advantage of docker is that docker is super fast, we can launch any container within seconds so if anytime we lost the connection then we can reconnect within seconds and it will not cause any loss.
* We can launch any container by simple command *docker run container_name*.

![screenshot run](https://user-images.githubusercontent.com/64313278/80468262-94859380-895c-11ea-8443-539c46cc4fc8.png)

* Firewall detect privilege escalations and suspicious process in hosts and containers and also do vulnerable scanning of hosts and running containers so we have to start and stop firewall according to situation, so we can start and stop firewall in following ways -

![screenshot stop firewall](https://user-images.githubusercontent.com/64313278/80468184-80da2d00-895c-11ea-98ff-75bcdddc2c31.png)

![screenshot firewall start](https://user-images.githubusercontent.com/64313278/80468311-a5cea000-895c-11ea-967d-81562a278c34.png)
