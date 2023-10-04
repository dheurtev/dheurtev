# My picks for SysAdmin and Ops - Pets management and MAAS/IAAS 

Tools and packages I am using are marked `in use`.
Tools and packages I used are marked as `past`.

- [Best practices](#best-practices)
- [Deploy](#deploy)
- [Operate](#operate)
- [Monitor](#monitor)
- [Other tools](#other-tools)

## Best practices ##
**[`^        back to top        ^`](#)**
- Provisioning should be automated after the server starts (use cloud-init).
- Infrastructure should be reproductible, disposable, consistent, with no end state
- Avoid manual changes with a GUI as it leads to a non-reproductible environment.
- Declarative configuration to avoid configuration drift => use containers, try to become immutable
- Do not store passwords in code. Use instead IAM or Vault. 
- Send and monitor logs

## Deploy ##
**[`^        back to top        ^`](#)**
### Provision ###
#### Bare Metal - Metal as a Service ####
- [Metal-As-A-Service (MAAS)](https://maas.io/) : Open-source bare metal server provisionning - [Uses PXE, IPMI, DHCP, DNS, KVM, LXD, etc](https://maas.io/how-it-works) - [Documentation](https://maas.io/docs) - Ubuntu based. `GNU AGPL, v3` `in use`
- [Foreman](https://theforeman.org/introduction.html): open source complete life cycle systems management tool for provisioning, configuring and monitoring of physical and virtual servers - Host provisioning, configuration, monitoring WebUI + CLI + API - `GPL-3.0`
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
#### Server management ####
- [Cockpit](https://cockpit-project.org/): See your server in a web browser and perform system tasks with a mouse. Linux. `GNU LGPL` `in use`
  * [How to manage KVM Machines](https://www.tecmint.com/manage-kvm-virtual-machines-using-cockpit-web-console/)
  * [cockpit-machines](https://github.com/cockpit-project/cockpit-machines): Cockpit User Interface for virtual machines. `GNU Lesser General Public License v2.1` `in use`
  * [cockpit-podman](https://github.com/cockpit-project/cockpit-podman): Cockpit User Interface for Podman. `GNU Lesser General Public License v2.1` `in use`
- [Portainer CE](https://hub.docker.com/r/portainer/portainer-ce): Portainer CE - a lightweight service delivery platform for containerized applications. *docker pull portainer/portainer-ce* `zlib license (permissive free software license)` `in use`
#### Clustering ####
- [Proxmox VE](https://www.proxmox.com/en/proxmox-ve) : Open-source virtualization management platform - Uses KVM, LXD, CEPH, etc - [Documentation](https://pve.proxmox.com/pve-docs/) - Debian based - `GNU AGPL, v3` `past`
- [oVirt](https://www.ovirt.org/): open-source virtualization management platform. Red-Hat based. Uses GlusterFS and Ansible. `past`
- [LXD Clustering](https://linuxcontainers.org/lxd/docs/master/clustering/): Works with [Metal-As-A-Service (MAAS)](https://maas.io/)
- [Clusterlabs](https://clusterlabs.org/quickstart.html): High Availability. Combines Corosync, Pacemaker, DRBD, ScanCore.
- [heartbeat + floating IPs with Corosync and Pacemaker - Ubuntu 14.04](https://www.digitalocean.com/community/tutorials/how-to-create-a-high-availability-setup-with-heartbeat-and-floating-ips-on-ubuntu-14-04) `past`
#### Infrastructure As a Service (IAAS) ####
- [OpenStack](https://www.openstack.org/): free, open standard cloud computing platform. `Apache 2.0 License`
- [Microstack](https://microstack.run/docs): OpenStack on a single machine. Supported services are currently Glance, Horizon, Keystone, Neutron (with OVN), and Nova. single-node install and a multi-node deployment. `MIT License`

#### Provision Management (CLI) ####
- virsh (libvirt): low level  `in use`
- lxc (LXC/LXD) : low level  `in use`
- [Multipass](https://multipass.run/): a CLI to launch and manage VMs on Windows, Mac and Linux that simulates a cloud environment with support for cloud-init. Canonical project. `GPLv3.0` `past`
- [Vagrant](https://www.vagrantup.com/): open-source software product for building and maintaining portable virtual software development environments; e.g., for VirtualBox, KVM, Hyper-V, Docker containers, VMware, and AWS. It tries to simplify the software configuration management of virtualization. Typically creates Virtualbox VMs but plugins support other platforms. HashiCorp Project. Was `MIT License`. Now [`Business Source License 1.1`](https://github.com/hashicorp/vagrant/blob/main/LICENSE) =>  `⚠ Proprietary`. `past`

#### Configuration Management ####
[Comparison : Chef, Puppet, Ansible, Saltstack](https://www.edureka.co/blog/chef-vs-puppet-vs-ansible-vs-saltstack/)
[Comparison : Chef, Puppet, Ansible, Saltstack](https://www.liquidweb.com/kb/puppet-salt-chef-ansible-a-comparison/)
[Comparison : Chef, Puppet, Ansible, Saltstack - IBM](https://www.ibm.com/cloud/blog/chef-ansible-puppet-terraform)

##### Traditional server configuration #####
- Single server : ssh, scp
- Multiple servers simult : parallel-scp, pssh
- Script languages : Bash, Python
##### Instance initialization #####
- [Cloud-init](https://cloud-init.io/): industry standard multi-distribution method for cross-platform cloud instance initialization. Provision server instance by bootstraping a bare minimum OS config (ssh, ssh-key, hostname, fqdn, manage-etc, network, ip, gw), account setup - Canonical Project. Dual licensing `GPLv3` or `Apache 2.0` `in use`
  * [Documentation](https://cloudinit.readthedocs.io/en/latest/)
##### Procedural style #####
- [Ansible](https://www.ansible.com/): agentless automation tool that you install on a single host - Connects to the server via SSH - Apply config changes, configuration of systems, software install, uses yaml documentation (admin oriented). Procedural style. Mutable. Pushed configuration. - Ansible uses the SSH (or RDP for Windows) protocols to open a connection to the client servers to execute its sequential commands Typically to configure VMs or for bare metal operations - RedHat Project. `GPL-3.0 license` `in use`
   * [Documentation](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)
   * [RedHat Ansible Automation platform (replaced Ansible Tower)](https://www.redhat.com/en/technologies/management/ansible/automation-controller)
   * [Ansible Semaphore](https://www.ansible-semaphore.com/) : WebUI for Ansible. `MIT License`. 
- [Chef](https://www.chef.io/), Chef DSL (dev oriented). Master-agent model. Client pulls config. Chef's configuration options consist of Cookbooks and Recipes. The recipes are the definition files that can be combined with attributes, files, libraries, and other recipes to build Cookbooks. These cookbooks can then be used for client deployment. Procedural style. Mutable. [License](https://docs.chef.io/chef_license/). Some `Apache 2.0 License`, some `⚠ Proprietary`.
##### Declarative style #####
- [Saltstack - Salt](https://saltproject.io/): Python-based, open-source software for event-driven IT automation, remote task execution, and configuration management. synchronous file server to speed deployment. Parallel execution of multiple commands at once encrypted via AES (Advanced Encryption Standard) and pushed to the client nodes via the SSH protocol. Yaml (admin oriented). Master-agent model. Push configuration. Declarative style. Mutable. Web Gui. Suitable for cloud use.  `Apache License 2.0`.
  * [Alcali](https://alcali.dev/): ``MIT License`  `⚠ Last commit 2021`
  * [SaltGUI - A web interface for managing SaltStack based infrastructure](https://github.com/erwindon/SaltGUI): covers only the basic functions of Salt (viewing minion status, executing jobs, applying states, etc) 
  * [Uyuni Project](https://www.uyuni-project.org/): Uyuni is an open source systems management solution, forked from Spacewalk. upstream community project from which SUSE Manager is derived. Enterprise oriented. `GPLv2`
- [Puppet](https://puppet.com/): software configuration management tool which includes its own declarative language to describe system configuration. It is a model-driven solution that requires limited programming knowledge to use. Master-agent model. Ruby DSL (sysadmin oriented). Client pulls config. Manifest files are fundamentally a set of configurations or tasks that determine how your network and operating system resources (such as services, packages, and files) are configured. Declarative style. Mutable. Suitable for cloud use. Open Source Puppet: `Apache` for >2.7.0, GPL for prior versions. Puppet Enterprise: `⚠ Proprietary`.

`Use Terraform for declarative immutable in container orchestration` (but beware of license change to non open-source)

![image](https://user-images.githubusercontent.com/4304311/185752513-7fde06dc-b6ad-4849-8bcd-14f897c61693.png )
Source: [IBM](https://www.ibm.com/cloud/blog/chef-ansible-puppet-terraform)

## Operate ##
**[`^        back to top        ^`](#)**

### Store ###
- Scaling with additional disks in a node (scale up) : ZFS with mirror or RAID-Z
- Scaling between nodes (scale out): CEPH
- User remote access to files : SMB (SAMBA)
- Shares for backups (on NAS) : NFS

### Schedule ###
Traditional approach :
- BASH + Cron 
- Python or Node scrips + Cron
- JAVA + Cron [past]
- [Anacron](https://linux.die.net/man/8/anacron): Cron that can turn on the server `GPLv2` `past`

### Network ###

#### Routers ####
- Non Linux Networking / Router distribution : [OPNsense](https://opnsense.org/) : PfSense fork. Can be virtualized. `BSD license`

##### Virtual Networking #####
- [Linux Bridge](https://wiki.linuxfoundation.org/networking/bridge): Linux native bridges, bonds, and vlan interfaces. `in use`
- [Open vSwitch (OVS)](https://www.openvswitch.org/): open-source implementation of a distributed virtual multilayer switch. `Apache License 2.0` `past`

#### DNS Servers ####
##### Local network #####
- [dnsmasq](https://thekelleys.org.uk/dnsmasq/doc.html): lightweight, easy to configure DNS forwarder, designed to provide DNS (and optionally DHCP and TFTP) services to a small-scale network. `GPLv2` or `GPLv3` `in use`
##### Authoritative or local network #####
- [Bind9](https://www.isc.org/bind/): Suite of software for interacting with the Domain Name System. Its most prominent component, named, performs both of the main DNS server roles, acting as an authoritative name server for DNS zones and as a recursive resolver in the network. `Mozilla Public License` `in use`
##### DNS as a service #####
- [Microsoft Azure DNS](https://azure.microsoft.com/en-us/services/dns/)
- [GCP Cloud DNS](https://cloud.google.com/dns)
- [AWS Route53](https://aws.amazon.com/route53/?nc1=h_ls)
- [Cloudflare DNS](https://www.cloudflare.com/dns/) `in use`

##### Load Balancer and reverse proxy #####
https://geekflare.com/open-source-load-balancer/
- [Nginx](https://docs.nginx.com/nginx/admin-guide/web-server/reverse-proxy/):  Open-source web server that can also be used as a reverse proxy, load balancer, mail proxy and HTTP cache. `BSD 2.0 license` `in use`

##### VPN #####
- [Wireguard](https://www.wireguard.com/): communication protocol and free and open-source software that implements encrypted virtual private networks. Cross-platform. `GPLv2` `in use` 
- [Tinc](https://www.tinc-vpn.org/): Virtual Private Network (VPN) daemon that uses tunnelling and encryption to create a secure private network between hosts on the Internet. Automatic full mesh routing. Cross-platform. `GPLv2`

## Monitor ##
**[`^        back to top        ^`](#)**

[My monitoring (logging and tracing)](monitoring.md)

## Other tools ##
**[`^        back to top        ^`](#)**
