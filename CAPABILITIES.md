# Capabilities

<!--
SPDX-FileCopyrightText: 2026 Manuel Gil
SPDX-License-Identifier: GPL-3.0-or-later
-->

This document describes the product-defining capabilities of Amonite.

Capabilities are documented according to edition maturity. They explain what Amonite intentionally promises as a product. They are not an inventory of every feature, every inherited Debian behaviour, or every desktop convenience.

Edition identity: [EDITIONS.md](EDITIONS.md).

## Scope

| Edition  | Maturity     | Capability documentation               |
| -------- | ------------ | -------------------------------------- |
| Standard | Alpha 2      | Published Alpha product capabilities   |
| Lite     | Alpha        | Published Alpha product capabilities   |
| Mobile   | Experimental | Identity only - no capability contract |

## Comparison

| Capability                        | Standard | Lite  | Mobile |
| --------------------------------- | :------: | :---: | :----: |
| Complete general-purpose desktop  |    Y     |   -   |   -    |
| Lightweight desktop               |    -     |   Y   |   -    |
| Secure installation               |    Y     |   Y   |   -    |
| Offline evaluation before install |    Y     |   Y   |   -    |
| Curated command-line environment  |    Y     |   Y   |   -    |
| Local AI inference                |    Y     |   Y   |   -    |

Ordinary desktop behaviours - such as screenshots, notifications, file previews, or archive handling - are expected consequences of shipping a desktop. They are not listed here as product-defining capabilities.

## Complete general-purpose desktop

Standard provides a complete general-purpose desktop operating system.

After install, it is intended for everyday computing, development, administration, and related desktop work without requiring the user to assemble the environment first.

Specific desktop technologies may change without changing that identity.

**Edition:** Standard (Alpha 2)

## Lightweight desktop

Lite provides a lightweight desktop operating system.

It preserves Amonite's product identity while offering a reduced graphical footprint.

Specific desktop technologies may change without changing that identity.

**Edition:** Lite (Alpha)

## Secure installation

Published Alpha editions provide guided installation with optional encrypted storage.

Installing Amonite and protecting disks should be deliberate, confirmable steps.

**Editions:** Standard, Lite

## Offline evaluation before install

Official installation media for published Alpha editions provide a live session that can be evaluated before any installed disk is modified.

**Editions:** Standard, Lite

## Curated command-line environment

Published Alpha editions include a curated command-line environment ready for development and administration from the first session.

**Editions:** Standard, Lite

## Local AI inference

Published Alpha editions include local AI inference as a deliberate capability.

Compatible models can run on the local machine, offline, with models and prompts under user control. Local applications can use an API-compatible interface without depending on external inference services.

Local AI is one intentional capability among others. Amonite is not an "AI operating system".

**Editions:** Standard, Lite

## Mobile

Mobile is experimental.

Its public documentation is limited to identity, purpose, and status in [EDITIONS.md](EDITIONS.md).

No product capability contract is published for Mobile at this maturity.

## Omissions

This document does not cover:

- Implementation choices and package selections
- Expected desktop utilities that do not define the product
- Capabilities inherited from Debian unless Amonite intentionally elevates them
- Capability claims for experimental Mobile beyond identity
- Hypothetical future editions

## Related documentation

- [EDITIONS.md](EDITIONS.md) - Edition identity and maturity
- [ARCHITECTURE.md](ARCHITECTURE.md) - Shared architecture
- [INSTALL.md](INSTALL.md) - Installation of published Alpha editions
- [FIRST_STEPS.md](FIRST_STEPS.md) - Getting started after install
