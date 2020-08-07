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