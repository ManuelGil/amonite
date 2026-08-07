# Editions

<!--
SPDX-FileCopyrightText: 2026 Manuel Gil
SPDX-License-Identifier: GPL-3.0-or-later
-->

Amonite is one operating system offered in multiple editions. An edition is defined by its **intended experience**, not by its implementation.

All editions belong to the **Nautilus** release family, the codename for the complete Amonite 1.x generation.

| Edition      | Identity                       | Maturity            |
| ------------ | ------------------------------ | ------------------- |
| **Standard** | Reference desktop experience   | Alpha 2 - published |
| **Lite**     | Lightweight desktop experience | Alpha - published   |
| **Mobile**   | Mobile computing direction     | Experimental        |

Maturity labels describe where an edition stands today. They are not a required sequence, and one edition reaching a label implies nothing about the others. See [BRANDING.md](BRANDING.md).

## Standard

Standard is the reference Amonite desktop: a complete general-purpose desktop operating system, ready for real work after install. It is for people who want a coherent day-one system for everyday computing, development, administration, and local AI without assembling that system themselves.

Ordinary desktop behaviours follow from that experience rather than defining it, and the technologies behind them may change.

**Alpha 2** - current release `1.0.0-alpha.2`. Intended for evaluation and testing, not a production-supported stable release.

Install: [INSTALL.md](INSTALL.md)

## Lite

Lite is Amonite with a reduced graphical footprint: the same identity and the same architecture in a lighter desktop. It suits people who prefer a lighter system, including on modest hardware, without leaving the product family.

Lite is a genuine edition, not a different operating system, and it is not defined by a particular compositor or package set. Its documentation is shorter than Standard's because its maturity differs, not because it is a lesser product.

**Alpha** - current release `1.0.0-alpha`. Intended for evaluation and testing.

Install: [INSTALL.md](INSTALL.md)

## Mobile

Mobile explores whether Amonite can serve mobile computing as a coherent product direction. It is for people following that direction, not for general use.

Mobile is **experimental**: no public ISO, no public installation path, no public feature contract. Identity and purpose are documented; capabilities are not. Do not treat it as an installable Amonite product.

## Shared identity

Every edition inherits the same commitments:

- every default is an intentional decision;
- software earns its place by enabling lasting work;
- defaults remain replaceable after install;
- the user remains in control of the system.

Editions do not redefine architecture, branding, versioning, or engineering philosophy. Those belong to Amonite - see [ARCHITECTURE.md](ARCHITECTURE.md).

## Related documentation

- [CAPABILITIES.md](CAPABILITIES.md) - Product-defining capabilities by edition maturity
- [BRANDING.md](BRANDING.md) - Naming, versioning, and Nautilus
- [INSTALL.md](INSTALL.md) - Installing published Alpha editions
- [ARCHITECTURE.md](ARCHITECTURE.md) - Shared Amonite architecture
