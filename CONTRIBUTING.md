# Contributing

<!--
SPDX-FileCopyrightText: 2026 Manuel Gil
SPDX-License-Identifier: GPL-3.0-or-later
-->

Thank you for your interest in Amonite.

Amonite is an independent GNU/Linux distribution designed, built, tested, cryptographically signed, and maintained by Manuel Gil.

At present, the most valuable contributions come from people who install a published Alpha edition (Standard or Lite), use it, and report what works and what does not.

## Ways to contribute

### Evaluate a release

1. Download an official ISO from [GitHub Releases](https://github.com/ManuelGil/amonite/releases).
2. Verify it - [VERIFY.md](VERIFY.md).
3. Install or run the live session - [INSTALL.md](INSTALL.md).
4. Share results in [r/Amonite](https://www.reddit.com/r/amonite/).

Useful reports include edition, version, hardware or virtualization platform, firmware mode (BIOS/UEFI), and the exact step that succeeded or failed.

### Discuss and report issues

Public discussion, questions, feedback, and non-security bug reports belong on [r/Amonite](https://www.reddit.com/r/amonite/).

That community is the primary support channel for the current published Alpha editions within Nautilus.

### Improve documentation

This repository is the canonical public documentation for Amonite.

Documentation contributions should:

- preserve factual accuracy against repository evidence;
- keep one responsibility per document;
- avoid inventing features, roadmaps, or unsupported claims;
- document each edition according to its actual maturity;
- treat experimental Mobile carefully and avoid unsupported capability claims;
- match the existing terminology and tone;
- update cross-references when adding or renaming pages;
- respect the documentation layers: product, architecture, engineering, implementation.

Start from the documentation map in [README.md](README.md).

### Report security vulnerabilities

Do not disclose security issues publicly when a private channel is available.

See [SECURITY](SECURITY) and contact `security@amonite.org`.

## Repository expectations

| Area              | Expectation                                                                                            |
| ----------------- | ------------------------------------------------------------------------------------------------------ |
| Factual integrity | Statements must be verifiable from source code, configuration, releases, or official project materials |
| Scope             | Document implemented and supported behaviour; omit speculation                                         |
| Style             | Professional, concise, neutral, repository-centric                                                     |
| Branding          | Follow [branding.md](branding.md); use `assets/logo.png` where appropriate; do not invent logos        |
| License           | Project documentation and software are under GPL-3.0-or-later unless a file states otherwise           |

## What not to claim

Do not add:

- unverified hardware compatibility lists;
- fabricated screenshots;
- roadmap items that are not published by the project;
- edition claims that invent editions that do not exist;
- capability claims that exceed an edition's documented maturity;
- architecture claims unsupported by the published product model;
- security advice that contradicts [SECURITY](SECURITY) or Debian practice without evidence.

## Sponsorship

Sponsorship is optional and helps sustain development, testing, infrastructure, hardware, documentation, and long-term maintenance.

- [GitHub Sponsors](https://github.com/sponsors/ManuelGil)

## Related documentation

- [README.md](README.md) - Project overview and documentation map
- [EDITIONS.md](EDITIONS.md) - Edition identity and maturity
- [branding.md](branding.md) - Naming and Nautilus
- [ARCHITECTURE.md](ARCHITECTURE.md) - Shared architecture
- [SECURITY](SECURITY) - Vulnerability reporting
- [CHANGELOG.md](CHANGELOG.md) - Release history
