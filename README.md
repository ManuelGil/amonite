# Amonite

> **A carefully integrated Debian-based GNU/Linux distribution.**

Amonite is an independent GNU/Linux distribution built on Debian.

Rather than redefining Linux or competing with the underlying platform, Amonite integrates a carefully selected set of engineering decisions to provide a coherent default system while preserving the modularity, transparency and user control that have long defined GNU/Linux.

Debian provides the platform.

Amonite provides a carefully considered set of defaults.

The project is guided by a simple principle:

> **Every default is an intentional decision.**

## Why Amonite?

Modern operating systems naturally accumulate software, services, integrations and automation over time.

Although each addition may solve a specific problem, the overall result is often increased complexity, higher maintenance costs and systems that become progressively harder to understand, adapt and maintain.

Amonite follows a different approach.

Instead of asking what else should be added, the project first asks:

> **Why should this exist by default?**

Every default should provide a clear capability, justify its existence and continue to provide value throughout the system's lifetime.

The objective is not to build a different Linux.

The objective is to let Linux remain Linux.

## Product Principles

Every engineering decision should reinforce one or more of the following principles.

### Efficiency

Include only capabilities that provide lasting value throughout the lifetime of the system.

Temporary installation requirements should not become permanent parts of the installed operating system.

### Security

Build upon Debian's mature security mechanisms before introducing additional software.

Security is primarily achieved through sound engineering decisions, sensible defaults and correct use of existing platform capabilities.

### Privacy

Protect user privacy through sensible defaults while preserving user choice.

Privacy should improve through reducing unnecessary exposure rather than restricting the flexibility expected from a GNU/Linux system.

### Lightweight

In this context, lightweight refers to engineering cost rather than package count.

Capabilities should be implemented with the lowest practical cost in terms of dependencies, maintenance and coupling.

### Simplicity

Maintain a coherent and understandable system where every engineering decision can be technically justified.

Complexity should never become a feature.

## Protected Engineering Decisions

Amonite intentionally maintains a small number of engineering decisions that define the identity of the default system.

Some decisions represent foundational technologies maintained by the project.

Others define capabilities whose implementations may evolve as better solutions become available.

Current protected decisions are:

- Python as the default automation and integration runtime.
- Local language model inference.
- A modern command-line environment.
- A lightweight desktop environment.
- A modern terminal experience.
- A guided Welcome experience.

Individual implementations may evolve without changing the engineering decision they support.

## Engineering Philosophy

Amonite evolves together with Debian.

Whenever practical, the project prefers:

- integration over replacement;
- configuration over customization;
- capabilities over workflows;
- simplicity over unnecessary abstraction;
- maintainability over feature accumulation.

Existing platform capabilities are always preferred before introducing project-specific infrastructure.

Engineering decisions remain subject to continuous evaluation whenever a demonstrably better solution exists.

## Scope

Amonite is:

- an independent Debian-based GNU/Linux distribution;
- a carefully integrated desktop operating system;
- conservative in its engineering decisions;
- focused on maintainability and long-term sustainability.

Amonite is not:

- a replacement for Debian;
- a heavily customized desktop;
- a technology showcase;
- a workflow-oriented operating system.

## Project Resources

| Resource        | Purpose                                          |
| --------------- | ------------------------------------------------ |
| Website         | Product information, documentation and downloads |
| GitHub Releases | Official releases                                |
| Community       | [r/Amonite](https://reddit.com/r/amonite)        |

The official Amonite community is hosted on Reddit. Questions, bug reports, feature ideas and general discussion are welcome in **r/Amonite**.

The website is the public source of truth for product information, capabilities, release information and community resources.

This repository documents the public engineering decisions that define Amonite.

See [CHANGELOG.md](CHANGELOG.md) for the project's public release history.

## License

Amonite is free software released under the GNU General Public License v3.0 or later.

See [LICENSE](LICENSE) for the complete license text.

Third-party software retains its respective licenses.
