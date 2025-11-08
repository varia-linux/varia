# Welcome to Varia

Varia Linux is a custom Arch Linux-based distribution, designed for daily use. This configuration is based on the official `releng` profile from Arch Linux, customized for the author's personal use. It provides a complete Budgie desktop environment.

## Features

*   **Desktop Environment:** Budgie Desktop
*   **Display Manager:** LightDM with a slick greeter
*   **File Manager:** Nemo
*   **System Tools:** Although intended for daily use, it includes some system administration and recovery tools like `clonezilla`, `gpart`, `testdisk`, and `ddrescue`.
*   **Boot:** Supports both legacy BIOS (via Syslinux) and modern UEFI (via systemd-boot) systems.

## Building the ISO

To build the Varia Linux ISO, you need to have the `archiso` package installed on an Arch Linux system.

1.  **Install `archiso`:**
    ```bash
    sudo pacman -S archiso
    ```

2.  **Clone the repository:**
    ```bash
    git clone <repository-url>
    cd releng
    ```

3.  **Build the ISO:**
    Run the `mkarchiso` command from within the `releng` directory.
    ```bash
    sudo mkarchiso -v -w /tmp/varia-work -o /tmp/varia-out .
    ```
    *   `-v`: Verbose output.
    *   `-w`: Sets the working directory.
    *   `-o`: Sets the output directory where the ISO file will be created.

The final ISO image will be located in the directory specified by the `-o` flag (e.g., `/tmp/varia-out`).

## How to Use

Once the ISO is built, you can write it to a USB drive or burn it to a DVD. Boot your computer from the created media to start the Varia Linux live environment.
