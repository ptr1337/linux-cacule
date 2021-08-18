# CacULE Scheduler based Kernel with several other patches and improvements

## General Informations

The CacULE CPU scheduler is a CFS patchset that is based on interactivity score mechanism. The interactivity score is inspired by the ULE scheduler (FreeBSD scheduler). The goal of this patch is to enhance system responsiveness/latency.

## Features

-   If compiling yourself you can set several features which you want to use
-   Choose between 2000Hz, 1000Hz (default), 500Hz
-   BBRv2 TCP tcp_congestion_control
-   LLVM FULL LTO provided with \*-llvm Kernel
-   automatic cpu detection and optimizing your kernel for your cpu architecture
-   LRNG Framework (default enabled)
-   FUTEX, WINESYNC and FUTEX2
-   GCC/CLANG CPU optimization
-   ANBOX support
-   latest ZSTD libary
-   BTRFS improvements
-   Protection of clean file pages (page cache) may be used to prevent thrashing, reducing I/O under memory pressure, avoid high latency and prevent livelock in near-OOM conditions
-   LRU Patchset
-   Improved BFQ Scheduler
-   NTFS3 driver

## CacULE Sysctl values

### Tips & Tricks:

You can tune the scheduler with following commands:

           ### Some general Network-Settings ##

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

## prebuilt Kernels

We are providing a repo which includes all kernels in generic v3 and generic and more optimized packages

### How to add the repo

-   I created a script which automaticly detects your cpu, if x86-64-v3 is detected it will add the the optimized repos, which includes Kernels and also KDE/XFCE packages.
-   If x86-64-v3 is not detected it will use the normal generic repo, which includes the Kernels and also little bit optimized KDE/XFCE packages.
-   Whats exactly in the repo you can find at <https://aur.cachyos.org>

### How to run the script:

Just run following command:

      wget https://build.cachyos.org/cachyos-repo.tar.xz
      tar xvf cachyos-repo.tar.xz
      cd repo
      sudo ./cachyos-repo.sh

This will also backup your old config. If you face in any issues you can easily revert it to use your old pacman.conf and run "sudo pacman -Suuy"

More informations you will find here:
[Gitlab](https://gitlab.com/cachyos)

or

at our [Discord](https://discord.gg/k39qfrxPNa)

## more explained Informations for the cacule scheduler

Here you find the repo from the creator of the scheduler:

<https://github.com/hamadmarri/cacule-cpu-scheduler>

# Credits

[Hamad Marri](https://github.com/hamadmarri)

[BL4CKH47H4CK3R](https://github.com/BL4CKH47H4CK3R)

[SirLucjan (Piotr Gorski)](https://github.com/sirlucjan)

Archlinux

GarudaLinux

and all other Kernel Developers
