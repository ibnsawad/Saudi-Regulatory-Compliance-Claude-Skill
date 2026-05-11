# NCA OSMACC-1:2021 — Organizations' Social Media Accounts Cybersecurity Controls

## At a glance

| Field | Value |
|-------|-------|
| Issuer | National Cybersecurity Authority (NCA), Kingdom of Saudi Arabia |
| Document | Organizations' Social Media Accounts Cybersecurity Controls (OSMACC-1:2021) |
| TLP / Classification | White / Open |
| Binding language | Arabic (English version is reference only) |
| Status | Mandatory for all in-scope entities using social media |
| Relationship to ECC | OSMACC is an **extension** to ECC-1:2018. ECC compliance is a **prerequisite** — OSMACC compliance cannot be achieved without continuous ECC compliance |
| Compliance basis | NCA mandate, Royal Decree No. 6801 dated 11/2/1439 AH; Article 10 item 3 |
| Compliance evaluation | Self-assessment by organisations and/or on-site audits by NCA |

---

## Purpose

Provides the minimum cybersecurity requirements to enable organisations to use social networks in a safe manner. Issued in response to growing risks of theft, misuse, and impersonation of official organisational social media accounts as their use increased across KSA government and related entities.

---

## Exact structure

| Level | Count |
|-------|-------|
| Main Domains | 3 |
| Subdomains | 12 |
| Main Controls | 15 |
| Subcontrols | 38 |

### Control numbering scheme

Same as ECC: `[Main Domain]-[Subdomain]-[Main Control]-[Subcontrol]`

Example: **2-3-2-6** → Main Domain 2, Subdomain 3, Control 2, Subcontrol 6.

---

## Applicability (OSMACC Scope of Work)

**Mandatory for:**
- Government organisations in KSA (ministries, authorities, establishments, and similar bodies)
- Their affiliated companies and entities
- Private-sector organisations owning, operating, or hosting sensitive national infrastructure

NCA strongly encourages all other KSA organisations to adopt these controls voluntarily as best practice.

**Statement of Applicability:** An organisation that uses social networks must adhere to all controls applicable to it, taking into account the diversity and nature of its work.

---

## ECC relationship — how the extension model works

OSMACC is **additive**, not standalone. The dependency is explicit in the document:
- 12 ECC subdomains have OSMACC controls layered on top
- 17 ECC subdomains have no OSMACC additions (ECC controls apply unchanged to those)

Assessors must always verify ECC compliance first, then apply the OSMACC overlay for any subdomain to which it adds requirements.

### OSMACC-to-ECC subdomain mapping

| OSMACC Subdomain | Extends ECC Control |
|-----------------|---------------------|
| 1-1 Cybersecurity Policies and Procedures | ECC 1-3-1 |
| 1-2 Cybersecurity Risk Management | ECC subdomain 1-5 |
| 1-3 Cybersecurity in Human Resources | ECC 1-9-4 |
| 1-4 Cybersecurity Awareness and Training Program | ECC 1-10-3 (awareness) and 1-10-4 (training) |
| 2-1 Asset Management | ECC subdomain 2-1 |
| 2-2 Identity and Access Management | ECC 2-2-3 (main); 2-2-3-5 (review cycle) |
| 2-3 Information System and Processing Facilities Protection | ECC 2-3-3 |
| 2-4 Mobile Device Security | ECC 2-6-3 |
| 2-5 Data and Information Protection | ECC 2-7-3 |
| 2-6 Cybersecurity Events Logs and Monitoring Management | ECC 2-12-3 |
| 2-7 Cybersecurity Incident and Threat Management | ECC 2-13-3 (also references Royal Decree 37140, 14/8/1438H) |
| 3-1 Third-Party Cybersecurity | ECC 4-1-2 |

---

## Domain 1 — Cybersecurity Governance (4 subdomains)

| Ref | Subdomain |
|-----|-----------|
| 1-1 | Cybersecurity Policies and Procedures |
| 1-2 | Cybersecurity Risk Management |
| 1-3 | Cybersecurity in Human Resources |
| 1-4 | Cybersecurity Awareness and Training Program |

### 1-1 Cybersecurity Policies and Procedures

**Objective:** Ensure cybersecurity requirements are documented, communicated, and complied with per related laws/regulations and organisational requirements.

Extends ECC control 1-3-1.

| Control | Obligation |
|---------|-----------|
| 1-1-1-1 | Define and document the cybersecurity requirements for the organisation's social media accounts **as part of the organisation's cybersecurity policies** |

**Audit note:** Social media cybersecurity must be explicitly called out in policy — it is not sufficient to rely on general IT policy coverage.

---

### 1-2 Cybersecurity Risk Management

**Objective:** Manage cybersecurity risks methodologically to protect information and technology assets.

Extends ECC subdomain 1-5 controls.

| Control | Obligation |
|---------|-----------|
| 1-2-1-1 | Assess cybersecurity risks for the organisation's social media accounts **at least once per year** |
| 1-2-1-2 | Assess cybersecurity risks **during planning and before permitting use** of the organisation's social media accounts |
| 1-2-1-3 | Include cybersecurity risks related to social media accounts in the organisation's **cybersecurity risk register**, and monitor the register at least once a year |

**Audit hot spot:** Risk assessments before permitting new social media account use (1-2-1-2) are routinely missed — organisations often launch accounts without a formal pre-approval risk step.

---

### 1-3 Cybersecurity in Human Resources

**Objective:** Ensure cybersecurity risks related to personnel are managed efficiently before, during, and after employment.

Extends ECC control 1-9-4. Additional requirements for **personnel responsible for managing the organisation's social media accounts:**

| Control | Obligation |
|---------|-----------|
| 1-3-1-1 | Cybersecurity awareness about social media accounts |
| 1-3-1-2 | Implementation of and compliance with the organisation's cybersecurity policies and procedures for social media accounts |

---

### 1-4 Cybersecurity Awareness and Training Program

**Objective:** Ensure personnel are aware of cybersecurity responsibilities and trained on required skills.

Extends ECC 1-10-3 (awareness) and 1-10-4 (training). Two main controls:

**1-4-1 Awareness program** (extends ECC 1-10-3) — must cover potential cyber risks and threats related to social media accounts, including:

| Sub-control | Topic |
|-------------|-------|
| 1-4-1-1 | Secure use and protection of **dedicated devices** for social media accounts; ensuring they do not contain classified data or are used for personal purposes |
| 1-4-1-2 | Secure handling of **identities, passwords, and security questions** |
| 1-4-1-3 | Social media accounts **restoration plan** and dealing with cybersecurity incidents |
| 1-4-1-4 | Secure handling of **applications and solutions** used for the organisation's social media accounts |
| 1-4-1-5 | **Not using** the organisation's social media accounts for personal purposes such as browsing |
| 1-4-1-6 | Avoiding access using **untrusted public devices or networks** |
| 1-4-1-7 | **Communicating directly with the cybersecurity department** if a cybersecurity threat is suspected |

**1-4-2 Training** (extends ECC 1-10-4) — personnel responsible for managing social media accounts must be trained on the required technical skills, plans, and procedures to implement cybersecurity requirements and practices.

---

## Domain 2 — Cybersecurity Defense (7 subdomains)

| Ref | Subdomain |
|-----|-----------|
| 2-1 | Asset Management |
| 2-2 | Identity and Access Management |
| 2-3 | Information System and Processing Facilities Protection |
| 2-4 | Mobile Device Security |
| 2-5 | Data and Information Protection |
| 2-6 | Cybersecurity Events Logs and Monitoring Management |
| 2-7 | Cybersecurity Incident and Threat Management |

### 2-1 Asset Management

**Objective:** Maintain accurate and detailed inventory of information and technology assets to support cybersecurity and operational requirements.

Extends ECC subdomain 2-1.

| Control | Obligation |
|---------|-----------|
| 2-1-1-1 | Identify and inventory the organisation's social media accounts and all related information and technology assets; **update the inventory at least once per year** |

---

### 2-2 Identity and Access Management

**Objective:** Ensure secure, restricted logical access to prevent unauthorised access.

Extends ECC control 2-2-3. Two main controls:

**2-2-1** (extends ECC 2-2-3) — minimum IAM requirements for social media accounts:

| Sub-control | Obligation |
|-------------|-----------|
| 2-2-1-1 | Use social media accounts **designated for organisations, not individuals** |
| 2-2-1-2 | Register using **official information** (official social-media-specific email and official mobile number); **do not use personal information** |
| 2-2-1-3 | **Verify** the organisation's social media accounts wherever possible; maintain a **consistent identity** across all accounts to facilitate identification of official accounts and detection of fraud or impersonation |
| 2-2-1-4 | Use a **secure and unique password** for each social media account; change passwords regularly; **do not reuse passwords** |
| 2-2-1-5 | Use **multi-factor authentication (MFA)** for all social media account logins |
| 2-2-1-6 | Activate and update security questions; **document them in a safe place** |
| 2-2-1-7 | Manage access rights based on **business need**, considering account sensitivity, access level, and type of devices/systems used |
| 2-2-1-8 | **Restrict access rights** of service providers of social media management, monitoring, or brand protection |
| 2-2-1-9 | Restrict access to the organisation's social media accounts to **specific devices** |

**2-2-2** (references ECC 2-2-3-5) — User identities and access rights for social media accounts must be **reviewed at least once every year**.

**Critical audit notes:**
- MFA (2-2-1-5) is mandatory on all social media logins, not just privileged accounts.
- Device restriction (2-2-1-9) means access from unmanaged or personal devices is non-compliant.
- Third-party social media management platforms must have access limited as per 2-2-1-8.

---

### 2-3 Information System and Processing Facilities Protection

**Objective:** Protect information systems and processing facilities against cyber risks.

Extends ECC control 2-3-3.

| Sub-control | Obligation |
|-------------|-----------|
| 2-3-1-1 | Apply **updates and security patches** for social media applications **at least once a month** |
| 2-3-1-2 | Review **configurations and hardening** of social media accounts and related technology assets **at least once a year** |
| 2-3-1-3 | Review and harden **default configurations** — including default passwords, pre-login settings, and lockout configurations |
| 2-3-1-4 | Restrict activation of **features and services** in social media accounts on a need-only basis; conduct a risk assessment before activating any feature |

---

### 2-4 Mobile Device Security

**Objective:** Protect mobile devices (laptops, smartphones, tablets) from cyber risks; ensure secure handling of organisational information on BYOD.

Extends ECC control 2-6-3.

| Sub-control | Obligation |
|-------------|-----------|
| 2-4-1-1 | **Centrally manage** all mobile devices used for social media accounts using a **Mobile Device Management (MDM) system** |
| 2-4-1-2 | Apply updates and security patches on mobile devices **at least once every month** |

---

### 2-5 Data and Information Protection

**Objective:** Ensure confidentiality, integrity, and availability of organisational data.

Extends ECC control 2-7-3.

| Sub-control | Obligation |
|-------------|-----------|
| 2-5-1-1 | Technology assets used for managing social media accounts **must not contain classified data**, per relevant regulations |

---

### 2-6 Cybersecurity Events Logs and Monitoring Management

**Objective:** Timely collection, analysis, and monitoring of cybersecurity events for early detection of potential attacks.

Extends ECC control 2-12-3.

| Sub-control | Obligation |
|-------------|-----------|
| 2-6-1-1 | **Activate all notifications and cybersecurity alerts** for social media accounts; maintain cybersecurity event logs on related technology assets |
| 2-6-1-2 | **Follow and monitor** the organisation's social media accounts to detect unauthorised content posts or unauthorised logins |
| 2-6-1-3 | **Monitor social media networks** to ensure the organisation is not being impersonated |
| 2-6-1-4 | Implement **automated monitoring** for any change in account patterns, indicators of compromise, or publication of unauthorised content or impersonation |

**Audit hot spot:** Automated monitoring (2-6-1-4) and anti-impersonation monitoring (2-6-1-3) are the most frequently absent controls — many organisations only monitor their own accounts, not the broader social media landscape for impersonation.

---

### 2-7 Cybersecurity Incident and Threat Management

**Objective:** Timely identification, detection, and effective handling of cybersecurity incidents and threats. References Royal Decree No. 37140, dated 14/8/1438H.

Extends ECC control 2-13-3.

| Sub-control | Obligation |
|-------------|-----------|
| 2-7-1-1 | Develop a **plan to recover** the organisation's social media accounts and to deal with cyber incidents |

---

## Domain 3 — Third-Party and Cloud Computing Cybersecurity (1 subdomain)

| Ref | Subdomain |
|-----|-----------|
| 3-1 | Third-Party Cybersecurity |

### 3-1 Third-Party Cybersecurity

**Objective:** Protect assets against cybersecurity risks from third parties, including outsourced and managed services.

Two main controls:

**3-1-1** — Conduct a **need assessment** for use of social media management, automated monitoring, or brand protection services, along with associated cybersecurity risks.

**3-1-2** (extends ECC 4-1-2) — Cybersecurity requirements for social media management, automated monitoring, or brand protection service contracts must include at minimum:

| Sub-control | Obligation |
|-------------|-----------|
| 3-1-2-1 | **Non-disclosure clauses** and secure removal of the organisation's data by the third party upon service termination |
| 3-1-2-2 | **Communication procedures** to report vulnerabilities and cyber incidents |
| 3-1-2-3 | Requirement for the third party to **comply with cybersecurity requirements and policies** protecting social media accounts, and with related laws and regulations |

---

## Audit hot spots — triage list

Ranked by frequency in compliance gap assessments:

1. **Pre-use risk assessment (1-2-1-2):** Risk assessment required before permitting use of any new social media account. Organisations routinely launch accounts without this step.
2. **MFA on all social media logins (2-2-1-5):** MFA is mandatory — not just for privileged or admin access. Verify across all platforms.
3. **Automated anti-impersonation monitoring (2-6-1-4, 2-6-1-3):** Monitoring for impersonation of the organisation across the broader social media landscape is frequently absent.
4. **Device restriction (2-2-1-9):** Access from personal or unmanaged devices is non-compliant. Requires MDM enrolment or dedicated device policy.
5. **MDM deployment (2-4-1-1):** Centralised MDM management of all mobile devices used for social media is mandatory. BYOD access without MDM is non-compliant.
6. **Social media account inventory (2-1-1-1):** Organisations often have unofficial or shadow accounts not in the asset register; annual update required.
7. **Account verification (2-2-1-3):** Official accounts should carry platform verification marks where available; consistent identity across platforms required.
8. **Default configuration hardening (2-3-1-3):** Default passwords and pre-login/lockout settings reviewed and hardened — frequently overlooked on social media management tools.
9. **Third-party access restriction (2-2-1-8):** Social media agencies and monitoring services often have excessive access; restrict to minimum required.
10. **Social media account recovery plan (2-7-1-1):** A documented plan to recover accounts and respond to incidents is required. Many organisations have no account-specific recovery procedure.
11. **Social media policy in cybersecurity documentation (1-1-1-1):** Social media cybersecurity requirements must be explicitly documented in the organisation's cybersecurity policies, not assumed to be covered by general IT policy.
12. **Annual access rights review (2-2-2):** Access rights and user identities for social media accounts reviewed at least annually (per ECC 2-2-3-5); leaver process for social media admins frequently breaks down.

---

## Evidence expectations

| Control area | Evidence an auditor will request |
|-------------|----------------------------------|
| Policy (1-1) | Approved cybersecurity policy with explicit social media section; version date and Authorized Official signature |
| Risk register (1-2) | Risk register entries for social media accounts; annual review evidence; pre-launch risk assessment records |
| HR / awareness (1-3, 1-4) | Awareness training completion records; role-specific social media cybersecurity training records |
| Asset inventory (2-1) | Social media account register with platform, URL, owner, linked email/phone; date of last update |
| IAM (2-2) | Evidence of official registration details; MFA configuration screenshots; access rights matrix; device restriction policy; annual review records |
| System hardening (2-3) | Patch application logs; configuration review records; feature activation risk assessments |
| MDM (2-4) | MDM enrolment records for social media management devices; patch logs |
| Data classification (2-5) | Data handling procedures for social media assets; evidence classified data is not stored on social media management assets |
| Monitoring (2-6) | Alert configuration screenshots; monitoring coverage documentation; automated monitoring tool evidence; anti-impersonation monitoring reports |
| Incident plan (2-7) | Documented social media account recovery and incident response plan; evidence of testing |
| Third-party contracts (3-1) | Need assessment documentation; vendor contracts with clauses 3-1-2-1 through 3-1-2-3 explicitly present |

---

## Common pitfalls

- Treating general IT policy as sufficient coverage for social media cybersecurity — OSMACC requires explicit documentation (1-1-1-1).
- No pre-launch risk assessment before opening a new social media account — the assessment is required before permitting use, not retrospectively (1-2-1-2).
- MFA configured only for admin roles, not all account managers — 2-2-1-5 applies to all logins.
- Social media monitoring scoped only to the organisation's own accounts — anti-impersonation monitoring (2-6-1-3) covers the broader platform landscape.
- Social media managed via personal email addresses or personal mobile numbers — 2-2-1-2 requires official information only.
- Third-party social media agencies granted admin-level access with no restriction — 2-2-1-8 requires minimum necessary access.
- No account recovery plan — 2-7-1-1 requires a documented plan; many organisations have only a general cybersecurity incident response plan which does not address social media account takeover specifics.
- Patches applied to corporate systems but not to social media mobile applications — 2-3-1-1 and 2-4-1-2 apply specifically to social media apps and their hosting devices.
- Missing annual inventory update — shadow accounts (unofficial departmental or individual accounts) are a common gap.

---

## Key definitions (from OSMACC Terms)

| Term | Usage in OSMACC |
|------|----------------|
| **Organization's Social Media Accounts** | Official social media accounts used by the organisation to communicate with beneficiaries |
| **Social Media Management Services** | Third-party services that manage the organisation's social media posting, scheduling, or engagement |
| **Automated Monitoring Services** | Third-party services that monitor social media for mentions, sentiment, or security events |
| **Brand Protection Services** | Third-party services that detect impersonation, fake accounts, or unauthorised use of the organisation's brand on social media |

---

## Relationship to NCA ECC — visual summary

OSMACC spans 12 of the ECC's 29 subdomains (across the 4 ECC domains) and adds social-media-specific controls. The 17 ECC subdomains not extended by OSMACC (e.g. Cryptography, Vulnerability Management, Penetration Testing, Physical Security) remain in full effect for the broader IT environment — OSMACC does not reduce those obligations.

Domain 3 of OSMACC maps to Domain 4 of ECC (Third-Party and Cloud Computing Cybersecurity), with the same structural logic: need assessment, contractual clauses, and compliance obligations on vendors.

---

## Related frameworks (read next)

| Need | File |
|------|------|
| ECC baseline (prerequisite) | `ECC-2-2024.md` |
| Data on social media management assets | `DCC-1-2022.md` |
| Cloud-based social media tools | `CCC-2-2024.md` |
| Third-party vendors / managed services | `ECC-2-2024.md` §Domain 4 |

---

## Verification note

Control counts (3 domains, 12 subdomains, 15 main controls, 38 subcontrols) and all control references above are taken directly from OSMACC-1:2021 as published by NCA (TLP: White, Classification: Open). The Arabic version is the binding text; the English version is for reference only. Where any control number or text conflicts with the official Arabic PDF, the official PDF governs. Do not invent control numbers — if uncertain, describe the obligation and flag it for verification against the source document.
