1. Docker Containers vs Virtual Machines:
=========================================
a)
    Docker is container based technology and containers are just user space of the operating    system
    Virtual Machine is not based on container technology and made up of user space plus kernel space of an operating system

b)
    Docker containers when running share the host OS kernel
    Virtual Machines share hardware resource from the host

c)
    Docker container is just a set of processes that are isolated from the rest of the system, running from a distinct image that provides all files necessary to support the processes
    Virtual Machine has Operating System & Application which run completely in isolation

d)
    Docer reduced IT management resources, reduced size of snapshots, quicker spinning up apps, reduced & simplified security updates, less code to transfer, migrate and upload workloads
    Virtual Machine reduced physical IT management resources, can be huge in size of snapshots, time required spinning up apps, complex security updates, large transfer, migrate and upload workloads

e)
    Docer container is faster to build
    Virtual Machine require time to build

d)
    Docker container / image is easy to portable
    Virtual Machine require more resources

References are taken from below link:
https://devopscon.io/blog/docker/docker-vs-virtual-machine-where-are-the-differences/

2. Docker Architecture:
=======================
a)
    Docker follows client-server architecture

b)
    Docker Client, Docker Host and Docker Registry are three main components of architecture

c)
    Docker Client: users commands (CLI) and REST APIs to communicate with the Docker Deamon (Server)
    docker build, docker pull, docker run are some commands used at docker client
    Dockr client can communicate with more than one docker deamon.

d)
    Docker Host: is used to provide an environment to execute and run applications
    It contains the docker daemon, images, containers, networks, and storage

e)
    Docker Registry: manages and stores the Docker images.
    There are two types of registries in the Docker:
        Pubic Registry: is also called as Docker hub
        Private Registry: is used to share images within the enterprise

References are taken from below link:
https://www.javatpoint.com/docker-architecture