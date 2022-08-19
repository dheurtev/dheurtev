# Virtualization and containers technologies

Tools and technologies I am using, have used or i am considering using.

## Virtualization technologies ##
### Level 1 Virtualization on Windows ###
- [Microsoft Hyper-V](https://docs.microsoft.com/en-us/virtualization/hyper-v-on-windows/quick-start/enable-hyper-v): Native Level 1 hypervisor to create virtual machines on x86-64 systems running Windows
### Level 1 Virtualization on Linux ###
- [Qemu](https://www.qemu.org/): Generic and open-source machine emulator and virtualizer for Linux
- [KVM](https://www.linux-kvm.org/page/Main_Page) : KVM (for Kernel-based Virtual Machine) is an open-source full virtualization solution for Linux on x86 hardware containing virtualization extensions (Intel VT or AMD-V)
- [Libvirt/libvirtd](https://libvirt.org/): Open-source API, daemon and management tool for managing platform virtualization in Linux
### Level 2 Virtualization ###
- Docker:
  * [Docker Desktop Windows](https://docs.docker.com/desktop/install/windows-install/): Docker Desktop for Windows
  * [Docker Desktop Linux](https://docs.docker.com/desktop/install/linux-install/): Docker Desktop for Linux [old]
- GUI:
  * [Oracle VM VirtualBox](https://www.virtualbox.org/): Open Source Level 2 x86 and AMD64/Intel64 virtualization product. Runs as an app on Windows, Linux, OS X, Solaris [old].
  * [Virt-Manager](https://virt-manager.org/): Desktop virtual machine monitor for KVM/QEMU/Libvirt. GPLv2. [old]

## Virtual Environment ##
- [LXC/LXD](https://linuxcontainers.org/): Linux Containers is an operating-system-level virtualization method for running multiple isolated Linux systems on a control host using a single Linux kernel. Chroot on steroids, near bare metal performance, not a VM, fully functionnal OS, standard Linux tools (CLI), Data stored in or outside the container, can be used for composite stacks, file system neutral, but shares same kernel as host, limited portability - GNU LGPL v.2.1. A Canonical Project
  * LXC : Linux container runtime that consists of tools, templates, and library and language bindings
  * LXD : System container and virtual machine manager
  * Used for stateful containers (e.g. stable services, database)
  * LXC does not allow live migration
- [chroot](https://www.howtogeek.com/441534/how-to-use-the-chroot-command-on-linux/): How to use the chroot command on Linux. Uses standard Linux backup tools. [old]

## Applications containers ##
- [Docker](https://www.docker.com/): open platform for developing, shipping, and running applications. Deployment constistence, portable (but not between Linux and Windows Docker), versioning, component reuse, REST API oriented but layered file system, ephemeral instances (persistent data storage is complicated), not native speed performance, limited monitoring - Apache version 2.0
  * For single app containers/microservices in large numbers
  * Good to try new software or software with multiple dependencies 
- [Podman](https://podman.io/): Daemonless container engine for developing, managing, and running OCI Containers on your Linux System. Containers can either be run as root or in rootless mode. Apache License 2.0. [Github](https://github.com/containers/podman)
