# Virtualization
## Part 1:Introduction to virtualization concepts
**Core Differences Between VMs and Containers**

**Architecture**
- *Virtual Machines (VMs)*: Run on hypervisors and include a complete operating system plus virtual hardware. Each VM contains its own kernel, libraries, and application.
- *Containers*: Share the host OS kernel and run as isolated processes. Containers package only the application code, runtime, system tools, and libraries needed to run the software.

**Resource Utilization**
- *VMs*: Higher resource consumption since each VM runs a complete OS instance with its own memory allocation, virtual CPU, and disk space.
- *Containers*: More efficient resource usage as they share the host kernel and don't require separate OS instances, allowing higher density deployment on the same hardware.

**Isolation Level**
- *VMs*: Provide strong isolation through hardware-level virtualization. Complete separation between guest OS and host OS with dedicated virtual hardware.
- *Containers*: Offer process-level isolation through OS features like namespaces and cgroups. While isolated, containers share the host kernel, providing lighter but less complete isolation than VMs.

**Performance**
- *VMs*: Generally slower to start and have higher overhead due to running complete OS instances.
- *Containers*: Faster startup (seconds vs minutes) and lower performance overhead since they avoid the hypervisor layer.

**Portability and Consistency**
- *VMs*: Harder to move between environments but offer consistent behavior across different infrastructure.
- *Containers*: Highly portable across environments that support the container runtime, though kernel-dependent features may cause inconsistencies.

**Security**
- *VMs*: Stronger security boundaries due to complete hardware virtualization and OS separation.
- *Containers*: More potential attack surface through the shared kernel, though modern container security features have significantly improved isolation.

## Part 2:Working with Multipass
**Basic commands:** 

- *multipass boot*: multipass launch --nanme myubuntu
- *multipass list*: multipass list
- *multipass info*: multipass info myubuntu
![alt text](image/7.png)
- *multipass shell*: multipass shell myubuntu
![alt text](image/77.png)
- *multipass exec*: multipass exec myubuntu -- ls /
- *multipass stop*: multipass stop myubuntu
- *multipass delete*: multipass delete myubuntu
![alt text](image/777.png)

**Cloud-init:**

*Experiment:* Create a cloud-init configuration file to customize the installation of a new instance. 
![alt text](image/7.2.png)


*File sharing:* tried several times ,still can't solve this problem.
![alt text](image/7.22.png)


## Part 3:Exploring LXD

*Create an Ubuntu container*

*enter container*

![alt text](image/LXD1.png)

*excute task in container*

![alt text](image/LXD2.png)

*stop and delete container*

![alt text](image/LXD3.png)

## part 4:How to Stick Apps with Docker
*install Docker engine*
![alt text](image/7.4.png)

*create a Dockerfile*
![alt text](image/7.44.png)

*create a Docker image:*
![alt text](image/7.444.png)
- *run*

- *visit web server*

- *stop and delete*
![alt text](image/7.4444.png)
![alt text](image/7.44444.png)



## Part 5:Snaps for Self-Contained Applications
*installed snapcraft*
*created a snap package:*
- created a project directory
- initialize the snap project
- edit the snapcraft.yaml file
- build the snap package
- install and test the snap package

![alt text](image/7.5.png)
![alt text](image/7.55.png)