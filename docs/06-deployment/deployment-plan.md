# Deployment Plan

| | |
|---|---|
| **Status** | ⏳ Not started |
| **Phase** | 20 — Deployment |
| **Depends on** | [Architecture](../03-design/architecture.md) |

---

## Purpose

Describe how VeriGlow-ai moves from a developer's machine to users, safely and repeatably.

## Environments (proposed)

| Environment | Purpose | Deployed from |
|---|---|---|
| Local | Development | Developer machine |
| Staging | Pre-release verification | `main` |
| Production | Real users | Tagged release |

## Sections (to be completed)

1. Hosting choice — with a linked ADR
2. CI/CD pipeline
3. Configuration and secrets management
4. Database migrations during deployment
5. Monitoring, logging, and alerting
6. Rollback procedure
7. Cost estimate

## Guiding Principle

Start with the **simplest** hosting that is reliable and affordable for an MVP. Add infrastructure complexity only when a measured need justifies it.
