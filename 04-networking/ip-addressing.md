---
id: ip-addressing
aliases:
- IP Addressing
---

# IP Addressing

[Domain map](README.md) · [Master curriculum](../CURRICULUM.md)

## Definition

IP addressing assigns network-layer addresses to interfaces so packets can identify destinations across connected networks.

## Why It Matters

Addressing underlies subnet design, route selection, and diagnosis of unreachable services.

## Prerequisites

- [[04-networking/README#TCP-IP Model|TCP-IP Model]] · [TCP-IP Model](README.md#tcp-ip)

## Core Concepts

### Address families

IPv4 uses 32-bit addresses; IPv6 uses 128-bit addresses. Both use prefixes to describe address ranges.

### Address scope

An address may have local or broader scope. An address alone does not prove that a route or access policy permits traffic.

### Assignment

Static configuration and dynamic assignment are different management choices; DHCP is one dynamic configuration mechanism.

## How It Works

A sender chooses a destination address. Its routing table determines whether to reach that destination on a directly connected link or through a next hop. The IP address remains conceptually distinct from the link-layer address used for local delivery.

## Practical Knowledge

Read interface addresses and prefix lengths. Distinguish loopback, private IPv4, link-local, and globally routable addresses. Explain why an interface can have multiple addresses.

## Troubleshooting

Inspect the assigned address, prefix, and route before changing DNS. Duplicate addresses, incorrect prefixes, and missing routes can all appear as connectivity failures.

## Common Confusions

A MAC address identifies a link-layer interface context; an IP address supports network-layer forwarding. A private address does not itself provide a firewall.

## Related Topics

- [[04-networking/README#Ethernet|Ethernet]] · [Ethernet](README.md#ethernet)
- [[18-security/README#Network Security|Network Security]] · [Network Security](../18-security/README.md#network-security)

## Leads To

- [[04-networking/subnetting|Subnetting]] · [Subnetting](subnetting.md)
- [[04-networking/README#TCP|TCP]] · [TCP](README.md#tcp)
- [[04-networking/README#UDP|UDP]] · [UDP](README.md#udp)

## Technology Implementations

Linux interfaces and AWS VPC subnets apply IP addressing. Kubernetes assigns Pod addresses through its networking implementation.

## References

[IPv6 specification, RFC 8200](https://www.rfc-editor.org/rfc/rfc8200) — packet and addressing context for IPv6.
