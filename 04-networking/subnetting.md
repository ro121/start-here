---
id: subnetting
aliases:
- Subnetting
---

# Subnetting

[Domain map](README.md) · [Master curriculum](../CURRICULUM.md)

## Definition

Subnetting divides an address range into smaller prefixes so address allocation and routing can reflect network boundaries.

## Why It Matters

It lets you allocate space deliberately, avoid overlaps, and recognize whether two addresses belong to the same prefix.

## Prerequisites

- [[04-networking/ip-addressing|IP Addressing]] · [IP Addressing](ip-addressing.md)

## Core Concepts

### Prefix length

A /n prefix fixes the first n bits. IPv4 has 32 total bits; IPv6 has 128.

### Boundaries

Subnet ranges align to powers of two. A smaller address range has a longer prefix.

### Address capacity

An IPv4 /26 contains 64 addresses. Usable interface counts depend on network conventions and platform reservations; do not blindly apply one formula everywhere.

## How It Works

Split 192.0.2.0/24 into four /26 ranges: 192.0.2.0/26, 192.0.2.64/26, 192.0.2.128/26, and 192.0.2.192/26. For example, 192.0.2.70 belongs to the second range. Membership follows matching prefix bits.

## Practical Knowledge

Calculate prefix membership, identify overlapping ranges, and reserve growth space before allocating subnets. Explain why IPv6 planning differs from conserving small IPv4 ranges.

## Troubleshooting

Check prefix boundaries when a host unexpectedly treats a peer as local. Look for overlapping allocations before diagnosing VPN or peering route problems.

## Common Confusions

A subnet is an address boundary; a VLAN is a link-layer segmentation mechanism. CIDR notation also describes route aggregates, not only individual subnets.

## Related Topics

- [[04-networking/ip-addressing|IP Addressing]] · [IP Addressing](ip-addressing.md)
- [[11-aws/README#AWS VPC|AWS VPC]] · [AWS VPC](../11-aws/README.md#aws-vpc)

## Leads To

- [[04-networking/README#Routing|Routing]] · [Routing](README.md#routing)
- [[11-aws/README#AWS VPC|AWS VPC]] · [AWS VPC](../11-aws/README.md#aws-vpc)

## Technology Implementations

Linux accepts address prefixes; AWS VPC uses subnet CIDRs. Routers use prefixes for route matching.

## References

[CIDR, RFC 4632](https://www.rfc-editor.org/rfc/rfc4632) — prefix-based allocation and aggregation.
