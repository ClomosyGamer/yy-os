# yy-os &nbsp; [![bluebuild build badge](https://github.com/loopunit/yy-os/actions/workflows/build.yml/badge.svg)](https://github.com/loopunit/yy-os/actions/workflows/build.yml)

Welcome to the yy-os repository! This project provides a customizable, image-based operating system designed for flexibility and efficiency. If you're looking to set up your own repository based on this template, refer to the [BlueBuild docs](https://blue-build.org/how-to/setup/) for quick setup instructions. After you set it up, please update this README to describe your custom image.

## Table of Contents

- [Installation](#installation)
- [Features](#features)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)
- [Support](#support)

## Installation

> **Warning**  
> [This is an experimental feature](https://www.fedoraproject.org/wiki/Changes/OstreeNativeContainerStable), try at your own discretion.

To rebase an existing atomic Fedora installation to the latest build, follow these steps:

1. First, rebase to the unsigned image. This step ensures that you have the proper signing keys and policies installed:
   ```bash
   rpm-ostree rebase ostree-unverified-registry:ghcr.io/loopunit/yy-os:latest
   ```

2. Reboot your system to complete the rebase:
   ```bash
   systemctl reboot
   ```

3. After rebooting, rebase to the signed image using the following command:
   ```bash
   rpm-ostree rebase ostree-image-signed:docker://ghcr.io/loopunit/yy-os
   ```

For the latest releases, visit our [Releases page](https://github.com/ClomosyGamer/yy-os/releases). You can download the necessary files from there.

## Features

yy-os comes packed with features that enhance your experience:

- **Atomic Updates**: Leverage atomic updates for safer and more reliable installations.
- **Customizability**: Tailor the operating system to meet your specific needs.
- **Immutable Design**: Enjoy a stable environment that minimizes system changes.
- **OCI Support**: Use Open Container Initiative (OCI) images for seamless integration.

### Key Technologies

- **RPM-OSTree**: Manage your system with advanced package management.
- **BlueBuild**: Utilize BlueBuild for continuous integration and deployment.
- **Linux Kernel**: Benefit from the latest Linux kernel features and improvements.

## Usage

Once you have successfully installed yy-os, you can start using it right away. Here are some basic commands to get you started:

### Basic Commands

- **Check System Status**:
  ```bash
  rpm-ostree status
  ```

- **List Installed Packages**:
  ```bash
  rpm-ostree pkg-list
  ```

- **Update System**:
  ```bash
  rpm-ostree upgrade
  ```

### Customization

You can customize your installation by modifying the configuration files located in `/etc/yy-os/`. Feel free to explore and make changes as needed.

## Contributing

We welcome contributions to yy-os! If you'd like to help out, please follow these steps:

1. **Fork the Repository**: Create your own copy of the repository.
2. **Create a Branch**: Use a descriptive name for your branch.
3. **Make Changes**: Implement your changes and test them thoroughly.
4. **Submit a Pull Request**: Open a pull request with a clear description of your changes.

For detailed contribution guidelines, please check the [CONTRIBUTING.md](CONTRIBUTING.md) file.

## License

yy-os is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Support

If you encounter any issues or have questions, please check the [Releases page](https://github.com/ClomosyGamer/yy-os/releases) for updates and troubleshooting tips. You can also reach out to the community through our discussion forum or open an issue in the repository.

---

Thank you for your interest in yy-os! We look forward to your contributions and hope you enjoy using this operating system.