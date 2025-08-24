+++
date = '2025-08-09T09:41:41+05:30'
draft = false
title = 'Kubernetes'
categories = ['DevOps']
+++
## Introduction
- Automated deployment, scaling, management
- Pods: Smallest deployable compute object in kubernetes
- Services: exposes an app running on a set of pods
- Automated rollouts/ rollbacks
- Storage orchestration: local/ network/ public cloud
- Horizontal scaling: metrics/ commands
- Automated bin packaging
- Secret and configuration management
- IPv4/ IPv6 stack
- Batch/ continuous integration workloads
- Self-healing
- Service discovery and load balancing
- Extensibility

## Kubernetes Control Plane
- kube-api-server: All communications in cluster utilize this API
- etcd: Distributed key-value store containing all cluster data (deployment configs, desired states, meta data etc)
- kube-scheduler: assigns new pods to nodes
- kube-controller-manager: Monitor and control cluster state
- cloud-controller-manager: interact with cloud providers. Link clusters to cloud provider’s API

## Kubernetes Worker Plane
- kubelet-communicates with kube-api-server
- Container runtime: Docker, podman, etc
- Kube-proxy: Network proxy
- Node: Worker machine (physical/ virtual)
