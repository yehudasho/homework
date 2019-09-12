# home assignment 

In this home assigments I was asked to create an echo-system which can run on  multiple environments.
1.	Deploy MySQL & Kafka on a K8s cluster
2. 2.	On the MySQL initial startup the container will import SQL file containing the data that will later on be shipped to Kafka from the following location
3.	On the Kafka initial startup the container will create topics that will later on be used by the consumer\producer services.
4.	Deploy the 2 data shipper services on the same K8s cluster
 	Containerize the services following Docker best practices and the build guidance in the Github repository. 
  
# Prerequisites

1. in order to get the system up and running on your local machine for development and testing purposes, you'll need Dokcer and Docker-compose.

How to install Docker and Docker-compose: On Linux (CentOs 7): https://github.com/NaturalHistoryMuseum/scratchpads2/wiki/Install-Docker-and-Docker-Compose-(Centos-7)

On Windows 10 64bit: Pro, Enterprise or Education (Build 15063 or later): https://docs.docker.com/docker-for-windows/install/

On other Windows versions: https://docs.docker.com/toolbox/toolbox_install_windows/

On mac: https://docs.docker.com/docker-for-mac/install/

2. based on DOcer-comopse you should install minikube, link for installation:
https://vocon-it.com/2018/11/19/single-node-kubernetes-cluster-1-installing-minikube-on-centos/

# Setting up on local machine ( i used CentOS 7 )

1. git clone the both services ( producer and consumer )
  https://github.com/surielb/devops-test
2. copy the contant of consumer file int app.properties
3. copy the contant of producer file int app.properties

# run the docker-compose

two servicses will be establish during the runtime of docker-compose 
  Mysql - and init script will be run
  Kafka

# Building 
so build order is:

* mvn install -f ./common/pom.xml
* mvn install -f ./producer/pom.xml
* mvn install -f ./consumer/pom.xml

# convert docker-compose.yaml to char via kompose
https://github.com/kubernetes/kompose



