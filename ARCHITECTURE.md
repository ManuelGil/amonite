# Architecture

<!--
SPDX-FileCopyrightText: 2026 Manuel Gil
SPDX-License-Identifier: GPL-3.0-or-later
-->

Amonite builds upon Debian rather than replacing it. There is exactly one Amonite architecture.

Every edition inherits it. Editions differ in intended experience and current implementation. They do not redefine architectural principles.

> **Every default is an intentional decision.**

## Architecture goals

Every architectural decision should reinforce one or more of the following goals.

### Simplicity

Prefer solutions that remain understandable by both users and maintainers. Complexity should never become a feature.

### Modularity

Keep engineering decisions loosely coupled whenever practical. Users should remain free to replace individual components without affecting unrelated parts of the system.

### Maintainability

Engineering decisions introduce long-term responsibility. The architecture minimizes future maintenance while preserving flexibility.

### Transparency

System behaviour should primarily be expressed through explicit packages and configuration rather than hidden automation. Trust begins with understanding.

### Platform integration

Whenever Debian already provides a mature capability, the platform should normally be preferred over project-specific implementations.

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

Stable rules for how Amonite relates to Debian and how defaults are chosen.

Examples:

- build upon Debian rather than replacing it;
- prefer platform capabilities before project-specific infrastructure;
- keep lifecycles separate: build, installation, and installed system;
- protect a small set of foundational product capabilities.

Architectural decisions should rarely change.

### Engineering decisions

Choices the project owns because they define the default system for a sustained period.

Examples:

- local language model inference as a default capability;
- a curated command-line environment;
- a desktop experience appropriate to the edition;
- a guided Welcome experience where the published product includes it.

Engineering decisions protect outcomes. Their implementations may change.

### Current implementation

The concrete technologies used in a given build or release.

Examples include specific desktop environments, compositors, audio stacks, installers, and individual packages.

Current implementation may change without rewriting product or architecture documentation.

## Protected decisions

Not every engineering decision has the same level of permanence.

### Foundational decisions

These decisions define permanent capabilities whose implementations are intentionally protected by the project.

Current foundational decisions include:

- a default automation and integration runtime;
- local language model inference.

Changing them requires reconsidering the architectural direction of the project rather than selecting a different implementation.

### Protected capabilities

Some engineering decisions protect the capability rather than the implementation.

Current examples include:

- modern terminal experience;
- desktop experience appropriate to the edition;
- guided Welcome experience where applicable;
- modern command-line environment.

Implementations may evolve whenever they provide measurable improvements while remaining consistent with the project principles.

### Evolutionary decisions

Some parts of the system intentionally evolve together with the platform.

Examples include supporting applications and non-foundational desktop components.

The goal is to preserve capabilities rather than individual packages.

## Integration model

Every engineering decision follows the same conceptual integration model.

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

Whenever possible:

- existing platform packages are preferred;
- configuration is preferred over customization;
- declarative mechanisms are preferred over imperative behaviour.

Project-specific logic should exist only when the platform cannot reasonably express the required capability.

## Editions and architecture

Editions share this architecture completely.

| Edition  | Intended experience              | Maturity            |
| -------- | -------------------------------- | ------------------- |
| Standard | Complete general-purpose desktop | Alpha 2 (published) |
| Lite     | Lightweight desktop              | Alpha (published)   |
| Mobile   | Mobile computing direction       | Experimental        |

Product positioning: [EDITIONS.md](EDITIONS.md).

Naming and release family: [branding.md](branding.md).

## Lifecycles

Amonite distinguishes three independent lifecycles.

| Lifecycle        | Responsibility                              |
| ---------------- | ------------------------------------------- |
| Build            | Produce installation artifacts.             |
| Installation     | Deploy the operating system.                |
| Installed system | Provide permanent capabilities to the user. |

Responsibilities belonging to one lifecycle should never leak into another.

Temporary installation behaviour should not become permanent system behaviour unless it continues providing value after installation.

## Runtime behaviour

The installed system is intended to remain close to Debian:

- software updates use standard Debian package management;
- security mechanisms prefer mature platform capabilities;
- desktop and terminal defaults are expressed through packages and configuration;
- local AI is available as an integrated capability without requiring external services.

Amonite avoids introducing additional background services, custom startup logic, or unnecessary integration layers when declarative configuration is sufficient.

## Distribution philosophy

Official published releases are distributed as signed ISO images with checksums and machine-readable metadata (`release.json`).

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

Changes that cannot satisfy these questions should normally not become part of Amonite.

## Continuous evolution

Technology evolves, Debian evolves, and Amonite evolves with them. Engineering decisions are periodically re-evaluated as better solutions become available.

The project protects capabilities rather than unnecessary implementation details, while preserving the small set of foundational decisions that define the identity of the distribution. Continuous improvement should never compromise simplicity, maintainability, or platform integration.

## Relationship with Debian

Debian provides the operating system platform. Amonite provides carefully selected engineering decisions on top of that platform.

The project minimizes divergence from Debian and avoids project-specific infrastructure unless it provides clear and lasting value. Amonite refines the default system through deliberate engineering decisions. It does not replace the platform.

> **Every default is an intentional decision.**
