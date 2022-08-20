# My picks for system operations (sysops) -  Platform As A Service (PAAS) and cattle management

Tools and packages I am using are marked `in use`.
Tools and packages I used are marked as `past`.

- [Best practices](#best-practices)
- [Deploy](#deploy)
- [Operate - infrastructure as a service](#operate---infrastructure-as-a-service)
- [Monitor](#monitor)
- [Other tools](#other-tools)

## Best practices ##
**[`^        back to top        ^`](#)**
- Infrastructure should be reproductible, disposable, consistent, with no end state
- Better to build and deploy server images often to avoid drift accumulation
- Immutable configuration to avoid configuration drift
- Do not store passwords in code. Use instead IAM or Vault. 
- Send and monitor logs

[List of cloud native tools - awesome-cloudnative](https://github.com/wh211212/awesome-cloudnative)

## Deploy ##
**[`^        back to top        ^`](#)**
### Configuration management ###
#### Infrastruction provision ####
- [Terraform](https://www.terraform.io/): Users define and provide data center infrastructure using a declarative configuration language known as HashiCorp Configuration Language, or optionally JSON to create, change and improve infrastructure. immutable infrastructure based on images. Typically for cloud and kubernetes. Config changes delete or recreate machines - Immutable / Déclarative - HashiCorp Project. `Mozilla Public License v2`

## Operate - Infrastructure as a Service ##
**[`^        back to top        ^`](#)**
### Scheduling and Orchestration ###
- [Kubernetes (K8s)](https://kubernetes.io/): open-source container orchestration system for automating software deployment, scaling, and management. Orchestrator and clustering solution for Docker containers + HELM (webui for its management). Google Project. [CNCF graduated project](https://www.cncf.io/projects/kubernetes/). `Apache 2.0 License`
- [Docker Swarm](https://docs.docker.com/engine/swarm/): Lightweight orchestration of docker containers. `Apache 2.0 license`
- [Nomad](https://www.nomadproject.io/): A cluster manager and scheduler. Task scheduling platform that can orchestrate different workload types as an extended feature Self-hosted possible. HashiCorp Project. `Mozilla Public License 2.0`
- [Rancher](https://rancher.com/): Open Source Platform for Running a Private Container Service. Rancher is an open source container management platform that includes full distributions of Kubernetes, Apache Mesos and Docker Swarm, and makes it simple to operate container clusters on any cloud or infrastructure platform. HashiCorp Project. `Apache License 2.0`
#### Kubernetes Utils ####
- [KubeVirt](https://kubevirt.io/): Unified development platform where developers can build, modify, and deploy applications residing in both Application Containers as well as Virtual Machines in a common, shared environment.  [CNCF project](https://www.cncf.io/projects/kubevirt/). `Apache License 2.0`
- [Minikube](https://minikube.sigs.k8s.io/docs/start/): Kubernetes on local computer. Kuberneted project. `Apache License 2.0`
- [MicroK8s](https://microk8s.io/): small, fast, single-package Kubernetes for developers, IoT and edge. Local or multi-node. Canonical Project. `Apache 2.0 license` 
#### Storage ####
- [Minio](https://min.io/): highly-available, S3 compatible object storage solution. `Affero General Public License Version 3 (AGPLv3)`
- [Rook](https://rook.io/): Open-Source Cloud-Native Storage for Kubernetes. for File, Block and Object Storage. [CCNF Graduated project](https://www.cncf.io/projects/rook/) [Github repo](https://github.com/rook/rook) `Apache v2.0 License`

### Network ###

#### DNS ####
- [CoreDNS](https://coredns.io/): DNS server/forwarder, written in Go, that chains plugins. Integrates with Kubernetes and etcd. Plugs with somme DNS as a service providers [Github repo](https://github.com/coredns/coredns). [CNCF graduated project](https://www.cncf.io/projects/coredns/). `Apache 2.0 License` 

#### Virtual Networking ####
**[`^        back to top        ^`](#)**
- [Project Calico](https://www.tigera.io/project-calico/): Container networking and security. `Apache 2.0 license` 


#### Proxy ####
- [Envoy](https://www.envoyproxy.io/): Open source edge and service proxy, designed for cloud-native applications. high performance C++ distributed proxy. `Apache 2.0 license`. [CCNF graduated project](https://www.cncf.io/projects/envoy/) - [Github repo](https://github.com/envoyproxy/envoy). `Apache 2.0 license`   





## Monitor ##
**[`^        back to top        ^`](#)**
[My monitoring page](https://github.com/dheurtev/dheurtev/blob/main/monitoring.md)

## Other tools ##
**[`^        back to top        ^`](#)**
[Cloud Native Computing Foundation (CNCF) Projects](https://www.cncf.io/projects/)


