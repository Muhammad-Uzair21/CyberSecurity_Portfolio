# TECHCORP — Enterprise Identity & Access Management Case Study

### Assess → Design → Implement

A cybersecurity case study based on an enterprise IAM scenario for **TechCorp**, a global technology organization with **150,000+ employees across 100+ countries**.

Completed as part of the **Tata Consultancy Services (TCS) Cybersecurity IAM Developer Virtual Job Simulation on Forage**.

---

## The Challenge

At TechCorp's scale, managing who has access to what — and making sure that access changes when people join, move roles, or leave — becomes a significant security and operational challenge.

The scenario involved:

* A global workforce across 100+ countries
* Extensive cloud and digital environments
* Legacy and third-party applications
* Manual identity and access processes
* Risks from excessive or outdated access
* Increasing security, compliance, and user-experience requirements

### The goal

Design an IAM approach that is **secure, scalable, automated, and practical for a global enterprise**.

---

# What I Did

I worked through the problem in three stages:

### 01 — ASSESS

**Evaluated TechCorp's IAM readiness**

I assessed the existing IAM strategy across:

* User onboarding, role changes and offboarding
* Access control and authentication
* Compliance and governance
* Existing application and system integration
* Cloud environments
* User experience

**Outcome:** Identified key IAM requirements, risks, and areas for improvement.

#### 📝 IAM Readiness Assessment

Completed an email-based IAM readiness assessment covering lifecycle management, access control, governance, system integration, cloud integration, and user experience.

[Explore Assessment →](./01-assess/)

---

### 02 — DESIGN

**Designed a custom enterprise IAM solution**

I translated the assessment findings into a proposed IAM architecture focused on:

* Automated identity lifecycle management
* Role-based access
* Least privilege
* Strong authentication
* Privileged access controls
* Application and cloud integration
* Centralized monitoring and governance

The design uses **Microsoft Entra ID as a reference identity platform** and incorporates industry-standard integration approaches.

**Outcome:** A scalable target architecture and security-control model aligned with TechCorp's business requirements.

📄 [View Custom IAM Solution Design](./02-design/custom-iam-solution-design.pdf)

---

### 03 — IMPLEMENT

**Created a phased implementation roadmap**

I then translated the proposed architecture into a practical rollout plan covering:

* Foundation and governance
* Identity integration
* Core access controls
* Access governance
* Global scaling and optimization

The plan also considered legacy applications, third-party integrations, cloud/SaaS sprawl, resources, risks, and measurable success criteria.

**Outcome:** A **30+ week implementation roadmap** designed to introduce the solution incrementally rather than through a disruptive enterprise-wide rollout.

📊 [View IAM Platform Implementation Plan](./03-implement/iam-platform-implementation-plan.pptx)

---

# The Solution — In One Picture

```text
                    ┌─────────────┐
                    │     HR      │
                    │ Identity    │
                    │   Data      │
                    └──────┬──────┘
                           │
                           ▼
                ┌────────────────────┐
                │ Central IAM        │
                │ Platform           │
                └─────────┬──────────┘
                          │
              ┌───────────┼───────────┐
              ▼           ▼           ▼
          Applications   Cloud     Privileged
          & SSO          Services    Access
              │           │           │
              └───────────┼───────────┘
                          ▼
                 ┌─────────────────┐
                 │ Monitoring &    │
                 │ Governance      │
                 └─────────────────┘
```

**The idea:** identity information flows from authoritative business processes into a centralized IAM platform, which controls and monitors access across the organization's digital environment.

---

# What I Produced

| Deliverable                               | What it demonstrates                                                     |
| ----------------------------------------- | ------------------------------------------------------------------------ |
| **01 — IAM Readiness Assessment**         | Security assessment, gap identification and recommendations              |
| **02 — Custom IAM Solution Design**       | IAM architecture and security-control design                             |
| **03 — IAM Platform Implementation Plan** | Implementation strategy, roadmap, risks and success metrics              |
| **Certificate**                           | Completion of the TCS Cybersecurity IAM Developer Virtual Job Simulation |

---

# Skills Demonstrated

**Cybersecurity**

`IAM` · `Identity Governance` · `Access Control` · `Least Privilege` · `Security Architecture` · `Risk Assessment` · `Security Controls`

**Identity & Authentication**

`RBAC` · `MFA` · `SSO` · `PAM` · `Conditional Access` · `Access Reviews`

**Enterprise Integration**

`Cloud Integration` · `Application Integration` · `SCIM` · `SAML` · `OIDC` · `OAuth 2.0` · `REST APIs` · `SIEM`

**Professional Skills**

`Requirements Analysis` · `Solution Design` · `Implementation Planning` · `Risk Analysis` · `Technical Documentation`

---

# Key Takeaway

The biggest lesson from this simulation was that **IAM is not simply about controlling logins**.

It connects people, business roles, applications, security controls, and governance into one continuous process.

A good IAM solution needs to answer simple but important questions:

> Who is this person?
> What should they have access to?
> Why do they need it?
> Who approved it?
> What happens when their role changes?
> What happens when they leave?

At enterprise scale, the answer cannot depend on manual intervention alone.

---

# Certification

Completed the **TCS Cybersecurity IAM Developer Virtual Job Simulation** on Forage.

📜 [View Certificate](./certificate/TCS-Cybersecurity-IAM-Developer-Certificate.pdf)

🔗 [Verify on Forage →](https://www.theforage.com/completion-certificates/ifobHAoMjQs9s6bKS/gmf3ypEXBj2wvfQWC_ifobHAoMjQs9s6bKS_6a5dff92ff6af99de17a4adc_1788606690524_completion_certificate.pdf)

---

# Explore the Case Study

Want the details?

| Section                | Explore                                             |
| ---------------------- | --------------------------------------------------- |
| 📋 **01 — Assess**     | [IAM Readiness Assessment](./01-assess/)            |
| 🏗️ **02 — Design**    | [Custom IAM Solution Design](./02-design/)          |
| 🗺️ **03 — Implement** | [IAM Platform Implementation Plan](./03-implement/) |

Each section contains the detailed reasoning, decisions, and original deliverable behind that stage of the project.

---

## Project Structure

```text
tcs-cybersecurity-iam/
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
```

---

### About the Simulation

This case study was completed through the **Tata Consultancy Services (TCS) Cybersecurity IAM Developer Virtual Job Simulation on Forage**.

The TechCorp scenario and requirements were provided as part of the simulation. The documents in this repository represent my completed work across **assessment, solution design, and implementation planning**.

Microsoft Entra ID is presented as a **reference identity platform** in the proposed architecture. This project involved solution design and implementation planning rather than deployment in a production environment.

---

### Project Focus

**Cybersecurity · Identity & Access Management · Security Architecture · Access Control · Identity Governance · Enterprise Security**

**TCS Cybersecurity IAM Developer Virtual Job Simulation — Forage**
