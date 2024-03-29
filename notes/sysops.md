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
- [Terraform](https://www.terraform.io/): Users define and provide data center infrastructure using a declarative configuration language known as HashiCorp Configuration Language, or optionally JSON to create, change and improve infrastructure. immutable infrastructure based on images. Typically for cloud and kubernetes. Config changes delete or recreate machines - Immutable / Déclarative - HashiCorp Project. Was `Mozilla Public License v2`. Now [`Business Source License 1.1`](https://github.com/hashicorp/terraform/blob/main/LICENSE) = `⚠ Proprietary for production`
  * OpenTF : Open Source fork of Terraform : [OpenTF](https://github.com/opentffoundation/opentf) `Mozilla Public License v2`

## Operate - Infrastructure as a Service ##
**[`^        back to top        ^`](#)**
### Scheduling and Orchestration ###
- [Kubernetes (K8s)](https://kubernetes.io/): open-source container orchestration system for automating software deployment, scaling, and management. Orchestrator and clustering solution for Docker containers + HELM (webui for its management). Google Project. [CNCF graduated project](https://www.cncf.io/projects/kubernetes/). `Apache 2.0 License`
- [Docker Swarm](https://docs.docker.com/engine/swarm/): Lightweight orchestration of docker containers. `Apache 2.0 license`
- [Nomad](https://www.nomadproject.io/): A cluster manager and scheduler. Task scheduling platform that can orchestrate different workload types as an extended feature Self-hosted possible. HashiCorp Project. Was `Mozilla Public License v2`. Now [`Business Source License 1.1`](https://github.com/hashicorp/nomad/blob/main/LICENSE) = `⚠ Proprietary for production`
- [Rancher](https://rancher.com/): Open Source Platform for Running a Private Container Service. Rancher is an open source container management platform that includes full distributions of Kubernetes, Apache Mesos and Docker Swarm, and makes it simple to operate container clusters on any cloud or infrastructure platform. HashiCorp Project. `Apache License 2.0`
#### Kubernetes Utils ####
- [KubeVirt](https://kubevirt.io/): Unified development platform where developers can build, modify, and deploy applications residing in both Application Containers as well as Virtual Machines in a common, shared environment.  [CNCF incubating project](https://www.cncf.io/projects/kubevirt/). `Apache License 2.0`
- [Minikube](https://minikube.sigs.k8s.io/docs/start/): Kubernetes on local computer. Kuberneted project. `Apache License 2.0`
- [MicroK8s](https://microk8s.io/): small, fast, single-package Kubernetes for developers, IoT and edge. Local or multi-node. Canonical Project. `Apache 2.0 license` 
#### Storage ####
- [Minio](https://min.io/): highly-available, S3 compatible object storage solution. `Affero General Public License Version 3 (AGPLv3)`
- [Rook](https://rook.io/): Open-Source Cloud-Native Storage for Kubernetes. for File, Block and Object Storage. [CNCF Graduated project](https://www.cncf.io/projects/rook/) [Github repo](https://github.com/rook/rook) `Apache v2.0 License`

### Network ###

#### DNS ####
- [CoreDNS](https://coredns.io/): DNS server/forwarder, written in Go, that chains plugins. Integrates with Kubernetes and etcd. Plugs with somme DNS as a service providers [Github repo](https://github.com/coredns/coredns). [CNCF graduated project](https://www.cncf.io/projects/coredns/). `Apache 2.0 License` 

#### Virtual Networking ####
**[`^        back to top        ^`](#)**
- [Project Calico](https://www.tigera.io/project-calico/): Container networking and security. `Apache 2.0 license`
- [CNI](https://www.cni.dev/): Container Networking Interface. a specification and libraries for writing plugins to configure network interfaces in Linux containers, along with a number of supported plugins. [CNCF incubated project](https://www.cncf.io/projects/container-network-interface-cni/) - [Github Repo](https://github.com/containernetworking/cni) `Apache 2.0 License` 

#### Proxy ####
- [Envoy](https://www.envoyproxy.io/): Open source edge and service proxy, designed for cloud-native applications. high performance C++ distributed proxy. `Apache 2.0 license`. [CNCF graduated project](https://www.cncf.io/projects/envoy/) - [Github repo](https://github.com/envoyproxy/envoy). `Apache 2.0 license`   

#### Message broker ####
- [NATS](https://nats.io/): cloud native open-source messaging system. written in the Go programming language. Client libraries to interface with the server are available for dozens of major programming languages. deployments models using clusters, superclusters, and leaf nodes. [CNCF incubated project](https://www.cncf.io/projects/nats/) - [Githbub repo](https://github.com/nats-io/nats-server) `Apache 2.0 license`. 

#### API Gateways ####
[List of API Gateways](https://geekflare.com/api-gateway/)
- [Kong Gateway](https://konghq.com/products/kong-gateway): It is a popular open sourse cloud-native API gateway that is built on top of a lightweight proxy. It is written in Lua and runs with the help of Nginx. It provides a template engine that helps to accelerate the event time. It guarantees high performance, reliability, and scalability. It has an API and CLI for managing APIs, plugins, and configurations. `Apache 2.0 License`. Enterprise version is proprietary. 

- [Tyk](https://tyk.io/): It is an open-source API gateway that is designed to be fast, scalable, and easy to use. It supports RESTful APIs, GraphQL APIs, and gRPC APIs. It provides features such as rate limiting, authentication, authorization, analytics, and more. It has an API for managing APIs and policies. `Mozilla Public License Version 2.0`.

- [Gravitee](https://www.gravitee.io/): It is an open-source API management platform that provides features such as API gateway, developer portal, analytics, and more. It supports RESTful APIs and GraphQL APIs. It has an API for managing APIs, applications, plans, and subscriptions. `Apache 2.0 License` 

- [KrakenD](https://www.krakend.io/): It is a high-performance open-source API gateway that can transform, aggregate or remove data from your own or third-party services. It implements the Backend for Frontend (BFF) and Micro-frontends patterns to eliminate the necessity of dealing with multiple backends. It has an API for managing APIs and configurations. Community Edition: `Apache 2.0 License`

## Monitor ##
**[`^        back to top        ^`](#)**
[My monitoring page](https://github.com/dheurtev/dheurtev/blob/main/monitoring.md)

## Other tools ##
**[`^        back to top        ^`](#)**
[Cloud Native Computing Foundation (CNCF) Projects](https://www.cncf.io/projects/)


