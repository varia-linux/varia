# Contributing to Varia Linux

We welcome contributions to Varia Linux! Whether you're fixing a bug, adding a new feature, or improving documentation, your help is appreciated.

## How to Contribute

There are several ways to contribute to the project:

*   **Reporting Issues:** If you find a bug or have a problem, please open an issue on our issue tracker.
*   **Suggesting Enhancements:** Have an idea for a new feature or a change to an existing one? We'd love to hear it.
*   **Pull Requests:** If you want to make changes to the code or configuration yourself, please submit a pull request.

## Development Workflow

The core of this project is the `archiso` configuration used to build the live ISO.

### Modifying Packages

To add or remove packages from the live environment, edit the `packages.x86_64` file. Simply add or remove package names from this list. Please ensure that any added packages are available in the Arch Linux repositories.

### Customizing the Live System

To change the configuration of the live system, you can modify the files within the `airootfs/` directory. This directory is an overlay that gets applied to the root filesystem of the live ISO. For example:

*   To change default shell configurations, edit files in `airootfs/etc/skel/`.
*   To add or modify systemd services, look inside `airootfs/etc/systemd/system/`.
*   To change the default LightDM or Budgie settings, you would add the appropriate configuration files in the corresponding `airootfs/etc/` locations.

### Building and Testing

After making your changes, it is crucial to build the ISO and test it to ensure it works as expected. You can build the ISO using the `mkarchiso` command as described in the `README.md`.

Test the resulting ISO in a virtual machine (like QEMU/KVM or VirtualBox) or by writing it to a spare USB drive.

### Submitting Changes

1.  Fork the repository.
2.  Create a new branch for your changes.
3.  Make your changes and commit them with a clear and descriptive message.
4.  Push your branch to your fork.
5.  Open a pull request from your branch to the main repository.

Thank you for contributing to Varia Linux!
