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

3. Write command to create an nginx container in detached mode with name assignment-2 running on host port 9090 on a custom network named assignment-2:
=======================================================================================================================================================
    docker container run -d --name assignment-2 --publish 9090:80 --network=assignment-2 nginx

4. Write command to see logs of the above container:
====================================================
    docker container logs assignment-2

5. Write commands to Exec into the container and cat the output of the default nginx file at /usr/share/nginx/html/index.html:
==============================================================================================================================
    docker container run -it --name=assignment-2 -p 9001:80 > /usr/share/nginx/html/index.html

6. Exit the above container, and now recreate the container by Volume using bind mounting:
==========================================================================================
    docker container run -it --name=assignment-2 -p 9001:80 -v /usr/share/nginx/html/:/workingfolder/

7. Command to exec into the above container and replace the default index.html to a custom one, which says that â€œI am becoming a Docker Expertâ€ and it 
should be persisted for the next times:
==========================================================================================================================================================
    cd workingfolder
	cat > index.html
	â€œI am becoming a Docker Expertâ€
	^C