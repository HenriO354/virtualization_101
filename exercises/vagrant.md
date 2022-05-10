# WHAT IS VAGRANT ?

Vagrant is an open-source tool that helps us to automate the creation and management of Virtual Machines. In a nutshell, we can specify the configuration of a virtual machine in a simple configuration file, and Vagrant creates the same Virtual machine using just one simple command. It provides command-line interfaces to automate such tasks. 

Virtual Machine is a machine that does not exist physically but can be used just like a physical computer. Any task that can be done on a physical machine can also be executed in a virtual machine. But Virtual Machine is built on top of a physical system, and multiple virtual machines can be created in a single physical computer. All the virtual machines share the same hardware, but each of them might have a separate operating system. The physical system that hosts all the virtual machines is called the Host Computer. The medium that separates the Host Computer hardware and the virtual environments is something called Hypervisor, or Hyper-V.  
 
Structure of <b>a Virtual Machine<b><br><br>
![](/assets/images/VM2.png)
<br>

Each Virtual Machine should have its own configuration like operating system, CPUs, RAM, Hard Disk Memory, networking, etc. And the creation of such VMs, manually configuring all the properties is really a hectic task. In this scenario, Vagrant comes into the picture. 

Why Vagrant?
An application consists of several components which need to be configured properly to run the application. For example, a modern web application might have components like Java, JavaScript, Python, etc. as a language, MySQL, Oracle, MongoDB, etc. as Databases, other components like webserver, load-balancer, API Gateway, Message Queue, etc. based on requirements.  

Prior to Vagrant, all these components need to be set up manually. During the setup process, a lot of issues are faced-

    In every machine, the setup needs to be done separately, which takes a lot of time.
    The manual configuration might be erroneous, which needs to debug and fix every time.
    The development, testing, and production environment should be identical. But due to this manual installation and setup of the components, there might be a slight difference which provides us a lot of pain, because, in such a scenario, the application might run in a development environment, but face issues in the production one.

Vagrant is the modern solution to all these problems. Instead of setting up all the components manually, Vagrant provides us the feature of using one configuration file (called Vagrantfile), where all the required software components and their configuration information are specified. So, while this same configuration file is executed in multiple machines, Vagrant creates the Virtual Machine on top of each physical machine, installs and setups all the mentioned components automatically, and provides a ready start-to-work Virtual Machine. And since this provides a Virtual Machine, there is no need to bother about whether one software component would run on Windows OS or Linux OS and what should be their configuration and also developer, QA both work in a separate machine, but both machines should have a completely identical setup.

Terminologies Of Vagrant: Before getting into the details of Installation and how to use Vagrant, let’s first discuss the basic terminologies related to Vagrant.

1. Vagrant Box: The basic unit of Vagrant setup is Vagrant Box. Just like Docker Image, Vagrant Box is a self-contained image of the Operating System. More specifically, it is a packaged Virtual Machine. Instead of installing an operating system and all the software components inside a VM manually, 

    The vagrant box is a ready-made base image of a Virtual Machine Environment.
    For example, if there is a need to get some VM with all default setups of Spring Boot application development, one can get the same Vagrant Box. All that is required to do is to download the Vagrant Box and run it. Vagrant creates the VM and development work can be started immediately.
    A lot of Vagrant Box is present in Vagrant Cloud box catalog, which we can use as a base image for our own Virtual Machine.

2. Vagrant File: Vagrant maintains one configuration file, called Vagrantfile, where all configurations of a VM are mentioned. And Vagrant creates the Virtual Machine with the same configuration mentioned in the file. Even if there is a need to install some software in the VM, one can specify the same in Vagrantfile, and Vagrant downloads and installs the same for us. 

    Let’s look into the steps for [provisioning](https://www.geeksforgeeks.org/what-is-vagrant/) one VM using Vagrant. 