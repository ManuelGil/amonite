# Installation Guide

<!--
SPDX-FileCopyrightText: 2026 Manuel Gil
SPDX-License-Identifier: GPL-3.0-or-later
-->

This guide explains how to install a published Amonite Alpha release.

> **Release family:** Nautilus (Amonite 1.x).
> **Published editions:** Standard (Alpha 2) and Lite (Alpha).
> **Mobile:** Experimental - no public installation path.

Alpha releases are for evaluation and testing, not production use.

## Download

1. Choose an edition - see [EDITIONS.md](EDITIONS.md).
2. Download the ISO and verification files from:
   - [GitHub Releases](https://github.com/ManuelGil/amonite/releases)
   - [amonite.org/downloads](https://amonite.org/downloads/)

### Current published images

| Edition  | Version         | Image                                                                                                                                                 |
| -------- | --------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| Standard | `1.0.0-alpha.2` | [`amonite-1.0.0-alpha.2-amd64.iso`](https://github.com/ManuelGil/amonite/releases/download/v1.0.0-alpha.2/amonite-1.0.0-alpha.2-amd64.iso)            |
| Lite     | `1.0.0-alpha`   | [`amonite-lite-1.0.0-alpha-amd64.iso`](https://github.com/ManuelGil/amonite/releases/download/lite%2Fv1.0.0-alpha/amonite-lite-1.0.0-alpha-amd64.iso) |

Also download the matching `.iso.asc`, `SHA256SUMS`, and `SHA256SUMS.asc` files from the same release.

3. Verify the download before writing media - [VERIFY.md](VERIFY.md).

Do not install an image that fails verification.

## Requirements

### Supported platform

| Requirement  | Value                |
| ------------ | -------------------- |
| Architecture | 64-bit x86 (`amd64`) |
| Firmware     | BIOS or UEFI         |
| Installer    | Graphical installer  |

Amonite currently publishes official images only for `amd64`.

### Practical expectations

Installing an operating system may modify or erase existing data. Back up important files before proceeding.

You need:

- a computer that can boot from USB;
- a USB flash drive large enough for the installation image;
- enough free storage for a Debian-based desktop system.

### Validated configuration

This configuration was used to validate the current Standard Alpha 2 release within Nautilus. It is a practical reference, not a statement of minimum or recommended production requirements.

| Item                  | Validated value       |
| --------------------- | --------------------- |
| Architecture          | `amd64`               |
| CPU                   | 1 core                |
| Memory                | 1 GiB RAM             |
| Storage               | 12 GiB                |
| Firmware              | BIOS and UEFI         |
| Virtualization        | QEMU/KVM              |
| Installed system size | Approximately 2.6 GiB |

Validation covered live ISO boot, graphical desktop, Welcome application, graphical installation, first boot, login, terminal, `apt update`, `apt upgrade`, and zero failed systemd services on that configuration.

For comfortable desktop use, prefer more RAM and storage than the validated minimum reference.

## Creating the installation media

Write the verified ISO to a USB flash drive using an image writing tool.

Examples of suitable tools include `dd`, balenaEtcher, and similar utilities that write raw disk images.

> **Warning**
>
> Writing the installation image erases all existing data on the USB flash drive.

Example using `dd` (replace the device path with your USB device):

```bash
sudo dd if=amonite-1.0.0-alpha.2-amd64.iso of=/dev/sdX bs=4M status=progress oflag=sync
```

Identify the correct device before running the command. Writing to the wrong device can destroy data.

## Booting the live environment

1. Insert the USB flash drive.
2. Boot the computer from the installation media.
3. Select the USB device from the firmware boot menu if the machine does not boot from it automatically.

If firmware settings need adjustment (boot order, Secure Boot policy, or legacy/UEFI mode), consult the hardware manufacturer's documentation.

Once the live environment has started, you can evaluate Amonite without changing installed disks. The live session runs from the USB drive until you confirm installation partitioning.

Launch the installer if it does not start automatically.

## Installation process

Typical steps include:

1. Selecting the installation language.
2. Choosing the keyboard layout.
3. Selecting the installation location.
4. Configuring storage and partitions.
5. Creating the user account.
6. Reviewing the installation summary.
7. Installing the operating system.

The exact sequence may vary slightly between releases while preserving the overall workflow.

## Partitioning

Amonite supports automatic and manual partitioning.

### Automatic partitioning

Automatic partitioning is recommended for most users.

The installer creates the required partitions automatically.

### Manual partitioning

Advanced users may configure storage manually.

You can preserve existing GNU/Linux installations, dual-boot configurations, and custom storage layouts when they are configured correctly.

### Encrypted installation

Encrypted layouts are supported through the graphical installer when required.

Encryption is an installer option, not a separate project-specific workflow.

## Completing installation

After confirming the installation summary, the installer copies the operating system to the selected storage device.

Depending on your hardware, this process may take several minutes.

Do not interrupt the installation once it has started.

## First boot

When installation completes:

1. Restart the computer.
2. Remove the installation media when requested.
3. Boot into the installed system.
4. Sign in with the user account created during installation.

Depending on the selected edition, Amonite may present the Welcome application during the first login.

Continue with [FIRST_STEPS.md](FIRST_STEPS.md).

## Troubleshooting

If the installer cannot start or installation fails:

- recreate the installation media from a freshly verified ISO;
- confirm that the target hardware is `amd64` and can boot the live image;
- try both UEFI and BIOS boot modes if your firmware supports them;
- review [CHANGELOG.md](CHANGELOG.md) and the release notes for release-specific information.

If the problem persists, share details in [r/Amonite](https://www.reddit.com/r/amonite/).

## Related documentation

- [VERIFY.md](VERIFY.md) - Verifying downloaded installation images
- [EDITIONS.md](EDITIONS.md) - Edition identity and maturity
- [FIRST_STEPS.md](FIRST_STEPS.md) - Getting started after installation
- [CHANGELOG.md](CHANGELOG.md) - Public release history
- [branding.md](branding.md) - Nautilus release family
