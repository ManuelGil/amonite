# First Steps

<!--
SPDX-FileCopyrightText: 2026 Manuel Gil
SPDX-License-Identifier: GPL-3.0-or-later
-->

What to do after installing a published Amonite Alpha edition, Standard or Lite.

Public editions are alpha within the Nautilus (1.x) release family. Expect ongoing polish, and report friction early. If installation is not finished yet, see [INSTALL.md](INSTALL.md).

## Welcome

Depending on the edition, Amonite may present a Welcome application during the first login.

The Welcome handbook is an introduction, not a control panel. It explains what Amonite is, who it is for, and why the default system stays minimal, and it links to the documentation and to common first tasks. Use it to orient yourself, then explore the desktop.

The default experience may also include a **Your System** view that reports the installation in plain terms - distribution and edition, Debian version, desktop and session, kernel, hardware summary. It is a practical status view of what is actually running.

## Updating the system

Install the latest available updates after the first login. This needs a network connection. Amonite uses the standard Debian package management system.

```bash
sudo apt update
sudo apt upgrade
```

Keeping the system up to date improves stability, compatibility, and security.

## Installing software

```bash
sudo apt install package-name
```

Prefer trusted repositories. Unofficial sources increase maintenance and security risk, so consult the Debian and Amonite documentation before enabling additional software sources.

## Local artificial intelligence

Published Alpha editions include local AI inference as a deliberate product capability. Models run offline under your control, and local applications can use an API-compatible interface without depending on external inference services.

See [CAPABILITIES.md](CAPABILITIES.md).

## Making it yours

Defaults are intentional starting points, not permanent constraints. After installation you may want to configure printers and other peripherals, connect online accounts, customize the desktop, set up backups, enable additional accessibility features, or replace any default component that does not fit your workflow. Available options vary by edition.

## Security recommendations

- Install software updates regularly.
- Install software only from trusted sources.
- Verify downloaded release images - [VERIFY.md](VERIFY.md).
- Keep regular backups of important data.
- Prefer encrypted installation when the machine stores sensitive data.

## Help

[r/Amonite](https://www.reddit.com/r/amonite/) is the place for questions, bug reports, and discussion. [CHANGELOG.md](CHANGELOG.md) and the GitHub release notes cover release-specific behaviour, and [amonite.org](https://amonite.org/) hosts the product pages and gallery.

When reporting a problem, include the edition, version, hardware or virtualization platform, and the step that failed.

## Related documentation

- [INSTALL.md](INSTALL.md) - Installing Amonite
- [VERIFY.md](VERIFY.md) - Verifying downloaded installation images
- [EDITIONS.md](EDITIONS.md) - Edition identity and maturity
- [CAPABILITIES.md](CAPABILITIES.md) - Product-defining capabilities
- [BRANDING.md](BRANDING.md) - Nautilus release family
- [CHANGELOG.md](CHANGELOG.md) - Public release history
