# roadmap.sh Reference Review

Reviewed 2026-09-18. These six user-provided roadmaps are reference lenses for the existing curriculum. Their overlaps are merged into canonical concepts rather than copied as six separate learning tracks.

The review used the linked pages and their public topic-file inventories at [upstream revision 253079f](https://github.com/nilbuild/developer-roadmap/tree/253079f3b0a317ba68b83dd9b4e7f88b2cbe2cc9/roadmaps). The page text did not expose the interactive diagram contents. Inventory inspection establishes topic coverage, not diagram-edge semantics; prerequisite edges here are our own editorial decisions. This is a selective scaffold review, not a complete node-by-node import or verification of every linked lesson.

## Reference Map

| Reference | Canonical homes | How it is used |
| --- | --- | --- |
| [Computer Science](https://roadmap.sh/computer-science) | [Foundations](../00-foundations/README.md), [Computer Systems](../01-computer-systems/README.md), [Operating Systems](../02-operating-systems/README.md), [Databases](../08-databases/README.md) | Check conceptual foundations and algorithmic depth |
| [System Design](https://roadmap.sh/system-design) | [System Design](../21-system-design/README.md), [Distributed Systems](../19-distributed-systems/README.md), [SRE](../20-sre/README.md) | Check architecture mechanisms and failure tradeoffs |
| [AWS](https://roadmap.sh/aws) | [Cloud Computing](../10-cloud/README.md), [AWS](../11-aws/README.md) | Connect cloud concepts to service implementations |
| [Python](https://roadmap.sh/python) | [Programming](../05-programming/README.md), [Software Engineering](../06-software-engineering/README.md) | Develop Python beyond small automation scripts |
| [Network Engineer](https://roadmap.sh/network-engineer) | [Networking](../04-networking/README.md), [Linux](../03-linux/README.md) | Extend host networking into network infrastructure |
| [DevOps](https://roadmap.sh/devops) | [Infrastructure as Code](../12-infrastructure-as-code/README.md), [Delivery](../15-ci-cd/README.md), [Observability](../17-observability/README.md), and platform domains | Check operational breadth and alternative implementations |

## Changes from the Review

### Computer Science

Added [Discrete Mathematics](../00-foundations/README.md#discrete-math) and [Algorithm Analysis](../00-foundations/README.md#algorithm-analysis). Expanded existing entries for representations, graph structures, data modeling, and software design. Algorithms build on data structures and mathematical reasoning; individual algorithms remain subtopics.

Specialized tree families, exhaustive algorithm catalogs, and deeper theoretical study remain available through the source. They are not required gates for Linux, cloud, or automation.

### System Design

Added [Content Delivery](../21-system-design/README.md#content-delivery), [Architecture Evolution](../21-system-design/README.md#architecture-evolution), [Service Discovery](../19-distributed-systems/README.md#service-discovery), and [Overload Protection](../19-distributed-systems/README.md#overload-protection). Existing caching, transactions, replication, messaging, and reliability topics remain their canonical homes.

Named architecture patterns are grouped by the problem they solve. An exhaustive pattern catalog is deferred until a concrete design or learning need warrants it.

### AWS

Added a vendor-neutral [Serverless Computing](../10-cloud/README.md#serverless-computing) topic before [AWS Serverless and Edge Delivery](../11-aws/README.md#aws-serverless-edge). Added [Managed Container Deployment](../11-aws/README.md#aws-managed-containers), complementing EKS. Expanded storage lifecycle, caching services, compute quotas, and architecture review coverage.

Email delivery and detailed service configuration remain reference branches. Product names are examples within conceptual groupings, not separate required learning tracks.

### Python

Added [Programming Paradigms](../05-programming/README.md#programming-paradigms), [Python Language Mechanics](../05-programming/README.md#python-language), [Concurrency](../05-programming/README.md#python-concurrency), and [Testing and Tooling](../05-programming/README.md#python-quality). Packaging and automation entries now include representative Python tools.

Framework-specific branches remain choices for later projects. Python uses the canonical testing, packaging, and concurrency concepts rather than duplicating them.

### Network Engineer

Added [Switching and VLANs](../04-networking/README.md#switching-vlans), [Dynamic Routing](../04-networking/README.md#dynamic-routing), [Tunneling and VPNs](../04-networking/README.md#vpn-tunneling), and [Network Automation](../04-networking/README.md#network-automation). Expanded diagnostic tools under troubleshooting.

Wireless, carrier networking, detailed QoS, and certification-specific paths remain source options for a networking specialization. They are not prerequisites for every cloud learner.

### DevOps

The scaffold already covers the central systems, delivery, infrastructure, and operations areas. Added [Service Mesh](../23-advanced/README.md#service-mesh) as a specialization and expanded tool examples inside existing topics for web serving, infrastructure provisioning, GitOps, and telemetry storage.

Alternative vendors, operating systems, and competing tools remain choices. The reference does not imply learning every product or inserting them all into a mandatory sequence.

## Rules for Future Use

- Use these references when categorizing the user's actual topic list and reviewing gaps.
- Preserve all meaningful personal topics, including ones absent from these roadmaps.
- Keep topic IDs stable and link implementations to their conceptual homes.
- Treat source diagrams as guidance; derive prerequisite edges from what understanding actually depends on.
- Prefer official technology documentation for implementation details and version-specific behavior.
- Record any later scope changes here. Deferred reference branches remain discoverable through their original links.

The review adds 18 map-level topics and expands existing scope entries. It adds no detailed notes or tracking features. All six source URLs and pinned inventory links are stored in [curriculum.yaml](../curriculum.yaml); domain maps render their assigned references automatically.
