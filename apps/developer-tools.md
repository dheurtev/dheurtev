# Developer tools
[Good list of self hosted apps](https://github.com/awesome-selfhosted/awesome-selfhosted)
#### SSH Server ####
- OpenSSH Server on Windows: 
  * https://www.it-connect.fr/installer-et-configurer-openssh-server-sur-windows-server-2019/
  * https://winaero.com/enable-openssh-server-windows-10/

- [Development kits](#development-kits)
- [Nas](#nas)
- [Text sharing](#text-sharing)
- [Web Dev](#web-dev)

## Development kits ## 
**[`^        back to top        ^`](#)**
### OCR ###
- [Tesseract](https://github.com/tesseract-ocr/tesseract): OCR originally developed at Hewlett-Packard Laboratories. `Apache v2.0 License` `past`

### Multimedia ###
- [FFMPEG](https://ffmpeg.org/): free and open-source software project consisting of a suite of libraries and programs for handling video, audio, and other multimedia files and streams. At its core is the command-line ffmpeg tool itself, designed for processing of video and audio files. `EXE` `Free` `LGPLv2.1` `in use`

#### HTTP server ####
- [XAMPP](https://www.apachefriends.org/):  Windows web development environment : Apache 2 + MariaDB database  + PHP + Perl. [Github Repo](https://github.com/ApacheFriends). `EXE` `Free` `Apache 2.0 License` `past`
- [WampServer](https://www.wampserver.com/en/):  Windows web development environment : Apache2, PHP and a MySQL database. [Sourceforge](https://sourceforge.net/projects/wampserver/) `EXE` `Free` `past`

Consider replacing by a docker container environment.

## Nas ##
**[`^        back to top        ^`](#)**
[8 best open source NAS operating systems for Linux (2019)](https://tipsmake.com/8-best-open-source-nas-operating-systems-for-linux)
[FreeNAS and TrueNAS are Unifying (2020)](https://www.truenas.com/blog/freenas-truenas-unification/)
[Best Free and Open Source NAS Solutions (2022)](https://www.serverwatch.com/storage/free-nas-solutions/)
### Proprietary ###
- [Synology](https://www.synology.com/fr-fr): NAS boxes offering multiple capabilities: multimedia, file management, groupware, backup and data protection, virtualization, user management, log servers, surveillance. SOHO to corporation oriented. [DSM OS](https://www.synology.com/en-global/dsm). `⚠ Proprietary` `in use`
- [QNAP](https://www.qnap.com/): NAS boxes offering multiple capabilities : backup and data protection, productivity, virtualization, IT management (logs), storage management 
  * Entry to mid-level : [QTS OS](https://www.qnap.com/qts/): + Multimedia capabilities. Wireguard support. AES-NI, ex-FAT, NVME-SSD cache, Teamviewer support. `⚠ Proprietary` `past` (older version)
  * High end: [quts-hero](https://www.qnap.com/en/operating-system/quts-hero): + Cloud capabilities. 128 bits Zfs based (RaidZ), VDI, 8K, Up to 5 PB shared folder, encrypted LUN. `⚠ Proprietary`
### OpenSource ###
- [OpenMediaVault](https://www.openmediavault.org/): Home user / storage oriented. free Linux distribution designed for network-attached storage. Debian based. It contains services like SSH, (S)FTP, SMB/CIFS, DAAP media server, RSync, BitTorrent client and many more. Plugins available. `Free` `GPLv3` `in use` 

### Python ###
- [RealPython](https://realpython.com/): Python tutorials. `Website` `Freemium`

## Text sharing ##
**[`^        back to top        ^`](#)**
- [Pastebin](https://pastebin.com/): number one paste tool since 2002. Pastebin is a website where you can store text online for a set period of time. Registration required. `SaaS` `Free` `⚠ Proprietary`
- [Hastebin](https://hastebin.com/about.md): self-hosted pastebin alternative. `SaaS` `Free` `MIT License`
   * [haste-client](https://github.com/toptal/haste-client)
   * [haste-server](https://github.com/toptal/haste-server)
- [Privatebin](https://github.com/PrivateBin/PrivateBin): self-hosted minimalist, open source online pastebin where the server has zero knowledge of pasted data. Data is encrypted and decrypted in the browser. [Github Repo](). `SaaS` `Free` `Zlib/libpng license` `GPLv2 license components`

## Web dev ## 
**[`^        back to top        ^`](#)**
### Static site generator ###
- [Hugo](https://gohugo.io/): fast open-source static site generator. Go based. Uses Go templates. Shortcodes, built-in templates, multilingual and i18n. `EXE` `Free` `Apache v2.0` `past`
