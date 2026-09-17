# Technical Learning — Curriculum and Knowledge Map

A long-term curriculum for senior DevOps, cloud, and software engineering. This repository organizes understanding: subjects, prerequisites, internal mechanics, practical application, and connections across domains.

Start with the [master curriculum](CURRICULUM.md), then open a domain map. Folder numbers help browsing; they are not a mandatory global sequence. Linux and networking can develop together. Security and observability enter early wherever a topic needs them.

## Structure

**Domain → Subject → Topic → Concepts.** Domains have a README map; subjects group topics; small concepts remain inside their parent topic. Most topics initially live as sections in a map. Six representative notes demonstrate the deeper format without creating hundreds of empty files.

## Relationships and navigation

- **Prerequisites:** `A → B` means understand A before B. These are explicit topic relationships, independent of category membership.
- **Implements / applies:** connects technology-specific knowledge to transferable concepts.
- **Related:** a useful connection without a required learning order.
- **Leads To:** downstream topics derived from prerequisites.

Every domain map includes purpose, entry prerequisites, recommended learning order, major areas, a small Mermaid dependency sketch, and downstream links. Diagrams show selected prerequisite edges and render on GitHub; YAML holds the complete graph.

Normal Markdown links support GitHub navigation. Path-qualified `[[...|Display title]]` links support Obsidian without ambiguity between the many README files. For example, [[04-networking/ip-addressing|IP Addressing]] is paired with [IP Addressing](04-networking/ip-addressing.md). Map-only topics use heading links until a note is warranted.

## Source of truth

[curriculum.yaml](curriculum.yaml) owns hierarchy, stable IDs, ordering, prerequisites, and conceptual relationships. [dependencies.yaml](dependencies.yaml), the master curriculum, and domain maps are generated from it. Individual topic notes are authored Markdown and are never overwritten by the generator.

See the [editing and model guide](CONTRIBUTING.md) for validation, future topic-list integration, and Obsidian migration. Open this repository folder as an Obsidian vault when ready; no database export or plugin is required to read it. This scaffold deliberately contains no progress tracking or schedules.
