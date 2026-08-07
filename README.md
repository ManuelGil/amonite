# Amonite

<!--
SPDX-FileCopyrightText: 2026 Manuel Gil
SPDX-License-Identifier: GPL-3.0-or-later
-->

<p align="center">
  <img src="assets/logo.png" alt="Amonite logo" width="160">
</p>

<p align="center">
  <strong>A carefully integrated Debian-based GNU/Linux distribution.</strong>
</p>

<p align="center">
  <a href="https://img.shields.io/github/downloads/ManuelGil/amonite/total"><img src="https://img.shields.io/github/downloads/ManuelGil/amonite/total" alt="GitHub Downloads"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-GPL--3.0--or--later-blue.svg" alt="License"></a>
  <a href="https://amonite.org/"><img src="https://img.shields.io/badge/website-amonite.org-0A7A5A.svg" alt="Website"></a>
</p>

Amonite is an independent GNU/Linux operating system built on Debian. It is engineered for what you do after install: desktop work, development, administration, networking, and local artificial intelligence.

Debian provides the platform. Amonite provides a carefully considered set of defaults.

The project is guided by a simple principle:

> **Every default is an intentional decision.**

Software earns its place by enabling work. Transitive convenience is not enough.

## Why Amonite exists

Modern operating systems accumulate software, services, integrations, and automation over time.

Each addition may solve a specific problem. The result is often higher complexity, higher maintenance cost, and systems that become harder to understand, adapt, and maintain.

Amonite asks a different first question:

> **Why should this exist by default?**

Every default should provide a clear capability, justify its existence, and remain useful throughout the system's lifetime.

The goal is not to invent a new kind of Linux. The goal is to let Linux remain Linux, and remain yours.

## Who it is for

Amonite is intended for people who want:

- a coherent day-one desktop without assembling the system by hand;
- a Debian-based platform that remains understandable and replaceable;
- development and administration tools ready from the first session;
- local model inference without depending on external AI services;
- deliberate defaults rather than software accumulation.

## Who should not use it yet

Current public editions are **alpha** within the **Nautilus** (1.x) release family.

They are intended for evaluation and testing.

Do not use current alpha releases as a production operating system if you require:

- a stable, production-supported release;
- guaranteed compatibility across all hardware;
- Mobile as an installable product (it is experimental and has no public ISO).

Pre-release versions may contain bugs, incomplete features, or compatibility issues.

## Core philosophy

Amonite follows three rules for what may ship:

1. **Capability over accretion** - software earns its place by enabling work.
2. **Replaceability** - useful on day one must not become a trap on day thirty.
3. **User ownership** - the person at the keyboard remains in control.

Amonite does not claim to be the fastest system, the most secure system, or an "AI operating system". Local AI is one deliberate capability among others.

## Design principles

Every engineering decision should reinforce one or more of the following principles.

| Principle   | Meaning                                                                                                                                              |
| ----------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| Efficiency  | Include only capabilities that provide lasting value. Temporary installation requirements should not become permanent parts of the installed system. |
| Security    | Build upon Debian's mature security mechanisms before introducing additional software.                                                               |
| Privacy     | Reduce unnecessary exposure while preserving user choice.                                                                                            |
| Lightweight | Prefer the lowest practical cost in dependencies, maintenance, and coupling, not the lowest package count for its own sake.                          |
| Simplicity  | Maintain a coherent system where every decision can be technically justified. Complexity should never become a feature.                              |

## Project goals

- Provide a curated Debian-based desktop that is ready for real work on day one.
- Keep engineering decisions few, explicit, and replaceable whenever practical.
- Prefer platform integration over project-specific infrastructure.
- Preserve maintainability as Debian evolves.
- Ship cryptographically signed release artifacts that users can independently verify.

## Project status

| Item                                  | Status                                        |
| ------------------------------------- | --------------------------------------------- |
| Release family                        | **Nautilus** (Amonite 1.x)                    |
| Standard                              | Alpha 2 - `1.0.0-alpha.2` (reference edition) |
| Lite                                  | Alpha - `1.0.0-alpha`                         |
| Mobile                                | Experimental - no public ISO                  |
| Typical hardware (published editions) | `amd64` personal computers                    |

See [branding.md](branding.md) for naming and maturity labels, and [CHANGELOG.md](CHANGELOG.md) for version history.

## Architecture

Amonite builds upon Debian rather than replacing it. There is one architecture for Amonite. Editions inherit it. Implementation may change without changing product identity.

Full detail: [ARCHITECTURE.md](ARCHITECTURE.md).

## Editions

Amonite is one operating system with multiple editions. Editions differ by intended experience and maturity, not by philosophy or architecture.

| Edition      | Identity                                            | Maturity                                                                                       |
| ------------ | --------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| **Standard** | A complete general-purpose desktop operating system | Alpha 2 - [`1.0.0-alpha.2`](https://github.com/ManuelGil/amonite/releases/tag/v1.0.0-alpha.2)  |
| **Lite**     | A lightweight desktop operating system              | Alpha - [`1.0.0-alpha`](https://github.com/ManuelGil/amonite/releases/tag/lite%2Fv1.0.0-alpha) |
| **Mobile**   | An experimental exploration of mobile computing     | Experimental - no public download                                                              |

Standard is currently the reference edition. Lite is currently Alpha. Mobile remains experimental.

These statements describe present maturity only.

Edition details: [EDITIONS.md](EDITIONS.md).

## What Amonite intentionally provides

Published Alpha editions intentionally provide:

- a desktop experience matching the chosen edition;
- secure, guided installation, with optional encryption;
- live evaluation before disks are modified;
- a curated command-line environment for development and administration;
- local AI inference under user control, without depending on external inference services.

These are product commitments. They are not a catalogue of every application or desktop convenience included in a release.

More detail: [CAPABILITIES.md](CAPABILITIES.md).

## Installation

1. Download a published Alpha ISO (Standard or Lite) from [GitHub Releases](https://github.com/ManuelGil/amonite/releases) or [amonite.org/downloads](https://amonite.org/downloads/).
2. Verify the image with OpenPGP signatures and SHA-256 checksums - [VERIFY.md](VERIFY.md).
3. Write the image to a USB flash drive and boot it.
4. Install with the graphical installer - [INSTALL.md](INSTALL.md).
5. After first login, continue with [FIRST_STEPS.md](FIRST_STEPS.md).

Minimum practical expectations for published Alpha releases:

- 64-bit x86 (`amd64`) hardware;
- BIOS or UEFI firmware;
- enough RAM and storage for a Debian desktop install (see [INSTALL.md](INSTALL.md)).

## Documentation map

| Document                           | Layer        | Purpose                                    |
| ---------------------------------- | ------------ | ------------------------------------------ |
| [README.md](README.md)             | Product      | Landing page                               |
| [EDITIONS.md](EDITIONS.md)         | Product      | Edition identity and public status         |
| [CAPABILITIES.md](CAPABILITIES.md) | Product      | Product-defining capabilities              |
| [branding.md](branding.md)         | Product      | Naming, versioning, Nautilus               |
| [ARCHITECTURE.md](ARCHITECTURE.md) | Architecture | Shared architecture and decision hierarchy |
| [INSTALL.md](INSTALL.md)           | User guide   | Installing the published release           |
| [VERIFY.md](VERIFY.md)             | User guide   | Verifying release authenticity             |
| [FIRST_STEPS.md](FIRST_STEPS.md)   | User guide   | After first login                          |
| [CHANGELOG.md](CHANGELOG.md)       | History      | Version history                            |
| [SECURITY](SECURITY)               | Policy       | Security policy                            |
| [CONTRIBUTING.md](CONTRIBUTING.md) | Process      | How to contribute                          |
| [security/](security/)             | Trust        | Release signing key                        |

## Development status

Amonite is designed, built, tested, cryptographically signed, and maintained by Manuel Gil as an independent project.

Nautilus is the 1.x release family. Current published editions include Standard at Alpha 2 and Lite at Alpha. Mobile remains experimental.

Product identity and architecture should remain stable while implementations evolve. Documentation records present maturity; it does not predict future releases.

## Community

| Channel                                                          | Purpose                                                           |
| ---------------------------------------------------------------- | ----------------------------------------------------------------- |
| [r/Amonite](https://www.reddit.com/r/amonite/)                   | Questions, feedback, bug reports, and discussion                  |
| [GitHub Releases](https://github.com/ManuelGil/amonite/releases) | Official published ISOs, checksums, signatures, and release notes |
| [GitHub Sponsors](https://github.com/sponsors/ManuelGil)         | Optional sponsorship for development and infrastructure           |
| [amonite.org](https://amonite.org/)                              | Product site, gallery, downloads, and project pages               |

## Contributing

Feedback from real installs of published Alpha editions is the most useful contribution at this stage.

See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

Amonite is free software released under the GNU General Public License v3.0 or later.

See [LICENSE](LICENSE) for the complete license text.

Third-party software retains its respective licenses.
