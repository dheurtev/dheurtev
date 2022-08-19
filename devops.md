# My Picks for DevOps

Tools i have used or consider using

## Collaborate - Application lifecycle management - Code Repository - Registry - Artefact Management ##
#### using ####
- [Gihub](https://github.com/)
- [Gitea](https://gitea.io/en-us/): open-source forge software package for hosting software development version control using Git as well as other collaborative features like bug tracking, wikis and code review. Self-hosted Github alternative. Apache License.
- [Docker Registry](https://docs.docker.com/registry/): Docker registry - Docker Project - [https://hub.docker.com/_/registry](docker pull registry)
- [Portainer CE](https://hub.docker.com/r/portainer/portainer-ce): Portainer CE - a lightweight service delivery platform for containerized applications. docker pull portainer/portainer-ce
- [Docker Registry Frontend](https://hub.docker.com/r/konradkleine/docker-registry-frontend/): Browse and modify your Docker registry in a browser. docker pull konradkleine/docker-registry-frontend
- [CraneOperator](https://hub.docker.com/r/parabuzzle/craneoperator): UI for browsing a Registry using the v2 api

#### used ####
- [Jira](https://www.atlassian.com/software/jira):  issue tracking product developed by Atlassian that allows bug tracking and agile project management. Atlassian Project. Proprietary

## Code ##
### Code Versioning (SCM/VCS) ###
#### using ####
- [Git](https://git-scm.com/): free and open source software for distributed version control. GPL 2.0 - [Documentation](https://git-scm.com/docs)
#### used ####
- [Apache Subversion](https://subversion.apache.org/): software versioning and revision control system distributed as open source under the Apache License. Apache-2.0 [old]
### Development environment ###
- [WSL/WSL2](https://docs.microsoft.com/en-us/windows/wsl/compare-versions): Windows Subsystem for Linux is a compatibility layer for running Linux binary executables natively on Windows 10, Windows 11, and Windows Server 2019.
- [MobaXTerm](https://mobaxterm.mobatek.net/): Xserver and tabbed SSH client for Windows. Proprietary
### Level 2 Virtualization ###
#### using ####
- For VMS:
  * [Multipass](https://multipass.run/): a CLI to launch and manage VMs on Windows, Mac and Linux that simulates a cloud environment with support for cloud-init. Canonical project
  * [Vagrant](https://www.vagrantup.com/): open-source software product for building and maintaining portable virtual software development environments; e.g., for VirtualBox, KVM, Hyper-V, Docker containers, VMware, and AWS. It tries to simplify the software configuration management of virtualization. Typically creates Virtualbox VMs but plugins support other platforms. HashiCorp Project.
- Docker:
  * [Docker Desktop Windows](https://docs.docker.com/desktop/install/windows-install/): Docker Desktop for Windows
#### used ####
- GUI:
  * [Oracle VM VirtualBox](https://www.virtualbox.org/): Open Source Level 2 x86 and AMD64/Intel64 virtualization product. Runs as an app on Windows, Linux, OS X, Solaris.
  * [Virt-Manager](https://virt-manager.org/): Desktop virtual machine monitor for KVM/QEMU/Libvirt. GPLv2.
#### considering ####
- [Docker Desktop Linux](https://docs.docker.com/desktop/install/linux-install/): Docker Desktop for Linux

### Code Editors ###
#### using ####
- [Microsoft Visual Studio Code](https://code.visualstudio.com/): VS Code. Source-code editor made by Microsoft for Windows, Linux and macOS. free for private or commercial use.
- [Notepad ++](https://notepad-plus-plus.org/): Text and source code editor for use with Microsoft Windows. GPLv2. [Use in Linux](https://itsfoss.com/notepad-plus-plus-linux/) - [Linux Clone - notepadqq](https://notepadqq.com/s/)
#### used ####
- [Atom](https://atom.io/): free and open-source text and source code editor for macOS, Linux, and Microsoft Windows with support for plug-ins written in JavaScript, and embedded Git Control. Cross-platform. MIT license. Sunsetting Dec. 2022.

### IDE ###
#### using ####
- [Jetbrains PyCharm CE](https://www.jetbrains.com/pycharm/): Python IDE.
#### used ####
- [Eclipse](https://www.eclipse.org/): integrated development environment used in computer programming. Eclipse Public License (EPL)
- [PyDev](https://www.pydev.org/): Python IDE for Eclipse. Eclipse Public License (EPL)
- [Microsoft Visual Studio](https://visualstudio.microsoft.com/fr/): integrated development environment from Microsoft. Proprietary

### API development ###
#### considering ####
- [OpenAPI](https://www.openapis.org/):OpenAPI Specification, previously known as the Swagger Specification, is a specification for machine-readable interface files for describing, producing, consuming, and visualizing RESTful web services 
- [Swagger](https://swagger.io/): suite of tools for API developers. Apache 2.0 License.
       
## Continuous Integration / Continous Distribution (CI/CD) ##
### Build ###
#### considering ####
- [Maven](https://maven.apache.org/): build automation tool used primarily for Java projects. can also be used to build and manage projects written in C#, Ruby, Scala, and other languages. Apache license 2.0
### Test ###
##### using #####
- [PyTest](https://docs.pytest.org/en/7.1.x/): Python testing framework. MIT License.
##### used #####
- [Selenium](https://www.selenium.dev/): open source umbrella project for a range of tools and libraries aimed at supporting browser automation. Apache License 2.0
#### CI/CD Platforms ####
##### considering #####
- [Jenkins](https://www.jenkins.io/): open-source automation server. It helps automate the parts of software development related to building, testing, and deploying, facilitating continuous integration and continuous delivery. MIT license.
- [Circle CI](https://circleci.com/): continuous integration and continuous delivery platform
- [Travis CI](https://www.travis-ci.com/): hosted continuous integration service used to build and test software projects hosted on GitHub and Bitbucket

