# Technical Learning — Curriculum and Knowledge Map

A long-term curriculum for senior DevOps, cloud, and software engineering. This repository organizes understanding: subjects, prerequisites, internal mechanics, practical application, and connections across domains.

Start with the [master curriculum](CURRICULUM.md), then open a domain map. Folder numbers help browsing; they are not a mandatory global sequence. Linux and networking can develop together. Security and observability enter early wherever a topic needs them.

The [roadmap.sh reference review](references/roadmap-sh.md) connects six external roadmaps to this curriculum and records additions, overlaps, and optional branches.

<!-- syllabus:start -->

## Syllabus

Expand a domain to browse **subjects → topics → subtopics**. Domain and topic links open their curriculum maps or notes. This index follows category order; consult topic prerequisites for learning order.

### Domain Index

- [00 · Foundations](#syllabus-foundations)
- [01 · Computer Systems](#syllabus-computer-systems)
- [02 · Operating Systems](#syllabus-operating-systems)
- [03 · Linux](#syllabus-linux)
- [04 · Networking](#syllabus-networking)
- [05 · Programming and Scripting](#syllabus-programming)
- [06 · Software Engineering](#syllabus-software-engineering)
- [07 · Git and Version Control](#syllabus-git)
- [08 · Databases and Data](#syllabus-databases)
- [09 · Virtualization and Containers](#syllabus-containers)
- [10 · Cloud Computing](#syllabus-cloud)
- [11 · AWS](#syllabus-aws)
- [12 · Infrastructure as Code](#syllabus-infrastructure-as-code)
- [13 · Configuration Management](#syllabus-configuration-management)
- [14 · Kubernetes and Container Orchestration](#syllabus-kubernetes)
- [15 · CI-CD](#syllabus-ci-cd)
- [16 · GitOps](#syllabus-gitops)
- [17 · Observability](#syllabus-observability)
- [18 · Security](#syllabus-security)
- [19 · Distributed Systems](#syllabus-distributed-systems)
- [20 · Site Reliability Engineering](#syllabus-sre)
- [21 · System Design](#syllabus-system-design)
- [22 · Production Operations](#syllabus-production-operations)
- [23 · Advanced and Specialization](#syllabus-advanced)

### Phase 0 — Foundations

<a id="syllabus-foundations"></a>
<details>
<summary>00 · Foundations</summary>

[Open Foundations curriculum map](00-foundations/README.md)

- **Computing Literacy**
  - [Computer Fundamentals](00-foundations/README.md#computer-fundamentals)
    - Hardware and software
    - Input and output
    - Binary
    - Bits and bytes
    - Units and encodings
    - Character encodings
    - Unicode
    - Bitwise operations
  - [Discrete Mathematics for Computing](00-foundations/README.md#discrete-math)
    - Logic
    - Sets
    - Relations
    - Combinatorics
    - Probability
    - Proof intuition
- **Programming Basics**
  - [Programming Fundamentals](00-foundations/README.md#programming-fundamentals)
    - Variables
    - Data types
    - Control flow
    - Functions
    - Error handling
  - [Data Structures and Algorithms](00-foundations/README.md#data-structures-algorithms)
    - Arrays
    - Lists
    - Maps
    - Trees
    - Searching
    - Sorting
    - Complexity
    - Stacks
    - Queues
    - Heaps
    - Graphs
    - Hash tables
  - [Algorithm Analysis and Problem Solving](00-foundations/README.md#algorithm-analysis)
    - Asymptotic bounds
    - Time and space tradeoffs
    - Recursion
    - Graph traversal
    - Greedy methods
    - Dynamic programming
    - Complexity classes

</details>

<a id="syllabus-computer-systems"></a>
<details>
<summary>01 · Computer Systems</summary>

[Open Computer Systems curriculum map](01-computer-systems/README.md)

- **Hardware and Execution**
  - [Computer Architecture](01-computer-systems/README.md#computer-architecture)
    - CPU
    - Instruction execution
    - Caches
    - Memory
    - Storage
    - I/O
    - Registers
    - Endianness
    - Floating-point representation
  - [Systems Performance](01-computer-systems/README.md#systems-performance)
    - Locality
    - CPU bottlenecks
    - Memory bandwidth
    - Storage latency

</details>

<a id="syllabus-operating-systems"></a>
<details>
<summary>02 · Operating Systems</summary>

[Open Operating Systems curriculum map](02-operating-systems/README.md)

- **Operating System Mechanics**
  - [Operating System Fundamentals](02-operating-systems/README.md#os-fundamentals)
    - Kernel
    - User space
    - System calls
    - Interrupts
    - Filesystems
  - [Processes and Threads](02-operating-systems/README.md#processes-threads)
    - Process address spaces
    - Threads
    - Scheduling
    - Context switching
  - [Memory Management](02-operating-systems/README.md#memory-management)
    - Virtual memory
    - Paging
    - Allocation
    - Page faults
    - Swap
  - [Concurrency](02-operating-systems/README.md#concurrency)
    - Race conditions
    - Locks
    - Deadlocks
    - Synchronization
    - Parallelism

</details>

### Phase 1 — Systems

<a id="syllabus-linux"></a>
<details>
<summary>03 · Linux</summary>

[Open Linux curriculum map](03-linux/README.md)

- **System Fundamentals**
  - [Linux Filesystem](03-linux/README.md#linux-filesystem)
    - Files
    - Directories
    - Inodes
    - Mounts
    - Paths
    - Package management
  - [Linux Users and Permissions](03-linux/README.md#linux-users-permissions)
    - Users
    - Groups
    - Ownership
    - Mode bits
    - sudo
    - ACLs
  - [Linux Shell](03-linux/README.md#linux-shell)
    - Shell
    - Bash
    - Environment variables
    - Pipes
    - Redirection
    - Exit codes
    - Text manipulation
    - Terminal editors
- **Runtime and Operations**
  - [Linux Processes](03-linux/README.md#linux-processes)
    - Process inspection
    - Threads
    - Signals
    - File descriptors
    - /proc
  - [Linux Services](03-linux/README.md#linux-services)
    - systemd
    - Units
    - Service lifecycle
    - Dependencies
    - Journal logs
  - [Linux Networking](03-linux/README.md#linux-networking)
    - Interfaces
    - Routes
    - Sockets
    - Resolver configuration
    - DNS resolution
    - SSH
  - [Linux Troubleshooting](03-linux/README.md#linux-troubleshooting)
    - Logs
    - CPU saturation
    - Memory pressure
    - Disk exhaustion
    - Socket inspection

</details>

<a id="syllabus-networking"></a>
<details>
<summary>04 · Networking</summary>

[Open Networking curriculum map](04-networking/README.md)

- **Models and Local Links**
  - [OSI Model](04-networking/README.md#osi-model)
    - Layers
    - Encapsulation
    - Model limitations
  - [TCP-IP Model](04-networking/README.md#tcp-ip)
    - Link layer
    - Internet layer
    - Transport layer
    - Application layer
  - [Ethernet](04-networking/README.md#ethernet)
    - Frames
    - MAC addresses
    - Switching
    - ARP
  - [Switching and VLANs](04-networking/README.md#switching-vlans)
    - MAC learning
    - Broadcast domains
    - VLANs
    - Trunks
    - Loop prevention
    - Spanning tree
    - Link aggregation
- **Addressing and Routing**
  - [IP Addressing](04-networking/ip-addressing.md)
    - IP
    - IPv4
    - IPv6
    - Public and private addresses
    - DHCP
  - [Subnetting](04-networking/subnetting.md)
    - CIDR
    - Prefixes
    - Subnet boundaries
    - IPv4 and IPv6 allocation
  - [Routing](04-networking/README.md#routing)
    - Route lookup
    - Longest-prefix match
    - Default gateways
    - Route tables
  - [NAT](04-networking/README.md#nat)
    - Source NAT
    - Destination NAT
    - Connection tracking
    - Port translation
  - [Dynamic Routing](04-networking/README.md#dynamic-routing)
    - Route advertisement
    - Metrics
    - Convergence
    - OSPF
    - BGP
    - Routing policy
- **Transport and Application Protocols**
  - [TCP](04-networking/README.md#tcp)
    - Ports
    - Three-way handshake
    - Sequence numbers
    - Retransmission
    - Flow and congestion control
  - [UDP](04-networking/README.md#udp)
    - Datagrams
    - Ports
    - Loss
    - Application-managed reliability
  - [DNS](04-networking/dns.md)
    - Zones
    - Records
    - Recursive resolution
    - Authoritative servers
    - Caching
    - TTL
  - [HTTP](04-networking/README.md#http)
    - Methods
    - Status codes
    - Headers
    - Caching semantics
    - HTTPS
    - Connection reuse
  - [TLS](04-networking/README.md#tls)
    - Handshake
    - Certificates
    - Peer verification
    - Transport encryption
- **Traffic Management and Diagnosis**
  - [Proxies and Load Balancing](04-networking/README.md#proxies-load-balancing)
    - Forward proxy
    - Reverse proxy
    - L4 and L7 balancing
    - Health checks
    - Web servers
    - NGINX
    - HAProxy
    - Caddy
  - [Network Troubleshooting](04-networking/README.md#network-troubleshooting)
    - Layered diagnosis
    - Packet capture
    - DNS failures
    - Connection timeouts
    - ICMP
    - ping
    - traceroute
    - Wireshark
    - MTU diagnosis
  - [Tunneling and VPNs](04-networking/README.md#vpn-tunneling)
    - Encapsulation
    - Site-to-site access
    - Remote access
    - IPsec
    - Tunnel MTU
    - Route overlap
  - [Network Automation](04-networking/README.md#network-automation)
    - Device APIs
    - Configuration validation
    - NETCONF
    - RESTCONF
    - YANG
    - Configuration backup

</details>

### Phase 2 — Software and Automation

<a id="syllabus-programming"></a>
<details>
<summary>05 · Programming and Scripting</summary>

[Open Programming and Scripting curriculum map](05-programming/README.md)

- **Automation Languages**
  - [Python Automation](05-programming/README.md#python-automation)
    - Functions and modules
    - File I/O
    - Exceptions
    - Environments
    - API clients
    - pathlib
    - subprocess
    - argparse
    - Regular expressions
  - [Shell Automation](05-programming/README.md#shell-automation)
    - Quoting
    - Pipelines
    - Exit handling
    - Script interfaces
    - Safe retries
  - [Programming Paradigms](05-programming/README.md#programming-paradigms)
    - Procedural decomposition
    - Object-oriented modeling
    - Composition
    - Functional transformations
    - Mutable and immutable state
  - [Python Language Mechanics](05-programming/README.md#python-language)
    - Scope
    - Collections
    - Comprehensions
    - Classes
    - Iterators
    - Generators
    - Decorators
    - Context managers
- **Program Runtime**
  - [Program Dependencies and Packaging](05-programming/README.md#program-dependencies)
    - Libraries
    - Dependency resolution
    - Lockfiles
    - Packaging
    - Distribution
    - Virtual environments
    - Package indexes
    - pip
    - uv
    - Lockfile reproducibility
  - [Network Programming](05-programming/README.md#network-programming)
    - Sockets
    - HTTP clients
    - Timeouts
    - Serialization
  - [Python Concurrency](05-programming/README.md#python-concurrency)
    - Threads
    - Processes
    - Async I/O
    - Cancellation
    - Runtime and GIL considerations
    - CPU-bound and I/O-bound work
  - [Python Testing and Tooling](05-programming/README.md#python-quality)
    - Type annotations
    - Static analysis
    - Formatting
    - pytest
    - unittest
    - Fixtures
    - Test isolation
    - pyproject.toml

</details>

<a id="syllabus-software-engineering"></a>
<details>
<summary>06 · Software Engineering</summary>

[Open Software Engineering curriculum map](06-software-engineering/README.md)

- **Design and Delivery Foundations**
  - [Software Lifecycle and Requirements](06-software-engineering/README.md#software-lifecycle)
    - SDLC
    - Requirements
    - Feedback
    - Change management
  - [Software Design Principles](06-software-engineering/README.md#software-design)
    - Architecture
    - Cohesion
    - Coupling
    - SOLID
    - Interface design
    - Design patterns
    - Dependency injection
    - Architecture diagrams
  - [API Design](06-software-engineering/README.md#api-design)
    - REST
    - Contracts
    - Versioning
    - Authentication
    - Authorization
    - Error handling
    - RPC
    - gRPC
    - GraphQL
    - Interface tradeoffs
- **Quality and Distribution**
  - [Software Testing](06-software-engineering/README.md#software-testing)
    - Unit testing
    - Integration testing
    - End-to-end testing
    - Test doubles
  - [Application Diagnostics](06-software-engineering/README.md#application-diagnostics)
    - Structured logging
    - Error context
    - Correlation identifiers

</details>

<a id="syllabus-git"></a>
<details>
<summary>07 · Git and Version Control</summary>

[Open Git and Version Control curriculum map](07-git/README.md)

- **History and Collaboration**
  - [Git Fundamentals](07-git/README.md#git-fundamentals)
    - Working tree
    - Index
    - Commits
    - Remote repositories
    - Tags
  - [Git Branching and Integration](07-git/README.md#git-branching)
    - Branches
    - Merge
    - Rebase
    - Cherry-pick
    - Merge conflicts
  - [Git Workflows](07-git/README.md#git-workflows)
    - Pull requests
    - Reviews
    - Trunk-based development
    - Release branches
- **Internals**
  - [Git Internals](07-git/README.md#git-internals)
    - Objects
    - Trees
    - Refs
    - Commit DAG
    - Reflog

</details>

<a id="syllabus-databases"></a>
<details>
<summary>08 · Databases and Data</summary>

[Open Databases and Data curriculum map](08-databases/README.md)

- **Models and Queries**
  - [Data Modeling](08-databases/README.md#data-modeling)
    - Entities
    - Relationships
    - Keys
    - Relational and document models
    - Normalization
    - Denormalization
    - Key-value and wide-column models
  - [SQL and Indexes](08-databases/README.md#sql-indexes)
    - Queries
    - Joins
    - Index structures
    - Query plans
- **Integrity and Operations**
  - [Database Transactions](08-databases/README.md#database-transactions)
    - ACID
    - Isolation
    - Locking
    - MVCC
  - [Database Operations](08-databases/README.md#database-operations)
    - Migrations
    - Connection pools
    - Backup consistency
    - Restore verification

</details>

### Phase 3 — Infrastructure

<a id="syllabus-containers"></a>
<details>
<summary>09 · Virtualization and Containers</summary>

[Open Virtualization and Containers curriculum map](09-containers/README.md)

- **Isolation and Runtime**
  - [Virtualization](09-containers/README.md#virtualization)
    - Hypervisors
    - Virtual machines
    - Guest kernels
  - [Container Fundamentals](09-containers/README.md#container-fundamentals)
    - Namespaces
    - cgroups
    - Shared kernel
    - OCI
    - Docker
    - Container runtimes
- **Images and Runtime Resources**
  - [Container Images](09-containers/README.md#container-images)
    - Layers
    - Dockerfile
    - ENTRYPOINT
    - CMD
    - Multi-stage builds
    - Registries
  - [Container Storage](09-containers/README.md#container-storage)
    - Writable layers
    - Bind mounts
    - Volumes
    - Persistence
  - [Docker Networking](09-containers/README.md#docker-networking)
    - Network namespaces
    - Bridges
    - Port publishing
    - Embedded DNS
  - [Container Troubleshooting](09-containers/README.md#container-troubleshooting)
    - Exit codes
    - Resource limits
    - Image failures
    - Connectivity failures

</details>

<a id="syllabus-cloud"></a>
<details>
<summary>10 · Cloud Computing</summary>

[Open Cloud Computing curriculum map](10-cloud/README.md)

- **Service and Resource Models**
  - [Cloud Fundamentals](10-cloud/README.md#cloud-fundamentals)
    - Service models
    - Regions
    - Availability zones
    - Shared responsibility
    - Compute
    - Storage
    - Networking
    - Managed databases
  - [Cloud Architecture](10-cloud/README.md#cloud-architecture)
    - Scalability
    - High availability
    - Failure domains
    - Managed services
    - Architecture review
    - Well-Architected tradeoffs
  - [Serverless Computing](10-cloud/README.md#serverless-computing)
    - Managed execution
    - Event triggers
    - Cold starts
    - Concurrency limits
    - Execution constraints
    - Operational ownership
- **Governance and Economics**
  - [Cloud Governance and Cost](10-cloud/README.md#cloud-governance)
    - Account boundaries
    - IAM application
    - Metering
    - Cost allocation
    - Budgets
    - Cloud security

</details>

<a id="syllabus-aws"></a>
<details>
<summary>11 · AWS</summary>

[Open AWS curriculum map](11-aws/README.md)

- **Identity and Network Foundation**
  - [AWS IAM and Organizations](11-aws/README.md#aws-iam)
    - Policies
    - Roles
    - Federation
    - Organizations
    - Service control policies
  - [AWS VPC](11-aws/README.md#aws-vpc)
    - Subnets
    - Route tables
    - Internet Gateway
    - NAT Gateway
    - Security Groups
    - NACLs
- **Compute Data and Traffic**
  - [AWS Compute](11-aws/README.md#aws-compute)
    - EC2
    - AMIs
    - EBS
    - Auto Scaling
    - Lambda
    - Quotas
    - Instance purchase models
    - User data
    - Launch templates
  - [AWS Data Services](11-aws/README.md#aws-data)
    - S3
    - RDS
    - DynamoDB
    - Durability
    - Access patterns
    - S3 lifecycle
    - Storage classes
    - DynamoDB indexes
    - ElastiCache
  - [AWS Traffic and DNS](11-aws/README.md#aws-traffic)
    - ALB
    - NLB
    - Route 53
    - Routing policies
  - [AWS Messaging](11-aws/README.md#aws-messaging)
    - SQS
    - SNS
    - Delivery semantics
    - Dead-letter queues
  - [AWS Managed Container Deployment](11-aws/README.md#aws-managed-containers)
    - ECR
    - ECS
    - Task definitions
    - Services
    - Fargate
    - Capacity and access boundaries
  - [AWS Serverless and Edge Delivery](11-aws/README.md#aws-serverless-edge)
    - Lambda
    - API Gateway
    - EventBridge
    - CloudFront
    - Origin access
    - Cache invalidation
- **Operations and Managed Kubernetes**
  - [AWS Operations and Secrets](11-aws/README.md#aws-operations)
    - CloudWatch
    - CloudTrail
    - Secrets Manager
    - KMS
  - [AWS EKS](11-aws/README.md#aws-eks)
    - Managed control plane
    - Worker nodes
    - Network integration
    - Access
    - Upgrades

</details>

<a id="syllabus-infrastructure-as-code"></a>
<details>
<summary>12 · Infrastructure as Code</summary>

[Open Infrastructure as Code curriculum map](12-infrastructure-as-code/README.md)

- **Conceptual Foundations**
  - [Desired State and Reconciliation](12-infrastructure-as-code/README.md#desired-state)
    - Declarative configuration
    - Observed state
    - Reconciliation
    - Drift
  - [Infrastructure as Code Principles](12-infrastructure-as-code/README.md#infrastructure-as-code-principles)
    - Resource graph
    - Planning
    - Change review
    - Lifecycle
    - Infrastructure ownership
    - CloudFormation
    - Pulumi
    - AWS CDK
- **Terraform Implementation**
  - [Terraform Configuration](12-infrastructure-as-code/README.md#terraform-configuration)
    - Providers
    - Resources
    - Data sources
    - Variables
    - Outputs
    - Locals
    - Dependency graph
    - Lifecycle
  - [Terraform State](12-infrastructure-as-code/terraform-state.md)
    - Resource bindings
    - Remote state
    - State locking
    - Import
    - Drift
    - Sensitive data
  - [Terraform Modules and Environments](12-infrastructure-as-code/README.md#terraform-modules)
    - Modules
    - Contracts
    - Workspaces
    - Environment isolation
  - [Infrastructure Testing and Delivery](12-infrastructure-as-code/README.md#infrastructure-testing)
    - Validation
    - Plan review
    - Policy
    - Terraform CI/CD
    - Integration testing

</details>

<a id="syllabus-configuration-management"></a>
<details>
<summary>13 · Configuration Management</summary>

[Open Configuration Management curriculum map](13-configuration-management/README.md)

- **Configuration Concepts**
  - [Configuration Management Principles](13-configuration-management/README.md#configuration-management-principles)
    - Host configuration
    - Convergence
    - Inventory
    - Configuration drift
- **Ansible Implementation**
  - [Ansible Automation](13-configuration-management/README.md#ansible-automation)
    - Inventory
    - Playbooks
    - Variables
    - Roles
    - Templates
    - Handlers
    - Secrets
    - Ansible automation
  - [Configuration Testing](13-configuration-management/README.md#configuration-testing)
    - Molecule
    - Idempotence tests
    - Check mode limitations
    - Integration environments

</details>

### Phase 4 — Platforms and Delivery

<a id="syllabus-kubernetes"></a>
<details>
<summary>14 · Kubernetes and Container Orchestration</summary>

[Open Kubernetes and Container Orchestration curriculum map](14-kubernetes/README.md)

- **Fundamentals Architecture and Objects**
  - [Kubernetes Architecture](14-kubernetes/README.md#kubernetes-architecture)
    - Orchestration
    - Control plane
    - API server
    - etcd
    - Scheduler
    - Controller manager
    - kubelet
    - kube-proxy
  - [Kubernetes Objects and Access](14-kubernetes/README.md#kubernetes-objects)
    - Objects
    - Namespaces
    - Contexts
    - kubectl
    - Labels
    - Selectors
  - [Kubernetes Pods and Workloads](14-kubernetes/README.md#kubernetes-pods)
    - Pods
    - ReplicaSets
    - Deployments
    - StatefulSets
    - DaemonSets
    - Jobs
    - CronJobs
- **Networking and Storage**
  - [Kubernetes Networking](14-kubernetes/README.md#kubernetes-networking)
    - Pod networking
    - CNI
    - CoreDNS
    - Service discovery
  - [Kubernetes Services](14-kubernetes/kubernetes-services.md)
    - ClusterIP
    - NodePort
    - LoadBalancer
    - EndpointSlices
    - Selectors
  - [Kubernetes Ingress and Gateway API](14-kubernetes/README.md#kubernetes-ingress)
    - Ingress
    - Ingress controllers
    - Gateway API
    - HTTP routing
  - [Kubernetes Storage](14-kubernetes/README.md#kubernetes-storage)
    - CSI
    - Volumes
    - PV
    - PVC
    - StorageClass
    - Access modes
- **Configuration Scheduling and Security**
  - [Kubernetes Configuration](14-kubernetes/README.md#kubernetes-configuration)
    - ConfigMaps
    - Secrets
    - Configuration delivery
    - Rollouts
  - [Kubernetes Scheduling and Resources](14-kubernetes/README.md#kubernetes-scheduling)
    - Taints
    - Tolerations
    - Affinity
    - Requests
    - Limits
    - HPA
    - VPA
  - [Kubernetes Security](14-kubernetes/README.md#kubernetes-security)
    - RBAC
    - ServiceAccounts
    - NetworkPolicy
    - Admission
    - Pod security
- **Diagnosis Extensions and Architecture**
  - [Kubernetes Troubleshooting](14-kubernetes/README.md#kubernetes-troubleshooting)
    - Events
    - Logs
    - Pending Pods
    - Crash loops
    - DNS
    - Storage diagnosis
  - [Kubernetes Extensions](14-kubernetes/README.md#kubernetes-extensions)
    - CRDs
    - Operators
    - Webhooks
    - Controller reconciliation
  - [Kubernetes Cluster Architecture and Operations](14-kubernetes/README.md#kubernetes-cluster-operations)
    - Control-plane availability
    - Upgrades
    - Backup
    - Node maintenance
    - Production operations

</details>

<a id="syllabus-ci-cd"></a>
<details>
<summary>15 · CI-CD</summary>

[Open CI-CD curriculum map](15-ci-cd/README.md)

- **Continuous Integration**
  - [Continuous Integration](15-ci-cd/README.md#ci-fundamentals)
    - Build
    - Test
    - Feedback
    - GitHub Actions
    - GitLab CI
    - Jenkins
    - Runners and agents
  - [Artifact Management](15-ci-cd/README.md#artifact-management)
    - Immutable artifacts
    - Versioning
    - Container build pipelines
    - Promotion
- **Continuous Delivery**
  - [Deployment Strategies](15-ci-cd/README.md#deployment-strategies)
    - Continuous delivery
    - Continuous deployment
    - Rolling deployment
    - Blue-green
    - Canary
    - Rollback
  - [Pipeline Security](15-ci-cd/README.md#pipeline-security)
    - Runner isolation
    - Secrets
    - Permissions
    - Provenance
    - Untrusted contributions

</details>

<a id="syllabus-gitops"></a>
<details>
<summary>16 · GitOps</summary>

[Open GitOps curriculum map](16-gitops/README.md)

- **Principles and Configuration**
  - [GitOps Principles](16-gitops/README.md#gitops-principles)
    - Versioned desired state
    - Pull-based delivery
    - Reconciliation
    - Drift
    - Ownership
    - Flux as an alternative controller
  - [Helm and Kustomize](16-gitops/README.md#helm-kustomize)
    - Charts
    - Values
    - Templates
    - Bases
    - Overlays
    - Rendered configuration
- **Controllers and Diagnosis**
  - [Argo CD](16-gitops/README.md#argo-cd)
    - Application
    - ApplicationSet
    - Sync
    - Sync waves
    - Health
    - Drift
  - [GitOps Troubleshooting](16-gitops/README.md#gitops-troubleshooting)
    - Render failures
    - Sync failures
    - Health checks
    - Competing controllers

</details>

### Phase 5 — Production Engineering

<a id="syllabus-observability"></a>
<details>
<summary>17 · Observability</summary>

[Open Observability curriculum map](17-observability/README.md)

- **Signals and Instrumentation**
  - [Telemetry and Observability](17-observability/README.md#telemetry)
    - Monitoring
    - Metrics
    - Logs
    - Traces
    - Signal context
    - Instrumentation
    - Log aggregation
    - Trace storage
    - Loki
    - Elastic Stack
    - Jaeger
  - [OpenTelemetry](17-observability/README.md#opentelemetry)
    - Instrumentation
    - Context propagation
    - Collectors
    - Exporters
- **Monitoring and Investigation**
  - [Prometheus and Grafana](17-observability/README.md#prometheus-grafana)
    - Scraping
    - Time series
    - Labels
    - PromQL
    - Dashboards
    - Cardinality
  - [Alerting and Incident Investigation](17-observability/README.md#alerting-investigation)
    - Actionable alerts
    - Symptoms
    - Correlation
    - Investigation queries

</details>

<a id="syllabus-security"></a>
<details>
<summary>18 · Security</summary>

[Open Security curriculum map](18-security/README.md)

- **Trust and Identity**
  - [Security Fundamentals](18-security/README.md#security-fundamentals)
    - Threat modeling
    - Least privilege
    - Defense in depth
    - Zero Trust concepts
  - [Identity and Access Management](18-security/identity-access.md)
    - Identity
    - Authentication
    - Authorization
    - IAM
    - RBAC
    - Federation
    - OIDC
    - SAML
  - [Cryptography and PKI](18-security/README.md#pki)
    - Encryption
    - Hashing
    - Signatures
    - Certificates
    - Trust chains
    - PKI
  - [Secrets and Key Management](18-security/README.md#secrets-key-management)
    - Secret lifecycle
    - Rotation
    - Encryption keys
    - Envelope encryption
- **System and Delivery Controls**
  - [Network Security](18-security/README.md#network-security)
    - Firewalls
    - Segmentation
    - Trust boundaries
    - Stateful filtering
  - [Container Security](18-security/README.md#container-security)
    - Image security
    - Runtime privileges
    - Vulnerability management
  - [Supply Chain Security](18-security/README.md#supply-chain-security)
    - Dependency trust
    - SBOM
    - Signing
    - Provenance
    - Vulnerability response
  - [Policy as Code](18-security/README.md#policy-as-code)
    - Policy evaluation
    - OPA
    - Gatekeeper
    - Audit and enforcement

</details>

<a id="syllabus-distributed-systems"></a>
<details>
<summary>19 · Distributed Systems</summary>

[Open Distributed Systems curriculum map](19-distributed-systems/README.md)

- **Failure and State**
  - [Distributed Systems Fundamentals](19-distributed-systems/README.md#distributed-fundamentals)
    - Partial failure
    - Time
    - Network partitions
    - CAP theorem
    - Consistency
    - Availability
    - Partition tolerance
  - [Replication and Consensus](19-distributed-systems/README.md#replication-consensus)
    - Replication
    - Leader election
    - Consensus
    - Quorum
  - [Partitioning and Sharding](19-distributed-systems/README.md#partitioning-sharding)
    - Partition keys
    - Hotspots
    - Rebalancing
    - Ownership
- **Communication and Reliability**
  - [Messaging and Event-Driven Architecture](19-distributed-systems/README.md#messaging)
    - Queues
    - Pub-sub
    - Events
    - Ordering
    - Delivery guarantees
  - [Idempotency](19-distributed-systems/README.md#idempotency)
    - Repeated operations
    - Stable effects
    - Deduplication keys
    - Safe automation
  - [Resilient Communication](19-distributed-systems/README.md#resilient-communication)
    - Timeouts
    - Retries
    - Backoff
    - Jitter
    - Circuit breakers
  - [Distributed Transactions](19-distributed-systems/README.md#distributed-transactions)
    - Atomic commit
    - Sagas
    - Outbox
    - Compensation
  - [Service Discovery](19-distributed-systems/README.md#service-discovery)
    - Naming and registration
    - Endpoint freshness
    - Health
    - Client-side discovery
    - Server-side discovery
  - [Overload Protection](19-distributed-systems/README.md#overload-protection)
    - Backpressure
    - Admission control
    - Rate limiting
    - Load shedding
    - Bulkheads
    - Retry amplification

</details>

<a id="syllabus-sre"></a>
<details>
<summary>20 · Site Reliability Engineering</summary>

[Open Site Reliability Engineering curriculum map](20-sre/README.md)

- **Reliability Foundations**
  - [Reliability Fundamentals](20-sre/README.md#reliability-fundamentals)
    - Reliability
    - Availability
    - Failure domains
    - Redundancy
  - [Reliability Objectives](20-sre/README.md#reliability-objectives)
    - SLI
    - SLO
    - SLA
    - Error budgets
    - User journeys
- **Capacity and Resilience**
  - [Capacity and Performance](20-sre/README.md#capacity-performance)
    - Capacity planning
    - Saturation
    - Scaling
    - Performance
    - Load tests
  - [Resilience Engineering](20-sre/README.md#resilience-engineering)
    - Resilience
    - Chaos engineering
    - Hypotheses
    - Blast radius
    - Recovery verification

</details>

<a id="syllabus-system-design"></a>
<details>
<summary>21 · System Design</summary>

[Open System Design curriculum map](21-system-design/README.md)

- **Requirements and Estimation**
  - [System Design Method](21-system-design/README.md#system-design-method)
    - Functional requirements
    - Non-functional requirements
    - Latency
    - Throughput
    - Capacity estimation
    - High-level architecture
    - Low-level design
    - Tradeoffs
- **Architecture Patterns and Tradeoffs**
  - [Caching](21-system-design/README.md#caching)
    - Cache keys
    - Invalidation
    - TTL
    - Eviction
    - Stampedes
  - [Scalable Architecture](21-system-design/README.md#scalable-architecture)
    - Horizontal scaling
    - Vertical scaling
    - Databases
    - Load balancing
    - Queues
    - Event-driven systems
    - Replication
    - Consistency
    - Failure modes
  - [Content Delivery and Edge Caching](21-system-design/README.md#content-delivery)
    - Origin and edge
    - Cache keys
    - Invalidation
    - TTL
    - Static content
    - Regional delivery
  - [Architecture Evolution](21-system-design/README.md#architecture-evolution)
    - Modular monoliths
    - Microservice boundaries
    - Strangler migration
    - CQRS
    - Event sourcing
    - Distributed complexity

</details>

<a id="syllabus-production-operations"></a>
<details>
<summary>22 · Production Operations</summary>

[Open Production Operations curriculum map](22-production-operations/README.md)

- **Readiness and Change**
  - [Operational Readiness](22-production-operations/README.md#operational-readiness)
    - Runbooks
    - Ownership
    - On-call
    - Handoffs
    - Safe changes
  - [Backup and Disaster Recovery](22-production-operations/README.md#backup-recovery)
    - Backup
    - Restore
    - Recovery
    - RPO
    - RTO
    - Disaster recovery
    - Restore exercises
- **Response and Learning**
  - [Incident Management](22-production-operations/README.md#incident-management)
    - Triage
    - Coordination
    - Communication
    - Mitigation
    - RCA
    - Blameless learning

</details>

### Phase 6 — Specialization

<a id="syllabus-advanced"></a>
<details>
<summary>23 · Advanced and Specialization</summary>

[Open Advanced and Specialization curriculum map](23-advanced/README.md)

- **Specialization Paths**
  - [Platform Engineering](23-advanced/README.md#platform-engineering)
    - Self-service interfaces
    - Golden paths
    - Platform contracts
    - Developer experience
  - [Systems Performance Specialization](23-advanced/README.md#performance-specialization)
    - Profiling
    - Workload characterization
    - Cross-layer bottlenecks
  - [Service Mesh](23-advanced/README.md#service-mesh)
    - Service-to-service traffic policy
    - Workload identity
    - Mutual TLS
    - Traffic telemetry
    - Istio
    - Linkerd
    - Operational cost

</details>
<!-- syllabus:end -->

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

[curriculum.yaml](curriculum.yaml) owns hierarchy, stable IDs, ordering, prerequisites, and conceptual relationships. The syllabus above, [dependencies.yaml](dependencies.yaml), the master curriculum, and domain maps are generated from it. Individual topic notes are authored Markdown and are never overwritten by the generator.

See the [editing and model guide](CONTRIBUTING.md) for validation, future topic-list integration, and Obsidian migration. Open this repository folder as an Obsidian vault when ready; no database export or plugin is required to read it. This scaffold deliberately contains no progress tracking or schedules.
