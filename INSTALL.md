# Installation Guide

<!--
SPDX-FileCopyrightText: 2026 Manuel Gil
SPDX-License-Identifier: GPL-3.0-or-later
-->

How to install a published Amonite Alpha release.

> **Release family:** Nautilus (Amonite 1.x).
> **Published editions:** Standard (Alpha 2) and Lite (Alpha).
> **Mobile:** Experimental - no public installation path.

Alpha releases are for evaluation and testing, not production use.

## Download

Choose an edition - see [EDITIONS.md](EDITIONS.md) - and download its image from [GitHub Releases](https://github.com/ManuelGil/amonite/releases) or [amonite.org/downloads](https://amonite.org/downloads/).

| Edition  | Version         | Image                                                                                                                                                |
| -------- | --------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| Standard | `1.0.0-alpha.2` | [`amonite-1.0.0-alpha.2-amd64.iso`](https://github.com/ManuelGil/amonite/releases/download/v1.0.0-alpha.2/amonite-1.0.0-alpha.2-amd64.iso)            |
| Lite     | `1.0.0-alpha`   | [`amonite-lite-1.0.0-alpha-amd64.iso`](https://github.com/ManuelGil/amonite/releases/download/lite%2Fv1.0.0-alpha/amonite-lite-1.0.0-alpha-amd64.iso) |

Download the matching `.iso.asc`, `SHA256SUMS`, and `SHA256SUMS.asc` from the same release, then verify the image before writing any media - [VERIFY.md](VERIFY.md).

Do not install an image that fails verification.

## Requirements

Official images are published for 64-bit x86 (`amd64`) only and boot under both BIOS and UEFI firmware. You need a computer that can boot from USB, a USB flash drive large enough for the installation image, and enough free storage for a Debian-based desktop system.

Installing an operating system may modify or erase existing data. Back up important files before you start.

### Validated configuration

The Standard Alpha 2 release was validated on the configuration below. It is a practical reference, not a statement of minimum or recommended production requirements.

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

For comfortable desktop use, allow more RAM and storage than the validated reference.

## Creating the installation media

Write the verified ISO to a USB flash drive with any tool that writes raw disk images - `dd`, balenaEtcher, and similar utilities.

> **Warning**
>
> Writing the installation image erases all existing data on the USB flash drive.

Example using `dd`, replacing the device path with your USB device:

```bash
sudo dd if=amonite-1.0.0-alpha.2-amd64.iso of=/dev/sdX bs=4M status=progress oflag=sync
```

Identify the correct device before running the command. Writing to the wrong device destroys data.

## Booting the live environment

Insert the USB flash drive and boot the computer from it, selecting the USB device from the firmware boot menu if the machine does not do so on its own. When firmware settings need adjustment - boot order, Secure Boot policy, legacy or UEFI mode - consult the hardware manufacturer's documentation.

The live session runs from the USB drive and leaves installed disks untouched until you confirm partitioning, so you can evaluate Amonite before committing to it. Launch the installer when you are ready, if it has not started automatically.

## Installation process

Typical steps:

1. Selecting the installation language.
2. Choosing the keyboard layout.
3. Selecting the installation location.
4. Configuring storage and partitions.
5. Creating the user account.
6. Reviewing the installation summary.
7. Installing the operating system.

The exact sequence may vary slightly between releases while preserving the overall workflow.

## Partitioning

Amonite supports automatic and manual partitioning. Automatic partitioning suits most users: the installer creates the required partitions for you.

Advanced users can configure storage manually, preserving existing GNU/Linux installations, dual-boot configurations, and custom storage layouts when they are configured correctly.

Encrypted layouts are available through the graphical installer. Encryption is an installer option, not a separate project-specific workflow.

## Completing installation

Once you confirm the installation summary, the installer copies the operating system to the selected storage device. Depending on the hardware this takes several minutes. Do not interrupt it.

When installation finishes, restart the computer, remove the installation media when prompted, and sign in with the account you created. Depending on the edition, Amonite may present the Welcome application during the first login.

Continue with [FIRST_STEPS.md](FIRST_STEPS.md).

## Troubleshooting

If the installer cannot start or installation fails:

- recreate the installation media from a freshly verified ISO;
- confirm that the target hardware is `amd64` and can boot the live image;
- try both UEFI and BIOS boot modes if your firmware supports them;
- review [CHANGELOG.md](CHANGELOG.md) and the release notes for release-specific information.

If the problem persists, share the details in [r/Amonite](https://www.reddit.com/r/amonite/).

## Related documentation

- [VERIFY.md](VERIFY.md) - Verifying downloaded installation images
- [EDITIONS.md](EDITIONS.md) - Edition identity and maturity
- [FIRST_STEPS.md](FIRST_STEPS.md) - Getting started after installation
- [CHANGELOG.md](CHANGELOG.md) - Public release history
- [BRANDING.md](BRANDING.md) - Nautilus release family
