# My Picks for DevOps

Tools and packages I am using are marked `in use`.
Tools and packages I used are marked as `past`.

- [Collaborate](https://github.com/dheurtev/dheurtev/blob/main/devops.md#collaborate)
- [Code](https://github.com/dheurtev/dheurtev/blob/main/devops.md#code)
- [Continuous Integration / Continous Distribution (CICD)](https://github.com/dheurtev/dheurtev/blob/main/devops.md#continuous-integration--continous-distribution-cicd)

## Collaborate ##
### Application lifecycle management ###
- [Jira](https://www.atlassian.com/software/jira):  issue tracking product developed by Atlassian that allows bug tracking and agile project management. Atlassian Project. `⚠ Proprietary` `Past`
- [Taiga](https://www.taiga.io/): free and open-source project management tool. `MPL 2.0`
- [Bugzilla](https://www.bugzilla.org/): open-source web-based bug tracking tool developed by Mozilla. `Mozilla Public License` `past`
- [Trac](https://trac.edgewall.org/): open-source, web-based project management, and issue tracking tool. Git, Subversion, Wiki. `GPL-2.0-or-later` `past`
- [Redmine](https://www.redmine.org/): open-source, web-based project management, and issue tracking tool. Some of the main features of Redmine are multiple projects support, flexible role-based access control, flexible issue tracking system, Gantt chart, multi-language support, issue creation via email, etc. SVN, CVS, Git, Mercurial, Bazaar and Darcs. `GPLv2`
### ERP/CRM with project management ###
- [Odoo](https://www.odoo.com/): suite of business management software tools including, for example, CRM, e-commerce, billing, accounting, manufacturing, warehouse, project management, and inventory management. "Community" version: `GNU Lesser General Public License v3`; "Enterprise" version: `⚠ Proprietary license`.

### Code Repository ###
- [Gihub](https://github.com/) `in use`
- [Gitea](https://gitea.io/en-us/): open-source forge software package for hosting software development version control using Git as well as other collaborative features like bug tracking, wikis and code review. Self-hosted Github alternative. `Apache License` `in use`
- [Bitbucket](https://bitbucket.org/product): Git-based source code repository hosting service owned by Atlassian. Bitbucket offers both commercial plans and free accounts with an unlimited number of private repositories. Git solution for teams using Jira. `⚠ Proprietary` `past`
- [Gitlab](https://about.gitlab.com): automate the builds, integration, and verification of your code. With SAST, DAST, code quality analysis, plus pipelines. [Self-hosted option](https://docs.gitlab.com/ee/topics/offline/quick_start_guide.html). GitLab Community Edition (CE) is licensed under the terms of the  `MIT License`. GitLab Enterprise Edition (EE) is licensed under `The GitLab Enterprise Edition (EE) license - ⚠ Proprietary license`  `past` 

## Code ##
### Code Versioning (SCM/VCS) ###
- [Git](https://git-scm.com/): free and open source software for distributed version control. `GPL 2.0` `in use` 
  * [Documentation](https://git-scm.com/docs)
- [Apache Subversion](https://subversion.apache.org/): software versioning and revision control system distributed as open source under the Apache License. `Apache-2.0` `past`
- [Mercurial](https://www.mercurial-scm.org/): distributed revision control tool for software developers. `GPLv2` `past`
#### Code Versioning tools ####

- [WinMerge](https://winmerge.org/source-code/?lang=en): Open Source differencing and merging tool for Windows. `GPLv2` `past`

### Development environment ###
- [WSL/WSL2](https://docs.microsoft.com/en-us/windows/wsl/compare-versions): Windows Subsystem for Linux is a compatibility layer for running Linux binary executables natively on Windows 10, Windows 11, and Windows Server 2019. `⚠ Proprietary` `in use`
- [MobaXTerm](https://mobaxterm.mobatek.net/): Xserver and tabbed SSH client for Windows. Free edition. `⚠ Proprietary` `past`
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
##### Public #####
- [Docker Hub](https://hub.docker.com/search?q=): Search docker images
- [Quay](https://quay.io/): Container Image repository server
- [Fedora Registry](registry.fedoraproject.org/)
- [PyPi](https://pypi.org/): repository of software for the Python programming language.
- [npm](https://www.npmjs.com/): npm is a package manager for the JavaScript programming language
##### Private #####
- [Docker Registry](https://docs.docker.com/registry/): Docker registry - Docker Project - [https://hub.docker.com/_/registry](docker pull registry)
##### Docker Registry Management #####
- [Docker Registry Frontend](https://hub.docker.com/r/konradkleine/docker-registry-frontend/): Browse and modify your Docker registry in a browser. docker pull konradkleine/docker-registry-frontend
- [CraneOperator](https://hub.docker.com/r/parabuzzle/craneoperator): UI for browsing a Registry using the v2 api

#### Security ####
- [HashiCorp Vault](https://www.vaultproject.io/): Secure, store and tightly control access to tokens, passwords, certificates, encryption keys for protecting secrets and other sensitive data using a UI, CLI, or HTTP API. Self hosted possible. HashiCorp Project. [Considering]
