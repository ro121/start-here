# Programming and Scripting

<!-- Generated map: edit curriculum.yaml, then run scripts/curriculum.py build. -->

[Master curriculum](../CURRICULUM.md) · [Model and editing guide](../CONTRIBUTING.md)

## Purpose

Turn programming fundamentals into reliable automation and maintainable programs.

## Prerequisites

[[00-foundations/README#Programming Fundamentals|Programming Fundamentals]] · [Programming Fundamentals](../00-foundations/README.md#programming-fundamentals); [[03-linux/README#Linux Shell|Linux Shell]] · [Linux Shell](../03-linux/README.md#linux-shell)

These orient entry into the domain; each topic below has its own requirements. They are not inherited gates.

## Recommended Learning Order

This is one dependency-compatible reading order. External prerequisites can be learned in parallel; numbering is guidance, not a completion checklist.

1. [Python Automation](README.md#python-automation)
2. [Shell Automation](README.md#shell-automation)
3. [Programming Paradigms](README.md#programming-paradigms)
4. [Python Language Mechanics](README.md#python-language)
5. [Program Dependencies and Packaging](README.md#program-dependencies)
6. [Network Programming](README.md#network-programming)
7. [Python Concurrency](README.md#python-concurrency)
8. [Python Testing and Tooling](README.md#python-quality)

## Major Areas

### Automation Languages

<a id="python-automation"></a>
#### Python Automation

**Concepts:** Functions and modules; File I/O; Exceptions; Environments; API clients; pathlib; subprocess; argparse; Regular expressions.

**Prerequisites:** [[00-foundations/README#Programming Fundamentals|Programming Fundamentals]] · [Programming Fundamentals](../00-foundations/README.md#programming-fundamentals); [[03-linux/README#Linux Shell|Linux Shell]] · [Linux Shell](../03-linux/README.md#linux-shell)

**Related:** [[05-programming/README#Python Language Mechanics|Python Language Mechanics]] · [Python Language Mechanics](README.md#python-language); [[05-programming/README#Python Testing and Tooling|Python Testing and Tooling]] · [Python Testing and Tooling](README.md#python-quality); [[05-programming/README#Python Concurrency|Python Concurrency]] · [Python Concurrency](README.md#python-concurrency)

<a id="shell-automation"></a>
#### Shell Automation

**Concepts:** Quoting; Pipelines; Exit handling; Script interfaces; Safe retries.

**Prerequisites:** [[03-linux/README#Linux Shell|Linux Shell]] · [Linux Shell](../03-linux/README.md#linux-shell)

<a id="programming-paradigms"></a>
#### Programming Paradigms

**Concepts:** Procedural decomposition; Object-oriented modeling; Composition; Functional transformations; Mutable and immutable state.

**Prerequisites:** [[00-foundations/README#Programming Fundamentals|Programming Fundamentals]] · [Programming Fundamentals](../00-foundations/README.md#programming-fundamentals)

<a id="python-language"></a>
#### Python Language Mechanics

**Concepts:** Scope; Collections; Comprehensions; Classes; Iterators; Generators; Decorators; Context managers.

**Prerequisites:** [[05-programming/README#Python Automation|Python Automation]] · [Python Automation](README.md#python-automation); [[05-programming/README#Programming Paradigms|Programming Paradigms]] · [Programming Paradigms](README.md#programming-paradigms)

### Program Runtime

<a id="program-dependencies"></a>
#### Program Dependencies and Packaging

**Concepts:** Libraries; Dependency resolution; Lockfiles; Packaging; Distribution; Virtual environments; Package indexes; pip; uv; Lockfile reproducibility.

**Prerequisites:** [[00-foundations/README#Programming Fundamentals|Programming Fundamentals]] · [Programming Fundamentals](../00-foundations/README.md#programming-fundamentals)

<a id="network-programming"></a>
#### Network Programming

**Concepts:** Sockets; HTTP clients; Timeouts; Serialization.

**Prerequisites:** [[05-programming/README#Python Automation|Python Automation]] · [Python Automation](README.md#python-automation); [[04-networking/README#HTTP|HTTP]] · [HTTP](../04-networking/README.md#http)

<a id="python-concurrency"></a>
#### Python Concurrency

**Concepts:** Threads; Processes; Async I/O; Cancellation; Runtime and GIL considerations; CPU-bound and I/O-bound work.

**Prerequisites:** [[05-programming/README#Python Language Mechanics|Python Language Mechanics]] · [Python Language Mechanics](README.md#python-language); [[02-operating-systems/README#Concurrency|Concurrency]] · [Concurrency](../02-operating-systems/README.md#concurrency)

**Implements / applies:** [[02-operating-systems/README#Concurrency|Concurrency]] · [Concurrency](../02-operating-systems/README.md#concurrency)

<a id="python-quality"></a>
#### Python Testing and Tooling

**Concepts:** Type annotations; Static analysis; Formatting; pytest; unittest; Fixtures; Test isolation; pyproject.toml.

**Prerequisites:** [[05-programming/README#Python Language Mechanics|Python Language Mechanics]] · [Python Language Mechanics](README.md#python-language); [[06-software-engineering/README#Software Testing|Software Testing]] · [Software Testing](../06-software-engineering/README.md#software-testing); [[05-programming/README#Program Dependencies and Packaging|Program Dependencies and Packaging]] · [Program Dependencies and Packaging](README.md#program-dependencies)

**Implements / applies:** [[06-software-engineering/README#Software Testing|Software Testing]] · [Software Testing](../06-software-engineering/README.md#software-testing); [[05-programming/README#Program Dependencies and Packaging|Program Dependencies and Packaging]] · [Program Dependencies and Packaging](README.md#program-dependencies)

## Dependency Sketch

Selected direct prerequisite edges, not the entire domain graph. Arrows mean “learn before”.

```mermaid
flowchart TD
    n0["Python Automation"]
    n1["Python Language Mechanics"]
    n2["Programming Paradigms"]
    n3["Network Programming"]
    n4["Python Concurrency"]
    n5["Python Testing and Tooling"]
    n6["Program Dependencies and Packaging"]
    n7["Programming Fundamentals"]
    n0 --> n1
    n2 --> n1
    n0 --> n3
    n1 --> n4
    n1 --> n5
    n6 --> n5
    n7 --> n0
    n7 --> n2
```

## Leads To

[[04-networking/README#Network Automation|Network Automation]] · [Network Automation](../04-networking/README.md#network-automation); [[09-containers/README#Container Images|Container Images]] · [Container Images](../09-containers/README.md#container-images); [[15-ci-cd/README#Continuous Integration|Continuous Integration]] · [Continuous Integration](../15-ci-cd/README.md#ci-fundamentals); [[17-observability/README#OpenTelemetry|OpenTelemetry]] · [OpenTelemetry](../17-observability/README.md#opentelemetry); [[18-security/README#Supply Chain Security|Supply Chain Security]] · [Supply Chain Security](../18-security/README.md#supply-chain-security)

## Reference Roadmaps

Use these for coverage and further exploration; the prerequisite relationships here are curated independently.

- [roadmap.sh — Python](https://roadmap.sh/python)

[Reference review and scope decisions](../references/roadmap-sh.md)
