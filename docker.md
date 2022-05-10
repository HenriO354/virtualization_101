# Let’s begin by understanding, What is Docker?
![](/assets/images/docker-logo.svg.png)

<b>Docker is a software platform that simplifies the process of building, running, managing and distributing applications. It does this by virtualizing the operating system of the computer on which it is installed and running.</b> The first edition of Docker was released in 2013.
Now let’s try to understand the problem, and the solution Docker has got to offer

<b>The Problem</b>

Let’s say you have three different Python-based applications that you plan to host on a single server. Each application makes use of a different version of Python, as well as the associated libraries and dependencies. This prevents us from hosting all three applications on the same computer.
The Solution

Docker would virtualize the operating system of the host on which it is installed and running, rather than virtualizing the hardware components. This allows each container to be isolated from the other present on the same host.
The Advantages and Disadvantages of using Docker

Advantages of using Docker

Docker is less demanding when it comes to the hardware required to run it. A container does not have an operating system installed on it. This reduces the bootup time to just a few seconds, as compared to a virtual machine.
Disadvantages of using Docker

Applications with different operating system requirements cannot be hosted together on the same Docker Host. For example, let’s say we have 4 different applications, out of which 3 applications require a Linux-based operating system.
Core Components of Docker

Docker Engine is a client-server based application and consists of 3 main components. Server runs a process called dockerd, which is nothing but a process. Server is responsible for creating and managing Docker Images, Containers, Networks and Volumes on the Docker platform. Client is a command line interface that allows users to interact with Docker using commands.
Docker Terminology

<b>Docker Images and Docker Containers</b> are the two essential things that you will come across daily. Let us take a quick look at some of the terminology associated with Docker. A <b>Docker Image</b> is a <b>template that contains the application and all the dependencies required to run that application on Docker</b>.

What is Docker Hub?

Docker Hub is the official online repository where you could find all the Docker Images that are available for us to use. We could also make them either public or private, based on our requirements. Free users are only allowed to keep one Docker Image as private.
Docker Editions

Docker is available in 2 different editions, as listed below: Community Edition (CE) Enterprise Edition (EE) Community Edition is suitable for individual developers and small teams. Enterprise Edition is further categorized into three different editions.
Installing Docker

One last thing that we need to know before we go ahead with Docker is actually to have Docker installed. You can follow these guides to install Docker on your machine.
Want to skip installation and head off straight to practicing Docker?

Play with Docker is an online playground for Docker. It allows users to practice Docker commands immediately, without having to install anything on your machine. The best part is it’s simple to use and available free of cost.
<br><br>
<b>Docker Commands</b>

Now it’s time to get our hands dirty with Docker commands, for which we all have been waiting till now.

<b>docker create</b>

The first command which we will be looking at is the docker create command. This command allows us to create a new container. The syntax for this command is as shown below: docker create [options] IMAGE [commands] [arguments]

<b>docker ps</b>

The docker ps command allows us to view all the containers that are currently running on the Docker Host. It only displays the container that are presently running. If you want to view containers that were created on this Docker Host, you would need to include the option -a. 

The next command we will look at is the docker ps.

<b>docker start</b>

The next command we will look at, is the docker start command. This command starts any stopped container(s) The syntax for this command is as shown below: docker start [options] CONTAINER ID/NAME [CONTAINERID/NAME…]

<b>docker stop</b>

The next command on the list is the docker stop command. This command stops any running container(s) The syntax for this command is as shown below: 

<b>docker stop.
docker restart</b>

The next command we will look at is the docker restart command. This command restarts any running container(s)<br><br>
The syntax for this command is as shown below: 

<b>docker restart.
docker run</b>

The next command we will be looking at is the docker run command. This command is a combination of the docker create and the docker start command. The syntax for this command is as shown below: docker run [options] IMAGE [commands] [arguments]
docker rm

If we want to delete a container, we use the docker rm command. The first container to be deleted is specified using its container ID, and the second container is specified by its name. The containers need to be in a stopped state in order to delete.
docker images

docker images is the next command on the list. This command lists out all the Docker Images that are present on your Docker Host.$ docker images.
docker rmi

The docker rmi command allows us to remove an image(s) from the Docker Host. The syntax for this command is as shown below. There are many more Docker commands to explore.