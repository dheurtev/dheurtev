# Developer tools

[Good list of self hosted apps](https://github.com/awesome-selfhosted/awesome-selfhosted)

- [Database](#database)
- [Design tools](#design-tools)
- [Development kits](#development-kits)
- [File sharing](#file-sharing)
- [File storage](#file-storage)
- [File transfer](#file-transfer)
- [Nas](#nas)
- [Networking](#networking)
- [Reference + training](#reference-training)
- [Remote Desktop](#remote-desktop)
- [Security](#security)
- [Text sharing](#text-sharing)
- [Utilities](#utilities)
- [Web Dev](#web-dev)

## Database ##
**[`^        back to top        ^`](#)**
[My page on databases](../databases.md)

## Design tools ##
**[`^        back to top        ^`](#)**
## Development kits ## 
**[`^        back to top        ^`](#)**
### OCR ###
- Tesseract
### Multimedia ###
- [FFMPEG](https://ffmpeg.org/): free and open-source software project consisting of a suite of libraries and programs for handling video, audio, and other multimedia files and streams. At its core is the command-line ffmpeg tool itself, designed for processing of video and audio files. `EXE` `Free` `LGPLv2.1` `in use`

## File sharing ##
### Large file transfer between users ###
- SendGB.com (<5GB, no account, password protection, encryption)
- WeTransfer.com
- Lufi (self hosted)
- Jirafeau (self hosted)

## File storage ##
- NextCloud
- OwnCloud

## File transfer ##
### Clients ###
- [OpenSSH](https://www.openssh.com/): suite of secure networking utilities based on the Secure Shell protocol, which provides a secure channel over an unsecured network in a client–server architecture. [Now available for windows in the windows extra apps](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse?tabs=gui). `Free` `BSD, ISC, public domain` `in use`
- Cyberduck
- [Bitvise SSH Client](https://www.bitvise.com/): Secure remote access software developed for Windows and available as a client and server. `EXE` `Free 
`⚠ Proprietary` `in use`
- [WinSCP](https://winscp.net/eng/download.php): WinSCP is a free and open-source SFTP, SCP, Amazon S3, WebDAV, and FTP client for Windows. `EXE` `Free` `GPLv3` `in use` (`APP` `Pay`) `in use`
- [FileZilla client](https://filezilla-project.org/): free and open-source, cross-platform FTP application. FTP, FTPS, SFTP. `EXE` `Free` `GPLv2` `past`
- [Putty](https://www.putty.org/):free and open-source terminal emulator, serial console and network file transfer application. It supports several network protocols, including SCP, SSH, Telnet, rlogin, and raw socket connection. `APP` `EXE` `Free ``MIT License` `past`
### Servers ###
#### HTTP server ####
- MiniShare - Minimal HTTP Server
#### FTP Server ####
- Filezilla
#### TFTP Server ####
- Tftpd64 / Tftpd32
- Solar Winds TFTP server
#### SSH Server ####
- OpenSSH Server on Windows: 
  * https://www.it-connect.fr/installer-et-configurer-openssh-server-sur-windows-server-2019/
  * https://winaero.com/enable-openssh-server-windows-10/

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
### Source Available ###
- [TrueNAS](https://www.truenas.com): Single Node; Scale-Up SAN/NAS/Object Storage Software; Plugins And VMs; 128-Bit Open ZFS File System. FreeBSD based.
  Free core version can support up to 400 drives in a single storage array. `Freemium`. [⚠ License is source available with EULA](https://www.truenas.com/docs/core/gettingstarted/useragreements/coreeula/). `⚠ Proprietary`   
### OpenSource ###
- [OpenMediaVault](https://www.openmediavault.org/): Home user / storage oriented. free Linux distribution designed for network-attached storage. Debian based. It contains services like SSH, (S)FTP, SMB/CIFS, DAAP media server, RSync, BitTorrent client and many more. Plugins available. `Free` `GPLv3` `in use` 
- [Openfiler](https://www.openfiler.com/): Storage oriented. full-fledged NAS/SAN appliance or IP storage gateway. iSCSI target for virtualization, Fibre Channel target support, block level replication and High Availabilty. 60TB max. `GPLv2` `⚠ Legacy - based on an unmaintained Linux OS distro (rpath)` `past`

## Networking ##
**[`^        back to top        ^`](#)**
- WiFi Analyzer: `APP` `Free` `⚠ Proprietary` `in use`
- [AngryIPScanner](https://angryip.org/): open-source and cross-platform network scanner designed to be fast and simple to use. `EXE` `Free` `GPLv2` `in use`
- [Wireshark](https://www.wireshark.org/): free and open-source packet analyzer. It is used for network troubleshooting, analysis, software and communications protocol development, and education `EXE` `Free` `GPLv2` `in use`
- [Nmap](https://nmap.org/): A command line port scanner for Windows, Mac OS, and Linux. `EXE` `Free` `Nmap Public Source License` `in use`
- Advanced IP Scanner
- psping
- http-console
- NetCut is a Tool helping Discover who is on your wireless/Wire network instantly. (IP/Device name/MAC address), Iphone/Xbox/Wii/PS3andriod/andriod
https://arcai.com/what-is-netcut/

## Reference + training ## 
**[`^        back to top        ^`](#)**
### Python ###
- RealPython

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

## Security ##
**[`^        back to top        ^`](#)**
### Penetration testing ###
- Metasploit: computer security project that provides information about security vulnerabilities and aids in penetration testing and IDS signature development.
### VPN ###
- OpenVPN
- Wireguard
- ShadowSocks
- Stunnel
- StrongSwan
- TincVPN
- https://www.softether.org/
### Zero Trust ###
- https://www.twingate.com/pricing/

## Text sharing ##
**[`^        back to top        ^`](#)**
- Pastebin
- Hastebin (self hosted)
- Privatebin (self hosted)

## Utilities ## 
**[`^        back to top        ^`](#)**
### Automation ###
- [AutoHotKey](https://www.autohotkey.com/): free and open-source custom scripting language for Microsoft Windows, initially aimed at providing easy keyboard shortcuts or hotkeys, fast macro-creation and software automation that allows users of most levels of computer skill to automate repetitive tasks in any Windows application `EXE` `APP` `Free` `GPLv2` `in use`
- [Auto Mouse Click](https://www.murgee.com/auto-mouse-click/) : Automate Mouse clicks. Define Click Type, X Co-ordinates, Y-Co-ordinate and specify whether to return mouse cursor back to original location and automate mouse clicks. `EXE` `Freemium`

## Web dev ## 
**[`^        back to top        ^`](#)**
### Server ###
- XAMPP
### Static site generator ###
- Hugo
