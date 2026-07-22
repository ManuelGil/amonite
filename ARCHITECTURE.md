# Amonite Architecture

<!--
SPDX-FileCopyrightText: 2026 Manuel Gil
SPDX-License-Identifier: GPL-3.0-or-later
-->

Amonite builds upon Debian rather than replacing it.

The project intentionally limits the number of engineering decisions it owns while relying on the platform whenever appropriate. This architecture exists to make those decisions understandable, maintainable and replaceable throughout the lifetime of the project.

> **Every default is an intentional decision.**

## Architecture Goals

Every architectural decision should reinforce one or more of the following goals.

### Simplicity

Prefer solutions that remain understandable by both users and maintainers.

Complexity should never become a feature.

### Modularity

Keep engineering decisions loosely coupled whenever practical.

Users should remain free to replace individual components without affecting unrelated parts of the system.

### Maintainability

Engineering decisions introduce long-term responsibility.

The architecture therefore seeks to minimize future maintenance while preserving flexibility.

### Transparency

System behaviour should primarily be expressed through explicit packages and configuration rather than hidden automation.

Trust begins with understanding.

### Platform Integration

Whenever Debian already provides a mature capability, the platform should normally be preferred over project-specific implementations.

## Engineering Decisions

An engineering decision is any capability whose long-term evolution becomes the responsibility of Amonite rather than the underlying platform.

Engineering decisions define the default system.

They do not prevent users from modifying, replacing or removing individual components.

The objective is not to maximize customization.

The objective is to provide a coherent default system.

## Protected Decisions

Not every engineering decision has the same level of permanence.

Amonite distinguishes between three categories.

### Foundational Decisions

These decisions define permanent capabilities whose implementations are intentionally protected by the project.

Current foundational decisions include:

- Python as the default automation and integration runtime.
- Local language model inference through `llama.cpp`.

These technologies form part of the identity of the default system.

Changing them requires reconsidering the architectural direction of the project rather than selecting a different implementation.

### Protected Capabilities

Some engineering decisions protect the capability rather than the implementation.

Current examples include:

- Modern terminal experience.
- Lightweight desktop environment.
- Guided Welcome experience.

Implementations may evolve whenever they provide measurable improvements while remaining consistent with the project principles.

### Evolutionary Decisions

Some parts of the system intentionally evolve together with the platform.

Examples include:

- command-line utilities;
- supporting applications;
- desktop components that are not considered foundational.

These decisions are continuously re-evaluated as Debian evolves.

The objective is to preserve capabilities rather than individual packages.

## Integration Model

Every engineering decision follows the same conceptual integration model.

```text
Engineering Decision
        ↓
Capability
        ↓
Implementation
        ↓
Configuration
        ↓
Installed System
```

Whenever possible:

- existing platform packages are preferred;
- configuration is preferred over customization;
- declarative mechanisms are preferred over imperative behaviour.

Project-specific logic should exist only when the platform cannot reasonably express the required capability.

## Lifecycles

Amonite distinguishes three independent lifecycles.

| Lifecycle        | Responsibility                              |
| ---------------- | ------------------------------------------- |
| Build            | Produce installation artifacts.             |
| Installation     | Deploy the operating system.                |
| Installed System | Provide permanent capabilities to the user. |

Responsibilities belonging to one lifecycle should never leak into another.

Temporary installation behaviour should not become permanent system behaviour unless it continues providing value after installation.

## Decision Process

Every engineering change should answer the following questions.

1. Does it reinforce an existing engineering decision?
2. Can Debian already provide the required capability?
3. Can configuration express the desired behaviour?
4. Does it avoid unnecessary coupling?
5. Does it reduce long-term maintenance?
6. Does it improve the coherence of the default system?

Changes that cannot satisfy these questions should normally not become part of Amonite.

## Continuous Evolution

Technology evolves.

Debian evolves.

Amonite evolves with them.

Engineering decisions are periodically re-evaluated as better solutions become available.

The project protects capabilities rather than unnecessary implementation details while preserving the small set of foundational decisions that define the identity of the distribution.

Continuous improvement should never compromise simplicity, maintainability or platform integration.

## Relationship with Debian

Debian provides the operating system platform.

Amonite provides carefully selected engineering decisions on top of that platform.

The project intentionally minimizes divergence from Debian and avoids introducing project-specific infrastructure unless it provides clear and lasting value.

Rather than replacing the platform, Amonite seeks to refine the default system through deliberate engineering decisions.

> **Every default is an intentional decision.**
