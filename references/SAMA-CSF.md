# SAMA — Cybersecurity Framework + IT Governance + Business Continuity

This file covers three SAMA frameworks that apply together to SAMA-supervised "Member Organisations".

---

## At a glance — SAMA Cybersecurity Framework (CSF)

| Field | Value |
|-------|-------|
| Issuer | Saudi Central Bank (SAMA — formally renamed from Saudi Arabian Monetary Agency, 2020) |
| Document | Cyber Security Framework |
| Version | v1.0, May 2017 |
| TLP / Classification | Public |
| Binding language | English |
| Status | Mandatory for all Member Organisations |
| Supersedes | All previous SAMA cybersecurity circulars (listed in Appendix A of the CSF) |
| Compliance mechanism | Annual cyber maturity self-assessment; SAMA reviews and audits; periodic regulatory reporting via SAMA portal |

---

## Member Organisations (in-scope entities)

- All banks operating in Saudi Arabia
- All insurance and/or reinsurance companies operating in Saudi Arabia
- All financing companies operating in Saudi Arabia
- All credit bureaus operating in Saudi Arabia
- The Financial Market Infrastructure

Outsourced service providers and subsidiaries of Member Organisations can fall in scope through contractual flow-down obligations required under Domain 3.4.

### Domain applicability exceptions — non-banking financial institutions

All four domains apply in full to the **banking sector**. For other financial institutions (insurance, financing, credit bureaus, financial market infrastructure):

| Exception | Detail |
|-----------|--------|
| Subdomain 3.1.2 (Cyber Security Strategy) | Alignment with the Banking Sector's cyber security strategy is **mandatory when applicable** |
| Subdomain 3.2.3 (Compliance with international industry standards) | **Excluded** — unless the organisation stores, processes, or transmits cardholder data or deals with SWIFT, in which case PCI-DSS and/or SWIFT Customer Security Controls Framework must be implemented |
| Subdomain 3.3.12 (Payment Systems) | **Excluded** |
| Subdomain 3.3.13 (Electronic Banking Services) | **Excluded** — unless the organisation provides online services for customers, in which case Multi-Factor Authentication must be implemented |

---

## Exact structure — CSF

| Domain | Subdomains |
|--------|-----------|
| 3.1 Cyber Security Leadership and Governance | 7 |
| 3.2 Cyber Security Risk Management and Compliance | 5 |
| 3.3 Cyber Security Operations and Technology | 17 |
| 3.4 Third Party Cyber Security | 3 |
| **Total subdomains** | **32** |

### Control numbering scheme

Controls are nested under domains and subdomains using a 4-level numbering system:

`[Domain].[Subdomain] – [Level 1].[Level 2].[Level 3].[Level 4]`

Example: **3.3.12 – 4.a.6.a** → Domain 3.3, Subdomain 12, sub-items 4.a.6.a.

---

## Maturity model

SAMA CSF uses a **six-level** maturity model (levels 0–5). Each control and subdomain is assessed against this scale:

| Level | Label | Definition and criteria |
|-------|-------|------------------------|
| **0** | Non-existent | No documentation; no awareness or attention for the control; controls not in place |
| **1** | Ad-hoc | Control not or only partially defined; performed inconsistently; design varies by department/owner; may only partially mitigate risk |
| **2** | Repeatable but informal | Execution based on informal, unwritten but standardised practice; objectives and design not formally defined or approved; limited structured review or testing |
| **3** | Structured and formalised | Controls defined, approved, and implemented; implementation demonstrable; policies, standards, and procedures established; compliance monitored (preferably via GRC tool); KPIs defined, monitored, and reported |
| **4** | Managed and measurable | Effectiveness periodically assessed and improved; periodic measurement and improvement opportunities documented; KRIs and trend reporting used; measurement results drive improvements |
| **5** | Adaptive | Continuous improvement plan in place; enterprise-wide programme focused on continuous compliance, effectiveness, and improvement; integrated with enterprise risk management; performance evaluated using peer and sector data |

**Minimum expected maturity:** Member Organisations should operate at **Level 3 or higher** for all applicable controls. SAMA expects entities to define a target maturity per control and demonstrate progression over time.

### Documentation pyramid supporting Level 3

| Tier | Document type | Answers | Endorsed by |
|------|--------------|---------|-------------|
| Top | Cybersecurity Policy | Why; what assets must be protected; what principles apply | Board of Directors |
| Middle | Cybersecurity Standards | What controls must be implemented (parameters, password rules, monitoring events, backup rules) | Senior Management / CISO |
| Base | Cybersecurity Procedures | How controls are executed step-by-step in the operating environment | CISO / Operational owners |

---

## Domain 3.1 — Cyber Security Leadership and Governance (7 subdomains)

| Ref | Subdomain |
|-----|-----------|
| 3.1.1 | Cyber Security Governance |
| 3.1.2 | Cyber Security Strategy |
| 3.1.3 | Cyber Security Policy |
| 3.1.4 | Cyber Security Roles and Responsibilities |
| 3.1.5 | Cyber Security in Project Management |
| 3.1.6 | Cyber Security Awareness |
| 3.1.7 | Cyber Security Training |

### 3.1.1 Cyber Security Governance

**Principle:** A cyber security governance structure should be defined, implemented, and endorsed by the board.

**Objective:** To direct and control the overall approach to cyber security within the Member Organisation.

| # | Key control |
|---|------------|
| 1 | A cyber security committee established and mandated by the board |
| 2 | Committee headed by an **independent senior manager from a control function** |
| 3 | Committee membership: senior managers from all relevant departments (COO, CIO, compliance officer, heads of relevant business departments); CISO; Internal Audit may attend as observer |
| 4 | Cyber security committee charter: committee objectives; roles and responsibilities; minimum meeting participants; meeting frequency (minimum quarterly) |
| 5 | Cyber security function established, **independent from the IT function** — separate reporting lines, budgets, and staff evaluations |
| 6 | Cyber security function reports directly to the CEO/managing director or general manager of a control function |
| 7 | Full-time CISO at senior management level appointed |
| 8 | CISO must: (a) hold Saudi nationality; (b) be sufficiently qualified; (c) obtain **no-objection from SAMA** before appointment |
| 9 | Board allocates sufficient budget for cyber security activities |

**Audit hot spots:** CISO SAMA no-objection not obtained (item 8c); CISO not independent from IT (item 5); no board-mandated committee charter.

---

### 3.1.2 Cyber Security Strategy

**Principle:** A cyber security strategy should be defined and aligned with the Member Organisation's strategic objectives and with the Banking Sector's cyber security strategy.

| # | Key control |
|---|------------|
| 1 | Strategy defined, approved, maintained, and executed |
| 2 | Aligned with: the Member Organisation's overall objectives; legal and regulatory compliance requirements; the Banking Sector's cyber security strategy |
| 3 | Strategy addresses: importance and benefits of cyber security; anticipated future state of resilience to emerging threats; which initiatives/projects should be executed and when |

---

### 3.1.3 Cyber Security Policy

**Principle:** A cyber security policy should be defined, approved, and communicated.

| # | Key control |
|---|------------|
| 1 | Policy defined, approved, and communicated |
| 2 | Reviewed periodically through a defined review process |
| 3 | Policy serves as input to other corporate policies (HR, Finance, IT); supported by detailed standards and procedures; based on best practices and (inter)national standards; communicated to relevant stakeholders |
| 4 | Policy content includes: definition of cyber security; overall objectives and scope; statement of board's intent; general and specific responsibilities; reference to supporting standards and procedures; cyber security requirements covering classification, protection, ownership, risk assessments, awareness, regulatory compliance, breach reporting, and business continuity |

---

### 3.1.4 Cyber Security Roles and Responsibilities

| Role | Key responsibilities |
|------|---------------------|
| **Board of Directors** | Ultimate responsibility; allocate budget; approve committee charter; endorse governance, strategy, and policy |
| **Cyber Security Committee** | Monitor and communicate risk appetite; review strategy; approve and monitor governance, strategy, policy, cyber programmes, risk management process, KRIs, and KPIs |
| **Senior Management** | Ensure standards and procedures reflect security requirements; ensure staff comply; ensure cyber security embedded in job descriptions |
| **CISO** | Develop and maintain: strategy, policy, architecture, risk management process; establish standards and procedures; deliver risk-based solutions; develop staff; oversee SOC; oversee incident investigations; gather and analyse threat intelligence; conduct risk assessments; define and conduct awareness programmes; measure and report KRIs/KPIs |
| **Internal Audit** | Perform cyber security audits |
| **All Staff** | Comply with cyber security policy, standards, and procedures |

---

### 3.1.5 Cyber Security in Project Management

**Principle:** Cyber security should be addressed in project management and project governance.

Key requirements:
- Cyber security integrated into the project management methodology
- Cyber security objectives included in all project objectives
- Cyber security function participates in all project phases
- Risk assessment at project start to identify cyber security risks and match to existing controls or requirements to develop
- Cyber security risks tracked in the project risk register
- Independent internal or external cyber security review performed before go-live

---

### 3.1.6 Cyber Security Awareness

**Principle:** Awareness programmes defined and conducted for staff, third parties, and customers.

Key requirements:
- Programmes tailored to different target groups through multiple channels; conducted periodically throughout the year
- Minimum content: explanation of cyber security measures; roles and responsibilities; information on emerging threats (e.g. spear-phishing, whaling)
- Customer awareness addresses both retail and commercial customers; includes listing of suggested cyber security mechanisms customers can implement to mitigate their own risk
- Programme evaluated to measure effectiveness and formulate improvements

---

### 3.1.7 Cyber Security Training

**Principle:** Staff provided with training on secure operation and cyber security controls.

Training is role-differentiated and targets:
- Key roles within the organisation
- Staff of the cyber security function
- Staff involved in developing and maintaining information assets
- Staff involved in risk assessments

---

## Domain 3.2 — Cyber Security Risk Management and Compliance (5 subdomains)

| Ref | Subdomain |
|-----|-----------|
| 3.2.1 | Cyber Security Risk Management |
| 3.2.2 | Regulatory Compliance |
| 3.2.3 | Compliance with (inter)national Industry Standards |
| 3.2.4 | Cyber Security Review |
| 3.2.5 | Cyber Security Audits |

### 3.2.1 Cyber Security Risk Management

**Principle:** A risk management process defined, approved, implemented, and aligned with enterprise risk management.

Four risk management activities:

| Activity | Subdomain | Key obligations |
|----------|-----------|----------------|
| Risk identification | 3.2.1.1 | Risks documented in a central register; addresses assets, threats, vulnerabilities, and existing controls |
| Risk analysis | 3.2.1.2 | Likelihood and potential business impact assessed |
| Risk response | 3.2.1.3 | Risk treated (accepted, avoided, transferred, or mitigated); treatment plan documented; residual risk signed off by business owner; accepting risk must be within risk appetite and must not contradict SAMA regulations |
| Risk monitoring and review | 3.2.1.4 | Treatment progress tracked; effectiveness of revised controls reviewed |

**Four mandatory risk assessment trigger scenarios** (risk management must be initiated):
1. At an early stage of the project
2. Prior to critical change
3. When outsourcing is being considered
4. When launching new products and technologies

Additional requirements:
- Existing assets periodically subject to risk assessment based on classification or risk profile
- Risk appetite and risk tolerance formally defined and approved
- Results reported to and endorsed by the relevant business owner (risk owner)
- Risk management involves: business owners, IT specialists, cyber security specialists, and key user representatives

---

### 3.2.2 Regulatory Compliance

Process established to identify, communicate, and comply with cyber security implications of relevant regulations. Process must be:
- Performed periodically or when new regulatory requirements become effective
- Involve representatives from key areas of the Member Organisation
- Result in updates to policy, standards, and procedures as necessary

---

### 3.2.3 Compliance with (inter)national Industry Standards

*(Applicable to banking sector; applies to other Member Organisations if they store, process, or transmit cardholder data or use SWIFT services.)*

Mandatory compliance with:
- Payment Card Industry Data Security Standard (**PCI-DSS**)
- EMV (Europay, MasterCard and Visa) technical standard
- **SWIFT Customer Security Controls Framework** (March 2017)

---

### 3.2.4 Cyber Security Review

**Principle:** Cyber security status subject to periodic review.

Key requirements:
- Cyber security reviews periodically performed for critical information assets
- Customer- and internet-facing services subject to **annual review and penetration tests**
- Review details recorded: results, issues identified, recommended actions; reported to business owner
- Follow-up reviews verify: all identified issues addressed; critical risks treated effectively; agreed actions ongoing

---

### 3.2.5 Cyber Security Audits

**Principle:** Information assets subject to thorough, independent, regular audits per generally accepted auditing standards and SAMA CSF.

Key requirements:
- Audits independent and per generally accepted auditing standards and the SAMA CSF
- Performed per the Member Organisation's audit manual and audit plan

---

## Domain 3.3 — Cyber Security Operations and Technology (17 subdomains)

| Ref | Subdomain |
|-----|-----------|
| 3.3.1 | Human Resources |
| 3.3.2 | Physical Security |
| 3.3.3 | Asset Management |
| 3.3.4 | Cyber Security Architecture |
| 3.3.5 | Identity and Access Management |
| 3.3.6 | Application Security |
| 3.3.7 | Change Management |
| 3.3.8 | Infrastructure Security |
| 3.3.9 | Cryptography |
| 3.3.10 | Bring Your Own Device (BYOD) |
| 3.3.11 | Secure Disposal of Information Assets |
| 3.3.12 | Payment Systems *(banking sector only)* |
| 3.3.13 | Electronic Banking Services *(banking sector; MFA mandatory if online services provided)* |
| 3.3.14 | Cyber Security Event Management |
| 3.3.15 | Cyber Security Incident Management |
| 3.3.16 | Threat Management |
| 3.3.17 | Vulnerability Management |

### 3.3.1 Human Resources

Cyber security requirements embedded in HR processes:
- Cyber security responsibilities and non-disclosure clauses in staff agreements (during and after employment)
- Cyber security awareness at employment start and during employment
- Defined disciplinary actions
- Screening and background checks
- Post-employment activities: revoke access rights immediately; return all information assets assigned (access badges, tokens, mobile devices, all electronic and physical information)

---

### 3.3.2 Physical Security

Facilities hosting information assets protected against intentional and unintentional security events. Process must include (at minimum):
- Physical entry controls (including visitor security)
- Monitoring and surveillance (CCTV, ATM GPS tracking, sensitivity sensors)
- Protection of data centres and data rooms
- Environmental protection
- Protection of information assets during lifecycle (transport, secure disposal, preventing unauthorised access and data leakage)

---

### 3.3.3 Asset Management

Unified asset register maintained — accurate and up-to-date. Process must include:
- Unified register
- Ownership and custodianship of information assets
- Reference to relevant other processes (financial, procurement, IT, cyber security)
- Information asset classification, labelling, and handling
- Discovery of new information assets

---

### 3.3.4 Cyber Security Architecture

Architecture must include:
- Strategic outline of cyber security capabilities and controls based on business requirements
- Approval of the defined architecture
- Requirement for qualified cyber security architects
- Design principles (security-by-design)
- Periodic review of the architecture

---

### 3.3.5 Identity and Access Management

IAM policy must cover:

| Area | Key requirements |
|------|-----------------|
| Access control basis | Need-to-have and need-to-know |
| User access management | Covers all user types (internal staff, third parties); HR instigates changes for internal staff; appointed accountable party for external staff/third parties; formal approval of requests; timely processing of changes; periodic review of rights; audit trail of all submitted, approved, and processed requests |
| Automation | User access management supported by automation |
| Centralisation | IAM function centralised |
| MFA | **Multi-factor authentication for sensitive and critical systems and profiles** |
| Privileged and remote access | **MFA for all remote access**; MFA for privileged access on critical systems (risk assessment basis); periodic review of privileged accounts; individual accountability; restriction and monitoring of non-personal privileged accounts; frequent password changes including at end of each session |

---

### 3.3.6 Application Security

Application security standard must cover:
- Secure coding standards
- Cyber security controls implemented (configuration parameters, monitoring events, IAM)
- Segregation of duties within the application (documented authorisation matrix)
- Data protection per classification (customer privacy, data leakage prevention)
- Vulnerability and patch management
- Backup and recovery procedures
- Periodic cyber security compliance review
- Application development must follow an approved **secure SDLC**

---

### 3.3.7 Change Management

Change management process must include:
- Cyber security requirements for controlling changes (impact assessment, classification, review)
- Security testing: penetration testing; code review for internally developed applications; code review or independent assurance statement for externally developed applications where source code unavailable
- **Business owner approval**
- **Cyber security function approval before Change Advisory Board (CAB)**
- **CAB approval**
- Post-implementation review of related cyber security controls
- Segregated development, testing, and implementation environments (technical and personnel)
- Emergency change and fix procedures
- Fall-back and roll-back procedures

---

### 3.3.8 Infrastructure Security

Standards must cover all instances across main data centres, disaster recovery sites, and office spaces, including all infrastructure types (OS, servers, VMs, firewalls, network devices, IDS/IPS, wireless, gateway/proxy/email servers, external connections, databases, file-shares, workstations, laptops, tablets, mobile devices, PBX).

Minimum content:

| Area | Key requirements |
|------|-----------------|
| Security controls | Configuration parameters, monitoring events, DLP, IAM, remote maintenance |
| Segregation of duties | Documented authorisation matrix |
| Data protection | Per classification scheme; customer privacy; data leakage prevention |
| Software and protocols | Approved software and secure protocols only |
| Network | Segmentation of networks |
| Malware protection | Malicious code/software and virus protection; application whitelisting; APT protection |
| Vulnerability and patching | Vulnerability and patch management |
| **DDoS protection** | Scrubbing services; bandwidth specification agreed; 24×7 monitoring by SOC, SP, and scrubbing provider; **DDoS scrubbing testing minimum twice per year**; DDoS services at main data centres AND disaster recovery sites |
| Backup and recovery | Backup and recovery procedures |
| Compliance review | Periodic cyber security compliance review |

---

### 3.3.9 Cryptography

Cryptographic security standard must include:
- Overview of approved cryptographic solutions and relevant restrictions (technical and legal)
- Circumstances when approved solutions must be applied
- Management of encryption keys: lifecycle management, archiving, and recovery

---

### 3.3.10 BYOD

When personal devices are permitted for business purposes, a BYOD cyber security standard is required covering:
- User responsibilities (including awareness training)
- Information on restrictions and consequences (modified/jailbroken devices; employment termination; loss/theft)
- Isolation of business information from personal information (containerisation)
- Regulation of corporate and approved public mobile applications
- Mobile Device Management (MDM): access controls and encryption on personal devices

---

### 3.3.11 Secure Disposal of Information Assets

Secure disposal standard must address:
- Disposal per legal and regulatory requirements (data privacy; data leakage prevention)
- Sensitive information destroyed using non-retrievable techniques: secure erase, secure wiping, incineration, double crosscut, shredding
- Third-party disposal providers comply with the standard; effectiveness periodically measured and evaluated

---

### 3.3.12 Payment Systems *(banking sector only)*

Controls cross-reference SAMA-mandated payment-system documents:

| System | Reference document |
|--------|--------------------|
| **SARIE** | SARIE Information Security Policy, Version 1.0 – June 2016 |
| **mada** | mada Rules and Standards Technical Book: Part IIIa (Security Framework, v6.0.0 – May 2016); Part IIIb (HSM Requirements, v6.0.0 – May 2016); SAMA CA IPK Certificate Procedures (v6.0.1 – October 2016) |

---

### 3.3.13 Electronic Banking Services *(banking sector; MFA mandatory if any online services provided)*

Electronic banking services security standard covers:

**Brand protection:** Measures to protect online services including social media.

**Online, mobile, and phone banking key requirements:**

| Area | Key requirement |
|------|----------------|
| Official channels | Use of official application stores and websites only |
| Threat detection | Detection and take-down of malicious apps and websites |
| App security | Sandboxing; non-caching techniques; anti-man-in-the-middle communications |
| **MFA — registration** | MFA during customer registration |
| **MFA — all services** | MFA for all electronic banking services |
| Token protection | Hard and soft tokens must be password-protected |
| Account lockout | Customer access revoked after 3 successive incorrect passwords or invalid PINs |
| Mobile number change | Customer mobile number change only via branch or ATM |
| MFA activation | Requesting and activating MFA through different delivery channels |
| MFA transactions | MFA mandatory for: sign-on; adding/modifying beneficiaries; adding utility and government payment services; high-risk transactions (exceeding predefined limits); password reset |
| Beneficiary activation | Adding and activating beneficiaries via different delivery channels |
| Availability | High availability ensured; scheduled downtime communicated to SAMA and customers |
| Contracts | Contractual agreements with customers covering roles, responsibilities, and liabilities |
| **SAMA approval** | **SAMA approval required before launching any new electronic banking service** |

**ATMs and POSs:**
- Prevention and detection of ATM/POS vulnerabilities (cables, USB ports, rebooting exploits)
- Hardening: OS hardening, malware protection, privacy screens, account/PIN masking, geo-blocking (disable cards for outside GCC by default; disable magnetic strip transactions), CCTV, card revocation after 3 invalid PINs, anti-skimming solutions (hardware and software), PIN-pad protection
- Remote stopping of ATMs in case of malicious activities

**SMS notification services:**
- SMS must not contain sensitive data (account balance — except for credit cards)
- SMS alert to both old and new mobile numbers when mobile number changed
- SMS notification when new MFA mechanism requested
- SMS notification for all retail and personal financial transactions
- SMS notification when beneficiaries added, modified, or activated

---

### 3.3.14 Cyber Security Event Management

Security event management process must include:

| Element | Requirement |
|---------|------------|
| SOC structure | Designated SOC team; skilled and continuously trained staff; restricted area for SOC activities and workspaces; 24×7 continuous monitoring |
| Detection | Detection and handling of malicious code/software; detection and handling of security events and anomalies |
| Network analysis | Security network packet analysis solution deployed |
| Log protection | Adequately protected logs |
| Compliance monitoring | Periodic monitoring of application and infrastructure cyber security standards |
| **SIEM** | **Automated and centralised analysis of security logs and correlation of events/patterns** |
| Incident reporting | Reporting of cyber security incidents |
| SOC effectiveness testing | Independent periodic red-team testing of SOC effectiveness |

---

### 3.3.15 Cyber Security Incident Management

Incident management process aligned with enterprise incident management. Must include:

| Element | Requirement |
|---------|------------|
| Team | Designated incident management team; skilled and trained staff |
| Forensics | Sufficient certified forensic capacity for major incidents (internal staff or contracted external forensic team) |
| Workspace | Restricted CERT workspace |
| Classification | Classification of cyber security incidents |
| Handling | Timely handling, recording, and monitoring of progress |
| Evidence | Protection of relevant evidence and logs |
| Post-incident | Forensics; root-cause analysis; improvements reported to CISO and Committee |
| Repository | Cyber security incident repository maintained |

**SAMA notification requirements — three-step process:**

| Step | Obligation |
|------|-----------|
| **1. Immediate notification** | Inform SAMA IT Risk Supervision **immediately** when a medium or high classified incident has occurred and been identified |
| **2. Media clearance** | Obtain **'no objection' from SAMA IT Risk Supervision before any media interaction** related to the incident |
| **3. Formal incident report** | Submit to SAMA IT Risk Supervision after resuming operations, including: title; classification; date/time of occurrence; date/time of detection; information assets involved; technical details; root-cause analysis; corrective activities performed and planned; impact description (data loss, service disruption, data modification, data leakage, customers impacted); total estimated cost; estimated cost of corrective actions |

---

### 3.3.16 Threat Management

Threat intelligence management process using multiple reliable sources:

| Source type | Examples |
|------------|----------|
| Internal | Access control, application and infrastructure logs, IDS/IPS, security tooling, SIEM, support functions (Legal, Audit, IT Helpdesk, Forensics, Fraud Management, Risk Management, Compliance) |
| External | SAMA, government agencies, security forums, security vendors, security organisations, specialist notification services |

Process must include:
- Defined methodology to periodically analyse threat information
- Documentation of relevant threat details: modus operandi, actors, motivation, type
- Assessment of relevance and actionability for SOC and Risk Management
- Sharing of relevant intelligence with stakeholders (e.g. SAMA, BCIS members)

---

### 3.3.17 Vulnerability Management

Vulnerability management process must include:
- Coverage of all information assets
- Frequency of vulnerability scans (risk-based)
- Classification of vulnerabilities
- Defined timelines to mitigate per classification
- Prioritisation for classified information assets
- Patch management and method of deployment

---

## Domain 3.4 — Third Party Cyber Security (3 subdomains)

| Ref | Subdomain |
|-----|-----------|
| 3.4.1 | Contract and Vendor Management |
| 3.4.2 | Outsourcing |
| 3.4.3 | Cloud Computing |

### 3.4.1 Contract and Vendor Management

**Principle:** Define, approve, implement, and monitor required cyber security controls within contract and vendor management processes.

**Contract management** process requirements:

| Area | Key requirement |
|------|----------------|
| Procurement | Cyber security risk assessment as part of the procurement process |
| Tender | Specific cyber security requirements defined in the tender |
| Evaluation | Vendor replies evaluated on defined cyber security requirements |
| Testing | Agreed cyber security requirements tested (risk-based) |
| Incident process | Communication/escalation process for cyber security incidents defined |
| Contract exit | Cyber security requirements defined for exiting, terminating, or renewing contracts (including escrow agreements where applicable) |
| Confidentiality | Mutual confidentiality agreement required |

**Vendor management (SLA / service level management)** requirements:
- Periodic reporting, reviewing, and evaluating contractually agreed cyber security requirements in SLAs
- Baseline cyber security requirements applied in all cases
- Right to periodically perform cyber security reviews and audits
- Cyber security function involvement actively required in due diligence

---

### 3.4.2 Outsourcing

**Principle:** Define, implement, and monitor required cyber security controls within the outsourcing policy and process.

Key requirements:
- **SAMA approval required prior to material outsourcing** (per SAMA circular on outsourcing: 424-BCS-34720, 20/7/2008)
- Cyber security function involvement in outsourcing decisions
- Compliance with the SAMA outsourcing circular
- Cyber security requirements defined, approved, and communicated in the outsourcing policy

---

### 3.4.3 Cloud Computing

**Principle:** Define, implement, and monitor required cyber security controls for hybrid and public cloud services. *This requirement is not applicable to private cloud services (internal cloud).*

Cloud computing policy for hybrid and public cloud must address:

| Area | Key requirements |
|------|-----------------|
| **Adoption process** | Cyber security risk assessment and due diligence on the CSP; **SAMA approval required before using cloud services or signing with the cloud provider**; contract with cyber security requirements in place before using cloud services |
| **Data location** | In principle, only cloud services located in Saudi Arabia should be used; **SAMA explicit approval required** when cloud services are used outside Saudi Arabia |
| **Data use limitations** | Cloud provider must not use the Member Organisation's data for secondary purposes |
| **Security** | CSP must implement and monitor cyber security controls protecting confidentiality, integrity, and availability of Member Organisation's data |
| **Data segregation** | Member Organisation's data logically segregated from other tenants; CSP must be able to identify and distinguish Member Organisation's data at all times |
| **Business continuity** | Business continuity requirements met per the Member Organisation's BCM policy |
| **Audit rights** | Right to perform cyber security review, audit, and examination at the CSP |
| **Exit rights** | Termination rights; CSP returns data in usable format on termination; CSP irreversibly deletes data on termination |

---

## SAMA IT Governance Framework (v1.0, 2022)

Applies to all Member Organisations alongside the CSF. Focuses on IT-strategy alignment, value delivery, IT risk, IT performance, and resource management. Structured around governance and management practices aligned to COBIT and ISO 38500.

### Key governance elements assessed by SAMA inspectors

| Area | What inspectors look for |
|------|--------------------------|
| IT Governance Committee | Documented charter; defined decision rights; board reporting cadence; membership includes senior management |
| IT Strategy | IT strategy aligned to and approved by business strategy; reviewed periodically; evidenced as operational |
| IT Risk Management | Integrated with enterprise risk; IT risk register maintained; treatment plans tracked to closure |
| IT Performance Management | KPIs defined and reported to board/executive management; dashboard or reporting mechanism in place |
| IT Investment Governance | IT investment portfolio managed with business-case discipline; post-implementation reviews conducted |
| IT Compliance Management | Applicable laws and regulations identified; compliance monitored; audit findings tracked to closure |

**Common gap:** IT Governance Committee exists in name only, without a documented charter, formal decision rights, or a regular board reporting cadence.

---

## SAMA Business Continuity Management Framework (v1.0, 2017)

Applies alongside CSF. Sets BCM expectations aligned to ISO 22301 and SAMA supervisory requirements.

### Key BCM elements

| Element | Key requirements |
|---------|-----------------|
| BCM Policy | Approved by the board; reviewed at least annually |
| Business Impact Analysis (BIA) | Covers all critical business processes; updated at least annually; RTO/RPO per process approved by board |
| BCM Strategy | Documented recovery strategy per business process and technology tier |
| Business Continuity Plans | Documented per critical process; assigned roles; crisis communication procedures included |
| Disaster Recovery Plans | Documented per critical IT system; RTO/RPO targets tested against actual system recovery times |
| Exercise Programme | Annual programme; full-scope live failover at defined intervals; tabletop exercises alone are insufficient |
| Crisis Management | Arrangements integrated with regulatory communications; senior management escalation paths documented |
| Reporting | Periodic management and board reporting; BCM KPIs tracked |

**Common gaps:** BIA updated more than 12 months ago; RTO/RPO defined but not validated by live failover tests; exercises run as tabletop only; no SAMA communication procedure in the crisis management plan.

---

## Audit hot spots — triage list

Ranked by frequency in SAMA inspections and cyber maturity reviews:

1. **CISO independence (3.1.1):** CISO not independent from IT operations — shared reporting lines, budget, or staff evaluations with CIO/IT department.
2. **CISO nationality and SAMA no-objection (3.1.1):** CISO appointed without SAMA no-objection; nationality requirement not satisfied.
3. **Risk management process not cyber-tailored (3.2.1):** Generic enterprise risk methodology applied; four mandatory trigger scenarios not documented or implemented.
4. **SAMA approval for outsourcing and cloud (3.4.2, 3.4.3):** Material outsourcing or cloud adoption started without SAMA pre-approval.
5. **Maturity self-assessed but not evidenced (all domains):** Maturity scores in the self-assessment tool not supported by policy documents, implementation records, or independent verification.
6. **Vendor contracts missing SAMA-required clauses (3.4.1):** Legacy contracts without NDA, incident-notification procedures, or cyber security compliance obligations.
7. **Cloud data residency (3.4.3):** Foreign-hosted cloud services used without explicit SAMA approval for data outside Saudi Arabia.
8. **SAMA incident notification process not tested (3.3.15):** No documented notification procedure; SAMA IT Risk Supervision contact details out of date; procedure never exercised.
9. **Threat intelligence consumed but not actioned (3.3.16):** Intelligence feeds subscribed but no process to convert intelligence into SOC use cases, risk register updates, or patch prioritisation.
10. **SOC maturity (3.3.14):** SOC exists but lacks 24×7 coverage, SIEM with active detection use cases, or independent red-team testing evidence.
11. **Electronic banking — SAMA approval before launch (3.3.13):** New digital services launched without SAMA approval; MFA not covering all required transaction types.
12. **DDoS protection (3.3.8):** Scrubbing services absent or untested; no evidence of twice-annual DDoS scrubbing tests.
13. **Change management security gates (3.3.7):** CAB process lacks cyber security function sign-off stage; penetration testing not performed before launch of internet-facing changes.
14. **BCM not tested / RTO-RPO not achievable (BCM Framework):** BIA outdated; recovery objectives defined but not validated by live failover; exercises run as tabletop only.
15. **Vulnerability management classification not defined (3.3.17):** All vulnerabilities treated equally; no classification-driven timelines; critical and high-risk items not prioritised.

---

## Evidence expectations

| Domain / Control | Evidence a SAMA inspector will request |
|-----------------|----------------------------------------|
| Governance (3.1.1) | Board-approved committee charter; CISO appointment letter with SAMA no-objection; organisational chart confirming cyber security independence from IT |
| Strategy (3.1.2) | Approved cyber security strategy with Authorized Official sign-off; action plan with documented progress |
| Policy (3.1.3) | Board-endorsed cyber security policy (version date); supporting standards and procedures; distribution records |
| Risk management (3.2.1) | Risk management methodology document; risk register with entries, owners, and treatment status; records of four mandatory trigger scenarios |
| Reviews and audits (3.2.4, 3.2.5) | Last penetration test report for internet-facing services; audit report with scope, findings, and corrective action plans; committee minutes showing review of results |
| IAM (3.3.5) | IAM policy; MFA configuration screenshots; privileged access procedure; periodic access review records; off-boarding process evidence with timestamps |
| Infrastructure (3.3.8) | DDoS scrubbing contract and twice-annual test evidence; SIEM active use-case list; log retention configuration |
| Incident management (3.3.15) | Incident management policy; SAMA notification procedure with contact details; incident repository; last exercise record |
| Outsourcing and cloud (3.4.2, 3.4.3) | SAMA pre-approval letter; cloud use policy; data-residency confirmation; CSP contract with cyber security clauses, audit rights, and exit provisions |
| BCM | Board-approved BCM policy and BIA; RTO/RPO register; BC/DR plans; last exercise report including live failover evidence; board reporting evidence |

---

## Common pitfalls

- Treating the annual maturity self-assessment as a compliance checkbox exercise rather than a genuine evidence-grounded measurement — SAMA inspectors compare self-assessed scores against supporting evidence.
- CISO role filled by the CIO or IT Director — the independence requirement is absolute.
- Risk assessment conducted once at system inception but not at the four mandatory trigger points.
- Cloud services adopted under the assumption that SAMA approval is only required for "sensitive" data — the approval requirement applies to all public/hybrid cloud use.
- Vendor SLAs containing cyber security language that has never been verified, reviewed, or tested against actual service delivery.
- SOC built around a SIEM that ingests logs but has no tuned detection use cases and no alert escalation process.
- Maturity self-assessed at Level 3 for a control where a policy exists but the process is not operationally implemented.
- SAMA incident notification procedure listing contact details that are out of date.
- BCM plans referencing RTO/RPO targets that have never been validated by actual recovery tests.
- Electronic banking services updated or extended without re-applying for SAMA approval.
- CISO contract or appointment made without first obtaining SAMA no-objection.

---

## Key definitions (SAMA CSF terms)

| Term | Usage in SAMA CSF |
|------|-------------------|
| **Member Organisation (MO)** | Any organisation regulated by SAMA and within scope of the CSF |
| **CISO** | Chief Information Security Officer — full-time senior manager of the cyber security function; must hold Saudi nationality and SAMA no-objection |
| **Cyber Security Committee** | Board-mandated governance committee headed by an independent senior manager from a control function; meets minimum quarterly |
| **GRC** | Governance, Risk and Compliance tool — preferred mechanism for monitoring compliance with cyber security documentation (Level 3 indicator) |
| **KPI** | Key Performance Indicator — used to evaluate implementation progress (Level 3 requirement) |
| **KRI** | Key Risk Indicator — defines effectiveness measurement thresholds; used for trend reporting (Level 4 requirement) |
| **BCIS** | Banking Cybersecurity Intelligence Sharing — forum for threat intelligence sharing among SAMA Member Organisations |
| **SOC** | Security Operations Centre — designated team for 24×7 security event monitoring |
| **CERT** | Computer Emergency Response Team — designated team for cyber security incident management |
| **SIEM** | Security Information and Event Management — automated, centralised log analysis and event correlation |
| **SAMA IT Risk Supervision** | The SAMA supervisory unit that receives cyber incident notifications; must be contacted immediately on medium/high incidents |
| **SARIE** | Saudi Arabian Riyal Interbank Express — SAMA's real-time gross settlement payment system |
| **mada** | Saudi national payment scheme operated by the Saudi Payments company |

---

## Reporting and notification timelines

| Event | Action and timing |
|-------|------------------|
| Medium or high classified cyber security incident identified | **Immediate** verbal notification to SAMA IT Risk Supervision |
| Media interaction related to an incident | **No objection from SAMA IT Risk Supervision required before any media statement** |
| Post-incident formal report | Submit to SAMA IT Risk Supervision after operations resume (all required data fields per 3.3.15) |
| Annual cyber maturity self-assessment | Submit per SAMA regulatory calendar |
| New electronic banking service | **SAMA approval required before launch** |
| Material outsourcing | **SAMA approval required before commencement** |
| Cloud services (hybrid/public) | **SAMA approval required before use or before signing with cloud provider** |
| Scheduled downtime of electronic banking services | **Timely communication to SAMA and customers required** |

> **Important:** Exact written-report timelines after verbal notification are defined in the SAMA Cyber Incident Reporting Procedure, not in the CSF itself. Confirm against the version currently in force before advising on specific timeframes.

---

## Cross-references

- SAMA-supervised entities processing personal data also subject to **PDPL + Implementing Regulations** (SDAIA) and the **Personal Data Transfer Regulation** where data leaves KSA
- Cloud adoption by SAMA Member Organisations requires coordination with **CST CCRF** (cloud service provider licensing) and SAMA cloud pre-approval
- **NCA ECC-2:2024** may apply where the entity is also under NCA scope (uncommon but possible for certain critical financial infrastructure designations)
- International alignment: **ISO/IEC 27001:2022** (cybersecurity controls), **ISO 22301:2019** (BCM), **ISO 38500:2015** (IT governance), **NIST CSF 2.0**

---

## Related frameworks (read next)

| Need | File |
|------|------|
| Personal data processing | `PDPL.md` |
| Cloud cybersecurity controls | `CCC-2-2024.md` and `CST-Regulations.md` |
| NCA baseline (if dual-regulated) | `ECC-2-2024.md` |
| Data management and localisation | `NDMO-Standards.md` |

---

## Verification note

Domain structure, subdomain titles, control obligations, maturity model levels (0–5), CISO requirements (Saudi nationality and SAMA no-objection), domain applicability exceptions for non-banking institutions, incident notification requirements, and cloud/outsourcing pre-approval obligations are taken directly from the SAMA Cyber Security Framework v1.0 (May 2017) as published by SAMA. That document is the primary source for this rewrite.

The SAMA IT Governance Framework (v1.0, 2022) and SAMA Business Continuity Management Framework (v1.0, 2017) sections reflect known SAMA supervisory practice and published framework summaries. For exact subdomain-level references in those two frameworks, cite the SAMA source documents directly.

Where incident reporting timelines matter, consult the latest version of SAMA's Cyber Incident Reporting Procedure rather than relying solely on this file. Do not invent control section numbers — if uncertain, describe the obligation and flag for verification against the source document.
