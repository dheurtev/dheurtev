# My picks for system admin and operations (sysops)

Technologies I am using or used in recent years or considering.

## Best practices ##
- Avoid manual changes and GUI as leads to non-reproductible environment.
- Better to build and deploy server images often to avoid drift accumulation
- Immutable configuration to avoid configuration drift
- Infrastructure should be reproductible, disposable, consistent, with no end state
- Provisioning should be automated after the server starts.
- Do not store passwords in code. Use instead IAM or Vault. 
- Send and monitor logs

## Deploy ##

### Bare Metal provisioning platform ###
- [Metal-As-A-Service (MAAS)](https://maas.io/) : Open-source bare metal server provisionning - [Uses PXE, IPMI, DHCP, DNS, KVM, LXD, etc](https://maas.io/how-it-works) - [Documentation](https://maas.io/docs) - Ubuntu based.
### Level 1 Virtualization on Linux ###
- [Qemu](https://www.qemu.org/): Generic and open-source machine emulator and virtualizer for Linux
- [KVM](https://www.linux-kvm.org/page/Main_Page) : KVM (for Kernel-based Virtual Machine) is an open-source full virtualization solution for Linux on x86 hardware containing virtualization extensions (Intel VT or AMD-V)
- [Libvirt/libvirtd](https://libvirt.org/): Open-source API, daemon and management tool for managing platform virtualization in Linux
- [Proxmox VE](https://www.proxmox.com/en/proxmox-ve) : Open-source virtualization management platform - Uses KVM, LXD, CEPH, etc - [Documentation](https://pve.proxmox.com/pve-docs/) - Debian based.
- [Cockpit](https://cockpit-project.org/): See your server in a web browser and perform system tasks with a mouse. Linux. GNU LGPL.
		* [How to manage KVM Machines](https://www.tecmint.com/manage-kvm-virtual-machines-using-cockpit-web-console/)
  * [cockpit-machines](https://github.com/cockpit-project/cockpit-machines): Cockpit User Interface for virtual machines. GNU Lesser General Public License v2.1. 
  * [cockpit-podman](https://github.com/cockpit-project/cockpit-podman): Cockpit User Interface for Podman. GNU Lesser General Public License v2.1 
- [oVirt](https://www.ovirt.org/): open-source virtualization management platform. Red-Hat based. Uses GlusterFS and Ansible. [Considering]
### Level 1 Virtualization on Windows ###
- [Microsoft Hyper-V](https://docs.microsoft.com/en-us/virtualization/hyper-v-on-windows/quick-start/enable-hyper-v): Native Level 1 hypervisor to create virtual machines on x86-64 systems running Windows

### Container technologies ###
#### Virtual Environment ####
- [chroot](https://www.howtogeek.com/441534/how-to-use-the-chroot-command-on-linux/): How to use the chroot command on Linux. Uses standard Linux backup tools.
- [LXC/LXD](https://linuxcontainers.org/): Linux Containers is an operating-system-level virtualization method for running multiple isolated Linux systems on a control host using a single Linux kernel. Chroot on steroids, near bare metal performance, not a VM, fully functionnal OS, standard Linux tools (CLI), Data stored in or outside the container, can be used for composite stacks, file system neutral, but shares same kernel as host, limited portability - GNU LGPL v.2.1. A Canonical Project
  * LXC : Linux container runtime that consists of tools, templates, and library and language bindings
  * LXD : System container and virtual machine manager
  * Used for stateful containers (e.g. stable services, database)
		* LXC does not allow live migration

#### Applications - Single host ####
- [Docker](https://www.docker.com/): open platform for developing, shipping, and running applications. Deployment constistence, portable (but not between Linux and Windows Docker), versioning, component reuse, REST API oriented but layered file system, ephemeral instances (persistent data storage is complicated), not native speed performance, limited monitoring - Apache version 2.0
  * For single app containers/microservices in large numbers
  * Good to try new software or software with multiple dependencies
 
- [Podman](https://podman.io/): Daemonless container engine for developing, managing, and running OCI Containers on your Linux System. Containers can either be run as root or in rootless mode. Apache License 2.0. [Github](https://github.com/containers/podman)
#### Artefact Management - Registries ####
- [Docker Hub](https://hub.docker.com/search?q=): Search docker images
- [Quay](https://quay.io/): Container Image repository server
- [Fedora Registry](registry.fedoraproject.org/)
- [PyPi](https://pypi.org/): repository of software for the Python programming language.
- [npm](https://www.npmjs.com/): npm is a package manager for the JavaScript programming language
### Security ###
- [HashiCorp Vault](https://www.vaultproject.io/): Secure, store and tightly control access to tokens, passwords, certificates, encryption keys for protecting secrets and other sensitive data using a UI, CLI, or HTTP API. Self hosted possible. HashiCorp Project. [Considering]

### Configuration Management ###
#### Traditional server configuration (pets) ####
- Single server : ssh, scp
- Multiple servers simult : parallel-scp, pssh
- Script languages : Bash, Python
#### KVM Management - CLI #####
- virsh
#### LXC container management ####
- lxc
#### Instance initialization ####
- [Cloud-init](https://cloud-init.io/): industry standard multi-distribution method for cross-platform cloud instance initialization - [Documentation](https://cloudinit.readthedocs.io/en/latest/) - Canonical Project
#### Server automation tool ####
- [Ansible](https://www.ansible.com/): agentless automation tool that you install on a single host - Connects to the server via SSH - Apply config changes, configuration of systems, software install, uses yaml documentation. Mutable. Typically to configure VMs or for bare metal operations - RedHat Project
   * [Documentation](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)
   * Ansible Tower or Ansible Semaphore : WebUI for Ansible
- Chef, Puppet, Salt [not used]

#### Infrastruction provision ####
- [Terraform](https://www.terraform.io/): Users define and provide data center infrastructure using a declarative configuration language known as HashiCorp Configuration Language, or optionally JSON to create, change and improve infrastructure. immutable infrastructure based on images. Typically for cloud and kubernetes. Config changes delete or recreate machines - Immutable / Déclarative - HashiCorp Project. [Considering]

## Operate - Infrastructure as a Service ##
### Orchestration - Bare Metal and VMs###
- [LXD Clustering](https://linuxcontainers.org/lxd/docs/master/clustering/): Works with [Metal-As-A-Service (MAAS)](https://maas.io/) [Considering]
- [OpenStack](https://www.openstack.org/): free, open standard cloud computing platform. Apache 2.0 License. [Considering]
- [Clusterlabs](https://clusterlabs.org/quickstart.html): High Availability. Combines Corosync, Pacemaker, DRBD, ScanCore.  [Considering]
#### References ####
- [heartbeat + floating IPs with Corosync and Pacemaker - Ubuntu 14.04](https://www.digitalocean.com/community/tutorials/how-to-create-a-high-availability-setup-with-heartbeat-and-floating-ips-on-ubuntu-14-04)

#### OpenStack Utils ####
- [Microstack](https://microstack.run/docs): OpenStack on a single machine. Supported services are currently Glance, Horizon, Keystone, Neutron (with OVN), and Nova. single-node install and a multi-node deployment. [Considering]
### Orchestration - Containers ###
- [Kubernetes (K8s)](https://kubernetes.io/): open-source container orchestration system for automating software deployment, scaling, and management. Orchestrator and clustering solution for Docker containers + HELM (webui for its management). Apache License 2.0. Google Project [Considering]
- [Docker Swarm](https://docs.docker.com/engine/swarm/): Lightweight orchestration of docker containers. [Considering]
- [Nomad](https://www.nomadproject.io/): A cluster manager and scheduler. Task scheduling platform that can orchestrate different workload types as an extended feature Self-hosted possible. HashiCorp Project. [Considering]
- [Rancher](https://rancher.com/): Open Source Platform for Running a Private Container Service. Rancher is an open source container management platform that includes full distributions of Kubernetes, Apache Mesos and Docker Swarm, and makes it simple to operate container clusters on any cloud or infrastructure platform. HashiCorp Project. [Considering]
#### Kubernetes Utils ####
- [KubeVirt](https://kubevirt.io/): Unified development platform where developers can build, modify, and deploy applications residing in both Application Containers as well as Virtual Machines in a common, shared environment. [Considering]
- [Minikube](https://minikube.sigs.k8s.io/docs/start/): Kubernetes on local computer [Considering] 
- [MicroK8s](https://microk8s.io/): small, fast, single-package Kubernetes for developers, IoT and edge. Local or multi-node [Considering]. Canonical Project. 

### Load Balancer ###
https://geekflare.com/open-source-load-balancer/

### Virtual Networking ###
- [Linux Bridge](https://wiki.linuxfoundation.org/networking/bridge): Linux native bridges, bonds, and vlan interfaces
- [Open vSwitch (OVS)](https://www.openvswitch.org/): open-source implementation of a distributed virtual multilayer switch. Apache License 2.0 [Used]
- [Project Calico](https://www.tigera.io/project-calico/): Container networking and security. Apache 2.0 license 

### Reverse Proxy ###
- [Nginx](https://docs.nginx.com/nginx/admin-guide/web-server/reverse-proxy/):  Open-source web server that can also be used as a reverse proxy, load balancer, mail proxy and HTTP cache. BSD 2.0 license.

### CDN ###
- [CloudFlare CDN](https://www.cloudflare.com/cdn/): content delivery network [used]

### DNS ###
- [CloudFlare DNS](https://www.cloudflare.com/dns/): enterprise-grade authoritative DNS service that offers the fastest response time, unparalleled redundancy, and advanced security with built-in DDoS mitigation and DNSSEC.

## Monitor ##
[Comparison](https://prometheus.io/docs/introduction/comparison/)
[ELK stack alternatives](https://betterstack.com/community/comparisons/elk-stack-alternatives/)
### ELK Stack ###
- [ELK](https://www.elastic.co/fr/elastic-stack/): Elasticsearch, Kibana, Beats et Logstash [considering]
  * [Beats](https://www.elastic.co/fr/beats/): Beats is a free and open platform for single-purpose data shippers. 
  * [Logstash](https://www.elastic.co/fr/logstash/): free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to an Elasticsearch data warehouse.
  * [Elasticsearch](https://www.elastic.co/): search engine based on the Lucene library. It provides a distributed, multitenant-capable full-text search engine with an HTTP web interface and schema-free JSON documents.
  * [Kibana](https://www.elastic.co/fr/kibana/): source-available data visualization dashboard software for Elasticsearch. Proprietary.
### Monitoring Tools ###
#### Basic Monitoring ####
- [SNMP](https://en.wikipedia.org/wiki/Simple_Network_Management_Protocol): Simple Network Management Protocol (SNMP) is an IP-based application layer protocol that exchanges information between a network management solution and any SNMP-enabled device. [using]
- [Nagios Core - Nagios](https://www.nagios.org/): free and open-source computer-software application that monitors systems, networks and infrastructure. GPLv2 [considering]
#### Event monitoring, Agent and metrics ####
- [Jabbix](https://www.zabbix.com/): open-source software tool to monitor IT infrastructure such as networks, servers, virtual machines, and cloud services. Zabbix collects and displays basic metrics. Agent. GPLv2. [used]
- [Collectd](https://collectd.org/): very popular collection agent. Unix daemon that collects, transfers and stores performance data of computers and network equipment. Used by Graphite and in Prometheus. MIT License & GNU General Public License, version 2. [considering]
- [StatsD](https://github.com/statsd/statsd): A network daemon that runs on the Node.js platform and listens for statistics, like counters and timers, sent over UDP or TCP and sends aggregates to one or more pluggable backend services (e.g., Graphite). [Also used in Datadog](https://www.datadoghq.com/blog/statsd/). [considering]
- [Prometheus](https://prometheus.io/): free software application used for event monitoring and alerting. It records real-time metrics in a time series database built using a HTTP pull model, with flexible queries and real-time alerting. Apache License 2.0 [considering]
### Event Logging - Dashboard ###
- [Graphite](https://graphiteapp.org/): Monitoring tool that runs equally well on cheap hardware or Cloud infrastructure. Teams use Graphite to track the performance of their websites, applications, business services, and networked servers. Store numeric time-series data. Render graphs of this data on demand. Not a collecting agent [considering]
- [InfluxDB](https://www.influxdata.com/): open-source time series database. MIT Licensed
- [Grafana](https://grafana.com/): multi-platform open source analytics and interactive visualization web application. GNU Affero General Public License, version 3.0 [Considering]
#### Monitoring as a service ####
- [Splunk](https://www.splunk.com/): log management and monitoring solution [considering]
- [Datadog](https://www.datadoghq.com/): monitoring and analytics tool for information technology (IT) and DevOps teams that can be used to determine performance metrics as well as event monitoring for infrastructure and cloud services. [considering]












