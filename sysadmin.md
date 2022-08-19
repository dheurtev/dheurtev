# My picks for SysAdmin Technologies - MAAS/IAAS (Pets management)

Tools and technologies i am using, have used or consider using

## Best practices ##
- Avoid manual changes and GUI as leads to non-reproductible environment.
- Immutable configuration to avoid configuration drift
- Infrastructure should be reproductible, disposable, consistent, with no end state
- Provisioning should be automated after the server starts.
- Do not store passwords in code. Use instead IAM or Vault. 
- Send and monitor logs

## Provision ##
### Bare Metal - Metal as a Service ###
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
### Server management ###
- [Cockpit](https://cockpit-project.org/): See your server in a web browser and perform system tasks with a mouse. Linux. GNU LGPL.
  * [How to manage KVM Machines](https://www.tecmint.com/manage-kvm-virtual-machines-using-cockpit-web-console/)
  * [cockpit-machines](https://github.com/cockpit-project/cockpit-machines): Cockpit User Interface for virtual machines. GNU Lesser General Public License v2.1. 
  * [cockpit-podman](https://github.com/cockpit-project/cockpit-podman): Cockpit User Interface for Podman. GNU Lesser General Public License v2.1 
### Clustering ###
- [Proxmox VE](https://www.proxmox.com/en/proxmox-ve) : Open-source virtualization management platform - Uses KVM, LXD, CEPH, etc - [Documentation](https://pve.proxmox.com/pve-docs/) - Debian based.
- [oVirt](https://www.ovirt.org/): open-source virtualization management platform. Red-Hat based. Uses GlusterFS and Ansible. [Considering]
- [LXD Clustering](https://linuxcontainers.org/lxd/docs/master/clustering/): Works with [Metal-As-A-Service (MAAS)](https://maas.io/) [Considering]
- [Clusterlabs](https://clusterlabs.org/quickstart.html): High Availability. Combines Corosync, Pacemaker, DRBD, ScanCore.  [Considering]
- [heartbeat + floating IPs with Corosync and Pacemaker - Ubuntu 14.04](https://www.digitalocean.com/community/tutorials/how-to-create-a-high-availability-setup-with-heartbeat-and-floating-ips-on-ubuntu-14-04) [Used]
### Infrastructure As a Service (IAAS) ###
- [OpenStack](https://www.openstack.org/): free, open standard cloud computing platform. Apache 2.0 License. [Considering]
- [Microstack](https://microstack.run/docs): OpenStack on a single machine. Supported services are currently Glance, Horizon, Keystone, Neutron (with OVN), and Nova. single-node install and a multi-node deployment. [Considering]

## Deploy ##
### Provision Management ###
#### CLI ####
- virsh: low level
- lxc : low level
- [Multipass](https://multipass.run/): a CLI to launch and manage VMs on Windows, Mac and Linux that simulates a cloud environment with support for cloud-init. Canonical project
- [Vagrant](https://www.vagrantup.com/): open-source software product for building and maintaining portable virtual software development environments; e.g., for VirtualBox, KVM, Hyper-V, Docker containers, VMware, and AWS. It tries to simplify the software configuration management of virtualization. Typically creates Virtualbox VMs but plugins support other platforms. HashiCorp Project.
#### GUI ####
- [Oracle VM VirtualBox](https://www.virtualbox.org/): Open Source Level 2 x86 and AMD64/Intel64 virtualization product. Runs as an app on Windows, Linux, OS X, Solaris [past].
- [Virt-Manager](https://virt-manager.org/): Desktop virtual machine monitor for KVM/QEMU/Libvirt. GPLv2. [past]

### Configuration Management ###
#### Traditional server configuration ####
- Single server : ssh, scp
- Multiple servers simult : parallel-scp, pssh
- Script languages : Bash, Python
#### Instance initialization ####
- [Cloud-init](https://cloud-init.io/): industry standard multi-distribution method for cross-platform cloud instance initialization. Provision server instance by bootstraping a bare minimum OS config (ssh, ssh-key, hostname, fqdn, manage-etc, network, ip, gw), account setup - Canonical Project
  * [Documentation](https://cloudinit.readthedocs.io/en/latest/)
#### Server automation tool ####
- [Ansible](https://www.ansible.com/): agentless automation tool that you install on a single host - Connects to the server via SSH - Apply config changes, configuration of systems, software install, uses yaml documentation. Mutable. Typically to configure VMs or for bare metal operations - RedHat Project
   * [Documentation](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)
   * Ansible Tower or Ansible Semaphore : WebUI for Ansible

## Monitor ##
https://github.com/dheurtev/dheurtev/blob/main/monitoring.md

## Other tools ##

### Load Balancer and reverse proxy ###
https://geekflare.com/open-source-load-balancer/

- [Nginx](https://docs.nginx.com/nginx/admin-guide/web-server/reverse-proxy/):  Open-source web server that can also be used as a reverse proxy, load balancer, mail proxy and HTTP cache. BSD 2.0 license.

### Virtual Networking ###
- [Linux Bridge](https://wiki.linuxfoundation.org/networking/bridge): Linux native bridges, bonds, and vlan interfaces
- [Open vSwitch (OVS)](https://www.openvswitch.org/): open-source implementation of a distributed virtual multilayer switch. Apache License 2.0 [Used]

