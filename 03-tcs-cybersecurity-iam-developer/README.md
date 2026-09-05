# TECHCORP — Enterprise Identity & Access Management Case Study

### Assess → Design → Implement

A cybersecurity case study focused on designing a scalable Identity and Access Management (IAM) strategy for a global enterprise with **150,000+ employees across 100+ countries**.

This project was completed as part of the **Tata Consultancy Services (TCS) Cybersecurity IAM Developer Virtual Job Simulation on Forage**, where I worked through an enterprise IAM scenario covering readiness assessment, custom solution design, and implementation planning.

---

## 🎓 Certification

Completed the **TCS Cybersecurity IAM Developer Virtual Job Simulation** on Forage.

[View Certificate](./03-tcs-cybersecurity-iam/certificate/TCS-Cybersecurity-IAM-Developer-Certificate.pdf)
[Verify on Forage ->](https://www.theforage.com/completion-certificates/ifobHAoMjQs9s6bKS/gmf3ypEXBj2wvfQWC_ifobHAoMjQs9s6bKS_6a5dff92ff6af99de17a4adc_1788606690524_completion_certificate.pdf)

---

## Overview

TechCorp is a global technology organization undergoing continued digital expansion across software systems, cloud services, and data repositories.

At this scale, manual identity administration, inconsistent access controls, legacy applications, and growing cloud adoption create significant challenges around:

* Identity lifecycle management
* Unauthorized and excessive access
* Employee onboarding and offboarding
* Privileged access
* Application integration
* Compliance and governance
* User experience and operational efficiency

The objective of this project was to develop an IAM approach that is **secure, scalable, automated, standards-based, and aligned with business processes**.

The project followed three stages:

```text
┌──────────────┐
│   01 ASSESS  │
│ IAM Readiness│
└──────┬───────┘
       │
       ▼
┌──────────────┐
│   02 DESIGN  │
│ Custom IAM   │
│   Solution   │
└──────┬───────┘
       │
       ▼
┌──────────────┐
│ 03 IMPLEMENT │
│ Implementation│
│     Plan     │
└──────────────┘
```

---

# 01 — IAM Readiness Assessment

The first stage focused on determining what TechCorp's IAM environment needed to support a global workforce and rapidly expanding digital environment.

### Assessment Areas

| Area                             | Focus                                                              |
| -------------------------------- | ------------------------------------------------------------------ |
| **User Lifecycle Management**    | Joiner, mover and leaver processes; dormant and orphaned accounts  |
| **Access Control**               | RBAC, least privilege, MFA and privileged access                   |
| **Compliance & Governance**      | Policies, audit trails, access reviews and regulatory requirements |
| **Existing Systems Integration** | Identity repositories, legacy systems, APIs and SIEM               |
| **Cloud Integration**            | SSO, MFA, cloud identity and privileged access                     |
| **User Experience**              | SSO, authentication friction and access-request processes          |

### Assessment Approach

The assessment followed a structured process:

**Document → Review → Identify Gaps → Prioritize → Recommend → Measure**

The resulting recommendations provided the foundation for the solution architecture developed in the next stage.

📄 **[View the IAM Readiness Assessment](./01-assess/iam-readiness-assessment.pdf)**

---

# 02 — Custom IAM Solution Design

The second stage translated the identified requirements into a proposed enterprise IAM architecture.

The design centered around two priorities:

1. **Automated User Lifecycle Management**
2. **Stronger Role-Based Access Control**

The proposed architecture establishes HR as the authoritative identity source and uses a centralized identity platform to manage lifecycle events and access across connected applications.

### Target Architecture

```text
                    ┌─────────────────────┐
                    │         HRIS        │
                    │  Authoritative      │
                    │  Identity Source    │
                    └──────────┬──────────┘
                               │
                         JML Events
                               │
                               ▼
              ┌──────────────────────────────┐
              │ Identity Governance &        │
              │ Lifecycle Engine             │
              └──────────────┬───────────────┘
                             │
                             ▼
                  ┌────────────────────┐
                  │   Central IdP      │
                  │ Microsoft Entra ID │
                  └─────────┬──────────┘
                            │
             ┌──────────────┼──────────────┐
             ▼              ▼              ▼
        SSO Apps       Cloud / SaaS       PAM
             │              │              │
             └──────────────┼──────────────┘
                            ▼
               ┌─────────────────────────┐
               │ Audit Logs + SIEM       │
               │ + Access Reviews        │
               └─────────────────────────┘
```

### Key Security Controls

**Identity Lifecycle**

* Automated Joiner-Mover-Leaver workflows
* HR-driven identity state
* Automated provisioning and deprovisioning
* Dormant/orphan account detection

**Access Control**

* Role-Based Access Control (RBAC)
* Least privilege
* Controlled entitlement workflows
* Segregation of Duties (SoD)
* Periodic access reviews

**Authentication**

* Mandatory MFA
* Conditional access
* Risk-based access decisions
* Phishing-resistant authentication for privileged/high-risk access
* Single Sign-On (SSO)

**Privileged Access**

* Just-in-time elevation
* Approval workflows
* Time-bound permissions
* Privileged session logging

**Integration & Monitoring**

* SCIM 2.0
* SAML 2.0
* OpenID Connect (OIDC)
* OAuth 2.0
* REST/API integrations
* SIEM integration

📄 **[View the Custom IAM Solution Design](./02-design/custom-iam-solution-design.pdf)**

---

# 03 — IAM Platform Implementation Plan

The final stage translated the proposed architecture into a phased implementation roadmap designed to minimize operational disruption while progressively expanding IAM capabilities.

## Implementation Roadmap

| Phase                       |     Timeline | Key Focus                                                     |
| --------------------------- | -----------: | ------------------------------------------------------------- |
| **1. Foundation**           |    Weeks 1–4 | Identity/application inventory, governance and data standards |
| **2. Identity Integration** |   Weeks 5–10 | HRIS integration and JML workflows                            |
| **3. Core Access**          |  Weeks 11–18 | RBAC, SSO, MFA and priority applications                      |
| **4. Governance**           |  Weeks 19–24 | Access reviews, SoD, PAM and remediation                      |
| **5. Scale & Optimise**     | Weeks 25–30+ | Global integrations, policy tuning and continuous improvement |

### Implementation Considerations

The plan also addressed:

* Legacy applications without modern federation or API support
* Inconsistent third-party application standards
* Cloud/SaaS identity sprawl
* Resource and stakeholder requirements
* Security controls
* Success metrics
* Implementation risks and mitigations

The proposed rollout prioritizes **high-risk applications and identity processes first**, allowing the IAM environment to mature incrementally before expanding globally.

📊 **[View the IAM Platform Implementation Plan](./03-implement/iam-platform-implementation-plan.pptx)**

---

# Security Architecture at a Glance

The proposed model brings several security principles together rather than relying on a single control:

```text
                    IDENTITY
                       │
                       ▼
              ┌─────────────────┐
              │     RBAC        │
              │ Least Privilege │
              └────────┬────────┘
                       │
             ┌─────────┴─────────┐
             ▼                   ▼
          MFA / CA              PAM
             │                   │
             └─────────┬─────────┘
                       ▼
                 APPLICATIONS
                       │
                       ▼
             ┌───────────────────┐
             │ Audit + SIEM      │
             │ Access Reviews    │
             └───────────────────┘
```

The underlying principle is simple:

> **Access should follow identity, responsibility and risk — not remain because someone forgot to remove it.**

---

# Key Design Decisions

### HR as the Authoritative Identity Source

Employment and organizational attributes originate from HR, making it the appropriate source for determining identity state and lifecycle changes.

### Automated JML

Automation reduces dependence on manual tickets and administrator memory, particularly important at enterprise scale.

### RBAC + Least Privilege

Business responsibilities are translated into roles, while sensitive access receives additional scrutiny through approval workflows.

### MFA + Conditional Access

Authentication strength and contextual signals can be used to apply stronger controls to sensitive and high-risk access.

### PAM

Privileged access is made temporary and controlled rather than permanently assigned wherever possible.

### Standards-Based Integration

SCIM, SAML, OIDC and OAuth 2.0 reduce reliance on custom integrations and support future application growth.

### Centralized Monitoring

Identity and access events are centralized for security monitoring, investigation and compliance evidence.

---

# Success Metrics

The implementation plan defined measurable indicators for evaluating the effectiveness of the IAM program:

* Percentage of joiners provisioned before their start date
* Time from termination event to identity disablement
* Percentage of applications using SSO and automated provisioning
* MFA coverage
* Number and age of orphaned/dormant accounts
* Access-review completion rate
* Excessive or conflicting entitlement remediation
* Reduction in manual provisioning and IAM-related support activity

---

# Risks Considered

| Risk                          | Mitigation                                            |
| ----------------------------- | ----------------------------------------------------- |
| Poor HR data quality          | Mandatory attributes, validation and ownership        |
| Legacy applications           | API/connector gateway and modernization priorities    |
| Overly broad roles            | Role mining, approvals and periodic reviews           |
| MFA resistance                | SSO, communication and user-friendly authentication   |
| Global regulatory differences | Global baseline with country-specific policy overlays |

---

# Skills Demonstrated

* Identity & Access Management (IAM)
* Identity Governance
* Role-Based Access Control (RBAC)
* Least Privilege
* User Lifecycle Management
* Access Governance
* Privileged Access Management (PAM)
* Multi-Factor Authentication (MFA)
* Conditional Access
* Single Sign-On (SSO)
* Security Architecture
* Enterprise Security
* Risk Assessment
* Security Controls
* IAM Implementation Planning
* Cloud & Application Integration
* Security Monitoring & SIEM

---

# Technologies & Standards

**Identity & Access**

`IAM` · `RBAC` · `PAM` · `MFA` · `SSO` · `Conditional Access`

**Integration**

`SCIM 2.0` · `SAML 2.0` · `OIDC` · `OAuth 2.0` · `REST APIs`

**Security & Governance**

`Least Privilege` · `Access Reviews` · `Segregation of Duties` · `SIEM` · `Audit Logging`

**Reference Platform**

`Microsoft Entra ID`

> Microsoft Entra ID is presented as a practical reference identity provider in the proposed architecture; this project involved solution design and implementation planning rather than deployment of the platform in a production environment.

---

# What I Learned

This project reinforced that enterprise IAM is much more than authentication.

Effective IAM connects **people, business roles, applications, security controls and governance** into one lifecycle.

A technically strong solution still has to answer practical questions:

* Where does identity data originate?
* What happens when someone's role changes?
* What happens when they leave?
* Who approves sensitive access?
* How is privileged access controlled?
* How do legacy applications integrate?
* How do we prove access remains appropriate?
* How does the solution scale across countries and systems?

The most important takeaway for me was the value of designing IAM as part of the **business process itself**, rather than treating it as a separate security layer.

---

# Project Deliverables

| Deliverable        | Description                                                                   |
| ------------------ | ----------------------------------------------------------------------------- |
| **01 — Assess**    | IAM readiness assessment and recommendation framework                         |
| **02 — Design**    | Custom IAM architecture covering lifecycle management and access control      |
| **03 — Implement** | Phased IAM implementation roadmap, resources, risks and success metrics       |
| **Certificate**    | TCS Cybersecurity IAM Developer Virtual Job Simulation completion certificate |

---

# About the Simulation

This case study was completed through the **Tata Consultancy Services (TCS) Cybersecurity IAM Developer Virtual Job Simulation on Forage**.

The TechCorp scenario, requirements and simulation context were provided as part of the program. The documents in this repository represent my completed deliverables and the resulting IAM analysis, solution design and implementation planning.

This repository is intended as a portfolio case study demonstrating my approach to **enterprise IAM assessment, security architecture and implementation planning**.

---

## Certificate

📜 **[View Certificate](./certificate/TCS-Cybersecurity-IAM-Developer-Certificate.pdf)**

---

## Project Structure

```text
tcs-cybersecurity-iam-developer/
│
├── README.md
│
├── certificate/
│   └── TCS-Cybersecurity-IAM-Developer-Certificate.pdf
│
├── 01-assess/
│   ├── README.md
│   └── iam-readiness-assessment.pdf
│
├── 02-design/
│   ├── README.md
│   └── custom-iam-solution-design.pdf
│
├── 03-implement/
│   ├── README.md
│   └── iam-platform-implementation-plan.pptx
│
├── documentation/
│   ├── iam-concepts.md
│   ├── architecture.md
│   ├── security-controls.md
│   ├── implementation-strategy.md
│   └── lessons-learned.md
│
└── assets/
    ├── architecture/
    └── diagrams/
```

---

### Project Focus

**Cybersecurity · Identity & Access Management · Security Architecture · Access Control · Identity Governance · Enterprise Security**

**TCS Cybersecurity IAM Developer Virtual Job Simulation — Forage**
