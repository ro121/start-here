---
id: terraform-state
aliases:
- Terraform State
---

# Terraform State

[Domain map](README.md) · [Master curriculum](../CURRICULUM.md)

## Definition

Terraform state records bindings between declared resource instances and remote objects.

## Why It Matters

Correct bindings let Terraform plan changes against the objects it manages.

## Prerequisites

- [[12-infrastructure-as-code/README#Terraform Configuration|Terraform Configuration]] · [Terraform Configuration](README.md#terraform-configuration)

## Core Concepts

### Bindings

Resource addresses map to remote identities.

### Shared state

A remote backend shares state; locking support depends on the backend.

### Drift and import

Drift is divergence from intended configuration. Import establishes a binding to an existing object; configuration must still describe the intended result.

## How It Works

Planning compares configuration with information from state and providers. Applying changes updates infrastructure and records resulting bindings. A failed operation requires inspecting both remote objects and state before retrying.

## Practical Knowledge

Inspect bindings, review plans, select a backend, and practice recovery in a disposable environment. Protect state because it can contain secrets.

## Troubleshooting

Investigate unexpected replacement plans through resource addresses, configuration changes, and provider behavior. Before handling a stale lock, verify that no operation is still running.

## Common Confusions

State is neither the desired configuration nor an infrastructure backup. A workspace is not automatically a strong security boundary.

## Related Topics

- [[12-infrastructure-as-code/README#Desired State and Reconciliation|Desired State and Reconciliation]] · [Desired State and Reconciliation](README.md#desired-state)
- [[18-security/README#Secrets and Key Management|Secrets and Key Management]] · [Secrets and Key Management](../18-security/README.md#secrets-key-management)

## Leads To

- [[12-infrastructure-as-code/README#Terraform Modules and Environments|Terraform Modules and Environments]] · [Terraform Modules and Environments](README.md#terraform-modules)

## Technology Implementations

Terraform implements resource bindings and backend-based persistence; backend choice determines available locking and storage controls.

## References

[Terraform state](https://developer.hashicorp.com/terraform/language/state) — state model. [State backends](https://developer.hashicorp.com/terraform/language/state/backends) — storage and locking behavior.
