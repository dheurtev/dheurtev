# My Picks for DevOps

Tools and technologies i am using, have used or consider using

- [Collaborate](https://github.com/dheurtev/dheurtev/blob/main/devops.md#collaborate)
- [Code](https://github.com/dheurtev/dheurtev/blob/main/devops.md#code)
- [Continuous Integration / Continous Distribution (CICD)](https://github.com/dheurtev/dheurtev/blob/main/devops.md#continuous-integration--continous-distribution-cicd))

## Collaborate ##
### Application lifecycle management ###
- [Jira](https://www.atlassian.com/software/jira):  issue tracking product developed by Atlassian that allows bug tracking and agile project management. Atlassian Project. Proprietary [past]
### Code Repository ###
- [Gihub](https://github.com/)
- [Gitea](https://gitea.io/en-us/): open-source forge software package for hosting software development version control using Git as well as other collaborative features like bug tracking, wikis and code review. Self-hosted Github alternative. Apache License.
### Registry ###
- [Docker Registry](https://docs.docker.com/registry/): Docker registry - Docker Project - [https://hub.docker.com/_/registry](docker pull registry)
### Artefact Management ###
- [Docker Registry Frontend](https://hub.docker.com/r/konradkleine/docker-registry-frontend/): Browse and modify your Docker registry in a browser. docker pull konradkleine/docker-registry-frontend
- [CraneOperator](https://hub.docker.com/r/parabuzzle/craneoperator): UI for browsing a Registry using the v2 api

## Code ##
### Code Versioning (SCM/VCS) ###
- [Git](https://git-scm.com/): free and open source software for distributed version control. GPL 2.0 - [Documentation](https://git-scm.com/docs)
- [Apache Subversion](https://subversion.apache.org/): software versioning and revision control system distributed as open source under the Apache License. Apache-2.0 [past]
- [WinMerge](https://winmerge.org/source-code/?lang=en): Open Source differencing and merging tool for Windows. GPL [past]

### Development environment ###
- [WSL/WSL2](https://docs.microsoft.com/en-us/windows/wsl/compare-versions): Windows Subsystem for Linux is a compatibility layer for running Linux binary executables natively on Windows 10, Windows 11, and Windows Server 2019.
- [MobaXTerm](https://mobaxterm.mobatek.net/): Xserver and tabbed SSH client for Windows. Proprietary.
### Code Editors ###
- [Microsoft Visual Studio Code](https://code.visualstudio.com/): VS Code. Source-code editor made by Microsoft for Windows, Linux and macOS. free for private or commercial use.
- [Notepad ++](https://notepad-plus-plus.org/): Text and source code editor for use with Microsoft Windows. GPLv2. [Use in Linux](https://itsfoss.com/notepad-plus-plus-linux/) - [Linux Clone - notepadqq](https://notepadqq.com/s/)
- [Atom](https://atom.io/): free and open-source text and source code editor for macOS, Linux, and Microsoft Windows with support for plug-ins written in JavaScript, and embedded Git Control. Cross-platform. MIT license. Sunsetting Dec. 2022. [past]

### IDE ###
- [Jetbrains PyCharm CE](https://www.jetbrains.com/pycharm/): Python IDE.
- [Eclipse](https://www.eclipse.org/): integrated development environment used in computer programming. Eclipse Public License (EPL) [past]
- [PyDev](https://www.pydev.org/): Python IDE for Eclipse. Eclipse Public License (EPL) [past]
- [Microsoft Visual Studio](https://visualstudio.microsoft.com/fr/): integrated development environment from Microsoft. Proprietary [past]

### API development ###
- [OpenAPI](https://www.openapis.org/):OpenAPI Specification, previously known as the Swagger Specification, is a specification for machine-readable interface files for describing, producing, consuming, and visualizing RESTful web services [considering]
- [Swagger](https://swagger.io/): suite of tools for API developers. Apache 2.0 License [considering].
       
## Continuous Integration / Continous Distribution (CI/CD) ##
### Build ###
#### Build tools #####
- [Maven](https://maven.apache.org/): build automation tool used primarily for Java projects. can also be used to build and manage projects written in C#, Ruby, Scala, and other languages. Apache license 2.0

#### Build images ####
- [Docker (docker build)](https://docs.docker.com/engine/reference/commandline/build/)
- [Podman (podman build)](https://docs.podman.io/en/latest/markdown/podman-build.1.html)
- [Packer](https://www.packer.io/): free and open source tool for creating golden images for multiple platforms from a single source configuration. AWS, Docker, Vagrant, VirtualBox, VMWARE, Openstack, etc [considering].

### Test ###
- [PyTest](https://docs.pytest.org/en/7.1.x/): Python testing framework. MIT License.
- [Selenium](https://www.selenium.dev/): open source umbrella project for a range of tools and libraries aimed at supporting browser automation. Apache License 2.0 [past]
#### CI/CD Platforms ####
- [Jenkins](https://www.jenkins.io/): open-source automation server. It helps automate the parts of software development related to building, testing, and deploying, facilitating continuous integration and continuous delivery. MIT license. [considering]
- [Circle CI](https://circleci.com/): continuous integration and continuous delivery platform [considering]
- [Travis CI](https://www.travis-ci.com/): hosted continuous integration service used to build and test software projects hosted on GitHub and Bitbucket [considering]

### Release ###
#### Artefact Management - Registries ####
- [Docker Hub](https://hub.docker.com/search?q=): Search docker images
- [Quay](https://quay.io/): Container Image repository server
- [Fedora Registry](registry.fedoraproject.org/)
- [PyPi](https://pypi.org/): repository of software for the Python programming language.
- [npm](https://www.npmjs.com/): npm is a package manager for the JavaScript programming language

#### Security ####
- [HashiCorp Vault](https://www.vaultproject.io/): Secure, store and tightly control access to tokens, passwords, certificates, encryption keys for protecting secrets and other sensitive data using a UI, CLI, or HTTP API. Self hosted possible. HashiCorp Project. [Considering]
