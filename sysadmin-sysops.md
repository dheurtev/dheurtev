# My picks for system admin operations and sysops

Technologies I am using or used in recent years or considering.

## Virtualization Technology ##
### Linux ###
- [Qemu](https://www.qemu.org/): Generic and open-source machine emulator and virtualizer for Linux
- [KVM](https://www.linux-kvm.org/page/Main_Page) : KVM (for Kernel-based Virtual Machine) is an open-source full virtualization solution for Linux on x86 hardware containing virtualization extensions (Intel VT or AMD-V)
- [Libvirt](https://libvirt.org/): Open-source API, daemon and management tool for managing platform virtualization in Linux

### Windows ###
- [Microsoft Hyper-V](https://docs.microsoft.com/en-us/virtualization/hyper-v-on-windows/quick-start/enable-hyper-v): Native Level 1 hypervisor to create virtual machines on x86-64 systems running Windows

## Bare Metal provisioning platform ##
- [Metal-As-A-Service (MAAS)](https://maas.io/) : Open-source bare metal server provisionning - [Uses PXE, IPMI, DHCP, DNS, KVM, LXD, etc](https://maas.io/how-it-works) - [Documentation](https://maas.io/docs) - Ubuntu based.

## Level 1 Virtualization and Container hypervisors - provisioning platforms - clustering ##
- [Proxmox VE](https://www.proxmox.com/en/proxmox-ve) : Open-source virtualization management platform - Uses KVM, LXD, CEPH, etc - [Documentation](https://pve.proxmox.com/pve-docs/) - Debian based.
- [Cockpit](https://cockpit-project.org/): See your server in a web browser and perform system tasks with a mouse. Linux. GNU LGPL.
  * [cockpit-machines](https://github.com/cockpit-project/cockpit-machines): Cockpit User Interface for virtual machines. GNU Lesser General Public License v2.1. 
  * [cockpit-podman](https://github.com/cockpit-project/cockpit-podman): Cockpit User Interface for Podman. GNU Lesser General Public License v2.1 
- [oVirt](https://www.ovirt.org/): open-source virtualization management platform. Red-Hat based. Uses GlusterFS and Ansible. [Considering]
- [Microsoft Hyper-V](https://docs.microsoft.com/en-us/virtualization/hyper-v-on-windows/quick-start/enable-hyper-v): Native Level 1 hypervisor to create virtual machines on x86-64 systems running Windows
- [Proxmox VE](https://www.proxmox.com/en/proxmox-ve): uses LXD, [Corosync](https://corosync.github.io/corosync/) and [Pacemaker](https://clusterlabs.org/pacemaker/).
- [Kubernetes](https://kubernetes.io/): open-source container orchestration system for automating software deployment, scaling, and management. Apache License 2.0.
- [LXD Clustering](https://linuxcontainers.org/lxd/docs/master/clustering/): Works with [Metal-As-A-Service (MAAS)](https://maas.io/)
- [Clusterlabs](https://clusterlabs.org/quickstart.html): High Availability. Combines Corosync, Pacemaker, DRBD, ScanCore. [Considering]

## Level 2 - Virtualization and Container Provisioning platforms ##
### Desktop GUI ###
- [Oracle VM VirtualBox](https://www.virtualbox.org/): Open Source Level 2 x86 and AMD64/Intel64 virtualization product. Runs as an app on Windows, Linux, OS X, Solaris.
- [Virt-Manager](https://virt-manager.org/): Desktop virtual machine monitor for KVM/QEMU/Libvirt. GPLv2.
- [Docker Desktop Windows](https://docs.docker.com/desktop/install/windows-install/): Docker Desktop for Windows
- [Docker Desktop Linux](https://docs.docker.com/desktop/install/linux-install/): Docker Desktop for Linux
### CLI ###
- [Multipass](https://multipass.run/): a CLI to launch and manage VMs on Windows, Mac and Linux that simulates a cloud environment with support for cloud-init. Canonical project
- [Vagrant](https://www.vagrantup.com/): open-source software product for building and maintaining portable virtual software development environments; e.g., for VirtualBox, KVM, Hyper-V, Docker containers, VMware, and AWS. It tries to simplify the software configuration management of virtualization. HashiCorp Project.

## Container technologies ##
### Virtual Environment ###
- [chroot](https://www.howtogeek.com/441534/how-to-use-the-chroot-command-on-linux/): How to use the chroot command on Linux
- [LXC/LXD](https://linuxcontainers.org/): Linux Containers is an operating-system-level virtualization method for running multiple isolated Linux systems on a control host using a single Linux kernel. GNU LGPL v.2.1. A Canonical Project
  * LXC : Linux container runtime that consists of tools, templates, and library and language bindings
  * LXD : System container and virtual machine manager
### Applications - Single host ###
- [Docker](https://www.docker.com/): open platform for developing, shipping, and running applications. Apache version 2.0 
- [Podman](https://podman.io/): Daemonless container engine for developing, managing, and running OCI Containers on your Linux System. Containers can either be run as root or in rootless mode. Apache License 2.0. [Github](https://github.com/containers/podman)
#### Useful sites ####
- [Docker Hub](https://hub.docker.com/search?q=): Search docker images
- [Quay](https://quay.io/): Container Image repository server
- [Fedora Registry](registry.fedoraproject.org/)

## Infrastructure as a service (IAAS) tools ##
- [Cloud-init](https://cloud-init.io/): industry standard multi-distribution method for cross-platform cloud instance initialization - [Documentation](https://cloudinit.readthedocs.io/en/latest/) - Canonical Project
- [Ansible](https://www.ansible.com/): agentless automation tool that you install on a single host - [Documentation](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html) - RedHat Project
- [Terraform](https://www.terraform.io/): Users define and provide data center infrastructure using a declarative configuration language known as HashiCorp Configuration Language, or optionally JSON to create, change and improve infrastructure. HashiCorp Project. [Considering]

## Utils ##
- [KubeVirt](https://kubevirt.io/): Unified development platform where developers can build, modify, and deploy applications residing in both Application Containers as well as Virtual Machines in a common, shared environment. [Considering]






