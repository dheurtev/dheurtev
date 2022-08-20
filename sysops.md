# My picks for system operations (sysops) -  Platform As A Service (PAAS) and cattle management

Tools and technologies i am using, have used or consider using

-[Best practices](https://github.com/dheurtev/dheurtev/blob/main/sysops.md#best-practices)
-[Deploy](https://github.com/dheurtev/dheurtev/blob/main/sysops.md#deploy)
-[Operate - infrastructure as a service](https://github.com/dheurtev/dheurtev/blob/main/sysops.md#operate---infrastructure-as-a-service)
-[Monitor](https://github.com/dheurtev/dheurtev/blob/main/sysops.md#monitor)
-[Other tools](https://github.com/dheurtev/dheurtev/blob/main/sysops.md#other-tools)

## Best practices ##
- Infrastructure should be reproductible, disposable, consistent, with no end state
- Better to build and deploy server images often to avoid drift accumulation
- Immutable configuration to avoid configuration drift
- Do not store passwords in code. Use instead IAM or Vault. 
- Send and monitor logs

## Deploy ##
### Configuration management ###
#### Infrastruction provision ####
- [Terraform](https://www.terraform.io/): Users define and provide data center infrastructure using a declarative configuration language known as HashiCorp Configuration Language, or optionally JSON to create, change and improve infrastructure. immutable infrastructure based on images. Typically for cloud and kubernetes. Config changes delete or recreate machines - Immutable / Déclarative - HashiCorp Project. [Considering]
#### Application automation tool ####
- Chef, Puppet, Salt [not used]

## Operate - Infrastructure as a Service ##
### Orchestration ###
- [Kubernetes (K8s)](https://kubernetes.io/): open-source container orchestration system for automating software deployment, scaling, and management. Orchestrator and clustering solution for Docker containers + HELM (webui for its management). Apache License 2.0. Google Project [Considering]
- [Docker Swarm](https://docs.docker.com/engine/swarm/): Lightweight orchestration of docker containers. [Considering]
- [Nomad](https://www.nomadproject.io/): A cluster manager and scheduler. Task scheduling platform that can orchestrate different workload types as an extended feature Self-hosted possible. HashiCorp Project. [Considering]
- [Rancher](https://rancher.com/): Open Source Platform for Running a Private Container Service. Rancher is an open source container management platform that includes full distributions of Kubernetes, Apache Mesos and Docker Swarm, and makes it simple to operate container clusters on any cloud or infrastructure platform. HashiCorp Project. [Considering]
#### Kubernetes Utils ####
- [KubeVirt](https://kubevirt.io/): Unified development platform where developers can build, modify, and deploy applications residing in both Application Containers as well as Virtual Machines in a common, shared environment. [Considering]
- [Minikube](https://minikube.sigs.k8s.io/docs/start/): Kubernetes on local computer [Considering] 
- [MicroK8s](https://microk8s.io/): small, fast, single-package Kubernetes for developers, IoT and edge. Local or multi-node [Considering]. Canonical Project. 

## Monitor ##
https://github.com/dheurtev/dheurtev/blob/main/monitoring.md

## Other tools ##

### Virtual Networking ###
- [Project Calico](https://www.tigera.io/project-calico/): Container networking and security. Apache 2.0 license 
