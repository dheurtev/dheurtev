# Virtualization and containers technologies

Tools and packages I am using are marked `in use`.
Tools and packages I used are marked as `past`.

- [Virtualization technologies](#virtualization-technologies)
- [Virtual Environment](#virtual-environment)
- [Application containers](#application-containers)

## Virtualization technologies ##
**[`^        back to top        ^`](#)**
### Level 1 Hypervisors Virtualization on Windows ###
- [Microsoft Hyper-V](https://docs.microsoft.com/en-us/virtualization/hyper-v-on-windows/quick-start/enable-hyper-v): Native Level 1 hypervisor to create virtual machines on x86-64 systems running Windows. Used by WSL2. `⚠ Proprietary` `in use`
### Linux virtualization technologies ###
- [Qemu](https://www.qemu.org/): Generic and open-source machine emulator and virtualizer for Linux. `GPLv2` `in use`
- [KVM](https://www.linux-kvm.org/page/Main_Page) : KVM (for Kernel-based Virtual Machine) is an open-source full virtualization solution for Linux on x86 hardware containing virtualization extensions (Intel VT or AMD-V). Part of Linux Kernel. `GPLv2` `in use`
- [Libvirt/libvirtd](https://libvirt.org/): Open-source API, daemon and management tool for managing platform virtualization in Linux. `LGPL` `in use`
### Level 1 Hypervisors in Linux ###
[Performance Evaluation of Xen, KVM, and Proxmox Hypervisors](https://www.researchgate.net/publication/327482365_Performance_Evaluation_of_Xen_KVM_and_Proxmox_Hypervisors)
- [Proxmox VE](https://www.proxmox.com/en/proxmox-ve) : Open-source virtualization management platform - Uses KVM, LXD, CEPH, etc - Documentation - Debian based - `GNU AGPL, v3` `in use`
- [Virt-Manager](https://virt-manager.org/): Desktop virtual machine monitor for KVM/QEMU/Libvirt. `GPLv2` `past`

### Level 2 Hypervisors ###
#### Cross-platform ####
  * [Oracle VM VirtualBox](https://www.virtualbox.org/): Open Source Level 2 x86 and AMD64/Intel64 virtualization product. Runs as an app on Windows, Linux, OS X, Solaris. Has a gui. `GPLv2` and `Proprietary` extentions `past`

## Virtual Environment ##
**[`^        back to top        ^`](#)**
- [LXC/LXD](https://linuxcontainers.org/): Linux Containers is an operating-system-level virtualization method for running multiple isolated Linux systems on a control host using a single Linux kernel. Chroot on steroids, near bare metal performance, not a VM, fully functionnal OS, standard Linux tools (CLI), Data stored in or outside the container, can be used for composite stacks, file system neutral, but shares same kernel as host, limited portability - Canonical Project - `GNU LGPL v.2.1`
  * LXC : Linux container runtime that consists of tools, templates, and library and language bindings
  * LXD : System container and virtual machine manager
  * Used for stateful containers (e.g. stable services, database)
  * LXC does not allow live migration
- [chroot](https://www.howtogeek.com/441534/how-to-use-the-chroot-command-on-linux/): How to use the chroot command on Linux. Uses standard Linux backup tools. `past`

## Application containers ##
[Compare Docker vs Containerd - Docker by itself is more suitable for a developer desktop environment than a production setup](https://earthly.dev/blog/containerd-vs-docker/)

[Compare Docker vs. Podman - No significant differences between Docker and Podman](https://www.techtarget.com/searchitoperations/tip/Compare-Docker-vs-Podman-for-container-management)

- [Docker](https://www.docker.com/): open platform for developing, shipping, and running applications. Deployment constistence, portable (but not between Linux and Windows Docker), versioning, component reuse, REST API oriented but layered file system, ephemeral instances (persistent data storage is complicated), not native speed performance, limited monitoring - `Apache version 2.0` with `Proprietary` tools `in use`
  * For single app containers/microservices in large numbers
  * Good to try new software or software with multiple dependencies 
  * [Docker Desktop Windows](https://docs.docker.com/desktop/install/windows-install/): Docker Desktop for Windows `in use`
  * [Docker Desktop Linux](https://docs.docker.com/desktop/install/linux-install/): Docker Desktop for Linux `past`
- [Containerd](https://containerd.io/): container runtime with an emphasis on simplicity, robustness and portability. Available as a daemon for Linux and Windows, which can manage the complete container lifecycle of its host system: image transfer and storage, container execution and supervision, low-level storage and network attachments, etc - [CNCF graduated project](https://www.cncf.io/projects/containerd/) - [Github repo](https://github.com/containerd/containerd) - Linux and Windows - `Apache v2.0 license`
- [Podman](https://podman.io/): Daemonless container engine for developing, managing, and running OCI Containers on your Linux System. Containers can either be run as root or in rootless mode - Linux only - `Apache License 2.0` `in use`
  * [Github](https://github.com/containers/podman)

