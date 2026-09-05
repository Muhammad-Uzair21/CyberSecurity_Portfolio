# 01 — IAM Readiness Assessment

## Overview

The first phase of the TechCorp IAM engagement focused on assessing whether the organisation was ready for a scalable, secure Identity and Access Management (IAM) transformation.

TechCorp operates across **100+ countries with 150,000+ employees**, alongside a growing environment of cloud services, proprietary systems and digital applications. At this scale, fragmented identity processes and inconsistent access controls can create security exposure, operational overhead and poor user experience.

The assessment therefore focused on six areas critical to enterprise IAM readiness:

* User Lifecycle Management
* Access Control
* Compliance & Governance
* Existing Systems Integration
* Cloud Integration
* User Experience

The objective was not simply to identify security weaknesses, but to determine what an IAM solution would need to support TechCorp's business processes and future growth.

---

## Assessment Approach

The assessment followed a structured progression:

```text
Current IAM Environment
        ↓
Business & Security Requirements
        ↓
IAM Readiness Gaps
        ↓
Risk & Business Impact
        ↓
Recommendations
        ↓
Implementation Roadmap
```

The checklist was designed to establish a baseline before proposing the target IAM architecture.

---

## 1. User Lifecycle Management

A central question was whether TechCorp could reliably manage identities throughout the employee lifecycle.

### Areas assessed

* Automated employee onboarding
* Role and department changes
* Immediate offboarding
* Dormant and inactive account detection
* Orphaned account removal
* Access changes following changes in responsibility

### Why it matters

Manual Joiner–Mover–Leaver processes create opportunities for access to remain active after an employee's role changes or employment ends.

At TechCorp's scale, lifecycle management needs to be **automated and driven by authoritative employee information**, rather than depending on administrators to manually update every connected system.

---

## 2. Access Control

The assessment examined whether access was being granted according to business responsibility and security requirements.

### Areas assessed

* Role-Based Access Control (RBAC)
* Least privilege
* Multi-Factor Authentication (MFA)
* Privileged access controls
* Excessive permissions
* Authentication and authorization
* Access logging and monitoring

### Key consideration

The goal was to move away from individually managed permissions toward **consistent, role-based and policy-driven access**.

Sensitive and privileged access should receive additional controls rather than being treated like ordinary workforce access.

---

## 3. Compliance & Governance

IAM must provide sufficient visibility and control to support TechCorp's regulatory and governance requirements across multiple countries.

### Areas assessed

* IAM policies
* Regulatory and industry requirements
* Audit trails
* Log retention
* Privileged activity monitoring
* Access reviews
* Approved exceptions
* Periodic audits

### Key consideration

Security controls are difficult to govern when access decisions cannot be traced.

The assessment therefore considered not only **who has access**, but also whether TechCorp could demonstrate **why that access exists and how it is being monitored**.

---

## 4. Existing Systems Integration

TechCorp's IAM platform would need to coexist with existing applications, identity repositories and potentially legacy systems.

### Areas assessed

* Application and system inventory
* Existing identity repositories
* Authentication compatibility
* Standard protocols and APIs
* HR system integration
* SIEM integration
* Legacy application support
* Identity synchronisation
* Integration gaps and dependencies

### Key consideration

A technically strong IAM platform is of limited value if it cannot integrate with the systems employees actually use.

The assessment therefore treated integration capability as a core architectural requirement rather than an afterthought.

---

## 5. Cloud Integration

With TechCorp expanding its use of cloud platforms and services, identity controls must extend beyond traditional corporate infrastructure.

### Areas assessed

* Cloud identity management
* Cross-cloud identity consistency
* Single Sign-On (SSO)
* MFA
* Cloud privileged access
* Least privilege
* Cloud logging and monitoring
* Policy alignment

### Key consideration

Cloud adoption can quickly increase identity sprawl when every service manages users independently.

Centralised identity, SSO and automated provisioning provide a way to maintain consistent controls while allowing TechCorp to continue adopting cloud services.

---

## 6. User Experience

Security controls should not create unnecessary friction for employees, partners or customers.

### Areas assessed

* Login and authentication experience
* SSO opportunities
* Number of authentication prompts
* MFA usability
* Access request simplicity
* User feedback
* Authentication-related support issues

### Key consideration

The assessment treated **security and usability as complementary objectives**.

SSO and streamlined access workflows can reduce password fatigue while simultaneously improving centralised security and visibility.

---

## Assessment Recommendations

Based on the readiness areas above, the proposed direction was to:

1. Establish a centralised IAM architecture.
2. Use authoritative HR information to drive identity lifecycle events.
3. Automate Joiner–Mover–Leaver processes.
4. Implement RBAC and least-privilege access.
5. Strengthen authentication with MFA and risk-aware controls.
6. Introduce stronger governance for privileged access.
7. Integrate existing and cloud applications using established standards.
8. Centralise identity logging and monitoring.
9. Establish periodic access reviews and governance processes.
10. Measure IAM performance through defined success metrics.

These recommendations became the foundation for **Task 2 — Custom IAM Solution Design**.

---

## From Assessment to Design

The assessment established the requirements; the next task translated them into an actual IAM architecture.

```text
ASSESS
Identify requirements, risks & gaps
        ↓
DESIGN
Build the target IAM architecture
        ↓
IMPLEMENT
Define a phased implementation roadmap
```

This progression was important because the solution was not designed in isolation. The architecture and implementation strategy were derived from the operational, security, integration and governance requirements identified during the assessment.

---

## Deliverable

**Task 1 — IAM Readiness Assessment**

An email-based readiness assessment and recommendation submitted as part of the simulation.

---

## Key Takeaways

* Enterprise IAM begins with understanding the organisation's existing identity processes and dependencies.
* **Joiner–Mover–Leaver automation** is fundamental at large organisational scale.
* Access control must reflect business responsibilities while enforcing least privilege.
* Integration with HR, existing applications, cloud services and security monitoring is essential.
* Governance and auditability need to be designed into IAM rather than added later.
* A successful IAM programme must balance **security, operational efficiency, scalability and user experience**.

**Outcome:** The assessment established the requirements and design priorities that informed the custom IAM solution developed in Task 2.
