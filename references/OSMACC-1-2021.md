# OSMACC-1:2021 — Organizations' Social Media Accounts Cybersecurity Controls
## NCA | Version 1 | 2021 | Sharing Notice: White | Classification: Open

---

## Document Metadata

| Field | Value |
|-------|-------|
| Full title | Organizations' Social Media Accounts Cybersecurity Controls |
| Identifier | OSMACC-1:2021 |
| Issuer | National Cybersecurity Authority (NCA) |
| Mandate basis | Royal Decree No. 6801 dated 11/2/1439 AH (NCA mandate, Article 10 item 3) |
| Sharing notice | White — No restrictions |
| Document classification | Open |
| Binding language | Arabic (English is a translation only) |
| ECC prerequisite | ECC-1:2018 (current references use ECC-2:2024 equivalent subdomains) |
| Structure | 3 main domains · 12 subdomains · 15 main controls · 38 subcontrols |

---

## Purpose and Rationale

The NCA developed OSMACC-1:2021 in response to increased official use of social networks by KSA government and private-sector organisations, which raised the risk of account theft, misuse, and impersonation. The framework sets the **minimum cybersecurity requirements** enabling organisations to use social networks safely and responds to the mandate to establish national cybersecurity policies and follow up on compliance.

---

## Objectives

- Contribute to raising the level of cybersecurity at the national level.
- Enable organisations to use social networks in a safe manner.
- Readiness to respond effectively to cyber incidents that may have negative impacts.

---

## Scope of Work and Applicability

### Scope of Work
OSMACC applies to:
- Government organisations in the Kingdom of Saudi Arabia, including ministries, authorities, establishments, and organisations and companies related to them.
- Private-sector organisations that own, operate, or host sensitive national infrastructure.

All are referred to as "The Organisation". The NCA strongly encourages all other KSA organisations to leverage the controls to implement best practices.

### Statement of Applicability
Controls are compatible with cybersecurity requirements for all organisations and sectors in the Kingdom, taking into account the diversity and nature of work. **Every organisation that uses social networks must adhere to all applicable controls.**

### Compliance Basis
Compliance with OSMACC cannot be achieved without achieving continuous compliance with the **Essential Cybersecurity Controls (ECC-1:2018)** where applicable. The NCA evaluates compliance via self-assessments and/or on-site audits.

---

## Framework Structure

### Coding Scheme

```
OSMACC - 1 : 2021
               └── Year of Issuance
         └── Version Number
  └── Organizations' Social Media Accounts Cybersecurity Controls

Control reference example:  2 - 3 - 2 - 6
                             │   │   │   └── Subcontrol No.
                             │   │   └── Main Control No.
                             │   └── Subdomain No.
                             └── Main Domain No.
```

### Domain Map

| Domain | Subdomain Ref | Subdomain Name |
|--------|---------------|----------------|
| 1 — Cybersecurity Governance | 1-1 | Cybersecurity Policies and Procedures |
| | 1-2 | Cybersecurity Risk Management |
| | 1-3 | Cybersecurity in Human Resources |
| | 1-4 | Cybersecurity Awareness and Training Program |
| 2 — Cybersecurity Defense | 2-1 | Asset Management |
| | 2-2 | Identity and Access Management |
| | 2-3 | Information System and Processing Facilities Protection |
| | 2-4 | Mobile Device Security |
| | 2-5 | Data and Information Protection |
| | 2-6 | Cybersecurity Events Logs and Monitoring Management |
| | 2-7 | Cybersecurity Incident and Threat Management |
| 3 — Third-Party and Cloud Computing Cybersecurity | 3-1 | Third-Party Cybersecurity |

### ECC Relationship Summary
OSMACC is an extension to ECC-1:2018 across **12 subdomains** where social-media-specific controls have been added, and references **17 ECC subdomains** to which no additional social-media controls were added (i.e., the ECC controls apply as-is).

---

## Domain 1 — Cybersecurity Governance

---

### 1-1 Cybersecurity Policies and Procedures

**Objective:** To ensure that cybersecurity requirements are documented, communicated and complied with by the organisation as per related laws and regulations, and organisational requirements.

**ECC reference:** Extends ECC control 1-3-1.

#### Control Table

| Control ID | Clause Text (verbatim from source) |
|------------|------------------------------------|
| 1-1-1 | Referring to control 1-3-1 in the ECC, cybersecurity policies and procedures must include the following: |
| 1-1-1-1 | Defining and documenting the cybersecurity requirements for organisations' social media accounts as part of the organisation's cybersecurity policies. |

#### Evidence Required

| Evidence Item | Format | Frequency |
|---------------|--------|-----------|
| Organisation-wide cybersecurity policy document | Policy (approved, version-controlled) | Review annually |
| Section/annex within the policy explicitly addressing social media accounts | Policy excerpt or standalone social media security policy | Current |
| Evidence of communication to relevant staff | Distribution records, email acknowledgements, or intranet post | Per policy update |

#### Audit Flags
> 🔴 **CRITICAL — 1-1-1-1:** Absence of any documented cybersecurity requirements for social media accounts within the organisation's policy framework constitutes a direct non-compliance finding and is the foundation control for all subsequent OSMACC obligations.

---

### 1-2 Cybersecurity Risk Management

**Objective:** To ensure managing cybersecurity risks in a methodological approach in order to protect the organisation's information and technology assets as per organisational policies and procedures, and related laws and regulations.

**ECC reference:** Extends ECC subdomain 1-5.

#### Control Table

| Control ID | Clause Text (verbatim from source) |
|------------|------------------------------------|
| 1-2-1 | In addition to the controls within subdomain 1-5 in the ECC, requirements for cybersecurity risk management should include at least the following: |
| 1-2-1-1 | Assessing cybersecurity risks for organisation's social media accounts, once per year at least. |
| 1-2-1-2 | Assessing cybersecurity risks during planning and before permitting use of organisation's social media accounts. |
| 1-2-1-3 | Including cybersecurity risks related to organisation's social media accounts in the organisation's cybersecurity risk register, and monitoring it at least once a year. |

#### Evidence Required

| Evidence Item | Format | Frequency |
|---------------|--------|-----------|
| Social media risk assessment report | Risk assessment document | Annually (minimum) |
| Pre-activation risk assessment for new accounts | Risk assessment record with approval | Before each new account activation |
| Cybersecurity risk register extract showing social media risks | Risk register (or dedicated section) | Reviewed ≥ annually |
| Risk monitoring / review sign-off records | Meeting minutes or review log | Annually (minimum) |

#### Audit Flags
> 🟠 **HIGH — 1-2-1-1:** Annual risk assessment cadence is a floor, not a ceiling. Auditors will check the date of the most recent assessment — assessments older than 12 months are a finding.
> 🟠 **HIGH — 1-2-1-2:** Absence of a pre-activation risk assessment for any social media account opened without prior risk assessment is a finding. Check account opening dates against risk assessment dates.
> 🟡 **MEDIUM — 1-2-1-3:** Risk register must explicitly name social media accounts as an asset class; a generic IT risk register without social media line items will not satisfy this control.

---

### 1-3 Cybersecurity in Human Resources

**Objective:** To ensure that cybersecurity risks and requirements related to personnel (employees and contractors) are managed efficiently prior to employment, during employment and after termination/separation as per organisational policies and procedures, and related laws and regulations.

**ECC reference:** Extends ECC control 1-9-4.

#### Control Table

| Control ID | Clause Text (verbatim from source) |
|------------|------------------------------------|
| 1-3-1 | In addition to the subcontrols within control 1-9-4 in the ECC, the cybersecurity requirements for personnel responsible for managing the organisation's social media accounts should include at least the following: |
| 1-3-1-1 | Cybersecurity awareness about social media accounts. |
| 1-3-1-2 | Implementation of and compliance with the cybersecurity requirements as per the organisational cybersecurity policies and procedures for the organisation's social media accounts. |

#### Evidence Required

| Evidence Item | Format | Frequency |
|---------------|--------|-----------|
| Role descriptions for social media account managers including cybersecurity responsibilities | HR/role documentation | Current |
| Signed acknowledgement of cybersecurity policy for social media staff | Signed forms or e-acknowledgements | On role assignment; annually |
| Records of cybersecurity awareness delivered to social media personnel | Training attendance records | Annually (minimum) |
| Offboarding checklist showing access revocation for departing social media staff | HR/IT offboarding records | Per departure |

#### Audit Flags
> 🟠 **HIGH — 1-3-1-1/1-3-1-2:** If personnel responsible for social media accounts have not received documented cybersecurity awareness specific to social media, this is a direct gap. Generic IT security awareness training does not satisfy this control without social-media-specific content.

---

### 1-4 Cybersecurity Awareness and Training Program

**Objective:** To ensure that personnel are aware of their cybersecurity responsibilities and have the essential cybersecurity awareness. It is also to ensure that personnel are provided with the required cybersecurity training, skills and credentials needed to accomplish their cybersecurity responsibilities and to protect the organisation's information and technology assets.

**ECC reference:** Extends ECC controls 1-10-3 and 1-10-4.

#### Control Table

| Control ID | Clause Text (verbatim from source) |
|------------|------------------------------------|
| 1-4-1 | In addition to the subcontrols within control 1-10-3 in the ECC, the cybersecurity awareness program must cover the awareness about the potential cyber risks and threats related to the organisation's social media accounts and the secure use to minimise these risks and threats, including the following: |
| 1-4-1-1 | Secure use and protection of devices dedicated to the organisation's social media accounts and ensuring that they do not contain classified data or used for personal purposes. |
| 1-4-1-2 | Secure handling of identities, passwords and security questions. |
| 1-4-1-3 | Organisation's social media accounts restoration plan and dealing with cybersecurity incidents. |
| 1-4-1-4 | Secure handling of applications and solutions used for the organisation's social media accounts. |
| 1-4-1-5 | Not to use the organisation's social media accounts for personal purposes such as browsing. |
| 1-4-1-6 | Avoiding accessing the organisation's social media accounts using untrusted public devices or networks. |
| 1-4-1-7 | Communicating directly with the cybersecurity department if a cybersecurity threat is suspected. |
| 1-4-2 | In addition to the subcontrols within control 1-10-4 in the ECC, personnel responsible for managing the organisation's social media accounts must be trained on the required technical skills, plans and procedures necessary to ensure the implementation of the cybersecurity requirements and practices when using the organisation's social media accounts. |

#### Evidence Required

| Evidence Item | Format | Frequency |
|---------------|--------|-----------|
| Cybersecurity awareness program documentation covering all 1-4-1-1 to 1-4-1-7 topics | Training curriculum / program doc | Reviewed annually |
| Awareness delivery records for social media personnel (including 1-4-1-1 through 1-4-1-7 topics) | Attendance sheets, LMS completion records | Annually (minimum) |
| Technical training records for social media account managers (1-4-2) | Training records/certificates | Per role assignment; annually |
| Awareness content samples (slides, e-learning modules) showing social-media-specific content | Training materials | Current |

#### Audit Flags
> 🟠 **HIGH — 1-4-1-1 to 1-4-1-7:** The awareness program must cover all seven specific topics. Auditors will verify content against this checklist — a general security awareness program without these seven elements will not satisfy the control.
> 🟡 **MEDIUM — 1-4-2:** Technical training must go beyond awareness to include skills, plans, and procedures. Completion of awareness-only training does not satisfy this separate technical training obligation.

---

## Domain 2 — Cybersecurity Defense

---

### 2-1 Asset Management

**Objective:** To ensure that the organisation has an accurate and detailed inventory of information and technology assets in order to support the organisation's cybersecurity and operational requirements to maintain the confidentiality, integrity and availability of information and technology assets.

**ECC reference:** Extends ECC subdomain 2-1.

#### Control Table

| Control ID | Clause Text (verbatim from source) |
|------------|------------------------------------|
| 2-1-1 | In addition to the controls within subdomain 2-1 in the ECC, cybersecurity requirements for managing information and technology assets must include at least the following: |
| 2-1-1-1 | Identifying and inventorying organisation's social media accounts, and information and technology assets related to them, and updating them at least once, every year. |

#### Evidence Required

| Evidence Item | Format | Frequency |
|---------------|--------|-----------|
| Social media account inventory (all official accounts, platforms, associated assets) | Asset register or inventory table | Updated annually (minimum) |
| Associated technology asset inventory (devices, applications, credentials stores) | Asset register section | Updated annually (minimum) |
| Evidence of last update (dated review) | Dated sign-off or change log | Annually |

#### Audit Flags
> 🟠 **HIGH — 2-1-1-1:** Unofficial or shadow social media accounts not in the inventory constitute an unmanaged risk. Auditors may cross-reference the organisation's public social media presence against the inventory.

---

### 2-2 Identity and Access Management

**Objective:** To ensure the secure and restricted logical access to information and technology assets in order to prevent unauthorised access and allow only authorised access for users which are necessary to accomplish assigned tasks.

**ECC reference:** Extends ECC control 2-2-3; also references ECC subcontrol 2-2-3-5.

#### Control Table

| Control ID | Clause Text (verbatim from source) |
|------------|------------------------------------|
| 2-2-1 | In addition to the subcontrols within control 2-2-3 in the ECC, cybersecurity requirements for identity and access management related to organisation's social media accounts shall include at least the following: |
| 2-2-1-1 | Using social media accounts designated for organisations, not individuals. |
| 2-2-1-2 | Registering using official information (official specific social media email and official mobile number), and do not use personal information. |
| 2-2-1-3 | Verifying organisation's social media accounts whenever possible and maintaining a consistent identity across all organisation's social media accounts used; to facilitate knowledge of official accounts, and to discover fraud or unofficial accounts. |
| 2-2-1-4 | Using a secure and specific password for each organisation's social media account, changing the password regularly, and not to repeat use of passwords. |
| 2-2-1-5 | Using multi-factor authentication for organisation's social media accounts logins. |
| 2-2-1-6 | Activating and updating security questions and documenting them in a safe place. |
| 2-2-1-7 | Managing organisation's social media accounts access rights based on business need, considering the sensitivity of the accounts, the level of access rights and the type of devices and systems used. |
| 2-2-1-8 | Restricting access rights of service providers of social media management, social media monitoring or brand protection. |
| 2-2-1-9 | Restricting access to organisation's social media accounts to specific devices. |
| 2-2-2 | With reference to ECC subcontrol 2-2-3-5, user identities and access rights used for organisation's social media accounts must be reviewed at least once every year. |

#### Evidence Required

| Evidence Item | Format | Frequency |
|---------------|--------|-----------|
| Account registration records showing official email/mobile used (2-2-1-2) | Registration confirmation records | Per account |
| Account verification status (platform verification badges) (2-2-1-3) | Screenshot/record of verified status | Current; check all accounts |
| Password policy for social media accounts (2-2-1-4) | Password policy document | Current |
| MFA activation records for all accounts (2-2-1-5) | Platform MFA settings screenshots or config records | Current |
| Security questions documentation stored securely (2-2-1-6) | Secure vault/password manager records | Current |
| Access rights matrix for social media accounts (2-2-1-7) | Access control matrix | Reviewed annually |
| Third-party access rights listing with restrictions (2-2-1-8) | Access control records / vendor agreements | Reviewed annually |
| Device restriction configuration records (2-2-1-9) | MDM or platform config records | Current |
| Annual access review records (2-2-2) | Access review sign-off | Annually |

#### Audit Flags
> 🔴 **CRITICAL — 2-2-1-5:** Absence of MFA on any official social media account is a critical finding — account takeover is the primary threat OSMACC was created to address. Auditors will verify MFA status directly.
> 🔴 **CRITICAL — 2-2-1-1:** Social media accounts registered to personal email addresses or personal mobile numbers violate this control and create irrecoverable account ownership risk.
> 🟠 **HIGH — 2-2-1-4:** Password reuse across social media accounts and absence of a password rotation schedule are both findings. Evidence of unique, regularly changed passwords is required.
> 🟠 **HIGH — 2-2-1-9:** Absence of device restrictions means accounts can be accessed from any device, including unmanaged personal devices — a significant control gap.
> 🟡 **MEDIUM — 2-2-2:** Annual access review is mandatory. Access reviews older than 12 months, or with no documentation, are a finding.

---

### 2-3 Information System and Processing Facilities Protection

**Objective:** To ensure the protection of information systems and information processing facilities (including workstations and infrastructures) against cyber risks.

**ECC reference:** Extends ECC control 2-3-3.

#### Control Table

| Control ID | Clause Text (verbatim from source) |
|------------|------------------------------------|
| 2-3-1 | In addition to the subcontrols in ECC control 2-3-3, cybersecurity requirements for protecting organisation's social media accounts and technology assets related to them must include at least the following: |
| 2-3-1-1 | Applying updates and security patches for social media applications at least once a month. |
| 2-3-1-2 | Reviewing configurations and hardening of organisation's social media accounts and technology assets related to them at least once a year. |
| 2-3-1-3 | Reviewing and hardening default configurations, such as default passwords, pre-login, and lockout, for organisation's social media accounts and technology assets related to them. |
| 2-3-1-4 | Restricting activation of features and services in social media accounts on need basis and carrying out risk assessment if there is a need to activate it. |

#### Evidence Required

| Evidence Item | Format | Frequency |
|---------------|--------|-----------|
| Patch/update records for social media applications (2-3-1-1) | Patch management log or mobile app update records | Monthly (minimum) |
| Annual hardening review records for accounts and assets (2-3-1-2) | Hardening review report or checklist | Annually |
| Default configuration hardening checklist (2-3-1-3) | Hardening checklist (default passwords changed, lockout set, pre-login configured) | Per account setup; reviewed annually |
| Feature/service activation records with associated risk assessment (2-3-1-4) | Feature activation log and risk assessment documents | Per activation event |

#### Audit Flags
> 🟠 **HIGH — 2-3-1-1:** Monthly patching cadence for social media apps is a specific calendar obligation. Gaps in the monthly patch log are a finding.
> 🟠 **HIGH — 2-3-1-3:** Default passwords on any social media management tool or account are a critical configuration gap. Auditors check lockout and default credential settings.
> 🟡 **MEDIUM — 2-3-1-4:** Any enabled features/services without a documented need-basis decision and risk assessment are a finding. Common examples: connected third-party apps, public API access, automated posting integrations.

---

### 2-4 Mobile Device Security

**Objective:** To ensure the protection of mobile devices (including laptops, smartphones, tablets) from cyber risks and to ensure the secure handling of the organisation's information (including sensitive information) while utilising Bring Your Own Device (BYOD) policy.

**ECC reference:** Extends ECC control 2-6-3.

#### Control Table

| Control ID | Clause Text (verbatim from source) |
|------------|------------------------------------|
| 2-4-1 | In addition to the subcontrols within control 2-6-3 in the ECC, cybersecurity requirements for mobile device security related to organisation's social media accounts must include at least the following: |
| 2-4-1-1 | Centrally manage mobile devices for organisation's social media accounts using a Mobile Device Management system (MDM). |
| 2-4-1-2 | Applying updates and security patches on mobile devices, at least once every month. |

#### Evidence Required

| Evidence Item | Format | Frequency |
|---------------|--------|-----------|
| MDM platform configuration showing social media devices enrolled (2-4-1-1) | MDM dashboard / device inventory export | Current |
| MDM policy applied to social media devices (2-4-1-1) | MDM policy document or configuration export | Current |
| Monthly mobile device patch/update records (2-4-1-2) | MDM patch compliance report | Monthly |

#### Audit Flags
> 🔴 **CRITICAL — 2-4-1-1:** Use of unmanaged personal BYOD devices for accessing official social media accounts without MDM enrolment is a critical control gap. OSMACC requires centralised MDM management for all devices used for social media account management.
> 🟠 **HIGH — 2-4-1-2:** Monthly update cadence mirrors the application patch requirement. Auditors will check MDM compliance reports for devices that are behind on patches.

---

### 2-5 Data and Information Protection

**Objective:** To ensure the confidentiality, integrity and availability of organisation's data and information as per organisational policies and procedures, and related laws and regulations.

**ECC reference:** Extends ECC control 2-7-3.

#### Control Table

| Control ID | Clause Text (verbatim from source) |
|------------|------------------------------------|
| 2-5-1 | In addition to the subcontrols in ECC control 2-7-3, cybersecurity requirements for protecting and handling data and information for organisation's social media accounts must include at least the following: |
| 2-5-1-1 | Technology assets for management of organisation's social media accounts must not contain classified data, per relevant regulations. |

#### Evidence Required

| Evidence Item | Format | Frequency |
|---------------|--------|-----------|
| Data classification policy showing prohibition of classified data on social media management assets | Policy document | Current |
| DLP or technical controls preventing classified data on social media devices/systems | Technical configuration records | Current |
| Periodic verification / scan records confirming absence of classified data | Scan reports or audit records | Annually (minimum) |

#### Audit Flags
> 🟠 **HIGH — 2-5-1-1:** Social media management devices containing national-classification-level data (e.g. PROTECTED, CONFIDENTIAL) represent a data leakage path to potentially publicly accessible platforms. Auditors may request evidence of DLP controls or device-level data-at-rest inspection.

---

### 2-6 Cybersecurity Events Logs and Monitoring Management

**Objective:** To ensure timely collection, analysis and monitoring of cybersecurity events for early detection of potential cyber-attacks in order to prevent or minimise the negative impacts on the organisation's operations.

**ECC reference:** Extends ECC control 2-12-3.

#### Control Table

| Control ID | Clause Text (verbatim from source) |
|------------|------------------------------------|
| 2-6-1 | In addition to the subcontrols in ECC control 2-12-3, cybersecurity requirements for event logs and monitoring management for organisation's social media accounts and technology assets related to them must include at least the following: |
| 2-6-1-1 | Activating all notifications and cybersecurity alerts for organisation's social media accounts and cybersecurity events logs on related technology assets. |
| 2-6-1-2 | Following organisation's social media accounts and monitoring them to ensure that they do not post any unauthorised content, or login any unauthorised access. |
| 2-6-1-3 | Monitoring social media networks to ensure the organisation is not being impersonated. |
| 2-6-1-4 | Automated monitoring for any change in the accounts pattern, indicators of compromise, or the publication of any unauthorised content or impersonation of the organisation. |

#### Evidence Required

| Evidence Item | Format | Frequency |
|---------------|--------|-----------|
| Platform notification/alert settings screenshots or config records (2-6-1-1) | Platform config records | Current |
| Account monitoring logs or dashboards showing ongoing monitoring (2-6-1-2) | Monitoring logs / SOC records | Continuous; reviewed periodically |
| Impersonation monitoring process and tooling records (2-6-1-3) | Tooling config or process document | Current |
| Automated monitoring configuration (brand monitoring tool, SIEM rules, or platform alerts) (2-6-1-4) | Tool config / SIEM rule documentation | Current |
| Records of alerts generated and responded to | Incident/alert log | Ongoing |

#### Audit Flags
> 🔴 **CRITICAL — 2-6-1-3:** Absence of impersonation monitoring is critical — impersonation of official accounts is a primary threat vector explicitly cited in the OSMACC introduction. This requires active monitoring, not passive detection.
> 🟠 **HIGH — 2-6-1-1:** All platform-available notifications must be activated. Auditors will check platform settings. Disabled login-anomaly or unusual-activity alerts are a finding.
> 🟠 **HIGH — 2-6-1-4:** Manual-only monitoring does not satisfy the automated monitoring requirement. Automated detection of unauthorised content or compromised patterns must be evidenced.

---

### 2-7 Cybersecurity Incident and Threat Management

**Objective:** To ensure timely identification, detection, effective management and handling of cybersecurity incidents and threats to prevent or minimise negative impacts on organisation's operation taking into consideration the Royal Decree number 37140, dated 14/8/1438H.

**ECC reference:** Extends ECC control 2-13-3.

**Special legal reference:** Royal Decree No. 37140, dated 14/8/1438H is explicitly cited and must be taken into account.

#### Control Table

| Control ID | Clause Text (verbatim from source) |
|------------|------------------------------------|
| 2-7-1 | In addition to the subcontrols within control 2-13-3 in ECC, cybersecurity requirements for incident and threat management in the organisation must include at least the following: |
| 2-7-1-1 | Developing a plan to recover the organisation's social media accounts and to deal with cyber incidents. |

#### Evidence Required

| Evidence Item | Format | Frequency |
|---------------|--------|-----------|
| Social media account recovery and incident response plan (2-7-1-1) | Documented plan (approved, version-controlled) | Reviewed annually; updated after incidents |
| Plan coverage checklist: account takeover scenarios, impersonation scenarios, unauthorised posting scenarios | Plan content review | Per plan review |
| Evidence of plan testing/tabletop exercise | Exercise records or test report | Annually (minimum) |
| Escalation contacts and NCA notification procedures | Plan section or RACI | Current |

#### Audit Flags
> 🔴 **CRITICAL — 2-7-1-1:** Absence of a documented and approved social media account recovery and cyber incident plan is a direct non-compliance finding. The plan must be specific to social media account scenarios (takeover, impersonation, unauthorised posting) — a generic IT incident response plan without social media scenarios does not satisfy this control.
> 🟠 **HIGH:** Plan must address Royal Decree No. 37140 (14/8/1438H) obligations — auditors will check alignment with the Decree's requirements.

---

## Domain 3 — Third-Party and Cloud Computing Cybersecurity

---

### 3-1 Third-Party Cybersecurity

**Objective:** To ensure the protection of assets against the cybersecurity risks related to third-parties including outsourcing and managed services as per organisational policies and procedures, and related laws and regulations.

**ECC reference:** Extends ECC control 4-1-2.

#### Control Table

| Control ID | Clause Text (verbatim from source) |
|------------|------------------------------------|
| 3-1-1 | A need assessment for the use of social media management, automated monitoring or brand protection services along with associated cybersecurity risks must be conducted. |
| 3-1-2 | In addition to the subcontrols within control 4-1-2 in ECC, cybersecurity requirements for use of social media management, automated monitoring or brand protection services in the organisation must include at least the following: |
| 3-1-2-1 | Non-disclosure clauses and secure removal of organisation's data by the third-party upon service termination. |
| 3-1-2-2 | Communication procedures to report vulnerabilities and cyber incidents. |
| 3-1-2-3 | Requirements for the third-party to comply with cybersecurity requirements and policies to protect organisations' social media accounts, and related laws and regulation. |

#### Evidence Required

| Evidence Item | Format | Frequency |
|---------------|--------|-----------|
| Need assessment for third-party social media services with risk evaluation (3-1-1) | Need assessment document | Before each engagement; reviewed annually |
| Third-party contracts/SLAs containing non-disclosure and data deletion clauses (3-1-2-1) | Signed contract | Per vendor engagement |
| Contractual provisions for vulnerability and incident reporting (3-1-2-2) | Contract section or addendum | Per vendor engagement |
| Contractual cybersecurity compliance requirements binding on the third-party (3-1-2-3) | Contract section; third-party compliance assessment | Per vendor engagement; annually |
| Evidence of third-party compliance review | Vendor assessment report or questionnaire | Annually |

#### Audit Flags
> 🔴 **CRITICAL — 3-1-1:** Engaging a social media management, monitoring, or brand protection provider without a prior need assessment and risk evaluation is a direct non-compliance finding. Third-party vendors are granted privileged access to official accounts — unassessed vendors present account takeover risk through the supply chain.
> 🟠 **HIGH — 3-1-2-1:** Contracts without explicit data deletion obligations upon termination create ongoing data exposure. Auditors will check contracts of all current and recently terminated vendors.
> 🟠 **HIGH — 3-1-2-3:** Third-party cybersecurity compliance requirements must be contractually binding, not aspirational. Evidence of third-party compliance (questionnaires, certifications, audits) is required.

---

## Quick-Reference: All Control IDs

| Control ID | Summary |
|------------|---------|
| 1-1-1-1 | Document social media cybersecurity requirements in organisational policy |
| 1-2-1-1 | Annual cybersecurity risk assessment for social media accounts |
| 1-2-1-2 | Pre-activation risk assessment before permitting social media account use |
| 1-2-1-3 | Include social media risks in cybersecurity risk register; monitor annually |
| 1-3-1-1 | Cybersecurity awareness for social media account managers |
| 1-3-1-2 | Compliance with cybersecurity policies by social media personnel |
| 1-4-1-1 | Awareness: secure use and protection of dedicated devices |
| 1-4-1-2 | Awareness: secure handling of identities, passwords, security questions |
| 1-4-1-3 | Awareness: account restoration plan and incident handling |
| 1-4-1-4 | Awareness: secure handling of social media applications and solutions |
| 1-4-1-5 | Awareness: no personal use of official social media accounts |
| 1-4-1-6 | Awareness: avoid untrusted public devices or networks |
| 1-4-1-7 | Awareness: report suspected threats directly to cybersecurity department |
| 1-4-2 | Technical training for social media personnel on skills, plans, and procedures |
| 2-1-1-1 | Inventory social media accounts and related assets; update annually |
| 2-2-1-1 | Use organisationally designated accounts, not personal accounts |
| 2-2-1-2 | Register accounts with official email and official mobile number |
| 2-2-1-3 | Verify accounts and maintain consistent identity; detect impersonation |
| 2-2-1-4 | Unique secure password per account; regular rotation; no reuse |
| 2-2-1-5 | MFA on all account logins |
| 2-2-1-6 | Activate, update, and securely document security questions |
| 2-2-1-7 | Access rights based on business need, sensitivity, and device type |
| 2-2-1-8 | Restrict access rights of social media management/monitoring vendors |
| 2-2-1-9 | Restrict account access to specific approved devices |
| 2-2-2 | Annual review of user identities and access rights (ref. ECC 2-2-3-5) |
| 2-3-1-1 | Monthly security patches for social media applications |
| 2-3-1-2 | Annual configuration review and hardening |
| 2-3-1-3 | Harden default configurations (passwords, pre-login, lockout) |
| 2-3-1-4 | Activate features/services on need basis with risk assessment |
| 2-4-1-1 | MDM for all social media management mobile devices |
| 2-4-1-2 | Monthly security patches on mobile devices |
| 2-5-1-1 | No classified data on social media management technology assets |
| 2-6-1-1 | Activate all platform notifications and cybersecurity alerts |
| 2-6-1-2 | Monitor accounts for unauthorised content and logins |
| 2-6-1-3 | Monitor for impersonation of the organisation |
| 2-6-1-4 | Automated monitoring for compromise indicators and unauthorised content |
| 2-7-1-1 | Documented plan for account recovery and cyber incident management |
| 3-1-1 | Need assessment and risk evaluation before engaging third-party social media services |
| 3-1-2-1 | NDA and secure data deletion clauses in third-party contracts |
| 3-1-2-2 | Third-party vulnerability and incident reporting procedures |
| 3-1-2-3 | Contractual obligation for third-party cybersecurity compliance |

---

## Critical Findings Quick Reference

| Severity | Control | Risk Scenario |
|----------|---------|---------------|
| 🔴 CRITICAL | 2-2-1-5 | No MFA on official social media accounts — primary account takeover vector |
| 🔴 CRITICAL | 2-2-1-1 | Accounts registered to personal identities — irrecoverable on departure |
| 🔴 CRITICAL | 2-4-1-1 | Unmanaged BYOD devices used for social media account management |
| 🔴 CRITICAL | 2-6-1-3 | No impersonation monitoring — official accounts may be spoofed undetected |
| 🔴 CRITICAL | 2-7-1-1 | No social-media-specific incident and recovery plan |
| 🔴 CRITICAL | 3-1-1 | Third