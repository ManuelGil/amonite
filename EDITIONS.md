# Editions

<!--
SPDX-FileCopyrightText: 2026 Manuel Gil
SPDX-License-Identifier: GPL-3.0-or-later
-->

Amonite is one operating system offered in multiple editions. Every edition belongs to the same product and shares the same philosophy, architecture, branding, and engineering principles.

An edition is defined by its **intended experience**, not by its implementation.

Editions belong to the **Nautilus** release family - the codename for the complete Amonite 1.x generation. See [branding.md](branding.md).

Each edition has its own current maturity. Maturity labels describe the present state of an edition; they do not define a required release sequence.

## Current edition state

| Edition      | Identity                       | Maturity            |
| ------------ | ------------------------------ | ------------------- |
| **Standard** | Reference desktop experience   | Alpha 2 - published |
| **Lite**     | Lightweight desktop experience | Alpha - published   |
| **Mobile**   | Mobile computing direction     | Experimental        |

Standard is currently the most mature published edition. Lite is also published, currently at Alpha. Mobile remains experimental.

These are descriptions of the present. They are not commitments about future releases.

## Shared identity

All editions inherit the same Amonite identity:

- every default is an intentional decision;
- software earns its place by enabling lasting work;
- defaults remain replaceable after install;
- the user remains in control of the system.

Editions do not redefine architecture, branding, versioning, or engineering philosophy.

Those belong to Amonite. See [ARCHITECTURE.md](ARCHITECTURE.md) and [branding.md](branding.md).

## Standard

### Purpose

To provide the reference Amonite desktop experience: a complete general-purpose desktop operating system ready for real work after install.

### Audience

People who want a coherent day-one desktop for everyday computing, development, administration, and local AI - without assembling the system themselves.

### Experience

A complete general-purpose desktop.

Standard is the reference Amonite desktop. Ordinary desktop behaviours are consequences of that experience; they do not define the edition.

### Relation to other editions

Standard is the reference edition within the same product family. Lite offers a lighter desktop experience. Mobile explores a different form factor at experimental maturity.

### Maturity

**Alpha 2**

Current release: `1.0.0-alpha.2` (Nautilus)

This is the current maturity of Standard. It does not imply further Alpha releases or any later maturity label.

For evaluation and testing. Not a production-supported stable release.

Install: [INSTALL.md](INSTALL.md)

## Lite

### Purpose

To provide Amonite as a lightweight desktop experience: the same product identity with a reduced graphical footprint.

### Audience

People who prefer a lighter Amonite desktop, including use on modest hardware, without leaving the product family.

### Experience

A lightweight desktop.

Lite is a genuine Amonite edition. It is not a different operating system and is not defined by a particular compositor or package set.

### Relation to other editions

Lite inherits the same architecture and philosophy as Standard. It stands beside Standard as a published Alpha edition with a lighter desktop experience.

### Maturity

**Alpha**

Current release: `1.0.0-alpha` (Nautilus)

This is the current maturity of Lite. It does not imply further releases or any later maturity label.

For evaluation and testing. Not a production-supported stable release.

Its documentation is shorter than Standard's because its current maturity differs, not because it is a lesser product identity.

Install: [INSTALL.md](INSTALL.md)

## Mobile

### Purpose

To explore whether Amonite can serve mobile computing as a coherent product direction.

### Audience

People following the project's mobile direction. It is not intended for general use.

### Experience

An experimental mobile direction.

### Maturity

**Experimental**

- No public ISO is available.
- No public installation workflow is available.
- No stable public feature contract is available.

Identity and purpose are documented. Product capabilities are not.

Do not treat Mobile as an installable Amonite product yet.

## Comparison

|                   | Standard                         | Lite                | Mobile                        |
| ----------------- | -------------------------------- | ------------------- | ----------------------------- |
| Identity          | Complete general-purpose desktop | Lightweight desktop | Experimental mobile direction |
| Maturity          | Alpha 2                          | Alpha               | Experimental                  |
| Public download   | Yes                              | Yes                 | No                            |
| Reference edition | Yes                              | No                  | No                            |

## Related documentation

- [CAPABILITIES.md](CAPABILITIES.md) - Product-defining capabilities by edition maturity
- [branding.md](branding.md) - Naming, versioning, and Nautilus
- [INSTALL.md](INSTALL.md) - Installing published Alpha editions
- [ARCHITECTURE.md](ARCHITECTURE.md) - Shared Amonite architecture
