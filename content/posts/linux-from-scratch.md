+++
date = '2025-08-24T20:54:01+05:30'
draft = false
title = 'Linux From Scratch'
+++
## Introduction
- New partition
  - Root partition: /root
  - Swap partition: 2xRAM capacity
  - Grub BIOS: GUID partition table (GPT), IMB
  - /boot: kernel + booting info
- New file system: ext4 etc
- Consists of labels, directory blocks, data blocks, indexing
- Mount new partition: Mount the file system embedded in partition
- Create basic directory layout: /etc, /var, /bin, /lib, /sbin, /lib64, /tools, /usr, /usr/bin, /usr/lib, /usr/sbin
- Cross-compilation: Build compiler for different machine
  - Build: Machine where we build programs
  - Host: Machine where built programs will run
  - Target: Machine that compiler produces code for
- Binutils: Contains linker, assembler, etc for handling object files
- GCC : GNU compiler collection. C and C++ compilers
- API headers: Expose kernel’s API for use by Glibc
- Glibc: Main C library which provides basic routines for allocating memory, searching directories, opening and closing files, pattern matching, arithmetic etc.
- libstdc++: Standard C++ library. Needed to compile the part of GCC which is written in C++
- M4: Macro processor
- Ncurses: Library for terminal independent character screens
- Bash: Bourne-again shell
- Coreutils: Basic utility programs needed by every OS
- Diffutils: Programs which show differences between files/ directories.
- File: Determine type of a given file(s)
- Findutils: programs to find files
- Gawk: Programs for manipulating text files
- Grep: Programs for searching through contents of files
- Gzip: Programs for compressing/ decompressing files
- Make: Program for controlling the generation of executables and other files of a package from source files
- Patch: Program for modify/ create files by applying a patch file typically created by diff program
- Sed: Stream editor
- Tar: To create tar archives and other archive manipulation
- xz: Compress/ decompress files. lzma, xz schemes.
- Binutils pass2:
- GCC Pass2:
- Prepare virtual kernel file systems: /dev, /proc, /sys, /run
- Mounting and populating /dev: In case of normal boot, kernel automatically mounts devtmpfs file system on /dev. Bind mount host system’s /dev directory
- Entering chroot environment
- Create root level directories: /boot, /home, /mnt, /opt, /srv
- Create essential files and symlinks
  - Mounted file systems : /etc/mtab —----> /proc
  - Create /etc/hosts
  - Root entries in /etc/passwd, /etc/group
- Gettext: Utilities for internationalisation and localisation
- Bison: Parser generator
- Perl: Practical extraction and report language
- Python3:
- Texinfo: Read, write, convert info pages
- Util-linux: Miscellaneous utility programs
- Installing basic system softwares:
  - Package manager
  - Man pages
  - Iana-etc: /etc/protocols, /etc/services...
- System V boot process
  - init program sets up basic processes such as login (via getty) and runs a script. The script named rc executes additional scripts to initialize. Init program controlled by /etc/inittab file.
- Run levels
  - 0 - Halt
  - 1 - Single user
  - 2 - User definable or 3
  - 3 - Full multiuser (network)
  - 4 - User definable or 3
  - 5 - Full multiuser (display)
  - 6 - Reboot
- lfsbootscripts: /etc/rc.d, /etc/init.d, /etc/sysconfig, /lib/services, /lib/lsb

## Device handling
- Traditionally static device creation method was used. Many device nodes were created in /dev where actual device connected or not
- udev method: Device nodes created only for those devices which are detected by kernel. Stored in /devtmpfs
- devfs: Had issues with naming conventions and race conditions
- sysfs: Provide information about system’s hardware configuration to userspace processes
- Device node creation
  - Drivers compiled in kernel register objects in sysfs(devtmpfs)
  - sysfs filesystem is mounted on /sys
  - Device files are created by kernel in devtmpfs file system.
  - Kernel sents uevent to udevd
- Network devices
  - Old: eth0, eth1
  - New: enp5s0, wlp3s0
- General network configuration:
  - /etc/sysconfig/: which interfaces are up and down
  - One file each named ifconfig.xyz —->xyz = network card
  - Create /etc/resolv.conf file
  - Customise /etc/hosts file

## System V bootscript
- During kernel initialisation, first program to run is init
- init reads initialisation files: /etc/inittab
