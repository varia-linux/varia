# Project Overview

This project is a profile for `archiso` to build **Varia Linux**, a customized Arch Linux distribution.

It is intended for daily use, not for rescue purposes. It's essentially a collection of `archiso` profiles for Arch Linux, customized for the author's own use.

The build process is based on `archiso`.

## Key Configuration Files

*   `profiledef.sh`: The main `archiso` profile configuration. It defines the ISO name (`varialinux`), publisher, boot modes, and other build parameters.
*   `packages.x86_64`: This file lists all the packages to be included in the live ISO. This includes a full desktop environment and various system rescue tools.
*   `pacman.conf`: The configuration for the `pacman` package manager. It includes the standard Arch Linux repositories (`core`, `extra`, `multilib`) and a local custom repository located at `/home/custompkgs`.
*   `airootfs/`: This directory contains the root filesystem overlay for the live environment. Customizations, such as default user configurations and systemd services, are placed here.

## Building the ISO

To build the ISO, you would typically use the `mkarchiso` command from the `archiso` package.

A likely command to build the ISO would be:

```bash
# TODO: Verify the exact build command
mkarchiso -v -w /tmp/archiso-work -o /tmp/out .
```

## Development Conventions

*   The project uses `syslinux` for legacy BIOS booting and `systemd-boot` for UEFI booting.
*   Although the primary focus is daily use, some system administration and recovery tools like `clonezilla`, `gpart`, and `testdisk` are included.
*   The default desktop environment is Budgie, with `lightdm` as the display manager.
*   There is a custom local package repository used during the build.
