---
name: Kubernetes
description: Production-ready guidance for designing, deploying, operating, and reviewing Kubernetes workloads.
version: 1.0.0
tags:
  - kubernetes
  - devops
  - platform
  - containers
  - cloud-native
---

# Purpose

Provide a structured engineering framework for building, deploying, securing,
and operating Kubernetes workloads in production.

This skill extends the Engineering Workflow foundation.

# Relationship to Engineering Workflow

Apply after architecture and implementation are complete to assess deployment,
operations, scalability, and production readiness.

# When to Use

- Designing Kubernetes platforms
- Reviewing manifests
- Production readiness reviews
- Troubleshooting clusters
- Capacity planning
- GitOps workflows
- CI/CD integration
- Security audits

# Objectives

- Reliable deployments
- Secure workloads
- Predictable scaling
- Observable systems
- Maintainable manifests
- Repeatable operations

# Core Principles

## Declarative Infrastructure

Treat manifests as the source of truth.

## Immutable Deployments

Replace workloads rather than modifying running containers.

## Least Privilege

Grant only required permissions.

## Small, Focused Services

Avoid monolithic deployments.

## Observability First

Metrics, logs and traces are mandatory.

# Cluster Organization

Prefer:

- Multiple namespaces
- Resource quotas
- Limit ranges
- Labels
- Annotations

Avoid deploying everything into the default namespace.

# Workloads

## Pods

- One responsibility
- Health probes
- Resource requests
- Resource limits

Avoid long-lived debug containers.

## Deployments

Review:

- Replica count
- Rolling updates
- Revision history
- Selector consistency

## StatefulSets

Use for stateful applications requiring stable identities.

## DaemonSets

Reserve for node-level services.

## Jobs

Use for finite workloads.

## CronJobs

Ensure idempotent execution.

# Services

Review:

- ClusterIP
- NodePort
- LoadBalancer
- Headless Services

Verify port mappings.

# Ingress

Review:

- TLS
- Routing
- Host rules
- Path matching
- Timeouts

# Configuration

## ConfigMaps

Store non-sensitive configuration.

## Secrets

Store credentials.

Never hardcode secrets into images or manifests.

# Storage

Review:

- PersistentVolumes
- PersistentVolumeClaims
- StorageClasses
- Backup strategy

# Networking

Review:

- Network Policies
- DNS
- Service discovery
- Ingress rules
- Egress restrictions

Default deny where practical.

# Security

Review:

- RBAC
- Service Accounts
- Pod Security
- Image provenance
- Admission policies
- Secret management

Containers should:

- Run as non-root
- Drop unnecessary capabilities
- Use read-only root filesystems where possible

# Resource Management

Every workload should define:

- CPU requests
- CPU limits
- Memory requests
- Memory limits

Prevent noisy neighbors.

# Health Probes

Implement:

- Startup Probe
- Readiness Probe
- Liveness Probe

Avoid identical probe definitions.

# Autoscaling

Review:

- Horizontal Pod Autoscaler
- Vertical Pod Autoscaler
- Cluster Autoscaler

Scale using meaningful metrics.

# Helm

Use Helm for reusable deployments.

Review:

- Values
- Templates
- Defaults
- Documentation

Avoid excessive template complexity.

# GitOps

Recommended workflow:

Developer
↓

Git Repository
↓

Pull Request
↓

Review
↓

Merge
↓

GitOps Controller
↓

Cluster

Keep manual changes out of production.

# CI/CD

Validate:

- Linting
- Unit tests
- Image scanning
- Manifest validation
- Policy validation
- Deployment verification

# Observability

Implement:

- Metrics
- Centralized logging
- Distributed tracing
- Dashboards
- Alerts

Monitor:

- CPU
- Memory
- Restarts
- Latency
- Error rates

# Logging

Prefer structured logs.

Avoid sensitive information.

# Monitoring

Review:

- Prometheus metrics
- Alert thresholds
- Dashboard coverage

# Backup

Document:

- Backup frequency
- Restore testing
- Recovery objectives

# Disaster Recovery

Define:

- RPO
- RTO
- Failover strategy
- Rollback strategy

# Performance

Review:

- Scheduling
- Bin packing
- Image size
- Startup time
- Network latency

# Troubleshooting Workflow

1. Verify workload status.
2. Review events.
3. Inspect logs.
4. Check probes.
5. Verify networking.
6. Validate storage.
7. Review metrics.
8. Inspect recent deployments.

# Manifest Review Checklist

- API version current
- Labels consistent
- Resources defined
- Probes configured
- Secrets externalized
- RBAC minimal
- Images pinned
- Pull policy appropriate
- Namespaces explicit

# Common Pitfalls

- Using latest image tags
- Missing limits
- Missing probes
- Excessive privileges
- Manual production changes
- Ignoring events
- Unbounded storage
- Weak monitoring

# Best Practices

- GitOps
- Infrastructure as Code
- Immutable deployments
- Automated rollback
- Progressive delivery
- Small container images
- Regular upgrades
- Policy enforcement

# Output Format

## Summary

Overall deployment assessment.

## Strengths

Positive observations.

## Findings

Each finding includes:

- Severity
- Resource
- Description
- Impact
- Recommendation

## Security Review

Assessment.

## Reliability Review

Assessment.

## Scalability Review

Assessment.

## Operational Readiness

Assessment.

## Final Recommendation

- Production Ready
- Ready with Changes
- Not Ready

# Validation Checklist

- Images trusted
- Resources defined
- Probes configured
- Secrets managed
- RBAC reviewed
- Policies enforced
- Monitoring enabled
- Logging centralized
- Backup documented
- Recovery tested

# Success Criteria

A successful Kubernetes deployment:

- Is reproducible
- Is observable
- Is secure
- Scales predictably
- Recovers gracefully
- Supports automation
- Minimizes operational risk

# Composition

Use with:

- Engineering Workflow
- Python Review
- React Development
- Technical Writing

Production readiness should be evaluated alongside application quality,
documentation, and operational procedures.
