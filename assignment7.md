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

## Part 3:Exploring LXD

## part 4:How to Stick Apps with Docker

## Part 5:Snaps for Self-Contained Applications
