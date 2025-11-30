# Typical Personal Computer specifications found during the PC golden age (circa 1992-2005)

The purpose of the summary table below is to help retrocomputing and retrogaming enthusiasts in their quest to recreate period accurate PCs using the [x86 architecture](https://en.wikipedia.org/wiki/X86).
It summarizes the typical hardware and software specifications for each PC architecture and period. 
The focus is on everyday computer buyers, including my own personal experience.

- [A piece of advice](#a-piece-of-advice)
- [Summary Table](#summary-table)
- [CPU architecture OS support](#cpu-architecture-os-support)
- [Some useful sources](#some-useful-sources)

## A piece of advice
**[`^        back to top        ^`](#)**
- Image floppy disks and external media as soon as possible to preserve their content.
- Vacuum clean the dust on old hardware and replace thermal paste. 
- Do not expose old hardware directly to the internet without a strict firewall (bots are scanning for known security vulnerabilities).
- Use virtual machines instead of physical machines when installing new untrusted software sources, so you don't damage old hardware.
- Beware of viruses on floppy disks. Some may corrupt or kill your hardware.
- Keep games and other intensive applications to virtual machines to avoid overheating or damaging components.
- Running newer OS on older CPU architectures may be possible to some extent (+/- 10-15 years), but will cause performance (CPU speed and memory) issues.

## Summary Table
**[`^        back to top        ^`](#)**
| **Architecture** | 16 bits | 16/32 bits | 32 bits |  32 bits | 32 bits  | 32/64 bits |  32/64 bits |
|--------------|---------|-------|---------|---|---|------------|---|
| **Year** | **1979-1991** | **1991-1995** | **1995-1998** | **1998-2000** | **2001** | **2004** | **2009** |
| **CPU Example** | 8086 / 8088 / 186 / 286  | 386 SX (16) / 386 DX (32) / 486 DX (socket 3) | Pentium 100 / P200 (socket 5) / MMX 233 (1996) / PII 300 (1997) / AMD K6 (socket 7 - 1997) | P III 600 | P IV | Athlon 64 | core i7 |
| **CPU - Maximum clock** | | | 2.1 Ghz | | | | |
| **Microsoft Windows (Consumer)** | 2.11 (1989) | 3.1 / 3.1.1 | 95 | 98 SE | XP | XP 64 SP2 | Windows 7 |
| **Microsoft Windows (NT Line - Business)** | | NT 3.1 (1994), NT 3.5 (1994) | NT 3.5.1 (1995) / NT 4.0 (1996) | Windows 2000 (Business) | XP Pro |
| **MS-DOS** | supported -> 6.22 | 3.1 -> 5.0 | 6.22 -> 7.0 | Supported: Windows 98 / Partial support : Windows 2000 | Emulation | | |
| **Memory - Maximum**| | 256 MB | 480 MB (unstable) | 1GB (problem with DOS Games if memory > 512 MB) | 4 GB | 128 GB  (XP64), 1TB (2000) | 4 GB (32 bit) / 8 GB (home) / 16 GB (home premium) / 192 GB (enterprise) |
| **Memory - Typical / Top** | 1 MB / 4 MB | 4 MB/ 8 MB | 8 MB / 32 MB (1997) to 64 MB / 128 MB (1998) | 128 MB / 512 MB | 256 MB/ 512 MB | 256 MB/ 1 GB | 1 GB / 2 GB |
| **Hard Drive - Typical capacity** | 20-40 MB | 40-320 MB | 1-7 GB | 4-9 GB | 60-120 GB | 200 GB | 500 GB - 1 TB |
| **Hard Drive - Maximum** | | | 32 GB | 137 GB (Service pack) | 2 TB | 16 TB | 2 TB (32), 16 TB (64) |
| **Hard drive - Interface** | Mechanical hard drive on PATA (1986)/IDE | PATA/IDE | PATA/IDE | PATA/IDE | PATA/IDE or SATA | PATA/IDE or SATA | SATA with SSD drive (TRIM) |
| **Hard drive - Partition** | FAT16 / HPFS (NT) | FAT16 / HPFS (NT) | FAT32 / NTFS (NT 3.5.1)| FAT32 / NTFS (NT)  | NTFS (Windows XP default) or FAT32 | NTFS (Windows XP default) | NTFS |
| **External Media - Floppy Drive** | 3"1/2 (1982) and 5"1/4 (1976) | 3"1/2 and 5"1/4 | 3"1/2 and Zip | 3"1/2 and Jazz | 3"1/2 (obsolete) and multi-format card readers | 3"1/2 (obsolete) and multi-format card readers | 3"1/2 (obsolete)  and multi-format card readers (obsolete) |
| **External Media - Memory Cards** | | PC Cards (PCMCIA) [1990] - Compact Flash (CF-I/CF-II) [1994] - SmartMedia (SM/SMC) [1995]| Multimedia Card (MMC) [1997] | Secure Digital Card (SD) [1999] / USB Drive [2000] |  | MiniSD [2003] | SDXC [2010] |
| **External Media - Drive** |  |  |  | CD-ROM | x32 CD-ROM / DVD-ROM | DVD-ROM (DVD-HD) | Blu-Ray |
| **External Media - USB** | | |  |  | USB 1.1 Flash Drive (2000) / USB Mass Storage (Windows 98SE / Windows 2000)  | USB 2.0 | USB 3.0 |
| **Motherboard - Expansion slots** | ISA | ISA / VESA | VESA / PCI | PCI | AGP/ PCI / PCI Express | PCI / PCI Express| PCI / PCI Express |
| **Motherboard - Ports** | PS/2, Serial (DB-25), Parallel, 15 pin game port | PS/2, Serial (RS232), Parallel, 15 pin game port | PS/2, Serial (RS232), Parallel, 15 pin game port | PS/2, USB 1.1 (W98SE/W2000) | PS/2, USB 1.1, USB 2.0 | PS/2, USB 1.1, USB 2.0 | PS/2, USB 1.1, USB 2.0, USB 3.0 |
| **Graphics card - Examples and frameworks** | ATI Small Wonder series ([ATI VGA Wonder XL24](https://www.techpowerup.com/gpu-specs/vga-wonder-xl24.c2039)), S3 911 (1 MB, 16 bit) [1991], OpenGL 1.0 [1992] | 1-8 MB cards, Direct3D, [Nvidia NV1 (4 MB)](https://www.techpowerup.com/gpu-specs/nv1.c2015) [1995]  | DirectX 1.0 [1995], [3dfx Voodoo](https://www.techpowerup.com/gpu-specs/voodoo-graphics-4-mb.c3570) [1996], [ATI 3D Rage](https://www.techpowerup.com/gpu-specs/3d-rage.c3166) [1996], [ATI 3D Rage II](https://www.techpowerup.com/gpu-specs/3d-rage-ii.c873) [1996], Nvidia RIVA 128 [1997], 3dfx Voodoo 2 [1998], [S3 Savage 3D](https://en.wikipedia.org/wiki/S3_Savage) [1998]|  Nvidia Geforce 256 (64 MB SDR ou DDR) [1999] - Nvidia GeForce2 [2000] - First GPU, [S3 Savage 4](https://en.wikipedia.org/wiki/S3_Savage) [1999] | [ATI Radeon 7000](https://www.techpowerup.com/gpu-specs/radeon-7000.c648) [2001], [Intel i830M Graphics](https://www.techpowerup.com/gpu-specs/i830m-graphics.c1910) [2001], [NVIDIA GeForce2 MX 200](https://www.techpowerup.com/gpu-specs/geforce2-mx-200.c788) | Nvidia GeForce FX series [2003] (DDR2, GDDR2 and GDDR3, Direct3D9) - [NVIDIA GeForce FX 5800](https://www.techpowerup.com/gpu-specs/geforce-fx-5800.c703)| Nvidia Geforce GT440 [2011] |
| **Sound card** | | | Creative Soundblaster | AC97 (standard) | | | |
| **Screen - Typical** | 256 colors 14" VGA (640x480) |  | 15" SVGA (800x600) - 16 bits colors | 15" SVGA (800x600) - 32 bits colors | 15" SVGA (800x600) - 32 bits colors | 17" XGA (1024×768) | 19" SXGA (1280x1024) |
| **Drivers** | | VDD [VXD](https://en.wikipedia.org/wiki/VxD) (Windows 3.1) or [Windows NT Driver Model](https://en.wikipedia.org/wiki/Windows_NT#Major_features)| VDD VXD (Windows 95) or [Windows NT Driver Model](https://en.wikipedia.org/wiki/Windows_NT#Major_features) | [WDM](https://en.wikipedia.org/wiki/Windows_Driver_Model) (Windows 98) + [Windows Driver Frameworks](https://en.wikipedia.org/wiki/Windows_Driver_Frameworks) (WDF) | WDM + WDF  | WDM + WDF | WDM + WDF |
| **Power Format** | AT | AT | ATX | ATX | ATX | ATX | ATX |
| **Microsoft Windows - Version last release** | | Windows 3.1.1 | Windows 95 OEM SP 5 | Windows 98 SE / Windows 2000 (SP4) | Window XP SP 4 (unofficial SP5) | Windows XP SP 4 (unofficial SP5) | Win 7 SP 3 |

## CPU architecture OS support
**[`^        back to top        ^`](#)**

### Intel 286:
- IBM PC DOS
- OS/2 1.X
  
[Wikipedia page on 286](https://en.wikipedia.org/wiki/Intel_80286)

### Intel 386: 
- Microsoft Windows, until Windows 95
- Debian (GNU/Linux), until 3.1 (2005)
- *"Among the BSDs, FreeBSD's 5.x releases were the last to support the 386; support for the 386SX was cut with release 5.2, while the remaining 386 support was removed with the 6.0 release in 2005. OpenBSD removed 386 support with version 4.2 (2007), DragonFly BSD with release 1.12 (2008), and NetBSD with the 5.0 release (2009)."* [Wikipedia - i386](https://en.wikipedia.org/wiki/I386) - [FreeBSD 5.x release notes](https://www.freebsd.org/releases/5.0R/relnotes-i386/)

### Intel 486:

*"The AMD Am5x86 and Cyrix Cx5x86 were the last i486 processors often used in late-generation i486 motherboards. They came with PCI slots and 72-pin SIMMs that were designed to run Windows 95, and also used for 80486 motherboards upgrades. While the Cyrix Cx5x86 faded when the Cyrix 6x86 took over, the AMD Am5x86 remained important given AMD K5 delays."*

*"Computers based on the i486 remained popular through the late 1990s, serving as low-end processors for entry-level PCs. Production for traditional desktop and laptop systems ceased in 1998, when Intel introduced the Celeron brand, though it continued to be produced for embedded systems through the late 2000s."*

*"In the general-purpose desktop computer role, i486-based machines remained in use into the early 2000s, especially as Windows 95 through 98 and Windows NT 4.0 were the last Microsoft operating systems to officially support i486-based systems. Windows 2000 could run on a i486-based machine, although with a less than optimal performance, due to the minimum hardware requirement of a Pentium processor"*

*"Linux 6 will likely be the last Linux kernel to support i486."*

[Wikipedia page on i486](https://en.wikipedia.org/wiki/I486)

## Some useful sources
**[`^        back to top        ^`](#)**
### DOS - Typical PC per year
- [DOS Days - Typical pc per year](https://www.dosdays.co.uk/topics/typical_pc_per_year.php)

### Monitors
- [CRT monitors](https://www.dosdays.co.uk/topics/monitors.php)

### Ports
- [Computer ports and their functions](https://recompute.co.zw/buying-guides/a-complete-guide-of-every-type-of-computer-port/)

### Floppy disk history
- 8" floppy: IBM 1971
- 5"1/4 : 1976
- 3": Manufactured during the 80s by several companies. Commonly used on Amstrad CPC.
- 3"1/2 : 1982 until the end of the 90s. Machinstosh 128K made it the de-facto standard
- Others : Non standard flopy disks (CP/M, Apple, Commodore, etc)
- Alternative : Magnetic tape readers (business/enterprise oriented) : [9 track tape](https://en.wikipedia.org/wiki/9-track_tape), QIC, DAT
- [Wikipedia - History of the floppy disk](https://en.wikipedia.org/wiki/History_of_the_floppy_disk)
- [Wikipedia - Floppy disk variants](https://en.wikipedia.org/wiki/Floppy_disk_variants)

### Memory Cards and USB Flash Drive / Mass storage
- [History and Evolution of Memory Cards](https://koofr.eu/blog/posts/history-and-evolution-of-memory-cards)
- [USB Flash Drive](https://en.wikipedia.org/wiki/USB_flash_drive)
- [USB mass storage device class](https://en.wikipedia.org/wiki/USB_mass_storage_device_class)

### Graphics GPU
- [Graphics](https://www.dosdays.co.uk/topics/graphics.php)
- [Nvidia GPU history](https://www.pocket-lint.com/nvidia-gpu-history/)
- [GPU consumer 3D graphics (1976-1995)](https://www.diskmfr.com/1-history-of-gpu-the-consumer-3d-graphics-cards-1976-1995/)
- [ATI Rage series](https://en.wikipedia.org/wiki/ATI_Rage_series)
- [3DFX (French)](https://www.tomshardware.fr/3dfx-de-la-voodoo-au-rampage-en-images/)
- [S3 Graphics](https://en.wikipedia.org/wiki/S3_Graphics)

