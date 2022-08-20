# My Picks for DevOps

Tools and packages I am using are marked `in use`.
Tools and packages I used are marked as `past`.

- [Collaborate](#collaborate)
- [Code](#code)
- [Continuous Integration / Continous Distribution (CICD)](#continuous-integration--continous-distribution-cicd)
  * [Build](#build)
  * [Release](#release)

## Collaborate ##
**[`^        back to top        ^`](#)**
### Application lifecycle management ###
- [Jira](https://www.atlassian.com/software/jira):  issue tracking product developed by Atlassian that allows bug tracking and agile project management. Atlassian Project. `⚠ Proprietary` `Past`
- [Taiga](https://www.taiga.io/): free and open-source project management tool. `MPL 2.0`
- [Bugzilla](https://www.bugzilla.org/): open-source web-based bug tracking tool developed by Mozilla. `Mozilla Public License` `past`
- [Trac](https://trac.edgewall.org/): open-source, web-based project management, and issue tracking tool. Git, Subversion, Wiki. `GPL-2.0-or-later` `past`
- [Redmine](https://www.redmine.org/): open-source, web-based project management, and issue tracking tool. Some of the main features of Redmine are multiple projects support, flexible role-based access control, flexible issue tracking system, Gantt chart, multi-language support, issue creation via email, etc. SVN, CVS, Git, Mercurial, Bazaar and Darcs. `GPLv2`
### ERP/CRM with project management ###
- [Odoo](https://www.odoo.com/): suite of business management software tools including, for example, CRM, e-commerce, billing, accounting, manufacturing, warehouse, project management, and inventory management. "Community" version: `GNU Lesser General Public License v3`; "Enterprise" version: `⚠ Proprietary license`.

## Code ##
**[`^        back to top        ^`](#)**
### Code Versioning (SCM/VCS) ###
- [Git](https://git-scm.com/): free and open source software for distributed version control. `GPLv2` `in use` 
  * [Documentation](https://git-scm.com/docs)
- [Apache Subversion](https://subversion.apache.org/): software versioning and revision control system distributed as open source under the Apache License. `Apache-2.0` `past`
- [Mercurial](https://www.mercurial-scm.org/): distributed revision control tool for software developers. `GPLv2` `past`
#### Code Versioning tools ####
- [Git for Windows](https://gitforwindows.org/): lightweight, native set of tools that bring the full feature set of the Git SCM to Windows. Offers GNU tools terminal with Cygwin. `GPLv2` `in use`
- [TortoiseGIT](https://tortoisegit.org/): Windows Shell Interface to Git. `GPLv2` `past`
- [TortoiseSVN](https://tortoisesvn.net/): Apache Subversion (SVN) client, implemented as a Windows shell extension. `GPLv2` `past`
- [TortoiseHG](https://tortoisehg.bitbucket.io/): Windows shell extension and a series of applications for the Mercurial distributed revision control system . `GPLv2` `past`
- [WinMerge](https://winmerge.org/source-code/?lang=en): Open Source differencing and merging tool for Windows. `GPLv2` `past`
### Code Repository and packages ###
#### Public ####
- Python :
  * [PyPi](https://pypi.org/): repository of software for the Python programming language.
- Javascript:
  * [npm](https://www.npmjs.com/): npm is a package manager for the JavaScript programming language
#### Private ####
- [Gitea](https://gitea.io/en-us/): open-source forge software package for hosting software development version control using Git as well as other collaborative features like bug tracking, wikis and code review. Self-hosted Github alternative. `Apache License` `in use`
#### Both ####
- [Gihub](https://github.com/) `in use`
- [Bitbucket](https://bitbucket.org/product): Git-based source code repository hosting service owned by Atlassian. Bitbucket offers both commercial plans and free accounts with an unlimited number of private repositories. Git solution for teams using Jira. `⚠ Proprietary` `past`
- [Gitlab](https://about.gitlab.com): automate the builds, integration, and verification of your code. With SAST, DAST, code quality analysis, plus pipelines. [Self-hosted option](https://docs.gitlab.com/ee/topics/offline/quick_start_guide.html). GitLab Community Edition (CE) is licensed under the terms of the  `MIT License`. GitLab Enterprise Edition (EE) is licensed under `The GitLab Enterprise Edition (EE) license - ⚠ Proprietary license`  `past` 
### Terminals ###
#### Windows ####
- [Windows Terminal](https://github.com/microsoft/terminal): multi-tabbed terminal emulator that Microsoft has developed for Windows 10 and later as a replacement for Windows Console. [Windows Store](https://www.microsoft.com/store/apps/9n0dx20hk701) `MIT License` `in use`
- [WSL/WSL2](https://docs.microsoft.com/en-us/windows/wsl/compare-versions): Windows Subsystem for Linux is a compatibility layer for running Linux binary executables natively on Windows 10, Windows 11, and Windows Server 2019. `⚠ Proprietary` `in use`
- [Cygwin](https://www.cygwin.com/): POSIX-compatible programming and runtime environment that runs natively on Microsoft Windows. `LGPLv3` `in use` (via git for windows)
- [MobaXTerm](https://mobaxterm.mobatek.net/): Xserver and tabbed SSH client for Windows. Free edition. `⚠ Proprietary` `past`

### Code Editors ###
- [Microsoft Visual Studio Code - VS Code](https://code.visualstudio.com/): Source-code editor made by Microsoft for Windows, Linux and macOS. free for private or commercial use. `MIT License` `in use`
- [Notepad ++](https://notepad-plus-plus.org/): Text and source code editor for use with Microsoft Windows. `GPLv2` `in use`
  * [Use in Linux](https://itsfoss.com/notepad-plus-plus-linux/)
  * [Linux Clone - notepadqq](https://notepadqq.com/s/)
- [Atom](https://atom.io/): free and open-source text and source code editor for macOS, Linux, and Microsoft Windows with support for plug-ins written in JavaScript, and embedded Git Control. Cross-platform. `MIT license` `⚠ Sunsetting Dec. 2022, Use Microsoft VS Code` `past`
- [Geany](https://www.geany.org/): free and open-source lightweight GUI text editor. `GPLv2` `past` 

### IDE ###
#### General ####
- [Eclipse](https://www.eclipse.org/): integrated development environment used in computer programming. `Eclipse Public License (EPL)` `past`
- [Microsoft Visual Studio](https://visualstudio.microsoft.com/fr/): integrated development environment from Microsoft. `⚠ Proprietary` `past`
#### Python ####
- [Jetbrains PyCharm CE](https://www.jetbrains.com/pycharm/): Python IDE. Community Edition : `Apache 2.0 license` and Professional edition : `⚠ Proprietary`. `in use`
- [PyDev](https://www.pydev.org/): Python IDE for Eclipse. `Eclipse Public License (EPL)` `past`
#### Desktop Development  / RAD ####
Cross-platform :
- CLI + API + HTML + CSS + JS + Webserver
- [Qt + Python](https://www.qt.io/qt-for-python): cross-platform. Usable in commercial projects. Dual license`GPL and LGPLv3 open source licenses`. 
- [Lazarus (Delphi)](https://www.lazarus-ide.org/): free cross-platform visual integrated development environment for rapid application development using the Free Pascal compiler. Usable in commercial projects. `GPL/LGPL` 
  * [Why Use](https://www.lazarus-ide.org/index.php?page=whyuse) 
  * [Licensing](https://wiki.lazarus.freepascal.org/licensing#Licensing_relating_to_FPC.2FLazarus_usage)
- [Delphi Community Edition (Embarcadero)](https://www.embarcadero.com/fr/products/delphi/starter):  integrated development environment (IDE) for rapid application development of desktop, mobile, web, and console software. For freelance developers, startups, students and non-profits. Startups (<5000$ revenus par an). iOS, Android, Windows et MacOS. `⚠ Proprietary` `past` 

### API development ###
- API specifications : [OpenAPI](https://www.openapis.org/):OpenAPI Specification, previously known as the Swagger Specification, is a specification for machine-readable interface files for describing, producing, consuming, and visualizing RESTful web services.
- API tools : [Swagger](https://swagger.io/): suite of tools for API developers. `Apache 2.0 License`.
- API Gateway: [gloo](https://www.solo.io/products/gloo-edge/): Kubernetes-native API Gateway Built on Envoy. `Apache 2.0 License`. 
### Databases ###
[My page on databases](databases.md)
### Streaming and messaging ####
- Messaging Broker: [RabbitMQ](https://www.rabbitmq.com/): open-source message-broker software that originally implemented the Advanced Message Queuing Protocol and has since been extended with a plug-in architecture to support Streaming Text Oriented Messaging Protocol, MQ Telemetry Transport, and other protocols. `Mozilla Public License` `in use`
		 * MQTT broker: [Eclipse Mosquito](https://mosquitto.org/): Eclipse Mosquitto is an open source (EPL/EDL licensed) message broker that implements the MQTT protocol.
- Message Broker (horizontal scaling): [Apache Kafka](https://kafka.apache.org/): distributed event store and stream-processing platform. It is an open-source system developed by the Apache Software Foundation written in Java and Scala. The project aims to provide a unified, high-throughput, low-latency platform for handling real-time data feed.  distributed publish-subscribe messaging system that receives data from disparate source systems and makes the data available to target systems in real time. `Apache License 2.0`
- Remote Procedure Call: [gRPC](open source high performance Remote Procedure Call (RPC) framework that can run in any environment). Uses a binary payload that is efficient to create and to parse, and it exploits HTTP/2 for efficient management of connectionsGoogle Project. [CNCF incubating project](https://www.cncf.io/projects/grpc/) `Apache 2.0 License`.

## Continuous Integration / Continous Distribution (CI/CD) ##
**[`^        back to top        ^`](#)**
[CI/CD, the what, why and how - Github](https://resources.github.com/ci-cd/)
### Build ###
**[`^        back to top        ^`](#)**
#### Build tools #####
- [Maven](https://maven.apache.org/): build automation tool used primarily for Java projects. can also be used to build and manage projects written in C#, Ruby, Scala, and other languages. `Apache license 2.0`

#### Build images ####
- [Docker (docker build)](https://docs.docker.com/engine/reference/commandline/build/)
- [Podman (podman build)](https://docs.podman.io/en/latest/markdown/podman-build.1.html)
- [Packer](https://www.packer.io/): free and open source tool for creating golden images for multiple platforms from a single source configuration. AWS, Docker, Vagrant, VirtualBox, VMWARE, Openstack, etc. HashiCorp Project. `Mozilla Public License 2.0`

### Test ###
- [PyTest](https://docs.pytest.org/en/7.1.x/): Python testing framework. `MIT License` `in use`
- [Selenium](https://www.selenium.dev/): open source umbrella project for a range of tools and libraries aimed at supporting browser automation. `Apache License 2.0` `past`

#### CI/CD Platforms ####
- [Jenkins](https://www.jenkins.io/): open-source automation server. It helps automate the parts of software development related to building, testing, and deploying, facilitating continuous integration and continuous delivery. `MIT license`
- [Circle CI](https://circleci.com/): continuous integration and continuous delivery platform.
- [Travis CI](https://www.travis-ci.com/): hosted continuous integration service used to build and test software projects hosted on GitHub and Bitbucket.
- Gitlab

### Release ###
**[`^        back to top        ^`](#)**
#### Artefact Management - Image Registries ####
- Docker:
  * [Docker Hub](https://hub.docker.com/search?q=): Search docker images
  * [Quay](https://quay.io/): Container Image repository server
  * [Fedora Registry](registry.fedoraproject.org/)
- Kubernetes:
  * [Artifacthub](https://artifacthub.io/)
  * [Helm](https://helm.sh/): Package manager for Kubernetes - [CNCF graduated project](https://www.cncf.io/projects/helm/) - [Github](https://github.com/helm/helm) `Apache 2.0 License`

##### Private #####
Create your own docker hub :

- [Docker Registry](https://docs.docker.com/registry/): Docker registry - Docker Project - [https://hub.docker.com/_/registry](docker pull registry) `Apache License 2.0` `in use`
  * [How to in Ubuntu 18.04](https://www.digitalocean.com/community/tutorials/how-to-set-up-a-private-docker-registry-on-ubuntu-18-04)
- [GitLab Container Registry](https://docs.gitlab.com/ee/user/packages/container_registry/): Docker registry integrated into Gitlab. Good for Gitlab users CI/CD.
##### Docker Registry Management #####
- [Docker Registry Frontend](https://hub.docker.com/r/konradkleine/docker-registry-frontend/): Browse and modify your Docker registry in a browser. *docker pull konradkleine/docker-registry-frontend*. `MIT License` `in use`
- [CraneOperator](https://hub.docker.com/r/parabuzzle/craneoperator): UI for browsing a Registry using the v2 api. *docker pull parabuzzle/craneoperator* `MIT License` `in use`
- [Portus](http://port.us.org/): open source authorization service and user interface for docker. Private registry. Enterprise oriented: LDAP, Oauth, OpenID integration. Suse project. `Apache 2.0 License` `⚠ Last updated in 2019`

##### Kubernetes Docker Registry Management #####
- [Harbor](https://goharbor.io/): open source registry that secures artifacts with policies and role-based access control, ensures images are scanned and free from vulnerabilities, and signs images as trusted. Takes time to setup. LDAP/AD integration.[CNCF Graduated project](https://www.cncf.io/projects/harbor/) - [Github repo](https://github.com/goharbor/harbor). `Apache 2.0 License`

#### Security ####
**[`^        back to top        ^`](#)**
- [HashiCorp Vault](https://www.vaultproject.io/): Secure, store and tightly control access to tokens, passwords, certificates, encryption keys for protecting secrets and other sensitive data using a UI, CLI, or HTTP API. Self hosted possible. HashiCorp Project. `Mozilla Public License 2.0`
