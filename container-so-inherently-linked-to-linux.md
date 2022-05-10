# Why are containers so inherently linked to Linux ?

Ultimately, <b>containers</b> are <b>a feature of Linux</b>. Containers have been a part of the Linux operating system for more than a decade, and go back even further in UNIX. 
That’s why, despite the very recent introduction of Windows containers, <b>the majority of containers we see are in fact Linux containers</b>. That also means that <b>if you’re deploying containers</b>, your <u><b>Linux choices</b></u> matter a lot.

![](/assets/images/Container-Internals-Lab-Kernel-Containers.png)
<br><br>
<b>First</b>, each containerized process is isolated from other processes running on the same Linux host, using kernel namespaces. Kernel namespaces provide a virtualized world for the container processes to run in. For example, the "PID" namespace causes a containerized process to only see other processes inside of that container, but not processes from other containers on the shared host. Additional security isolation is provided by kernel features like dropped capabilities, read-only mounts and seccomp. Additional file system security isolation is provided by SELinux in distributions like Red Hat Enterprise Linux. This isolation helps ensure that one container cannot exploit other containers or take down the underlying host.

<b>Second</b>, the resources consumed by each container process (memory, cpu, I/O, etc.) are confined to specified limits, using Linux control groups (or "cgroups"). This helps eliminate noisy neighbor issues, by keeping one container from over-consuming Linux host resources and starving other containers.

This ability to both isolate containerized processes and confine the resources they consume is what enables multiple application containers to run more securely on a shared Linux host. The combination of isolation and resource confinement is what makes a Linux process a Linux container. In other words, containers are Linux. Let’s explore some of the implications of this.
