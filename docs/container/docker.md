# Docker

For full documentation visit [docker.com](https://www.docker.com/){:target="_blank"}.

## Installation

	$ cd /Users/upurusa/container/docker 
	$ docker pull opensuse/portus
	$ docker images
	$ docker container ls
	$ docker run opensuse/portus

	$ docker --version
	$ docker-compose --version
	$ docker-machine --version

	$ docker rmi -f fd484f19954f    

List all containers (only IDs)

	$ docker ps -aq

Stop all running containers

	$ docker stop $(docker ps -aq)

Remove all containers

	$ docker rm $(docker ps -aq)

Remove all images

	$ docker rmi $(docker images -q)


## Steps to download logs from Docker

From outside the docker container (i.e the EC2 host machine) execute the below

	$ sudo docker cp e67771f76d8a:/resourcesearch-service.log /home/ec2-user

From outside the EC2 instance (i.e bridge machine) execute the below

	$ scp -i /etc/ssh/RealizeProd.pem ec2-user@10.2.1.53:/home/ec2-user/resourcesearch-service.log /home/upurusa

From outside the Bridge machine (i.e your local machine) execute the below

	$ scp upurusa@bridge-prod.realizedev.com:/home/upurusa/resourcesearch-service.log /Users/upurusa


[BACK to TOC](./../README.md)

----------