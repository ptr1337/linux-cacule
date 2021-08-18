<h1><center>Linux Kernel With CacULE Scheduler, Several Other Patches & Improvements</center></h1>

### General Informations

The CacULE CPU Scheduler is a improved alternative to CFS Patchset which is based on interactivity score mechanism. The interactivity score is inspired by the ULE Scheduler (FreeBSD Scheduler). The goal of this scheduler is to enhance system performance, responsiveness and latency.

### Features

-   At the time of compiling you can set several features which you want to use
-   GCC/CLANG Optimization with Auto CPU Optmization
-   Choose between 500Hz, 1000Hz (default), 2000Hz
-   Improved BFQ Scheduler
-   Latest LRU Patchset
-   BBRv2 tcp_congestion_control
-   LLVM FULL LTO provided with \*-llvm Kernel
-   LRNG Framework (default)
-   FUTEX, WINESYNC & FUTEX2 patchset
-   Android ANBOX patchset
-   Latest Paragon NTFS3 driver support
-   Latest & improved ZSTD patchset
-   Latest BTRFS improvements & fixes
-   Protection of clean file pages (page cache) may be used to prevent thrashing, reducing I/O under memory pressure, avoid high latency and prevent livelock in near OOM (Out Of Memory) conditions

### CacULE Tips & Tricks (Sysctl Values)

You can tune the scheduler by setting these sysctl values

    net.core.netdev_max_backlog = 16384
    net.core.somaxconn = 8192
    net.core.rmem_default = 1048576
    net.core.rmem_max = 16777216
    net.core.wmem_default = 1048576
    net.core.wmem_max = 16777216
    net.core.optmem_max = 65536
    net.ipv4.tcp_rmem = 4096 1048576 2097152
    net.ipv4.tcp_wmem = 4096 65536 16777216
    net.ipv4.udp_rmem_min = 8192
    net.ipv4.udp_wmem_min = 8192
    net.ipv4.tcp_fastopen = 3
    net.ipv4.tcp_keepalive_time = 60
    net.ipv4.tcp_keepalive_intvl = 10
    net.ipv4.tcp_keepalive_probes = 6
    net.ipv4.conf.default.log_martians = 1
    net.ipv4.conf.all.log_martians = 1
    net.ipv4.tcp_mtu_probing = 1
    net.ipv4.tcp_syncookies = 1
    net.core.default_qdisc = cake
    net.ipv4.tcp_congestion_control = bbr2

### Prebuilt Kernel Server

We are providing a [repo](https://build.cachyos.org/?dir=repo) which includes all kernels in generic-v3 and generic and more optimized packages

### How to add our Repo automaticly with cpu detection (if x86-64-v3 is supported):

Just run following command:

      wget https://build.cachyos.org/cachyos-repo.tar.xz
      tar xvf cachyos-repo.tar.xz
      cd repo
      sudo ./cachyos-repo.sh

This script will also backup your old pacman.conf.

More informations you will find here [CachyOS](https://gitlab.com/cachyos) or [Discord](https://discord.gg/k39qfrxPNa)

### More Informations for the CacULE Scheduler

Here you find more informatiom from the [repo](https://github.com/hamadmarri/cacule-cpu-scheduler) of the creator

### Valueable Contributors

[Hamad Marri](https://github.com/hamadmarri) for the CacULE Scheduler

[BL4CKH47H4CK3R](https://github.com/BL4CKH47H4CK3R) for Optimization, Bug Hunting & Support

[SirLucjan (Piotr Gorski)](https://github.com/sirlucjan) for many cool patches

[Archlinux](https://archlinux.org) for the great linux operating system

[GarudaLinux](https://garudalinux.org) for suggestions and supports

[And all other Kernel Developers and Supporters](https://github.com/torvalds/linux)
