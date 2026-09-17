---
id: identity-access
aliases:
- Identity and Access Management
---

# Identity and Access Management

[Domain map](README.md) · [Master curriculum](../CURRICULUM.md)

## Definition

Identity and access management establishes who or what is acting and which actions that principal may perform.

## Why It Matters

It provides a consistent way to reason about human and workload access across hosts, cloud APIs, and clusters.

## Prerequisites

- [[18-security/README#Security Fundamentals|Security Fundamentals]] · [Security Fundamentals](README.md#security-fundamentals)

## Core Concepts

### Authentication

Authentication establishes a principal using evidence such as credentials or a federated assertion.

### Authorization

Authorization evaluates whether a principal may act on a resource in a given context.

### Access models

Roles group permissions; policies describe decisions. Federation connects trust domains. OIDC and SAML are protocols used in identity federation, not universal authorization models.

## How It Works

A request carries identity evidence. The receiving system verifies it, establishes a principal, and evaluates access policy for the requested action and resource. The system should record enough context to investigate the decision.

## Practical Knowledge

Identify the principal, action, resource, and relevant policy. Design scoped workload identities and explain credential expiry, delegation, and least privilege.

## Troubleshooting

Separate failed identity verification from denied permission. Inspect token expiry, audience, role assumptions, policy scope, and the effective principal before broadening access.

## Common Confusions

Successful login does not grant every action. An identity, credential, role, and session are different objects. Similar IAM terminology does not imply identical policy evaluation rules across systems.

## Related Topics

- [[03-linux/README#Linux Users and Permissions|Linux Users and Permissions]] · [Linux Users and Permissions](../03-linux/README.md#linux-users-permissions)
- [[11-aws/README#AWS IAM and Organizations|AWS IAM and Organizations]] · [AWS IAM and Organizations](../11-aws/README.md#aws-iam)
- [[14-kubernetes/README#Kubernetes Security|Kubernetes Security]] · [Kubernetes Security](../14-kubernetes/README.md#kubernetes-security)
- [[18-security/README#Secrets and Key Management|Secrets and Key Management]] · [Secrets and Key Management](README.md#secrets-key-management)

## Leads To

- [[03-linux/README#Linux Users and Permissions|Linux Users and Permissions]] · [Linux Users and Permissions](../03-linux/README.md#linux-users-permissions)
- [[06-software-engineering/README#API Design|API Design]] · [API Design](../06-software-engineering/README.md#api-design)
- [[10-cloud/README#Cloud Governance and Cost|Cloud Governance and Cost]] · [Cloud Governance and Cost](../10-cloud/README.md#cloud-governance)
- [[11-aws/README#AWS IAM and Organizations|AWS IAM and Organizations]] · [AWS IAM and Organizations](../11-aws/README.md#aws-iam)
- [[14-kubernetes/README#Kubernetes Security|Kubernetes Security]] · [Kubernetes Security](../14-kubernetes/README.md#kubernetes-security)
- [[18-security/README#Secrets and Key Management|Secrets and Key Management]] · [Secrets and Key Management](README.md#secrets-key-management)
- [[18-security/README#Network Security|Network Security]] · [Network Security](README.md#network-security)
- [[18-security/README#Policy as Code|Policy as Code]] · [Policy as Code](README.md#policy-as-code)

## Technology Implementations

Linux users and groups, AWS IAM, Kubernetes RBAC, Vault policies, and Keycloak federation apply different parts of this model.

## References

[AWS IAM introduction](https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html) — one concrete implementation of identities and access policies; compare its semantics with host and cluster access.
