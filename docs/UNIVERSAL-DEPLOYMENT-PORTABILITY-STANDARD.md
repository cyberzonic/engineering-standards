# CyberZonic Universal Deployment Portability Standard

Standard ID: CZ-ENG-PORTABILITY-001
Date: 2026-09-29
Status: OWNER_AUTHORIZED_PENDING_INDEPENDENT_REVIEW

## Purpose

This standard implements the CyberZonic universal-product principle: products must remain usable across cloud, private, sovereign, on-premises, edge and future infrastructure while supporting multiple enterprise deployment and DevOps toolchains.

## Mandatory rules

### P1 — Product core neutrality
Product-domain logic MUST NOT require a specific IaC language, CI/CD service, marketplace or cloud provider merely because the first reference deployment uses it.

### P2 — Deployment contract first
Every production-capable CyberZonic product MUST define or inherit a provider-neutral deployment capability contract covering, as applicable: compute/runtime, network/ingress, identity/workload identity, secrets/key management, persistence/database, messaging/events, storage, observability, backup/restore, resilience/rollback, release identity/provenance and security/privacy invariants.

### P3 — Multiple toolchains per cloud
A cloud provider MUST NOT be equated with one deployment language.

Certified or compatible paths may include:
- Azure: Bicep, Terraform, OpenTofu, Pulumi and customer-defined automation.
- AWS: Terraform, OpenTofu, CloudFormation, CDK, Pulumi and customer-defined automation.
- GCP: Terraform, OpenTofu, provider-native/configuration tooling, Pulumi and customer-defined automation.
- Kubernetes/OpenShift: Helm, Kustomize, Operators, GitOps/Crossplane and customer-defined automation.

This list is expandable and non-exclusive.

### P4 — Provider adapters
Provider-specific services SHOULD be accessed through product capability boundaries rather than scattered provider assumptions. Examples include SecretsProvider, IdentityProvider, MessagingProvider, ObjectStorageProvider, ObservabilityProvider and KeyManagementProvider.

### P5 — CI/CD neutrality
Build, validation, migration, deployment and conformance operations SHOULD be exposed as portable commands, APIs, containers or scripts so they can run in GitHub Actions, Azure DevOps, GitLab CI/CD, Jenkins, Bitbucket, Tekton, Argo and customer systems.

### P6 — Conformance is authoritative
A deployment is judged by required outcomes, not by the tool used to create it. Applicable conformance MUST verify security and operational outcomes including private data-plane controls, secrets externalisation, least privilege, TLS/ingress, health/readiness, migrations, backup/restore, rollback, immutable release identity, safe observability and product-specific security invariants.

### P7 — Commercial-channel neutrality
Marketplace or reseller state MUST remain subordinate to CyberZonic commercial authority and MUST NOT directly grant cryptographic, tenant, administrative or infrastructure authority.

### P8 — Support classes
Deployment profiles MUST be identified as CYBERZONIC_CERTIFIED, CYBERZONIC_COMPATIBLE or CUSTOMER_DEFINED. Claims MUST reflect actual evidence.

### P9 — No artificial lock-in
New work MUST NOT create unnecessary dependency on a cloud vendor, IaC engine, CI/CD vendor, marketplace, identity vendor or proprietary managed service when an appropriate capability boundary can preserve portability without reducing security or product quality.

### P10 — Security beats portability
No portability requirement authorises weakening security. Unsupported platforms MUST fail qualification rather than silently receive degraded controls.

## Review gate

Architecture, platform and release review MUST reject a material change that violates P1-P10 unless an approved, independently reviewed exception ADR exists.

## Applicability

This standard applies to AegisVault, VAST, VAST Agent, Chronyx, Mission Control, CyberZonic Intelligence Fabric and future CyberZonic products and services.