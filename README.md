# 🛡️ Cloud Security Home Lab v2.0

> A production-inspired Cloud Security & DevSecOps learning roadmap focused on Kubernetes, AKS, CNAPP, Supply Chain Security, Runtime Security, and Platform Engineering.

---

# 🎯 Goal

Build an enterprise-grade Cloud Security Platform from scratch instead of learning isolated tools.

By the end of this project, I will have hands-on experience with:

- Azure Kubernetes Service (AKS)
- GitHub Actions CI/CD
- GitOps (Argo CD)
- Azure Workload Identity
- Azure Key Vault
- HashiCorp Vault
- Runtime Security
- Policy as Code
- Supply Chain Security
- Wiz CNAPP
- Enterprise Kubernetes Security

---

# 🏗️ Final Architecture

```text
                          GitHub

                             │

                   GitHub Actions CI

                             │

          GitLeaks → CodeQL → Trivy → SBOM

                             │

                     Cosign Image Signing

                             │

                        Azure ACR

                             │

                          Argo CD

                             │

                          AKS Cluster

      ┌──────────────────────┼────────────────────────┐
      │                      │                        │
      ▼                      ▼                        ▼
Azure Workload ID      HashiCorp Vault        Azure Key Vault
      │                      │                        │
      ▼                      ▼                        ▼
 CSI Driver           Vault Agent Injector     CSI Driver
      │                      │                        │
      └───────────────┬──────┴───────────────┬────────┘
                      ▼                      ▼
                 Kubernetes Applications

                      │
                      ▼

                  Kyverno Policies

                      │
                      ▼

                  Falco Runtime

                      │
                      ▼

             Prometheus + Grafana

                      │
                      ▼

                     Wiz CNAPP
```

---

# 📚 Module 1 – Secure Kubernetes Foundation ✅

## Objective

Build a secure Kubernetes platform using GitOps and Azure-native authentication.

## Labs

- [x] Azure Kubernetes Service (AKS)
- [x] Azure Container Registry (ACR)
- [x] GitHub Actions CI/CD
- [x] Argo CD GitOps
- [x] Helm
- [x] Kubernetes Namespaces
- [x] Azure Workload Identity
- [x] User Assigned Managed Identity
- [x] Federated Credentials
- [x] Azure Key Vault
- [x] Key Vault Access Policies
- [x] Secrets Store CSI Driver
- [x] Azure Key Vault Provider
- [x] SecretProviderClass
- [x] Mount Key Vault Secret inside Pod

---

## Skills Learned

- GitOps
- Kubernetes
- AKS
- OIDC Authentication
- Managed Identity
- Workload Identity
- Secret Management
- CSI Drivers
- Azure Key Vault
- Kubernetes Authentication
- Authentication Troubleshooting
- Authorization Troubleshooting

---

# 🔐 Module 2 – Enterprise Secret Management

## Objective

Understand why enterprises use HashiCorp Vault alongside Azure Key Vault.

## Labs

- [ ] Install HashiCorp Vault
- [ ] Vault Architecture
- [ ] Kubernetes Authentication
- [ ] Vault Policies
- [ ] Vault KV Secret Engine
- [ ] Vault Agent Injector
- [ ] Dynamic Secrets
- [ ] PostgreSQL Dynamic Credentials
- [ ] Secret Rotation
- [ ] Lease & Renewal
- [ ] Transit Secret Engine
- [ ] PKI Secret Engine

---

## Skills

- Vault
- Kubernetes Auth
- Vault Agent
- Dynamic Secrets
- PKI
- Transit Encryption
- Secret Rotation

---

# 🛡️ Module 3 – Runtime Security

## Objective

Detect attacks running inside Kubernetes.

## Labs

- [ ] Install Falco
- [ ] Runtime Security Rules
- [ ] Detect Reverse Shell
- [ ] Detect Privileged Containers
- [ ] Detect Crypto Miners
- [ ] Detect Container Escape
- [ ] Custom Falco Rules
- [ ] Slack / Teams Alerts

---

## Skills

- Runtime Security
- eBPF
- Threat Detection
- Detection Engineering

---

# 📜 Module 4 – Policy as Code

## Objective

Prevent insecure deployments before they reach production.

## Labs

- [ ] Kyverno
- [ ] Gatekeeper
- [ ] Open Policy Agent (OPA)
- [ ] Admission Controllers

---

## Example Policies

- No latest image tag
- RunAsNonRoot
- ReadOnlyRootFilesystem
- Resource Limits Required
- Approved Image Registry
- Block Privileged Containers

---

## Skills

- Policy as Code
- Kubernetes Governance
- Compliance

---

# 📦 Module 5 – Supply Chain Security

## Objective

Secure the complete software supply chain.

## Labs

- [ ] GitLeaks
- [ ] Trivy
- [ ] Syft
- [ ] SBOM Generation
- [ ] Cosign
- [ ] Image Signature Verification
- [ ] SLSA Overview

---

## Skills

- Image Scanning
- SBOM
- Image Signing
- Software Supply Chain

---

# 🔍 Module 6 – GitHub Advanced Security

## Objective

Shift Security Left.

## Labs

- [ ] CodeQL
- [ ] Dependabot
- [ ] Secret Scanning
- [ ] Branch Protection
- [ ] Required Reviews
- [ ] Required Status Checks

---

## Skills

- SAST
- Dependency Management
- Secure CI/CD

---

# ☁️ Module 7 – Wiz CNAPP

## Objective

Learn Cloud-Native Application Protection Platform.

## Labs

- [ ] CSPM
- [ ] CWPP
- [ ] KSPM
- [ ] CIEM
- [ ] DSPM
- [ ] Vulnerability Management
- [ ] Image Scanning
- [ ] Kubernetes Security
- [ ] Cloud Misconfiguration Labs

---

## Skills

- Wiz
- CNAPP
- Cloud Security
- Kubernetes Security
- Cloud Governance

---

# 🛡️ Module 8 – Microsoft Defender for Cloud

## Objective

Compare Microsoft Defender with Wiz.

## Labs

- [ ] Defender for Containers
- [ ] Defender Recommendations
- [ ] Defender Alerts
- [ ] Secure Score
- [ ] Compare Wiz vs Defender

---

# 🌐 Module 9 – Service Mesh Security

## Objective

Secure Service-to-Service Communication.

## Labs

- [ ] Istio Installation
- [ ] mTLS
- [ ] Authorization Policies
- [ ] Peer Authentication
- [ ] JWT Authentication
- [ ] Ingress Gateway
- [ ] Egress Policies
- [ ] SPIFFE / SPIRE

---

# 🧨 Module 10 – Cloud Attack Simulation

## Objective

Build vulnerable environments and secure them.

## Labs

- [ ] Privileged Pod
- [ ] Public Storage
- [ ] IAM Misconfiguration
- [ ] Container Escape
- [ ] Reverse Shell
- [ ] Crypto Miner
- [ ] Kubernetes Secret Exposure

---

## Skills

- Threat Modeling
- Incident Response
- Cloud Attack Simulation

---

# 🏗️ Module 11 – Terraform Security

## Objective

Secure Infrastructure as Code.

## Labs

- [ ] Checkov
- [ ] tfsec
- [ ] Terrascan
- [ ] OPA on Terraform
- [ ] Drift Detection

---

# 📊 Module 12 – Security Monitoring

## Objective

Observe and investigate security events.

## Labs

- [ ] Prometheus
- [ ] Grafana
- [ ] Loki
- [ ] Fluent Bit
- [ ] Kubernetes Audit Logs
- [ ] OpenTelemetry

---

# 🤖 Module 13 – AI Security

## Objective

Secure AI workloads.

## Labs

- [ ] AI Container Security
- [ ] AI API Protection
- [ ] LLM Secret Management
- [ ] Prompt Injection Basics
- [ ] AI Runtime Security

---

# 🎓 Final Capstone Project

Build a complete enterprise Cloud Security Platform integrating:

- GitHub
- GitHub Actions
- CodeQL
- GitLeaks
- Trivy
- Syft
- Cosign
- Azure Container Registry
- Argo CD
- Azure Kubernetes Service
- Azure Workload Identity
- Azure Key Vault
- HashiCorp Vault
- Secrets Store CSI Driver
- Vault Agent Injector
- Kyverno
- Falco
- Prometheus
- Grafana
- Wiz CNAPP

---

# 🎯 Target Roles

This project prepares for roles such as:

- Cloud Security Engineer
- DevSecOps Engineer
- Platform Security Engineer
- Kubernetes Security Engineer
- CNAPP Engineer
- Container Security Engineer
- Cloud Infrastructure Security Engineer

---

# 📖 Learning Philosophy

Each lab follows the same structure:

1. Problem Statement
2. Business Use Case
3. Architecture
4. Hands-on Implementation
5. Troubleshooting
6. Production Best Practices
7. Interview Questions
8. Resume Talking Points

The goal is not just to deploy tools, but to understand **why** they exist, **how** they integrate into enterprise platforms, and **how to troubleshoot them in production**.

---

# 🚀 Progress

## Module Completion

- ✅ Module 1 – Secure Kubernetes Foundation
- ⏳ Module 2 – Enterprise Secret Management
- ⏳ Module 3 – Runtime Security
- ⏳ Module 4 – Policy as Code
- ⏳ Module 5 – Supply Chain Security
- ⏳ Module 6 – GitHub Advanced Security
- ⏳ Module 7 – Wiz CNAPP
- ⏳ Module 8 – Microsoft Defender for Cloud
- ⏳ Module 9 – Service Mesh Security
- ⏳ Module 10 – Cloud Attack Simulation
- ⏳ Module 11 – Terraform Security
- ⏳ Module 12 – Security Monitoring
- ⏳ Module 13 – AI Security

---

**"Build. Break. Secure. Repeat."** 🔐