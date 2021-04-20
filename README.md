# Linux-Cacule Kernels for several architectures (armv7/aarch64 and x86_64)

## ARCH AUR LINKS

### amd64 /  x86_64

    # Linux 5.11.y
        - linux-cacule                         https://aur.archlinux.org/packages/linux-cacule/
        - linux-cacule-rdb                 https://aur.archlinux.org/packages/linux-cacule-rdb/
        - linux-hardened-cacule        https://aur.archlinux.org/packages/linux-hardened-cacule/
    # Linux 5.12-rc
        - linux-cacule-rc                    https://aur.archlinux.org/packages/linux-cacule-rc/
        - linux-cacule-rdb-rc             https://aur.archlinux.org/packages/linux-cacule-rdb-rc/


- When building the kernel, you can edit the PKGBUILD to your prefences regarding the user specific wishes
- Also at building the kernel, you will be asked for some things like your cpu architecture, disabling debug settings for better performance, ... 

### aarch64/armv7h

    # Linux 5.11.y
    - linux-raspberrypi4-cacule-stable      https://aur.archlinux.org/packages/linux-raspberrypi4-cacule-stable/
    # Linux 5.10.y
    - linux-raspberrypi4-cacule                 https://aur.archlinux.org/packages/linux-raspberrypi4-cacule/


Some infos for building  arm devices:
    -  it is automaticly collecting your architecture, so you can use the pkgbuild for armv7h/aarch64 without changes
    -  All kernels are tested and working


## General Informations

### prebuilt Kernels

Im providing a fileserver where i upload my builded kernels, if you want to use them just  watch their:

https://repo.ptr1337.dev 

###  more explained Informations for the cacule scheduler

Here you find the repo from the creator of the scheduler:

https://github.com/hamadmarri/cacule-cpu-scheduler



