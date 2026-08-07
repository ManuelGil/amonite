# Architecture

<!--
SPDX-FileCopyrightText: 2026 Manuel Gil
SPDX-License-Identifier: GPL-3.0-or-later
-->

Amonite builds upon Debian rather than replacing it. There is exactly one Amonite architecture.

Every edition inherits it. Editions differ in intended experience and current implementation; they do not redefine architectural principles.

## Architecture goals

Every architectural decision should reinforce one or more of these goals.

**Simplicity.** Prefer solutions that remain understandable by both users and maintainers. Complexity should never become a feature.

**Modularity.** Keep engineering decisions loosely coupled whenever practical, so that users can replace individual components without affecting unrelated parts of the system.

**Maintainability.** Every engineering decision introduces long-term responsibility. The architecture minimizes future maintenance while preserving flexibility.

**Transparency.** System behaviour should be expressed through explicit packages and configuration rather than hidden automation. Trust begins with understanding.

**Platform integration.** Where Debian already provides a mature capability, the platform is preferred over a project-specific implementation.

## Documentation layers

Keep these layers separate.

| Layer          | Describes                                         | Stability          |
| -------------- | ------------------------------------------------- | ------------------ |
| Product        | Identity, philosophy, editions, audience          | Stable             |
| Architecture   | Principles, integration model, decision hierarchy | Rarely changes     |
| Engineering    | Owned decisions and repository practices          | Evolves carefully  |
| Implementation | Concrete technologies in a given build            | Changes frequently |

Implementation must never redefine the product or the architecture.

## Levels of decision

### Architectural decisions

Stable rules for how Amonite relates to Debian and how defaults are chosen:

- build upon Debian rather than replacing it;
- prefer platform capabilities before project-specific infrastructure;
- keep lifecycles separate: build, installation, and installed system;
- protect a small set of foundational product capabilities.

These should rarely change.

### Engineering decisions

Choices the project owns because they define the default system for a sustained period: local language model inference as a default capability, a curated command-line environment, a desktop experience appropriate to the edition, a guided Welcome experience where the published product includes it.

Engineering decisions protect outcomes. Their implementations may change.

### Current implementation

The concrete technologies used in a given build or release - desktop environments, compositors, audio stacks, installers, individual packages.

Implementation may change without rewriting product or architecture documentation.

## Protected decisions

Not every engineering decision carries the same permanence.

Two are foundational: a default automation and integration runtime, and local language model inference. They define permanent capabilities whose implementations the project deliberately protects, and changing either means reconsidering the architectural direction of the project rather than selecting a different implementation.

Most decisions protect a capability instead of an implementation - a modern terminal experience, a desktop experience appropriate to the edition, a guided Welcome experience where applicable, a modern command-line environment. Those implementations may evolve whenever they offer measurable improvements and remain consistent with the project principles.

The rest are evolutionary. Supporting applications and non-foundational desktop components move with the platform, and the goal there is to preserve capabilities rather than individual packages.

## Integration model

Every engineering decision follows the same conceptual path.

```text
Engineering Decision
        |
Capability
        |
Implementation
        |
Configuration
        |
Installed System
```

Whenever possible, existing platform packages are preferred over new ones, configuration over customization, and declarative mechanisms over imperative behaviour. Project-specific logic should exist only when the platform cannot reasonably express the required capability.

## Editions and architecture

Editions share this architecture completely.

| Edition  | Intended experience              | Maturity            |
| -------- | -------------------------------- | ------------------- |
| Standard | Complete general-purpose desktop | Alpha 2 (published) |
| Lite     | Lightweight desktop              | Alpha (published)   |
| Mobile   | Mobile computing direction       | Experimental        |

Product positioning: [EDITIONS.md](EDITIONS.md). Naming and release family: [BRANDING.md](BRANDING.md).

## Lifecycles

Three lifecycles stay independent: the build produces installation artifacts, installation deploys the operating system, and the installed system provides permanent capabilities to the user.

Responsibilities belonging to one lifecycle should never leak into another. Temporary installation behaviour should not become permanent system behaviour unless it keeps providing value after installation.

## Runtime behaviour

The installed system is intended to remain close to Debian:

- software updates use standard Debian package management;
- security mechanisms prefer mature platform capabilities;
- desktop and terminal defaults are expressed through packages and configuration;
- local AI is available as an integrated capability without requiring external services.

Amonite avoids additional background services, custom startup logic, and extra integration layers when declarative configuration is sufficient.

## Distribution philosophy

Official releases are distributed as signed ISO images with checksums and machine-readable metadata (`release.json`).

Users should be able to:

1. download a published release;
2. verify authenticity and integrity independently;
3. boot a live session without modifying installed disks;
4. install with the graphical installer;
5. replace defaults after installation without fighting the system.

Verification: [VERIFY.md](VERIFY.md). Installation: [INSTALL.md](INSTALL.md).

## Decision process

Every engineering change should answer these questions.

1. Does it reinforce an existing engineering decision?
2. Can Debian already provide the required capability?
3. Can configuration express the desired behaviour?
4. Does it avoid unnecessary coupling?
5. Does it reduce long-term maintenance?
6. Does it improve the coherence of the default system?

A change that cannot satisfy them should normally not become part of Amonite.

## Relationship with Debian

Debian provides the operating system platform. Amonite provides carefully selected engineering decisions on top of that platform.

Technology evolves, Debian evolves, and Amonite evolves with them. Engineering decisions are re-evaluated as better solutions appear, but the project minimizes divergence from Debian and avoids project-specific infrastructure unless it provides clear and lasting value. Improvement should never cost simplicity, maintainability, or platform integration.

Amonite refines the default system through deliberate engineering decisions. It does not replace the platform.

> **Every default is an intentional decision.**
