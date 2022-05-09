# <center>CONTAINERS<br>
 
- What's a container ?
<br><br>
Containers are the products of operating system virtualization. They provide a lightweight virtual environment that groups and isolates a set of processes and resources such as memory, CPU, disk, etc., from the host and any other containers. The isolation guarantees that any processes inside the container cannot see any processes or resources outside the container..<br>

![docker-containerized-applications](/assets/images/docker-containerized-appliction-blue-border_2.png.webp)

# Containers exist in two main form <br>(application and system), how do they differ?<br><br>

# Application containers<br>
+ Are designed to package and run a single service. Container technologies like Docker and Rocket are examples ofSo even though they share the same kernel of the host there are subtle differences make them different.

# System containers<br>
+ are virtual environments that share the kernel of the host operating system but provide user space isolation. For all practical purposes, you can think of OS containers as VMs. You can install, configure and run different applications, libraries, etc., just as you would on any OS. Just as a VM, anything running inside a container can only see resources that have been assigned to that container.

+ OS containers are useful when you want to run a fleet of identical or different flavors of distros. Most of the times containers are created from templates or images that determine the structure and contents of the container. It thus allows you to create containers that have identical environments with the same package versions and configurations across all containers.

# Why are containers so inherently linked to Linux?<br>

- Can you list some containers technologies and explain their use?<br><br>

