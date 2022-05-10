# Linux cgroups and namespaces
<br>

# Cgroups:

A control group (cgroup) is a Linux kernel feature that limits, accounts for, and isolates the resource usage (CPU, memory, disk I/O, network, and so on) of a collection of processes.

Cgroups provide the following features:

    Resource limits – You can configure a cgroup to limit how much of a particular resource (memory or CPU, for example) a process can use.

    Prioritization – You can control how much of a resource (CPU, disk, or network) a process can use compared to processes in another cgroup when there is resource contention.

    Accounting – Resource limits are monitored and reported at the cgroup level.

    Control – You can change the status (frozen, stopped, or restarted) of all processes in a cgroup with a single command.

So basically you use cgroups to control how much of a given key resource (CPU, memory, network, and disk I/O) can be accessed or used by a process or set of processes. Cgroups are a key component of containers because there are often multiple processes running in a container that you need to control together. In a Kubernetes environment, cgroups can be used to implement resource requests and limits and corresponding QoS classes at the pod level.

The following diagram illustrates how when you allocate a particular percentage of available system resources to a cgroup (in this case cgroup‑1), the remaining percentage is available to other cgroups (and individual processes) on the system.<br><br>

#   namespaces:

<b>“Namespaces"</b> are a feature of the Linux kernel that partitions kernel resources such that one set of processes sees one set of resources while another set of processes sees a different set of resources.”

In other words, the key feature of namespaces is that they isolate processes from each other. On a server where you are running many different services, isolating each service and its associated processes from other services means that there is a smaller blast radius for changes, as well as a smaller footprint for security‑related concerns. Mostly though, isolating services meets the architectural style of microservices as described by Martin Fowler.

Using containers during the development process gives the developer an isolated environment that looks and feels like a complete VM. It’s not a VM, though – it’s a process running on a server somewhere. If the developer starts two containers, there are two processes running on a single server somewhere – but they are isolated from each other.<br><br>

<b>Types of Namespaces</b><br><br>
![Namespaces-cgroups_resources-limits.svg](/assets/images/Namespaces-cgroups_resource-limits.svg)

Within the Linux kernel, there are different types of namespaces. Each namespace has its own unique properties:
<br>

+ A user namespace has its own set of user IDs and group IDs for assignment to processes. In particular, this means that a process can have root privilege within its user namespace without having it in other user namespaces.<br>

+ A process ID (PID) namespace assigns a set of PIDs to processes that are independent from the set of PIDs in other namespaces. The first process created in a new namespace has PID 1 and child processes are assigned subsequent PIDs. If a child process is created with its own PID namespace, it has PID 1 in that namespace as well as its PID in the parent process’ namespace. See below for an example.


+ A network namespace has an independent network   stack: its own private routing table, set of IP addresses, socket listing, connection tracking table, firewall, and other network‑related resources.

+ A mount namespace has an independent list of mount points seen by the processes in the namespace. This means that you can mount and unmount filesystems in a mount namespace without affecting the host filesystem.


+ An interprocess communication (IPC) namespace   has its own IPC resources, for example POSIX message queues.
    
+ A UNIX Time‑Sharing (UTS) namespace allows a single system to appear to have different host and domain names to different processes.
