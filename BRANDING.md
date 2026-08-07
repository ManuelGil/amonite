# Branding

<!--
SPDX-FileCopyrightText: 2026 Manuel Gil
SPDX-License-Identifier: GPL-3.0-or-later
-->

Canonical branding and release-naming reference for Amonite. Branding belongs to **Amonite**, not to an edition. All editions share this philosophy.

## Identity

Debian is the technical foundation. Amonite is the public-facing identity built on top of it.

Users interact with Amonite: its name, visual identity, release naming, and defaults. Branding must not leak platform implementation details into anything the user is expected to understand as product identity.

Project logo: [assets/logo.png](assets/logo.png)

## Versioning

Amonite uses [Semantic Versioning](https://semver.org/) (`MAJOR.MINOR.PATCH`), with optional pre-release labels when a release needs them.

The SemVer number is the authoritative version identifier for packaging, scripting, and comparison.

Version numbers and pre-release labels exist only when a release requires them. They are not a fixed numbering policy and do not imply further numbered releases.

Examples of forms that may appear:

- `1.0.0-experimental`
- `1.0.0-alpha`
- `1.0.0-alpha.2`
- `1.0.0-beta`
- `1.0.0-rc`
- `1.0.0`

These are illustrations, not a required sequence.

`1.0.0-alpha.2` does not imply `1.0.0-alpha.3`.

The presence of Alpha does not imply Beta, Release Candidate, or Stable.

## Maturity labels

Maturity labels describe the **current state** of an edition or release.

Possible labels include, but are not limited to:

- Experimental
- Alpha
- Beta
- Release Candidate
- Stable

These labels are observations, not mandatory milestones. They do not define a required lifecycle. They do not require every edition to reach every label.

Each edition evolves independently. An edition may remain at one maturity indefinitely, skip labels, or publish an additional numbered pre-release only when the project state justifies it.

Documentation records present maturity. It does not predict future releases.

## Release family: Nautilus

**Nautilus** is the codename for the complete Amonite **1.x** generation. Every release belonging to the 1.x series belongs to Nautilus, regardless of that release's maturity label.

Nautilus names the generation. Maturity labels name the current state of a given edition or version within that generation.

| Concept                    | Meaning                                                  |
| -------------------------- | -------------------------------------------------------- |
| Nautilus                   | Codename of the Amonite 1.x family                       |
| `1.0.0-alpha.2`            | A specific version that currently exists within Nautilus |
| Alpha / Beta / RC / Stable | Possible maturity labels - not a required path           |

## Editions and branding

Editions may differ in experience and current maturity.

They do not receive separate branding philosophies, versioning schemes, or release-family names.

Standard, Lite, and Mobile are editions of Amonite under the same identity.

## Related documentation

- [README.md](README.md) - Product landing page
- [EDITIONS.md](EDITIONS.md) - Edition identity and current maturity
- [CHANGELOG.md](CHANGELOG.md) - Version history
- [ARCHITECTURE.md](ARCHITECTURE.md) - Shared architecture
