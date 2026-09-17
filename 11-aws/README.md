# AWS

<!-- Generated map: edit curriculum.yaml, then run scripts/curriculum.py build. -->

[Master curriculum](../CURRICULUM.md) · [Model and editing guide](../CONTRIBUTING.md)

## Purpose

Map transferable cloud concepts onto AWS service boundaries and operational choices.

## Prerequisites

[[10-cloud/README#Cloud Governance and Cost|Cloud Governance and Cost]] · [Cloud Governance and Cost](../10-cloud/README.md#cloud-governance); [[18-security/identity-access|Identity and Access Management]] · [Identity and Access Management](../18-security/identity-access.md)

These orient entry into the domain; each topic below has its own requirements. They are not inherited gates.

## Recommended Learning Order

This is one dependency-compatible reading order. External prerequisites can be learned in parallel; numbering is guidance, not a completion checklist.

1. [AWS Data Services](README.md#aws-data)
2. [AWS IAM and Organizations](README.md#aws-iam)
3. [AWS Operations and Secrets](README.md#aws-operations)
4. [AWS VPC](README.md#aws-vpc)
5. [AWS Compute](README.md#aws-compute)
6. [AWS Traffic and DNS](README.md#aws-traffic)
7. [AWS Messaging](README.md#aws-messaging)
8. [AWS EKS](README.md#aws-eks)

## Major Areas

### Identity and Network Foundation

<a id="aws-iam"></a>
#### AWS IAM and Organizations

**Concepts:** Policies; Roles; Federation; Organizations; Service control policies.

**Prerequisites:** [[10-cloud/README#Cloud Governance and Cost|Cloud Governance and Cost]] · [Cloud Governance and Cost](../10-cloud/README.md#cloud-governance); [[18-security/identity-access|Identity and Access Management]] · [Identity and Access Management](../18-security/identity-access.md)

**Implements / applies:** [[18-security/identity-access|Identity and Access Management]] · [Identity and Access Management](../18-security/identity-access.md)

<a id="aws-vpc"></a>
#### AWS VPC

**Concepts:** Subnets; Route tables; Internet Gateway; NAT Gateway; Security Groups; NACLs.

**Prerequisites:** [[10-cloud/README#Cloud Fundamentals|Cloud Fundamentals]] · [Cloud Fundamentals](../10-cloud/README.md#cloud-fundamentals); [[04-networking/subnetting|Subnetting]] · [Subnetting](../04-networking/subnetting.md); [[04-networking/README#Routing|Routing]] · [Routing](../04-networking/README.md#routing); [[04-networking/README#NAT|NAT]] · [NAT](../04-networking/README.md#nat); [[18-security/README#Network Security|Network Security]] · [Network Security](../18-security/README.md#network-security)

**Implements / applies:** [[04-networking/README#Routing|Routing]] · [Routing](../04-networking/README.md#routing); [[04-networking/subnetting|Subnetting]] · [Subnetting](../04-networking/subnetting.md); [[18-security/README#Network Security|Network Security]] · [Network Security](../18-security/README.md#network-security)

### Compute Data and Traffic

<a id="aws-compute"></a>
#### AWS Compute

**Concepts:** EC2; AMIs; EBS; Auto Scaling; Lambda.

**Prerequisites:** [[11-aws/README#AWS VPC|AWS VPC]] · [AWS VPC](README.md#aws-vpc); [[09-containers/README#Container Fundamentals|Container Fundamentals]] · [Container Fundamentals](../09-containers/README.md#container-fundamentals)

<a id="aws-data"></a>
#### AWS Data Services

**Concepts:** S3; RDS; DynamoDB; Durability; Access patterns.

**Prerequisites:** [[10-cloud/README#Cloud Fundamentals|Cloud Fundamentals]] · [Cloud Fundamentals](../10-cloud/README.md#cloud-fundamentals); [[08-databases/README#Data Modeling|Data Modeling]] · [Data Modeling](../08-databases/README.md#data-modeling); [[08-databases/README#Database Transactions|Database Transactions]] · [Database Transactions](../08-databases/README.md#database-transactions)

<a id="aws-traffic"></a>
#### AWS Traffic and DNS

**Concepts:** ALB; NLB; Route 53; Routing policies.

**Prerequisites:** [[11-aws/README#AWS VPC|AWS VPC]] · [AWS VPC](README.md#aws-vpc); [[04-networking/README#Proxies and Load Balancing|Proxies and Load Balancing]] · [Proxies and Load Balancing](../04-networking/README.md#proxies-load-balancing); [[04-networking/dns|DNS]] · [DNS](../04-networking/dns.md)

**Implements / applies:** [[04-networking/dns|DNS]] · [DNS](../04-networking/dns.md); [[04-networking/README#Proxies and Load Balancing|Proxies and Load Balancing]] · [Proxies and Load Balancing](../04-networking/README.md#proxies-load-balancing)

<a id="aws-messaging"></a>
#### AWS Messaging

**Concepts:** SQS; SNS; Delivery semantics; Dead-letter queues.

**Prerequisites:** [[19-distributed-systems/README#Messaging and Event-Driven Architecture|Messaging and Event-Driven Architecture]] · [Messaging and Event-Driven Architecture](../19-distributed-systems/README.md#messaging); [[10-cloud/README#Cloud Fundamentals|Cloud Fundamentals]] · [Cloud Fundamentals](../10-cloud/README.md#cloud-fundamentals)

**Implements / applies:** [[19-distributed-systems/README#Messaging and Event-Driven Architecture|Messaging and Event-Driven Architecture]] · [Messaging and Event-Driven Architecture](../19-distributed-systems/README.md#messaging)

### Operations and Managed Kubernetes

<a id="aws-operations"></a>
#### AWS Operations and Secrets

**Concepts:** CloudWatch; CloudTrail; Secrets Manager; KMS.

**Prerequisites:** [[11-aws/README#AWS IAM and Organizations|AWS IAM and Organizations]] · [AWS IAM and Organizations](README.md#aws-iam); [[17-observability/README#Telemetry and Observability|Telemetry and Observability]] · [Telemetry and Observability](../17-observability/README.md#telemetry); [[18-security/README#Secrets and Key Management|Secrets and Key Management]] · [Secrets and Key Management](../18-security/README.md#secrets-key-management)

**Implements / applies:** [[17-observability/README#Telemetry and Observability|Telemetry and Observability]] · [Telemetry and Observability](../17-observability/README.md#telemetry); [[18-security/README#Secrets and Key Management|Secrets and Key Management]] · [Secrets and Key Management](../18-security/README.md#secrets-key-management)

<a id="aws-eks"></a>
#### AWS EKS

**Concepts:** Managed control plane; Worker nodes; Network integration; Access; Upgrades.

**Prerequisites:** [[14-kubernetes/README#Kubernetes Cluster Architecture and Operations|Kubernetes Cluster Architecture and Operations]] · [Kubernetes Cluster Architecture and Operations](../14-kubernetes/README.md#kubernetes-cluster-operations); [[11-aws/README#AWS VPC|AWS VPC]] · [AWS VPC](README.md#aws-vpc); [[11-aws/README#AWS IAM and Organizations|AWS IAM and Organizations]] · [AWS IAM and Organizations](README.md#aws-iam)

## Dependency Sketch

Selected direct prerequisite edges, not the entire domain graph. Arrows mean “learn before”.

```mermaid
flowchart TD
    n0["AWS VPC"]
    n1["AWS Compute"]
    n2["AWS Traffic and DNS"]
    n3["AWS IAM and Organizations"]
    n4["AWS Operations and Secrets"]
    n5["AWS EKS"]
    n6["Cloud Governance and Cost"]
    n7["Identity and Access Management"]
    n0 --> n1
    n0 --> n2
    n3 --> n4
    n3 --> n5
    n0 --> n5
    n6 --> n3
    n7 --> n3
```

## Leads To

Specialize further according to real systems and learning needs.
