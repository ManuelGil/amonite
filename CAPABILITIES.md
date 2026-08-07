# Capabilities

<!--
SPDX-FileCopyrightText: 2026 Manuel Gil
SPDX-License-Identifier: GPL-3.0-or-later
-->

Capabilities are what Amonite intentionally promises as a product, documented according to edition maturity. They are not an inventory of every feature, every inherited Debian behaviour, or every desktop convenience.

Edition identity: [EDITIONS.md](EDITIONS.md).

| Capability                        | Standard (Alpha 2) | Lite (Alpha) | Mobile |
| --------------------------------- | :----------------: | :----------: | :----: |
| Complete general-purpose desktop  |         Y          |      -       |   -    |
| Lightweight desktop               |         -          |      Y       |   -    |
| Secure installation               |         Y          |      Y       |   -    |
| Offline evaluation before install |         Y          |      Y       |   -    |
| Curated command-line environment  |         Y          |      Y       |   -    |
| Local AI inference                |         Y          |      Y       |   -    |

Mobile is experimental. No capability contract is published for it; its public documentation is limited to identity, purpose, and status in [EDITIONS.md](EDITIONS.md).

Ordinary desktop behaviours - screenshots, notifications, file previews, archive handling - are expected consequences of shipping a desktop. They are not product-defining capabilities.

## Desktop

Standard provides a complete general-purpose desktop operating system. After install it is intended for everyday computing, development, administration, and related desktop work without requiring the user to assemble the environment first.

Lite provides a lightweight desktop: the same product identity with a reduced graphical footprint.

Specific desktop technologies may change without changing either identity.

## Secure installation

Published Alpha editions install through a guided installer with optional encrypted storage. Installing Amonite and protecting disks should be deliberate, confirmable steps.

## Offline evaluation before install

Official installation media provide a live session that can be evaluated before any installed disk is modified.

## Curated command-line environment

Published Alpha editions include a curated command-line environment, ready for development and administration from the first session.

## Local AI inference

Compatible models run on the local machine, offline, with models and prompts under user control. Local applications can use an API-compatible interface without depending on external inference services.

Local AI is one intentional capability among others. Amonite is not an "AI operating system".

## What is not covered here

- Implementation choices and package selections
- Expected desktop utilities that do not define the product
- Capabilities inherited from Debian, unless Amonite intentionally elevates them
- Capability claims for experimental Mobile beyond identity
- Hypothetical future editions

## Related documentation

- [EDITIONS.md](EDITIONS.md) - Edition identity and maturity
- [ARCHITECTURE.md](ARCHITECTURE.md) - Shared architecture
- [INSTALL.md](INSTALL.md) - Installation of published Alpha editions
- [FIRST_STEPS.md](FIRST_STEPS.md) - Getting started after install
