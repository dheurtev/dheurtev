# Developer tools
[Good list of self hosted apps](https://github.com/awesome-selfhosted/awesome-selfhosted)
#### SSH Server ####
- OpenSSH Server on Windows: 
  * https://www.it-connect.fr/installer-et-configurer-openssh-server-sur-windows-server-2019/
  * https://winaero.com/enable-openssh-server-windows-10/


- [Development kits](#development-kits)
- [Nas](#nas)
- [Reference + training](#reference-training)
- [Remote Desktop](#remote-desktop)
- [Security](#security)
- [Text sharing](#text-sharing)
- [Utilities](#utilities)
- [Web Dev](#web-dev)

## Development kits ## 
**[`^        back to top        ^`](#)**
### OCR ###
- [Tesseract](https://github.com/tesseract-ocr/tesseract): OCR originally developed at Hewlett-Packard Laboratories. `Apache v2.0 License` `past`

### Multimedia ###
- [FFMPEG](https://ffmpeg.org/): free and open-source software project consisting of a suite of libraries and programs for handling video, audio, and other multimedia files and streams. At its core is the command-line ffmpeg tool itself, designed for processing of video and audio files. `EXE` `Free` `LGPLv2.1` `in use`

## File transfer ##
### Servers on Windows ###
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
## Reference + training ## 
**[`^        back to top        ^`](#)**
### Python ###
- [RealPython](https://realpython.com/): Python tutorials. `Website` `Freemium`

## Remote Desktop ##
**[`^        back to top        ^`](#)**
- [Google Chrome Remote Desktop](https://remotedesktop.google.com/?pli=1): `Chrome extension` `Free` `⚠ Proprietary` `in use`
- [AnyDesk](https://anydesk.com/en): Remote desktop application. Cross-platform. Proprietary. `EXE` `Freemium` `⚠ Proprietary` `in use`
- [TeamViewer](https://www.teamviewer.com/fr/): Remote access and remote control computer software, allowing maintenance of computers and other devices. Cross-platform. Proprietary `EXE` `APP` `Freemium` `⚠ Proprietary` `past`
- [RustDesk](https://rustdesk.com/): An open-source self-hosted AnyDesk clone. [Server component](https://github.com/rustdesk/rustdesk-server) - [Desktop component](https://github.com/rustdesk/rustdesk) `EXE` `Free` `AGPL-3.0` 
- [FreeRDP](https://www.freerdp.com/): free implementation of the Remote Desktop Protocol (RDP). `EXE` `Apache license` `Free`
- [NoMachine](https://www.nomachine.com/fr): NX. proprietary cross-platform software application for remote access, desktop sharing, virtual desktop and file transfer between computers. Cross-Platform. `EXE` `Freeware` `past`
- [X2GO (NX)](https://wiki.x2go.org/doku.php):  open source remote desktop software for Linux that uses a modified NX 3 protocol. Cross-Platform. `EXE` `Free` `GPLv2` `past`
- [TightVNC](https://www.tightvnc.com/): TightVNC is a free and open-source remote desktop software server and client application for Linux and Windows. A server for macOS is available under a commercial source code license only. `EXE` `Free` `GPLv2` `past`
- [UltraVNC](https://uvnc.com/): open-source remote-administration/remote-desktop-software utility. The client supports Microsoft Windows and Linux but the server only supports Windows. `EXE` `Free` `GPLv2` `past`

## Text sharing ##
**[`^        back to top        ^`](#)**
- [Pastebin](https://pastebin.com/): number one paste tool since 2002. Pastebin is a website where you can store text online for a set period of time. Registration required. `SaaS` `Free` `⚠ Proprietary`
- [Hastebin](https://hastebin.com/about.md): self-hosted pastebin alternative. `SaaS` `Free` `MIT License`
   * [haste-client](https://github.com/toptal/haste-client)
   * [haste-server](https://github.com/toptal/haste-server)
- [Privatebin](https://github.com/PrivateBin/PrivateBin): self-hosted minimalist, open source online pastebin where the server has zero knowledge of pasted data. Data is encrypted and decrypted in the browser. [Github Repo](). `SaaS` `Free` `Zlib/libpng license` `GPLv2 license components`

## Utilities ## 
**[`^        back to top        ^`](#)**
### Automation ###
- [AutoHotKey](https://www.autohotkey.com/): free and open-source custom scripting language for Microsoft Windows, initially aimed at providing easy keyboard shortcuts or hotkeys, fast macro-creation and software automation that allows users of most levels of computer skill to automate repetitive tasks in any Windows application `EXE` `APP` `Free` `GPLv2` `in use`
- [Auto Mouse Click](https://www.murgee.com/auto-mouse-click/) : Automate Mouse clicks. Define Click Type, X Co-ordinates, Y-Co-ordinate and specify whether to return mouse cursor back to original location and automate mouse clicks. `EXE` `Freemium`

## Web dev ## 
**[`^        back to top        ^`](#)**
### Static site generator ###
- [Hugo](https://gohugo.io/): fast open-source static site generator. Go based. Uses Go templates. Shortcodes, built-in templates, multilingual and i18n. `EXE` `Free` `Apache v2.0` `past`
