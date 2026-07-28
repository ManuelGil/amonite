# Installation Guide

<!--
SPDX-FileCopyrightText: 2026 Manuel Gil
SPDX-License-Identifier: GPL-3.0-or-later
-->

## Installing Amonite

This guide explains how to install the Amonite GNU/Linux distribution.

> **Note**
>
> This guide applies to all official Amonite editions unless stated otherwise.

## Requirements

Before you begin, ensure that you have:

- A 64-bit x86 (amd64) computer.
- At least 4 GB of RAM.
- At least 20 GB of available storage.
- A USB flash drive with sufficient capacity for the installation image.

Installing an operating system may modify or erase existing data.

Always back up important files before proceeding.

## Creating the Installation Media

Write the downloaded installation image to a USB flash drive using an image
writing tool.

> **Warning**
>
> Writing the installation image erases all existing data on the USB flash
> drive.

## Booting the Installer

Insert the USB flash drive and boot the computer from the installation media.

Depending on your hardware, you may need to select the USB device from the
firmware boot menu.

If your hardware requires additional firmware configuration, consult the
manufacturer's documentation before proceeding.

Once the live environment has started, launch the installer if it does not
start automatically.

## Installation Process

The installer guides you through the installation process.

Typical steps include:

1. Selecting the installation language.
2. Choosing the keyboard layout.
3. Selecting the installation location.
4. Configuring storage and partitions.
5. Creating the user account.
6. Reviewing the installation summary.
7. Installing the operating system.

The exact sequence may vary slightly between releases while preserving the
overall installation workflow.

## Partitioning

Amonite supports both automatic and manual partitioning.

### Automatic Partitioning

Automatic partitioning is recommended for most users.

The installer creates the required partitions automatically.

### Manual Partitioning

Advanced users may manually configure storage according to their
requirements.

You can preserve existing GNU/Linux installations and dual-boot configurations,
and use custom storage layouts, when they are configured correctly.

## Installation

After confirming the installation summary, the installer copies the operating
system to the selected storage device.

Depending on your hardware, this process may take several minutes.

Do not interrupt the installation once it has started.

## First Boot

When the installation completes:

1. Restart the computer.
2. Remove the installation media if requested.
3. Boot into the installed system.
4. Sign in using the user account created during installation.

Depending on the selected edition, Amonite may present a Welcome application
during the first login.

## Troubleshooting

If the installer cannot start or the installation fails:

- recreate the installation media;
- confirm that the target hardware satisfies the minimum requirements;
- review the changelog for release-specific information.

If the problem persists, report it through the project's official issue
tracker.

## Supported Platforms

Amonite currently supports modern 64-bit x86 (amd64) systems.

## Editions

All official Amonite editions follow the same installation workflow.

Differences between editions affect the installed software and capabilities
rather than the installation process itself.

## Related Documentation

The following documents complement this guide:

- `VERIFY.md` — Verify downloaded installation images.
- `FIRST_STEPS.md` — Getting started after installation.
- [`CHANGELOG.md`](CHANGELOG.md) — Public release history.
