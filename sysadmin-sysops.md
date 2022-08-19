# My picks for system admin operations and sysops

Technologies I am using or used in recent years.

## Provisioning platforms ##
### Linux ###
- [Proxmox VE](https://www.proxmox.com/en/proxmox-ve) : Open-source virtualization management platform - Uses KVM, LXD, CEPH, etc - [Documentation](https://pve.proxmox.com/pve-docs/) - Debian based.
- [Metal-As-A-Service (MAAS)](https://maas.io/) : Open-source bare metal server provisionning - [Uses PXE, IPMI, DHCP, DNS, KVM, LXD, etc](https://maas.io/how-it-works) - [Documentation](https://maas.io/docs) - Ubuntu based.
- [Cockpit](https://cockpit-project.org/): See your server in a web browser and perform system tasks with a mouse. Linux. GNU LGPL.
  * [cockpit-machines](https://github.com/cockpit-project/cockpit-machines): Cockpit User Interface for virtual machines. GNU Lesser General Public License v2.1. 
  * [cockpit-podman](https://github.com/cockpit-project/cockpit-podman): Cockpit User Interface for Podman. GNU Lesser General Public License v2.1 
- [oVirt](https://www.ovirt.org/): open-source virtualization management platform. Red-Hat based. Uses GlusterFS and Ansible. 

### Windows ###
- [Microsoft Hyper-V](https://docs.microsoft.com/en-us/virtualization/hyper-v-on-windows/quick-start/enable-hyper-v): Native Level 1 hypervisor to create virtual machines on x86-64 systems running Windows

## Virtualization ##

### Level 1 ###

#### Linux ####
- [Qemu](https://www.qemu.org/): Generic and open-source machine emulator and virtualizer for Linux
- [KVM](https://www.linux-kvm.org/page/Main_Page) : KVM (for Kernel-based Virtual Machine) is an open-source full virtualization solution for Linux on x86 hardware containing virtualization extensions (Intel VT or AMD-V)
- [Libvirt](https://libvirt.org/): Open-source API, daemon and management tool for managing platform virtualization in Linux

#### Windows ####
- [Microsoft Hyper-V](https://docs.microsoft.com/en-us/virtualization/hyper-v-on-windows/quick-start/enable-hyper-v): Native Level 1 hypervisor to create virtual machines on x86-64 systems running Windows

### Level 2 - Cross Platform - Desktop GUI ###
- [Oracle VM VirtualBox](https://www.virtualbox.org/): Open Source Level 2 x86 and AMD64/Intel64 virtualization product. Runs as an app on Windows, Linux, OS X, Solaris.
- [Virt-Manager](https://virt-manager.org/): Desktop virtual machine monitor for KVM/QEMU/Libvirt. GPLv2.

## Container technologies ##
### Virtual Environment ###
- [chroot]():
### Virtual Environment ###
### Applications - Single host ###
- [Docker](https://www.docker.com/): open platform for developing, shipping, and running applications. Apache version 2.0 
- [Podman](https://podman.io/): Daemonless container engine for developing, managing, and running OCI Containers on your Linux System. Containers can either be run as root or in rootless mode. Apache License 2.0. [Github](https://github.com/containers/podman)
#### Useful sites ####
- [Docker Hub](https://hub.docker.com/search?q=): Search docker images
- [Quay](https://quay.io/): Container Image repository server
- [Fedora Registry](registry.fedoraproject.org/)
- [Docker Desktop Windows](https://docs.docker.com/desktop/install/windows-install/): Docker Desktop for Windows
- [Docker Desktop Linux](https://docs.docker.com/desktop/install/linux-install/): Docker Desktop for Linux
