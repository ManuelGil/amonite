# First Steps

<!--
SPDX-FileCopyrightText: 2026 Manuel Gil
SPDX-License-Identifier: GPL-3.0-or-later
-->

This guide covers the first steps after installing a published Amonite Alpha edition (Standard or Lite).

Current public editions are alpha within the Nautilus (1.x) release family. Expect ongoing polish and report friction early.

## Before you begin

Confirm that:

- installation completed successfully;
- the system boots normally;
- you can sign in with the account created during installation;
- the computer is connected to the network, if available.

If installation is not finished yet, see [INSTALL.md](INSTALL.md).

## Welcome

Depending on the installed edition, Amonite may present a Welcome application during the first login.

The Welcome handbook is an introduction, not a control panel. It provides:

- a short explanation of what Amonite is;
- who it is for;
- why the default system stays minimal;
- quick access to documentation and common first tasks.

Use it to orient yourself, then explore the desktop.

## Your System

The default experience may include a **Your System** view that reports the installation in plain terms, such as:

- distribution and edition;
- Debian version;
- desktop and session;
- kernel;
- hardware summary.

This is a practical status view of what is actually running.

## Updating the system

After the first login, install the latest available updates.

Amonite uses the standard Debian package management system.

```bash
sudo apt update
sudo apt upgrade
```

Keeping the system up to date improves stability, compatibility, and security.

## Installing software

Install additional software with the standard package management tools:

```bash
sudo apt install package-name
```

Refer to Debian and Amonite documentation before enabling additional software sources.

Prefer trusted repositories. Unofficial sources increase maintenance and security risk.

## Desktop orientation

### Standard

Standard is the reference Amonite desktop: a complete general-purpose desktop experience.

### Lite

Lite is a lightweight Amonite desktop: the same product identity with a reduced graphical footprint.

Mobile is experimental and is not covered here as an installable product. See [EDITIONS.md](EDITIONS.md).

## Local artificial intelligence

Published Alpha editions include local AI inference as a deliberate product capability.

Models can run offline under your control. Local applications can use an API-compatible interface without depending on external inference services.

See [CAPABILITIES.md](CAPABILITIES.md).

## Configuration

After installation you may wish to:

- configure printers and other peripherals;
- connect online accounts, if desired;
- customize the desktop environment;
- configure backups;
- enable additional accessibility features;
- replace any default component that does not fit your workflow.

Available options may vary by edition. Defaults are intentional starting points, not permanent constraints.

## Security recommendations

- Install software updates regularly.
- Install software only from trusted software sources.
- Verify downloaded release images whenever possible - [VERIFY.md](VERIFY.md).
- Keep regular backups of important data.
- Prefer encrypted installation when the machine stores sensitive data.

## Help

Useful resources:

- this repository's documentation map in [README.md](README.md);
- [CHANGELOG.md](CHANGELOG.md) and release notes on GitHub;
- [r/Amonite](https://www.reddit.com/r/amonite/) for questions, bug reports, and discussion;
- [amonite.org](https://amonite.org/) for product pages and the gallery.

When reporting a problem, include the edition, version, hardware or virtualization platform, and the step that failed.

## Related documentation

- [INSTALL.md](INSTALL.md) - Installing Amonite
- [VERIFY.md](VERIFY.md) - Verifying downloaded installation images
- [EDITIONS.md](EDITIONS.md) - Edition identity and maturity
- [CAPABILITIES.md](CAPABILITIES.md) - Product-defining capabilities
- [branding.md](branding.md) - Nautilus release family
- [CHANGELOG.md](CHANGELOG.md) - Public release history
