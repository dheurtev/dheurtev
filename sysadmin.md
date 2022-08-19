# SysAdmin Technologies (Pets management)

Technologies I am using or used in recent years or considering.

#### To create Metal As A Service - Bare Metal ####
- [Metal-As-A-Service (MAAS)](https://maas.io/) : Open-source bare metal server provisionning - [Uses PXE, IPMI, DHCP, DNS, KVM, LXD, etc](https://maas.io/how-it-works) - [Documentation](https://maas.io/docs) - Ubuntu based.
- [Foreman](https://theforeman.org/introduction.html): open source complete life cycle systems management tool for provisioning, configuring and monitoring of physical and virtual servers - Host provisioning, configuration, monitoring WebUI + CLI + API - GPL-3.0 - [Considering]
  * Discover, provision and upgrade your entire bare-metal infrastructure
  * Create and manage instances in virtualization environment and across private and public clouds
  * Install operating systems via PXE, local media or from templates or images
  * Control and gather reports from your configuration management software
  * Group your hosts and manage them in bulk, regardless of location
  * Review historical changes for auditing or troubleshooting
  * Web user interface, JSON REST API and CLI for Linux
  * Extend as needed via a robust plugin architecture
  * Puppet, Ansible, Chef and Salt are supported
  * IPAM: Manage DHCP reservations on various providers like ISC DHCP, MS DHCP or Infoblox, free IP addresses can be allocated on the fly or via Foreman database.
  * DNS and identity management: DNS or realm entries can be automatically created for each host in Foreman inventory.  
  * OS supported: Red Hat Enterprise Linux, CentOS, Fedora, Ubuntu, Debian, Solaris 8, 10, OpenSUSE, SLES, Oracle Linux, CoreOS, FreeBSD, Junos
  * Cloud provider supported : Amazon EC2, Google Compute Engine, Libvirt, OpenStack, oVirt, RHEV, Rackspace, VMware
#### Provision platform - Linux ####
- [Proxmox VE](https://www.proxmox.com/en/proxmox-ve) : Open-source virtualization management platform - Uses KVM, LXD, CEPH, etc - [Documentation](https://pve.proxmox.com/pve-docs/) - Debian based.
- [Cockpit](https://cockpit-project.org/): See your server in a web browser and perform system tasks with a mouse. Linux. GNU LGPL.
  * [How to manage KVM Machines](https://www.tecmint.com/manage-kvm-virtual-machines-using-cockpit-web-console/)
  * [cockpit-machines](https://github.com/cockpit-project/cockpit-machines): Cockpit User Interface for virtual machines. GNU Lesser General Public License v2.1. 
  * [cockpit-podman](https://github.com/cockpit-project/cockpit-podman): Cockpit User Interface for Podman. GNU Lesser General Public License v2.1 
- [oVirt](https://www.ovirt.org/): open-source virtualization management platform. Red-Hat based. Uses GlusterFS and Ansible. [Considering]

