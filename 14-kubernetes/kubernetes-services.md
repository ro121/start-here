---
id: kubernetes-services
aliases:
- Kubernetes Services
---

# Kubernetes Services

[Domain map](README.md) · [Master curriculum](../CURRICULUM.md)

## Definition

A Kubernetes Service provides a stable network access abstraction for a set of endpoints.

## Why It Matters

It decouples clients from changing Pod addresses.

## Prerequisites

- [[14-kubernetes/README#Kubernetes Networking|Kubernetes Networking]] · [Kubernetes Networking](README.md#kubernetes-networking)
- [[04-networking/README#TCP|TCP]] · [TCP](../04-networking/README.md#tcp)
- [[04-networking/README#Proxies and Load Balancing|Proxies and Load Balancing]] · [Proxies and Load Balancing](../04-networking/README.md#proxies-load-balancing)

## Core Concepts

### Endpoint selection

Selectors commonly identify Pods; EndpointSlices describe endpoints.

### Exposure types

ClusterIP provides cluster-internal access. NodePort exposes a node port. LoadBalancer requests an external balancing implementation.

### Ports

A Service port and the backend targetPort can differ.

## How It Works

For a typical selector-based Service, controllers track matching endpoints. The cluster networking implementation directs traffic to eligible backends. Service DNS helps clients discover access addresses; the Service object itself is not a userspace proxy process.

## Practical Knowledge

Inspect a Service, its selectors, and EndpointSlices, then trace a connection to a listening application port.

## Troubleshooting

Empty endpoints suggest label or readiness issues. Existing endpoints with failed connections suggest application binding, target ports, policy, or the networking implementation.

## Common Confusions

A Service does not replace HTTP routing through Ingress or Gateway API. A LoadBalancer Service requires an implementation. Headless Services use a different discovery pattern from virtual-IP Services.

## Related Topics

- [[04-networking/dns|DNS]] · [DNS](../04-networking/dns.md)
- [[14-kubernetes/README#Kubernetes Pods and Workloads|Kubernetes Pods and Workloads]] · [Kubernetes Pods and Workloads](README.md#kubernetes-pods)
- [[14-kubernetes/README#Kubernetes Ingress and Gateway API|Kubernetes Ingress and Gateway API]] · [Kubernetes Ingress and Gateway API](README.md#kubernetes-ingress)

## Leads To

- [[14-kubernetes/README#Kubernetes Ingress and Gateway API|Kubernetes Ingress and Gateway API]] · [Kubernetes Ingress and Gateway API](README.md#kubernetes-ingress)
- [[14-kubernetes/README#Kubernetes Troubleshooting|Kubernetes Troubleshooting]] · [Kubernetes Troubleshooting](README.md#kubernetes-troubleshooting)

## Technology Implementations

kube-proxy or an alternative service data plane implements forwarding; cloud controllers can provision external load balancers.

## References

[Kubernetes Services](https://kubernetes.io/docs/concepts/services-networking/service/) — semantics, endpoint discovery, and exposure types.
