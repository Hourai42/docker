# docker
Aiight, let's learn how to use docker so you can install Anaconda on these macs. 

Commands used!
-------------
docker version
docker-machine create --driver virtualbox Char
docker-machine rm [name]
docker-machine ls
docker-machine ip Char
docker-machine env Char
eval $(docker-machine env Char)
docker ps
docker pull [image]
docker run [image]
docker inspect [container]
exit
docker --help
docker volume create [name]
docker volume ls
docker stop [container]
docker exec [container] env
docker logs spawning-pool
docker restart [container]
docker-machine ssh [virtual machine]
docker-machine scp [file] [virtual machine]:[location]
docker exec
docker swarm init --advertise-addr [IP ADDRESS OF VIRTUAL MACHINE]
docker-machine rm default to clear an inactive machine
docker swarm join --token [TOKEN]
docker swarm join-token manager
docker network create [name]
docker node ls
docker node inspect [node ID]
docker service ls
docker service logs [service]
docker service scale [service]=[number of replicas]
docker service rm [service]
docker rmi [image]
docker images
docker-machine rm [machine]

Vocabulary
----------

docker - why use it? Deploy, develop, and run application w/ containers, also known as containerization.

image - executable package that includes everything needed to run an application

container - runtime instance of what the image becomes in memory when executed. runs natively and shares kernel of the host machine

virtual machine - a full-blown guest operating system with virtual access to host resources

dockerfile - a portable image that defines what's going on in the environment inside the container. Access to resources like networking interfaces and disk drives is virtualized inside the environment, so ports need to be mapped manually

volume - preferred mechanism for persisting data generated by and used by Docker containers-- completely managed by Docker

bind mounts - dependent on directory structure of host machine, limited functionality compared to volumes

swarm - a clustering and scheduling tool for Docker containers-- admins and developers can establish and manage a cluster of Docker nodes as a single virtual system

replica - a replicated service is a docker swarm service that has a specified number of replicas running. Consists of multiple instances of the specified docker container
