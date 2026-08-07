# Contributing

<!--
SPDX-FileCopyrightText: 2026 Manuel Gil
SPDX-License-Identifier: GPL-3.0-or-later
-->

Thank you for your interest in Amonite.

Amonite is an independent GNU/Linux distribution designed, built, tested, cryptographically signed, and maintained by Manuel Gil. The most valuable contributions today come from people who install a published Alpha edition, Standard or Lite, use it, and report what works and what does not.

## Evaluate a release

1. Download an official ISO from [GitHub Releases](https://github.com/ManuelGil/amonite/releases).
2. Verify it - [VERIFY.md](VERIFY.md).
3. Install it, or run the live session - [INSTALL.md](INSTALL.md).
4. Share the results in [r/Amonite](https://www.reddit.com/r/amonite/).

A useful report names the edition, version, hardware or virtualization platform, firmware mode (BIOS or UEFI), and the exact step that succeeded or failed.

## Discuss and report issues

Public discussion, questions, feedback, and non-security bug reports belong on [r/Amonite](https://www.reddit.com/r/amonite/), the primary support channel for the published Alpha editions.

Security vulnerabilities are different: do not disclose them publicly while a private channel exists. See [SECURITY](SECURITY) and write to `security@amonite.org`.

## Improve documentation

These documents are the canonical public documentation for Amonite. Start from the documentation map in [README.md](README.md).

Documentation contributions should:

- preserve factual accuracy against repository evidence;
- keep one responsibility per document;
- avoid inventing features, roadmaps, or unsupported claims;
- document each edition according to its actual maturity;
- treat experimental Mobile carefully and avoid unsupported capability claims;
- match the existing terminology and tone;
- update cross-references when adding or renaming pages;
- respect the documentation layers: product, architecture, engineering, implementation.

Every statement must be verifiable from source code, configuration, releases, or official project materials. Document implemented and supported behaviour, and leave speculation out. Keep the tone professional, concise, and neutral. Follow [BRANDING.md](BRANDING.md), use `assets/logo.png` where a logo is needed, and do not invent logos. Documentation and software are licensed GPL-3.0-or-later unless a file states otherwise.

Do not add unverified hardware compatibility lists, fabricated screenshots, unpublished roadmap items, editions that do not exist, capability claims beyond an edition's documented maturity, architecture claims unsupported by the published product model, or security advice that contradicts [SECURITY](SECURITY) or Debian practice without evidence.

## Sponsorship

Sponsorship is optional and helps sustain development, testing, infrastructure, hardware, documentation, and long-term maintenance.

- [GitHub Sponsors](https://github.com/sponsors/ManuelGil)

## Related documentation

- [README.md](README.md) - Project overview and documentation map
- [EDITIONS.md](EDITIONS.md) - Edition identity and maturity
- [BRANDING.md](BRANDING.md) - Naming and Nautilus
- [ARCHITECTURE.md](ARCHITECTURE.md) - Shared architecture
- [SECURITY](SECURITY) - Vulnerability reporting
- [CHANGELOG.md](CHANGELOG.md) - Release history
