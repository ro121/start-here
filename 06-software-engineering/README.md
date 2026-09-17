# Software Engineering

<!-- Generated map: edit curriculum.yaml, then run scripts/curriculum.py build. -->

[Master curriculum](../CURRICULUM.md) · [Model and editing guide](../CONTRIBUTING.md)

## Purpose

Design, test, and evolve software with explicit interfaces and maintainability.

## Prerequisites

[[00-foundations/README#Programming Fundamentals|Programming Fundamentals]] · [Programming Fundamentals](../00-foundations/README.md#programming-fundamentals)

These orient entry into the domain; each topic below has its own requirements. They are not inherited gates.

## Recommended Learning Order

This is one dependency-compatible reading order. External prerequisites can be learned in parallel; numbering is guidance, not a completion checklist.

1. [Software Lifecycle and Requirements](README.md#software-lifecycle)
2. [Software Design Principles](README.md#software-design)
3. [Software Testing](README.md#software-testing)
4. [Application Diagnostics](README.md#application-diagnostics)
5. [API Design](README.md#api-design)

## Major Areas

### Design and Delivery Foundations

<a id="software-lifecycle"></a>
#### Software Lifecycle and Requirements

**Concepts:** SDLC; Requirements; Feedback; Change management.

**Prerequisites:** [[00-foundations/README#Programming Fundamentals|Programming Fundamentals]] · [Programming Fundamentals](../00-foundations/README.md#programming-fundamentals)

<a id="software-design"></a>
#### Software Design Principles

**Concepts:** Architecture; Cohesion; Coupling; SOLID; Interface design.

**Prerequisites:** [[06-software-engineering/README#Software Lifecycle and Requirements|Software Lifecycle and Requirements]] · [Software Lifecycle and Requirements](README.md#software-lifecycle); [[00-foundations/README#Data Structures and Algorithms|Data Structures and Algorithms]] · [Data Structures and Algorithms](../00-foundations/README.md#data-structures-algorithms)

<a id="api-design"></a>
#### API Design

**Concepts:** REST; Contracts; Versioning; Authentication; Authorization; Error handling.

**Prerequisites:** [[06-software-engineering/README#Software Design Principles|Software Design Principles]] · [Software Design Principles](README.md#software-design); [[04-networking/README#HTTP|HTTP]] · [HTTP](../04-networking/README.md#http); [[18-security/identity-access|Identity and Access Management]] · [Identity and Access Management](../18-security/identity-access.md)

### Quality and Distribution

<a id="software-testing"></a>
#### Software Testing

**Concepts:** Unit testing; Integration testing; End-to-end testing; Test doubles.

**Prerequisites:** [[06-software-engineering/README#Software Design Principles|Software Design Principles]] · [Software Design Principles](README.md#software-design)

<a id="application-diagnostics"></a>
#### Application Diagnostics

**Concepts:** Structured logging; Error context; Correlation identifiers.

**Prerequisites:** [[06-software-engineering/README#Software Testing|Software Testing]] · [Software Testing](README.md#software-testing)

## Dependency Sketch

Selected direct prerequisite edges, not the entire domain graph. Arrows mean “learn before”.

```mermaid
flowchart TD
    n0["Software Lifecycle and Requirements"]
    n1["Software Design Principles"]
    n2["API Design"]
    n3["Software Testing"]
    n4["Application Diagnostics"]
    n5["Programming Fundamentals"]
    n6["Data Structures and Algorithms"]
    n7["HTTP"]
    n0 --> n1
    n1 --> n2
    n1 --> n3
    n3 --> n4
    n5 --> n0
    n6 --> n1
    n7 --> n2
```

## Leads To

[[07-git/README#Git Workflows|Git Workflows]] · [Git Workflows](../07-git/README.md#git-workflows); [[12-infrastructure-as-code/README#Infrastructure Testing and Delivery|Infrastructure Testing and Delivery]] · [Infrastructure Testing and Delivery](../12-infrastructure-as-code/README.md#infrastructure-testing); [[13-configuration-management/README#Configuration Testing|Configuration Testing]] · [Configuration Testing](../13-configuration-management/README.md#configuration-testing); [[14-kubernetes/README#Kubernetes Extensions|Kubernetes Extensions]] · [Kubernetes Extensions](../14-kubernetes/README.md#kubernetes-extensions); [[15-ci-cd/README#Continuous Integration|Continuous Integration]] · [Continuous Integration](../15-ci-cd/README.md#ci-fundamentals); [[21-system-design/README#System Design Method|System Design Method]] · [System Design Method](../21-system-design/README.md#system-design-method)
