# <center>WHAT'S A VIRTUAL MACHINE ?

<b>A Virtual Machine Is A Virtual Computer Within A Computer</b>

- A virtual machine, commonly shortened to just VM, is no different than any other physical computer like a laptop, smart phone, or server. 

- It has a CPU, memory, disks to store your files, and can connect to the internet if needed. While the parts that make up your computer (called hardware) are physical and tangible, VMs are often thought of as virtual computers or software-defined computers within physical servers, existing only as code.<br><br>
![virtual computers within computers](/assets/images/vm.png)

- <b>Virtual hosts</b> are able to share resources between multiple guests, or virtual machines, each with their own operating system instance. The two basic types of virtual machines are process and system VMs.

    A process virtual machine allows you to run a single process as an application on a host machine.
    An example of a process virtual machine is the Java Virtual Machine (JVM) which allows any system to run Java applications as if they were native to the system.
    A system virtual machine is a fully virtualized VM designed to be a substitute for a physical machine. It runs on a different host machine by utilizing a hypervisor such as VMware ESXi to access the underlying machine’s resources.<br><br>

+ What's a hypervisor?<br><br>
A hypervisor is a program for creating and running virtual machines. <b>Hypervisors</b> have traditionally been split into <two classes: type one, or "bare metal" hypervisors> that run guest virtual machines directly on a system's hardware, essentially behaving as an operating system. 
<b>Type two, or "hosted" hypervisors</b> behave more like traditional applications that can be started and stopped like a normal program. In modern systems, this split is less prevalent, particularly with systems like KVM. KVM, short for kernel-based virtual machine, is a part of the Linux kernel that can run virtual machines directly, although you can still use a system running KVM virtual machines as a normal computer itself..<br><br>
![Vocabulary](/assets/images/hypervisor.jpeg)
<br><br>

+ Can you list some <b>VM technologies</b> and explain their use?<br><br>
<b>Vocabulary</b>: 

![Vocabulary](/assets/images/vocabulary.png)
<br><br><br>
![6 open source virtualization technologies](/assets/images/6-open-source-virtualization-technologies.png)

