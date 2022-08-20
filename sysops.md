# My picks for system operations (sysops) -  Platform As A Service (PAAS) and cattle management

Tools and packages I am using are marked `in use`.
Tools and packages I used are marked as `past`.

- [Best practices](#best-practices)
- [Deploy](#deploy)
- [Operate - infrastructure as a service](#operate---infrastructure-as-a-service)
- [Monitor](#monitor)
- [Other tools](#other-tools)

## Best practices ##
- Infrastructure should be reproductible, disposable, consistent, with no end state
- Better to build and deploy server images often to avoid drift accumulation
- Immutable configuration to avoid configuration drift
- Do not store passwords in code. Use instead IAM or Vault. 
- Send and monitor logs

## Deploy ##
### Configuration management ###
#### Infrastruction provision ####
- [Terraform](https://www.terraform.io/): Users define and provide data center infrastructure using a declarative configuration language known as HashiCorp Configuration Language, or optionally JSON to create, change and improve infrastructure. immutable infrastructure based on images. Typically for cloud and kubernetes. Config changes delete or recreate machines - Immutable / Déclarative - HashiCorp Project. `Mozilla Public License v2`
#### Configuration / Application automation tool ####
- Chef, 
- Puppet, 
- Salt

## Operate - Infrastructure as a Service ##
### Scheduling and Orchestration ###
- [Kubernetes (K8s)](https://kubernetes.io/): open-source container orchestration system for automating software deployment, scaling, and management. Orchestrator and clustering solution for Docker containers + HELM (webui for its management). Google Project. [CNCF graduated project](https://www.cncf.io/projects/kubernetes/). `Apache 2.0 License`
- [Docker Swarm](https://docs.docker.com/engine/swarm/): Lightweight orchestration of docker containers. `Apache 2.0 license`
- [Nomad](https://www.nomadproject.io/): A cluster manager and scheduler. Task scheduling platform that can orchestrate different workload types as an extended feature Self-hosted possible. HashiCorp Project. `Mozilla Public License 2.0`
- [Rancher](https://rancher.com/): Open Source Platform for Running a Private Container Service. Rancher is an open source container management platform that includes full distributions of Kubernetes, Apache Mesos and Docker Swarm, and makes it simple to operate container clusters on any cloud or infrastructure platform. HashiCorp Project. `Apache License 2.0`
#### Kubernetes Utils ####
- [KubeVirt](https://kubevirt.io/): Unified development platform where developers can build, modify, and deploy applications residing in both Application Containers as well as Virtual Machines in a common, shared environment.  [CNCF project](https://www.cncf.io/projects/kubevirt/). `Apache License 2.0`
- [Minikube](https://minikube.sigs.k8s.io/docs/start/): Kubernetes on local computer. Kuberneted project. `Apache License 2.0`
- [MicroK8s](https://microk8s.io/): small, fast, single-package Kubernetes for developers, IoT and edge. Local or multi-node. Canonical Project. `Apache 2.0 license` 

## Monitor ##
https://github.com/dheurtev/dheurtev/blob/main/monitoring.md

## Other tools ##
[Cloud Native Computing Foundation (CNCF) Projects](https://www.cncf.io/projects/)

### Virtual Networking ###
- [Project Calico](https://www.tigera.io/project-calico/): Container networking and security. `Apache 2.0 license` 
