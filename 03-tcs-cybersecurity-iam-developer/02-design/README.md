# 02 — Custom IAM Solution Design

## Overview

Following the IAM readiness assessment, the second phase translated TechCorp's requirements into a proposed enterprise IAM architecture.

The design addresses two primary priorities:

1. **Automated User Lifecycle Management**
2. **Stronger Role-Based Access Control**

The solution is designed for TechCorp's environment of **150,000+ employees across 100+ countries**, with support for existing applications, cloud services, privileged access and security monitoring.

> **Scope:** This is a solution design proposal created within the TCS Cybersecurity IAM Developer Virtual Job Simulation. Microsoft Entra ID is used as a practical reference identity provider. No production deployment was performed.

---

## Design Objectives

The architecture was designed to provide:

| Requirement           | Design Response                                 |
| --------------------- | ----------------------------------------------- |
| Fast onboarding       | HR-driven automated provisioning                |
| Secure offboarding    | Automated disablement and de-provisioning       |
| Scalable access       | Centralised RBAC and group-based assignment     |
| Least privilege       | Role/attribute-based access with approvals      |
| Strong authentication | MFA + conditional access                        |
| Cloud adoption        | SSO + SCIM + federation protocols               |
| Governance            | Access reviews, audit logs and SIEM integration |

The objective was to create a model that could scale without relying on manual administrator intervention for every identity or access change.

---

# Target IAM Architecture

```text
                    ┌──────────────────────┐
                    │       HRIS           │
                    │ Authoritative Source │
                    └──────────┬───────────┘
                               │
                         JML Events
                               ↓
              ┌────────────────────────────┐
              │ Identity Governance &      │
              │ Lifecycle Engine           │
              └──────────────┬─────────────┘
                             ↓
              ┌────────────────────────────┐
              │ Central Identity Provider  │
              │  Microsoft Entra ID*       │
              └───────┬────────┬───────────┘
                      │        │
              ┌───────┘        └──────────┐
              ↓                           ↓
        SSO Applications              Cloud / SaaS
                                      SCIM Provisioning
              │                           │
              └──────────┬────────────────┘
                         ↓
                Privileged Access
                         │
                         ↓
          ┌──────────────────────────────┐
          │ Central Audit Logs + SIEM    │
          │ + Periodic Access Reviews    │
          └──────────────────────────────┘
```

*Reference implementation; not a production deployment.

The architecture establishes **HR as the authoritative source for workforce identity attributes**. Identity events are processed centrally before access is provisioned to connected systems.

---

# 1. Automated User Lifecycle Management

The proposed solution uses an automated **Joiner–Mover–Leaver (JML)** model.

### Joiner — Onboarding

```text
HR creates employee record
        ↓
IAM validates identity attributes
        ↓
Digital identity created
        ↓
Baseline access assigned
        ↓
Sensitive access → approval
        ↓
SSO + MFA
        ↓
Audit event recorded
```

Baseline access can be determined using attributes such as:

* Department
* Employment type
* Country
* Job role

This allows standard access to be automated while keeping elevated permissions behind an approval process.

---

### Mover — Role Change

When an employee changes department, title, manager or other organisational attributes:

```text
HR attribute change
        ↓
IAM detects change
        ↓
Roles & entitlements recalculated
        ↓
Unjustified access removed
        ↓
New sensitive access → approval
        ↓
Conflicting permissions checked
        ↓
Change recorded for audit
```

The important principle is that **access follows responsibility**.

Employees should not accumulate permissions simply because they previously held a different role.

---

### Leaver — Offboarding

Termination triggers an automated de-provisioning workflow:

```text
Termination recorded in HRIS
        ↓
Identity disabled
        ↓
Sessions / tokens revoked
        ↓
Application access de-provisioned
        ↓
Privileged / VPN / badge access revoked
        ↓
Data ownership transferred
        ↓
Offboarding record retained
```

This directly addresses one of the most significant lifecycle risks: an employee retaining access after leaving the organisation.

---

# 2. RBAC & Least Privilege

RBAC was selected as the primary access-control model because it maps technical permissions to **business responsibilities rather than individual users**.

Example role model:

| Role                 | Typical Access                                   | Risk     |
| -------------------- | ------------------------------------------------ | -------- |
| HR Analyst           | HR applications and approved employee records    | Medium   |
| Software Developer   | Source repositories and development environments | Medium   |
| Finance Analyst      | Finance applications and reporting data          | High     |
| System Administrator | Infrastructure administration                    | Critical |

Higher-risk access is subject to additional approval and privileged-access controls.

### Least Privilege Principle

The design follows:

> **Give users the minimum access required to perform their responsibilities.**

Where roles alone are insufficient, attributes can refine access decisions.

---

# 3. MFA & Conditional Access

MFA is proposed as a mandatory control for workforce identities, with stronger requirements for sensitive and privileged access.

Conditional-access decisions can consider:

* Device compliance
* Location
* Sign-in risk
* Application sensitivity
* Authentication strength

For privileged or high-risk access, the design recommends phishing-resistant authentication such as **FIDO2 security keys or passkeys where feasible**.

This creates a layered approach rather than relying solely on passwords.

---

# 4. Privileged Access Management

Administrative access should not remain permanently assigned where it can be avoided.

The proposed PAM model uses:

* Just-in-time elevation
* Approval workflows
* Strong authentication
* Session logging
* Time-bound permissions

The objective is to reduce **standing privilege** and limit the potential impact of compromised administrator credentials.

---

# 5. Governance & Access Reviews

IAM needs continuous governance, not a one-time configuration.

The design introduces periodic access reviews where managers and resource owners certify that users still require their assigned access.

Additional controls include:

* More frequent reviews for sensitive/privileged access
* Segregation of Duties (SoD)
* Automatic remediation of stale access
* Detection of orphaned and dormant accounts
* Explicit approval for high-risk entitlements

For example, incompatible financial responsibilities should not be assigned to the same user without appropriate controls.

---

# 6. Integration Strategy

The architecture deliberately uses established standards to reduce custom integration effort.

### Standards

* **SCIM 2.0** — automated provisioning
* **SAML 2.0** — federated SSO
* **OpenID Connect (OIDC)** — modern authentication
* **OAuth 2.0** — delegated authorization
* **REST APIs / connectors** — HRIS and application integration

This allows the IAM platform to act as a central identity layer while supporting a heterogeneous enterprise environment.

---

# 7. Audit & Security Monitoring

Significant identity events should be centrally logged, including:

* Authentication attempts
* MFA events
* Privilege elevation
* Role changes
* Provisioning
* De-provisioning
* Access-policy decisions

These logs feed the enterprise **SIEM** to support:

**Detection → Investigation → Compliance → Auditability**

This provides visibility into not only who has access, but also how identity and access decisions are being made.

---

# Key Design Decisions

| Decision                    | Why                                                                    |
| --------------------------- | ---------------------------------------------------------------------- |
| HR as authoritative source  | Employment data originates from the business system responsible for it |
| Centralised IdP             | Provides a single control plane for authentication and policy          |
| JML automation              | Removes dependency on manual tickets and administrator memory          |
| RBAC                        | Maps permissions to business responsibilities                          |
| Least privilege + approvals | Limits unnecessary and high-risk access                                |
| MFA + conditional access    | Adds protection when credentials are compromised                       |
| SCIM / SAML / OIDC          | Enables standards-based application integration                        |
| PAM                         | Reduces standing administrative privilege                              |
| Audit + SIEM                | Provides visibility, traceability and investigation capability         |

---

# Business Alignment

The proposed IAM architecture directly supports TechCorp's business processes:

| Business Process    | IAM Integration                       | Benefit                       |
| ------------------- | ------------------------------------- | ----------------------------- |
| Recruitment         | HR event → identity creation          | Faster employee readiness     |
| Internal transfers  | Attribute change → role recalculation | Access follows responsibility |
| Termination         | HR event → de-provisioning            | Rapid risk reduction          |
| Cloud/SaaS adoption | SSO + SCIM                            | Reduced account sprawl        |
| IT support          | Centralised identity + self-service   | Fewer repetitive tickets      |
| Compliance          | Access reviews + audit trails         | Easier evidence collection    |

The design therefore treats IAM as part of the **business operating model**, rather than as an isolated security system.

---

# Implementation Roadmap

The solution was designed for incremental deployment:

```text
01  Foundation
    ↓
02  Identity Integration
    ↓
03  Core Access
    ↓
04  Governance
    ↓
05  Scale & Optimise
```

This approach allows TechCorp to establish its identity foundation first, integrate HR-driven lifecycle management, introduce core access controls, and then expand governance and application coverage.

The detailed implementation plan is developed in **Task 3**.

---

# Success Metrics

The design proposes measuring:

* Joiners provisioned automatically before their start date
* Time from termination event to identity disablement
* Applications using SSO and automated provisioning
* MFA coverage
* Number and age of orphaned/dormant accounts
* Access-review completion rate
* Excessive/conflicting entitlements remediated
* Reduction in IAM-related support tickets and manual provisioning

These metrics provide a way to determine whether the IAM programme is actually improving security and operational efficiency.

---

# Risks Considered

| Risk                          | Mitigation                                          |
| ----------------------------- | --------------------------------------------------- |
| Poor HR data quality          | Mandatory attributes, validation and ownership      |
| Legacy applications           | APIs, connectors or controlled gateway workflows    |
| Overly broad roles            | Role mining, approvals and periodic reviews         |
| MFA resistance                | SSO, communication and user-friendly authentication |
| Global regulatory differences | Global baseline + country-specific overlays         |

---

# Deliverable

**Task 2 — Custom IAM Solution Design**

The original deliverable is included in this repository:

📄 [`custom-iam-solution-design.pdf`](./custom-iam-solution-design.pdf)

---

# Key Takeaways

This task moved the project from **assessment to architecture**.

The most important design principle was that IAM should be **automated, centralised, risk-aware and connected to business processes**.

The resulting architecture combines:

**HR-driven JML + RBAC + Least Privilege + MFA + PAM + Standards-Based Integration + Governance + SIEM**

Together, these controls provide a scalable foundation for managing identity and access across TechCorp's global environment.

**Next:** Task 3 translates this architecture into a phased implementation plan.
