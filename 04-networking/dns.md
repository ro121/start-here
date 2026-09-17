---
id: dns
aliases:
- DNS
---

# DNS

[Domain map](README.md) · [Master curriculum](../CURRICULUM.md)

## Definition

DNS is a distributed naming system that publishes typed records in a hierarchical namespace.

## Why It Matters

Names let applications discover endpoints without hard-coding addresses. Understanding resolution separates naming failures from transport failures.

## Prerequisites

- [[04-networking/README#UDP|UDP]] · [UDP](README.md#udp)
- [[04-networking/README#TCP|TCP]] · [TCP](README.md#tcp)

## Core Concepts

### Authority

A zone has authoritative servers responsible for its records.

### Recursion

A recursive resolver follows referrals on behalf of a client.

### Caching

TTL influences how long a cached answer can be reused. A changed authoritative answer does not instantly replace every cached copy.

## How It Works

A client asks its configured resolver for a record. If a usable cached answer is absent, the resolver follows the namespace hierarchy to authoritative data, returns the answer, and caches it according to DNS rules.

## Practical Knowledge

Use dig to compare answers from the configured resolver and an authoritative server. Explain A, AAAA, CNAME, and NS records, and separate authority from recursion.

## Troubleshooting

Distinguish NXDOMAIN from a timeout or server failure. Compare resolver configuration, response codes, and cached answers before assuming that the application endpoint is down.

## Common Confusions

DNS resolution is not an HTTP redirect and does not test endpoint health. DNS-based traffic policies are distinct from a proxy that forwards application connections.

## Related Topics

- [[04-networking/README#HTTP|HTTP]] · [HTTP](README.md#http)
- [[14-kubernetes/README#Kubernetes Networking|Kubernetes Networking]] · [Kubernetes Networking](../14-kubernetes/README.md#kubernetes-networking)
- [[11-aws/README#AWS Traffic and DNS|AWS Traffic and DNS]] · [AWS Traffic and DNS](../11-aws/README.md#aws-traffic)

## Leads To

- [[03-linux/README#Linux Networking|Linux Networking]] · [Linux Networking](../03-linux/README.md#linux-networking)
- [[04-networking/README#HTTP|HTTP]] · [HTTP](README.md#http)
- [[04-networking/README#Network Troubleshooting|Network Troubleshooting]] · [Network Troubleshooting](README.md#network-troubleshooting)
- [[11-aws/README#AWS Traffic and DNS|AWS Traffic and DNS]] · [AWS Traffic and DNS](../11-aws/README.md#aws-traffic)
- [[14-kubernetes/README#Kubernetes Networking|Kubernetes Networking]] · [Kubernetes Networking](../14-kubernetes/README.md#kubernetes-networking)

## Technology Implementations

Linux resolvers consume DNS; CoreDNS provides DNS services in many Kubernetes clusters; Route 53 provides AWS DNS services. These are applications of the same naming model.

## References

[DNS concepts, RFC 1034](https://www.rfc-editor.org/rfc/rfc1034) — naming, authority, and resolution. Consult its listed updates for protocol refinements.
