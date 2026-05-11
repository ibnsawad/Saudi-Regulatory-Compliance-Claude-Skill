# CST CRF — Cybersecurity Regulatory Framework for Service Providers in the ICT Sector

## At a glance

| Field | Value |
|-------|-------|
| Instrument | Cybersecurity Regulatory Framework (CRF) for Service Providers in the Information and Communications Technology Sector |
| Issuer | Communications, Space and Technology Commission (CST), Kingdom of Saudi Arabia |
| Document code | RT08 |
| Version | Second Version, October 2023 |
| Previous version | First Version, September 2020 (covered ICT and Postal Sector; postal scope removed in 2023 revision) |
| Legal basis | Communications and Information Technology Act and its Bylaw; CST Ordinance related to maintaining user information and confidential documents, protecting the public interest, user trust, and confidentiality of communications |
| Binding language | Arabic (official); English translation is for information purposes only — Arabic original prevails in any discrepancy |
| Status | Mandatory for CST-licensed and CST-registered service providers; application may be mandatory to all, mandatory and heuristic, or partially mandatory at CST's sole discretion |
| Regulator | CST (formerly CITC) |
| Relationship to other frameworks | Applies alongside NCA ECC-2:2024; CNI-classified SPs must also comply with NCA ECC (via NCA's Essential Cybersecurity Controls); CRF does **not** overwrite or replace other issued regulatory frameworks — it supplements them. NCA monitors CNI-classified SP compliance with ECC separately. |

> **Scope clarification:** The CRF is **distinct** from both (a) the NCA ECC-2:2024 (which applies to government entities and CNI operators broadly) and (b) the CST Cloud Computing Services Provisioning Regulations RS10 (which covers cloud licensing and subscriber rights). The CRF is CST's own cybersecurity framework specifically for CST-licensed/registered ICT Service Providers — telecom operators, ISPs, managed service providers, and similar entities.

> **CITC → CST rename note:** The 2020 first version was issued under CITC. All obligations carry over under the renamed CST. References to CITC in older documents should be read as CST.

---

## Purpose

The CRF provides requirements for better management of cybersecurity risks through a consistent approach aligned with international best practices and local cybersecurity regulations. Stated objectives:

1. Regulate and empower cybersecurity practices of ICT-sector Service Providers (SPs).
2. Increase the overall cybersecurity maturity level of the ICT sector.
3. Adopt a risk management methodology to achieve cybersecurity requirements.
4. Encourage ICT-sector SPs to apply good practices for establishing appropriate cybersecurity measures.
5. Ensure confidentiality, integrity, and availability of services provided to customers.

---

## Exact structure

The CRF divides service providers into two tiers based on CNI classification, with different obligations for each.

### Non-CNI SP structure (the primary control set — Section 6)

| Level | Count |
|-------|-------|
| Requirement domains | 6 |
| Subdomains (categories) | 25 |
| Compliance levels defined | 3 (CL 1, CL 2, CL 3) |

### CNI SP structure (Section 5)

CNI-classified SPs follow the NCA Essential Cybersecurity Controls (ECC) rather than the non-CNI control table. CRF adds reporting and governance obligations on top.

### Compliance level tiers (Annex II)

| Compliance Level | Description |
|-----------------|-------------|
| **CL 1** | Basic security controls — foundational/mandatory baseline |
| **CL 2** | Advanced requirements — builds on CL 1 |
| **CL 3** | Efficiency monitoring and continuous improvement — builds on CL 1 and CL 2 |

Compliance with a higher level requires compliance with all preceding levels. CST defines the compliance target (level and date) for each SP category and communicates it officially.

---

## Applicability and classification

### SP classification

Service Providers under the CRF fall into two categories:

| Classification | Definition | Primary obligation |
|----------------|------------|-------------------|
| **CNI SP** | SP classified as Critical National Infrastructure by CST and/or NCA — assets, facilities, systems, networks, processes, and key operators whose loss or vulnerability could result in significant negative impact on the availability, integration, or delivery of basic ICT services | ECC (NCA) + CRF governance/reporting obligations |
| **Non-CNI SP** | All SPs licensed or registered by CST that are **not** classified as CNI | Full CRF control set (Domains 1–6) |

### Who is in scope

- All SPs licensed or registered by CST
- Those subject to CST as regulator of the ICT sector in KSA
- The framework applies regardless of whether a SP is inside or outside the Kingdom if subject to CST regulation

CST may, in its sole discretion, determine the scope of application (mandatory to all / mandatory and heuristic / partially mandatory).

---

## Section 5 — SP classified as Critical National Infrastructure

### Mandatory compliance obligation

All CNI SPs must comply with the **Essential Cybersecurity Controls (ECC)** issued by NCA (published on the NCA website).

### Roles and Responsibilities

| # | Obligation |
|---|-----------|
| 1 | CNI SP has full responsibility for its cybersecurity. |
| 2 | NCA monitors compliance of CNI SPs with ECC. |
| 3 | CNI SPs shall apply and implement controls in accordance with specified ECC compliance requirements. |
| 4 | CNI SPs shall provide CST with a **copy of compliance reports** submitted to NCA. |
| 5 | CNI SPs shall **share critical cybersecurity risks** with CST. |
| 6 | When a cybersecurity incident occurs, CNI SP must **immediately report to NCA** and **notify CST**. |
| 7 | CNI SPs shall share **security alerts, threat intelligence information, Indicators of Compromise (IoCs), and cybersecurity incident reports** with CST. |
| 8 | CST may add additional controls at any time; will define compliance targets and monitor through self-assessment, field inspections, compliance workshops, and proactive/incident-triggered audits. |

---

## Section 6 — Non-CNI SP: All domains, subdomains, and controls

### Domain overview

| Domain # | Domain name |
|----------|------------|
| 1 | Governance |
| 2 | Asset Management |
| 3 | Cybersecurity Risk Management |
| 4 | Logical Security |
| 5 | Physical Security |
| 6 | Third Party Security |

---

### Domain 1 — Governance

#### Requirements summary

| Ref | Requirement |
|-----|-------------|
| 1.1 | Define a cybersecurity strategy and develop an implementation roadmap to achieve defined objectives |
| 1.2 | Define and implement the relevant cybersecurity organisation structure responsible for cybersecurity activities |
| 1.3 | Ensure compliance with internal and relevant external (national, international) regulatory requirements |
| 1.4 | Conduct periodic independent cybersecurity audits covering internal and external compliance requirements |
| 1.5 | Conduct periodic cybersecurity awareness and trainings to ensure personnel has the necessary qualifications and skills |
| 1.6 | Provide customers with relevant cybersecurity information related to provided services |
| 1.7 | Ensure organisational cybersecurity requirements are included in the applied project management methodology |
| 1.8 | Ensure cybersecurity requirements related to human resources are addressed in case of any changes of employment status |

#### Subdomains and controls

**1.1 — Cybersecurity Strategy**

| Control ID | CL | Control |
|------------|-----|---------|
| 1.1.1 | CL 1 | Define and document requirements for the **[Cybersecurity Strategy]** covering: overall mission, objectives and activities in relation to cybersecurity; relevant legislative and regulatory compliance requirements; establishment of the cybersecurity program; top management commitment towards cybersecurity |
| 1.1.2 | CL 1 | Ensure the **[Cybersecurity Strategy]** is approved by top management |
| 1.1.3 | CL 1 | Ensure the **[Action Plan]** for the implementation of the cybersecurity strategy considers: Activities, Budget, Timeline, Resources (e.g. capabilities, personnel) |
| 1.1.4 | CL 3 | Continuously measure, review and update the **[Cybersecurity Strategy]** and corresponding **[Action Plan]** especially in case of changes in legislative/regulatory requirements, major organisational changes, or lessons learned from previous action plans |

*References: NIST CSWP – ID.BE; NIST.sp.800-53-r4 – PM-1; NCA ECC-1-1-1 through 1-1-3; NCA CSCC-1-1-1 through 1-1-3*

**1.2 — Cybersecurity Management**

| Control ID | CL | Control |
|------------|-----|---------|
| 1.2.1 | CL 1 | Define and document requirements for the **[Cybersecurity Organisation]** covering: cybersecurity committee with members representing different areas; needed cybersecurity functions/departments to implement the Action Plan; direct reporting to top management to avoid conflict of interest; allocating roles and responsibilities with conflicting duties and areas clearly segregated |
| 1.2.2 | CL 1 | Implement the defined **[Cybersecurity Organisation]** |
| 1.2.3 | CL 1 | Implement the **[Action Plan]** through the defined **[Cybersecurity Organisation]** |
| 1.2.4 | CL 1 | Oversee the implementation of the **[Action Plan]** by the cybersecurity committee through monitoring, dealing with conflicts, and enforcing necessary improvement measures |
| 1.2.5 | CL 3 | Continuously measure, review and optimise requirements for the **[Cybersecurity Organisation]** to ensure an efficient Cybersecurity Organisation |

*References: ISO 27001-5; ISO 27002-6.1.1 and 6.1.2; NCA ECC-1-2-1 through 1-2-3*

**1.3 — Cybersecurity Compliance**

| Control ID | CL | Control |
|------------|-----|---------|
| 1.3.1 | CL 1 | Define and document **[Requirements for Cybersecurity Compliance]** covering: relevant national legislative and regulatory requirements related to cybersecurity; locally accredited international/cross-border requirements (e.g. included in internationally agreements or commitments); organisation's internal requirements |
| 1.3.2 | CL 1 | Define and implement the **[Compliance Process]** to ensure compliance requirements are identified periodically, documented and communicated (e.g. when new regulatory requirements become effective) |
| 1.3.3 | CL 1 | Ensure the compliance requirements are incorporated within the organisation |
| 1.3.4 | CL 3 | Continuously measure, review and optimise the **[Requirements for Cybersecurity Compliance]** and the effectiveness of the process to ensure compliance |

*References: ISO 27002-18.1; NCA ECC-1-7-1 and 1-7-2*

**1.4 — Cybersecurity Audit**

| Control ID | CL | Control |
|------------|-----|---------|
| 1.4.1 | CL 2 | Define and document **[Requirements for Cybersecurity Audit]** covering: conducting independent and periodical audits (e.g. at least once a year for critical systems); protection and retention of **[Audit Records]**; reporting to top management |
| 1.4.2 | CL 2 | Define and implement **[Internal Audit]** process to verify compliance with the identified **[Requirements for Cybersecurity Compliance]** |
| 1.4.3 | CL 2 | Conduct independent audits at planned intervals (or when significant changes occur) to review implementation of the **[Requirements for Cybersecurity Compliance]** |
| 1.4.4 | CL 2 | Document the findings and recommendations and present them to top management |
| 1.4.5 | CL 2 | Protect the **[Audit Records]** from unauthorised access, modification, and destruction |
| 1.4.6 | CL 2 | Ensure that audit records are retained as proof of compliance with legislative and regulatory requirements |
| 1.4.7 | CL 3 | Continuously measure, review and optimise the **[Requirements for Cybersecurity Audit]** and the effectiveness of the process and review activities |

*References: ISO 27002-18.2 and 18.1.3; NIST.sp.800-53r4 – AU-6, AU-9, AU-11; NCA ECC-1-8; NCA CSCC-1-4*

**1.5 — Cybersecurity Awareness & Training**

| Control ID | CL | Control |
|------------|-----|---------|
| 1.5.1 | CL 1 | Define and document **[Requirements for Cybersecurity Awareness & Training]** covering: goals and scope; number and frequency of trainings/year; allocated resources |
| 1.5.2 | CL 1 | Define and implement a **[Cybersecurity Awareness & Training Program]** covering: cybersecurity roles and responsibilities of the targeted audience; trending cybersecurity events and threats (e.g. social engineering attacks, phone scams, impersonation calls); advice to personnel not to attempt unauthorised activities; secure handling of portable devices, storage media, email services (especially spam and phishing emails), internet surfing services and social media; clear desk and clear screen policy |
| 1.5.3 | CL 2 | Enhance the program to include periodic validation tests to evaluate effectiveness (e.g. check whether personnel will click on a suspicious link in an email) and record results |
| 1.5.4 | CL 2 | Define circumstances under which the program has to be provided (e.g. initial cybersecurity trainings to new users, training upon changes to information systems or job roles) |
| 1.5.5 | CL 2 | Tailor the program to provide specialised/security-related skills and trainings to: cybersecurity department; IT personnel; personnel working in software development; personnel involved in cybersecurity risk management; personnel with privileged access to critical information assets; executive personnel |
| 1.5.6 | CL 3 | Continuously measure, review and optimise the **[Requirements for Cybersecurity Awareness & Training]** |

*References: ISO 27002-7.2.2; SANS v6.1-17.4; NIST.sp.800-53r4 – AT-2; NCA ECC-1-9-4 through 1-10-5*

**1.6 — Customer Cybersecurity Awareness**

| Control ID | CL | Control |
|------------|-----|---------|
| 1.6.1 | CL 1 | Define and document **[Requirements for Customer Cybersecurity Awareness]** covering: goals and scope; number and frequency of trainings/year; allocated resources |
| 1.6.2 | CL 1 | Define and implement a **[Customer Cybersecurity Awareness Program]** covering: information on relevant emerging cybersecurity events and threats (e.g. social engineering attacks such as phone scams and impersonation calls); specific recommendations related to the provisioned service (e.g. how to be secure online, SMishing, and secure your mobile device) |
| 1.6.3 | CL 2 | Enhance and implement the **[Requirements for Customer Cybersecurity Awareness]** to periodically conduct the **[Customer Cybersecurity Awareness Program]** for the organisation's customers |
| 1.6.4 | CL 3 | Continuously measure, review and optimise the **[Requirements for Customer Cybersecurity Awareness]** |

*References: ISO 27002-7.2.2*

> **ICT-specific note:** The Customer Cybersecurity Awareness subdomain (1.6) is unique to the CST CRF and reflects the ICT sector's direct relationship with end users/subscribers. There is no equivalent in the NCA ECC.

**1.7 — Cybersecurity in Project Management**

| Control ID | CL | Control |
|------------|-----|---------|
| 1.7.1 | CL 1 | Define and document **[Requirements for Cybersecurity in Project Management]** covering: defining integration of cybersecurity in project management (e.g. cybersecurity personnel as part of the project team); defining project objectives to ensure cybersecurity is included in all phases of the project |
| 1.7.2 | CL 1 | Perform a risk assessment at the beginning and during each project in accordance with the **[Cybersecurity Risk Assessment]** to identify cybersecurity risks and define mitigation plans |
| 1.7.3 | CL 2 | Track the identified cybersecurity risks and monitor the implementation of the mitigation plans during the project **[Cybersecurity Risk Treatment and Monitoring]** |
| 1.7.4 | CL 3 | Continuously measure, review and optimise the **[Requirements for Cybersecurity in Project Management]** |

*References: ISO 27002-6-1-5; NCA ECC-1-6-1 through 1-6-4*

**1.8 — Cybersecurity in Human Resources**

| Control ID | CL | Control |
|------------|-----|---------|
| 1.8.1 | CL 1 | Define and document **[Requirements for Cybersecurity in Human Resources]** covering: defining cybersecurity requirements related to personnel (including contractors) before employment, during their work, and upon completion/termination of work; conducting background verification checks on all candidates for employment; hiring highly professional personnel on jobs related to critical systems; ensuring employment terms and agreements also cover code of conduct (e.g. non-disclosure agreements, cybersecurity responsibilities) during and after termination of employment; ensuring the code of conduct is signed by all personnel; enforcing the **[Acceptable Use of Information Assets]** |
| 1.8.2 | CL 1 | Ensure necessary actions (e.g. modify access authorisations to new operational role) are performed when individuals are reassigned or transferred to other positions |
| 1.8.3 | CL 1 | Ensure all suspected breaches of relevant cybersecurity requirements by personnel are subject to proper investigation and appropriate disciplinary action |
| 1.8.4 | CL 1 | Ensure necessary actions (e.g. revoking personnel access rights and privileges, retrieving assigned information assets, retaining access to information assets formerly controlled by the terminated individual) have been carried out upon completion of professional services or termination of personnel |
| 1.8.5 | CL 3 | Continuously measure, review and optimise the **[Requirements for Cybersecurity in Human Resources]** |

*References: ISO 27002-7.1.1 through 7.3.1 and 8.1.4; NIST.sp.800-53r4 – PS-4 and PS-5; NCA ECC-1-9-1 through 1-9-6; NCA CSCC-1-9-3 and CSCC-1-5-1*

---

### Domain 2 — Asset Management

#### Requirements summary

| Ref | Requirement |
|-----|-------------|
| 2.1 | Maintain an accurate and up-to-date asset inventory of all information assets with relevant details for efficient protection |
| 2.2 | Classify information assets to ensure risk-based protection |
| 2.3 | Manage use of personnel devices for business purposes to protect from cybersecurity risks (BYOD) |
| 2.4 | Define and enforce acceptable use policy to protect from risks imposed by inappropriate use of information assets |
| 2.5 | Maintain information assets to ensure continued availability and integrity |
| 2.6 | Ensure secure disposal of information assets to prevent unauthorised disclosure or modification |

**2.1 — Asset Discovery**

| Control ID | CL | Control |
|------------|-----|---------|
| 2.1.1 | CL 1 | Define and document **[Requirements for Asset Discovery]** covering: defining an inventory of information assets **[Asset Inventory]** (e.g. software, hardware, information, critical information assets, equipment, databases); defining the frequency for updating the **[Asset Inventory]**; ownership of the information assets |
| 2.1.2 | CL 1 | Define and implement an **{Asset Discovery}** process to identify all information assets belonging to the organisation and update the **[Asset Inventory]**; assign an asset owner to each information asset |
| 2.1.3 | CL 1 | Review and update the **[Asset Inventory]** based on the defined frequency or whenever there are modifications to information assets (addition and removal) |
| 2.1.4 | CL 2 | Use dedicated and automated tools to discover information assets; integrate and track them from a central system |
| 2.1.5 | CL 3 | Continuously measure, review and optimise the **[Requirements for Asset Discovery]** and the effectiveness of the process |

*References: ISO 27002-8.1 and 8.2 and 8.3.2; SANS v7.0-1.1, 1.2, 2.3, 2.5; NCA ECC-2-1-1 and 2-1-2 and 2-1-6; NCA CSCC-2-1-1 and 2-1-2 and 2-1-6*

**2.2 — Asset Classification**

| Control ID | CL | Control |
|------------|-----|---------|
| 2.2.1 | CL 1 | Define and document **[Requirements for Asset Classification]** covering: classification and labelling of information assets and the respective protective measures for identification, handling, transfer, storage, return, deletion and disposal |
| 2.2.2 | CL 1 | Define and implement an **{Asset Classification}** process to classify and label information assets within the **[Asset Inventory]** according to specific criteria (e.g. criticality, business value, legal requirements, confidentiality, integrity and availability) and the **[Requirements for Information Protection]** |
| 2.2.3 | CL 3 | Continuously measure, review and optimise the **[Requirements for Asset Classification]** and effectiveness of the process |

*References: ISO 27002-8.1.2, 8.2.1, 8.2.3; NIST CSWP – ID.AM-5; NCA ECC-2-1-5*

**2.3 — Bring Your Own Device (BYOD)**

| Control ID | CL | Control |
|------------|-----|---------|
| 2.3.1 | CL 1 | Define and document **[Cybersecurity Requirements for BYOD]** covering: isolation of personal information from business information; restrictions on use of devices depending on business interest; restrictions on access of critical systems; secure deletion of the organisation's information |
| 2.3.2 | CL 1 | Enforce the defined **[Cybersecurity Requirements for BYOD]** |
| 2.3.3 | CL 1 | Securely delete the organisation's information after completion of associated job function and when information is no longer necessary |
| 2.3.4 | CL 2 | Ensure the organisation's information stored on the devices are encrypted |
| 2.3.5 | CL 3 | Continuously measure, review and optimise the **[Cybersecurity Requirements for BYOD]** |

*References: SANS v6.1-15.9; NCA ECC-2-6-1 through 2-6-3; NCA CSCC-2-6-3 and CSCC-2-5-1*

**2.4 — Acceptable Use of Information Assets**

| Control ID | CL | Control |
|------------|-----|---------|
| 2.4.1 | CL 1 | Define and document the **[Requirements for Acceptable Use of Information Assets]** covering: the acceptable use of information assets |
| 2.4.2 | CL 1 | Ensure implementation of the **[Requirements for Acceptable Use of Information Assets]** (e.g. prohibiting installation of unwanted software, controlling access to web pages, allow use of removable media based on business-needs only) |
| 2.4.3 | CL 3 | Continuously measure, review and optimise the requirements for the **[Requirements for Acceptable Use of Information Assets]** |

*References: ISO 27002-8.1.3; NCA ECC-2-1-3 and 2-1-4*

**2.5 — Asset Maintenance**

| Control ID | CL | Control |
|------------|-----|---------|
| 2.5.1 | CL 2 | Define and document **[Requirements for Asset Maintenance]** covering: asset maintenance; tracking and monitoring; recovery plan |
| 2.5.2 | CL 2 | Define and implement an **{Asset Maintenance}** process to maintain and repair the organisation's information assets (including offsite assets) and keeping a log of these activities |
| 2.5.3 | CL 2 | As per the organisation-defined recovery plan, execute asset recovery during or after a security incident |
| 2.5.4 | CL 2 | Monitor information assets appropriately, based on the **[Asset Classification]** |
| 2.5.5 | CL 3 | Continuously measure, review and optimise the **[Requirements for Asset Maintenance]** and effectiveness of the process |

*References: NIST CSWP – PR.MA-1 and PR.MA-2 and RC.RP-1; NIST.sp.800-53r4 – PE-20; ISO 27002-11.2.4*

**2.6 — Secure Disposal of Assets**

| Control ID | CL | Control |
|------------|-----|---------|
| 2.6.1 | CL 1 | Define and document **[Requirements for Secure Disposal of Assets]** covering: setting rules for information asset disposal based on the classification and labelling of the information asset defined in the **[Asset Inventory]** |
| 2.6.2 | CL 1 | Define and implement a **{Secure Asset Disposal}** process to handle the disposal of information assets based on the **[Requirements for Secure Disposal of Assets]** using appropriate techniques (e.g. secure erase, drilling, shredding) in order to prevent unauthorised disclosure or modification of information stored on the assets |
| 2.6.3 | CL 3 | Continuously measure, review and optimise the **[Requirements for Secure Disposal of Assets]** and effectiveness of the process |

*References: ISO 27002-8.3.2; SANS v7.0-1.6 and v7.0-2.6; NCA ECC 2-14-3-4*

---

### Domain 3 — Cybersecurity Risk Management

#### Requirements summary

| Ref | Requirement |
|-----|-------------|
| 3.1 | Establish and implement an appropriate cybersecurity risk assessment approach to identify, analyse, and evaluate risks to protect information assets |
| 3.2 | Establish and implement an appropriate cybersecurity risk treatment and monitoring approach to manage identified risks and monitor treatment plans |

**3.1 — Cybersecurity Risk Assessment**

| Control ID | CL | Control |
|------------|-----|---------|
| 3.1.1 | CL 1 | Define and document **[Requirements for Cybersecurity Risk Assessment]** covering: purpose and scope of the risk assessment; the frequency and circumstances when risk assessment should be conducted; ensuring requirements cover risks to information assets of the organisation, individuals, and other organisations |
| 3.1.2 | CL 1 | Define and implement a **{Risk Assessment}** process consisting of: Risk identification (identify and document internal and external risks based on information assets **[Asset Discovery]** and maintain in a **[Risk Register]**); Risk analysis (analyse and document identified risks in terms of probability and impact); Risk evaluation (identify, prioritise, and document which risk should be treated or accepted based on risk appetite — must be officially approved by top management); Report the top cybersecurity risks within the **[Risk Register]** along with remediation plans to CST |
| 3.1.3 | CL 2 | Integrate the **{Risk Assessment}** process into the organisation's risk management framework and apply it at least for: in the early stages of major technical projects or major changes to the organisation or technical architecture; before launching new products and services |
| 3.1.4 | CL 3 | Continuously measure, review and optimise the **[Requirements for Cybersecurity Risk Assessment]** and effectiveness of the process |

*References: ISO 27005-7.2; NIST.sp.800-53r4 – RA-1 and RA-3 and PM-9 and PM-10; NIST CSWP – ID.RA and ID.SC; NCA ECC-1.5.1 through 1.5.4; NCA CSCC-1-5-1 through 1-5-4*

**3.2 — Cybersecurity Risk Treatment & Monitoring**

| Control ID | CL | Control |
|------------|-----|---------|
| 3.2.1 | CL 1 | Define and document **[Requirements for Cybersecurity Risk Treatment and Monitoring]** covering: the risk treatment plan; the risk monitoring plan |
| 3.2.2 | CL 1 | Define and implement a **{Risk Treatment}** process describing how assessed risks are treated, resulting in a **[Risk Treatment Plan]** |
| 3.2.3 | CL 1 | Define and implement a **{Risk Monitoring}** process that monitors and reviews the identified risks, the implementation of the risk treatment plan, the residual risk, and the status of accepted risks |
| 3.2.4 | CL 3 | Continuously measure, review and optimise the **[Requirements for Cybersecurity Risk Treatment and Monitoring]** and effectiveness of the processes |

*References: ISO 27005-9.3; NIST.sp.800-53r4 – PM-9; NIST CSWP – ID.RA and ID.SC; NCA ECC-1.5.1 through 1.5.4; NCA CSCC-1-5-1 and 1-5-2 and 1-5-4*

---

### Domain 4 — Logical Security

#### Requirements summary

| Ref | Requirement |
|-----|-------------|
| 4.1 | Ensure effective and adequate use of cryptography to provide confidentiality, integrity, authenticity and non-repudiation of information in transit, at rest, and in use |
| 4.2 | Manage changes to information assets to control consequences of changes |
| 4.3 | Identify vulnerabilities of information assets to prioritise and recommend remediation actions |
| 4.4 | Ensure cybersecurity patches are applied in appropriate timeframe to fix known issues and enhance resilience |
| 4.5 | Protect networks operated by the organisation from malicious activities and ensure network resilience against cyber threats |
| 4.6 | Monitor and protect event logs of information assets and report suspicious events |
| 4.7 | Manage access rights and implement appropriate authentication mechanisms to prevent unauthorised access |
| 4.8 | Create and enforce a list of software applications authorised to be installed and used within the organisation |
| 4.9 | Detect and respond to cybersecurity incidents to contain and minimise impact |
| 4.10 | Detect malware and prevent its spread in the organisation |
| 4.11 | Classify the organisation's information to ensure adequate protection |
| 4.12 | Take necessary measures including backup to ensure recovery of information assets after an incident |
| 4.13 | Implement baseline configuration settings to increase resilience of information assets |
| 4.14 | Implement a secure software development lifecycle |
| 4.15 | Protect email and web browsers against cybersecurity threats |
| 4.16 | Conduct penetration tests to evaluate the organisation's defense capabilities and detect vulnerabilities |

**4.1 — Cryptography**

| Control ID | CL | Control |
|------------|-----|---------|
| 4.1.1 | CL 1 | Define and document **[Requirements for Cryptography]** covering: defining basic cryptographic protocols and techniques (e.g. AES 256, RSA 2048, and PKI) together with relevant restrictions (e.g. self-signed certificates, MD5); conditions under which approved cryptographic protocols should be applied (data in transit, at rest, in use) taking into account the **[Requirements for Information Protection]** |
| 4.1.2 | CL 1 | Create a list of **[Cryptographic Solutions]** (e.g. products, algorithms and protocols) in accordance with relevant restrictions (e.g. legal, technical, national) and make sure it is approved by responsible roles |
| 4.1.3 | CL 1 | Use the **[Cryptographic Solutions]** based on identified circumstances, in order to protect information throughout its complete lifecycle (in transit, at rest, in use) according to classification **[Requirements for Information Protection]** |
| 4.1.4 | CL 2 | Define and implement a **{Life Cycle Management of Cryptographic Keys}** process for handling the generation, protection, archiving, recovery, and destruction of cryptographic keys |
| 4.1.5 | CL 3 | Continuously measure, review and optimise the **[Requirements for Cryptography]** |

*References: ISO 27002-10.1.1 and 10.1.2; SANS v7.0-16.4 and v7.0-18.5; NIST.sp.800-53r4 – SC-12 and SC-13; NCA ECC-2-8-1 through 2-8-4; NCA CSCC-2-8-3*

**4.2 — Change Management**

| Control ID | CL | Control |
|------------|-----|---------|
| 4.2.1 | CL 1 | Define and document **[Requirements for Change Management]** covering: identifying, classifying, and prioritising changes to information assets that affect cybersecurity |
| 4.2.2 | CL 1 | Define and implement the **{Change Management}** process to authorise cybersecurity-relevant changes (e.g. applied patches, configuration changes as part of remediation, upgrading or introduction of new equipment) |
| 4.2.3 | CL 1 | Plan and test the identified changes; assess the potential impact **[Cybersecurity Risk Assessment]** on cybersecurity, communicate the changes, and obtain approval from defined authorised roles (personnel/committee) |
| 4.2.4 | CL 2 | Enhance and implement the **[Requirements for Change Management]** to consider the procedure for emergency changes |
| 4.2.5 | CL 3 | Continuously measure, review and optimise the **[Requirements for Change Management]** and effectiveness of the process |

*References: ISO 27002-12.1.2; NCA ECC-1-6-2; NCA CSCC-1-6-2*

**4.3 — Vulnerability Management**

| Control ID | CL | Control |
|------------|-----|---------|
| 4.3.1 | CL 1 | Define and document **[Requirements for Vulnerability Management]** covering: scope, tools and technology, reporting; frequency of scans; timeframes for remediating vulnerabilities (based on criticality) |
| 4.3.2 | CL 1 | Define and implement a **{Vulnerability Management}** process consisting of: Scanning (conduct vulnerability scans on information assets using relevant tools according to defined frequency, e.g. monthly for critical systems); Analysing (analyse the impact, assign a criticality, and define timeframes for remediation); Reporting (report vulnerabilities **[Vulnerabilities Report]** along with criticality to respective departments and define the recommended action **[Patch Management]**) |
| 4.3.3 | CL 2 | Perform vulnerability scans triggered by distinct events (e.g. product release, major technical change, new equipment added to networks) |
| 4.3.4 | CL 2 | Use specialised and automated vulnerability scanning tools (e.g. dedicated tools for webservers, mobile apps) |
| 4.3.5 | CL 3 | Enhance vulnerability classification and reporting based on inputs from other sources (e.g. penetration testing, threat intelligence) |
| 4.3.6 | CL 3 | Continuously measure, review and optimise the **[Requirements for Vulnerability Management]** and effectiveness of the process |

*References: ISO 27002-12.6; SANS v7-3 and v6.1-4.1 and v6.1-4.8; NIST.sp.800-53r4 – RA-5 and CA-8; NCA ECC-2-10-1 through 2-10-4; NCA CSCC-2-9-2 and 2-10-1 through 2-10-3*

**4.4 — Patch Management**

| Control ID | CL | Control |
|------------|-----|---------|
| 4.4.1 | CL 1 | Define and document **[Requirements for Patch Management]** covering: scope of patch management; tools and techniques and patch management triggers; patch testing environment; frequency (incorporating regular patching) |
| 4.4.2 | CL 1 | Define and implement a **{Patch Management}** process that develops a **[Remediation Plan]** considering: **[Vulnerabilities Report]**; **[Cybersecurity Risk Assessment]**; testing patches before deploying in production and creating necessary backups; **[Change Management]**; regular patch releases |
| 4.4.3 | CL 2 | Ensure installed patches are successful and detected vulnerabilities have been remediated |
| 4.4.4 | CL 2 | Enhance and implement the **[Requirements for Patch Management]** to include emergency patch activities for highly critical vulnerabilities |
| 4.4.5 | CL 2 | Apply patch packages (or software updates) on a regular basis for all information assets |
| 4.4.6 | CL 2 | Automate and enforce patch management wherever possible (e.g. end user devices) |
| 4.4.7 | CL 2 | Enhance the **[Remediation Plan]** and execute it based on threat intelligence, **[Penetration Testing]** and other sources |
| 4.4.8 | CL 3 | Continuously measure, review and optimise the **[Requirements for Patch Management]** and effectiveness of the process |

*References: SANS v6.1-4.4 and v6.1-4.5 and v6.1-4.7; SANS v7.0-3.7; NCA ECC-2-3-3-3 and 2-10-3-4; NCA CSCC-2-3-1 and 2-9-1*

**4.5 — Network Security**

| Control ID | CL | Control |
|------------|-----|---------|
| 4.5.1 | CL 1 | Define and document **[Requirements for Network Security]** covering: managing and controlling the security of networks operated by the organisation and information assets connected to it; segregation of networks; security requirements to protect network services and information transferred through it |
| 4.5.2 | CL 1 | Document the **[Network Plan]** which clearly reflects the actual state of the network (e.g. all connections into the networks, network devices, critical servers) — *ICT-specific* |
| 4.5.3 | CL 1 | Ensure incoming and outgoing traffic is controlled (e.g. preventing malicious traffic, monitoring traffic loads, controlling unwanted communication such as email, SMS) — *ICT-specific* |
| 4.5.4 | CL 1 | Ensure only trusted and authorised protocols and IP address ranges are allowed to cross the boundary (e.g. using firewalls); disable unused protocols (e.g. disabling IPv6 if not used) to reduce the attack surface |
| 4.5.5 | CL 1 | Protect the information transferred (e.g. from interception, copying, modification) through the organisation's network and ensure confidentiality and integrity are maintained (e.g. encryption) |
| 4.5.6 | CL 1 | Segregate the network into zones (e.g. domains, subnets) depending on the criticality of information assets or services present in those zones (e.g. isolating production network from development and testing networks, separating network containing user workstations from authentication servers) |
| 4.5.7 | CL 1 | Restrict access to the organisation's network (both wired and wireless networks) based on the access control list **[Identity and Access Management]** |
| 4.5.8 | CL 1 | Secure end user data, voice and signalling information transferred through the organisation's telecommunications network (e.g. VoIP/SIP traffic, SS7) — *ICT-specific* |
| 4.5.9 | CL 1 | Segregate the hosted customer network from the organisation's telecommunication operational network — *ICT-specific* |
| 4.5.10 | CL 2 | Cooperate with other organisations that own or operate interconnected networks to detect and protect connected users and networks from malicious acts (e.g. block email spams, DDoS, abnormal traffic patterns, implement Caller ID authentication to block illegal caller ID spoofing) — *ICT-specific* |
| 4.5.11 | CL 2 | Ensure interfaces (e.g. Internet Exchange Points) to other networks are appropriately secured (e.g. securing BGP infrastructure, implementing high availability through redundancy, using strong cryptography) — *ICT-specific* |
| 4.5.12 | CL 2 | Enhance and implement the **[Requirements for Network Security]** to handle internal and external attacks (e.g. DoS/DDoS) against the organisation's network |
| 4.5.13 | CL 2 | Ensure mechanisms are in place at the ICT facilities to detect and avoid network congestion which results in disruptions of services (e.g. implementation of additional facilities to balance the traffic load) — *ICT-specific* |
| 4.5.14 | CL 2 | Use specific tools to analyse and filter all traffic (e.g. port filtering, host-based filtering) to detect any unauthorised traffic in the network |
| 4.5.15 | CL 3 | Continuously measure, review and optimise the **[Requirements for Network Security]** |

*References: ISO 27002-13.1.1, 13.1.3, 13.2.1; ISO 27011-X.1051 multiple TEL controls; SANS v7.0-9.4, 12.3, 12.4, 12.6, 12.7; NCA ECC-2-5-1 through 2-5-3-6; NCA CSCC-2-5-3 and 2-4-1*

**4.6 — Logging and Monitoring**

| Control ID | CL | Control |
|------------|-----|---------|
| 4.6.1 | CL 1 | Define and document **[Requirements for Logging and Monitoring]** covering: logging the events (e.g. login attempts, configuration changes, firewall logs) related to information assets; monitoring of event logs and analysis of detected events; required retention period and protection of event logs |
| 4.6.2 | CL 1 | Activate event logging and record event logs (e.g. user activities, exceptions, information security events, privileged operations) related to information assets |
| 4.6.3 | CL 1 | Protect log information and logging facilities from unauthorised access and tampering |
| 4.6.4 | CL 1 | Periodically review event logs and report suspicious events and detected anomalies to responsible personnel **[Incident Management]** |
| 4.6.5 | CL 1 | Retain logs for a defined time duration as specified in the requirements (e.g. 12 months) |
| 4.6.6 | CL 2 | Collect, monitor and analyse events using a log management tool (e.g. SIEM) that includes advanced detection and integration capabilities |
| 4.6.7 | CL 2 | Real-time monitoring and review of event logs of critical information assets |
| 4.6.8 | CL 2 | Improve the event detection methods by use of dedicated tools (e.g. Threat Intelligence Platforms) to update the rules of log management tools |
| 4.6.9 | CL 3 | Continuously measure, review and optimise the **[Requirements for Logging and Monitoring]** |

*References: ISO 27002-12.4.1 and 12.4.2; SANS v7.0-6.6; NIST CSWP – DE.AE-4 and DE.DP-5; NCA ECC-2-12-1 through 2-12-4; NCA CSCC-2-12-3 and 2-11-1 and 2-11-2 and 2-12-1*

**4.7 — Identity and Access Management (IAM)**

| Control ID | CL | Control |
|------------|-----|---------|
| 4.7.1 | CL 1 | Define and document **[Requirements for Identity and Access Management]** covering: user accounts, privilege accounts, granting and revoking access rights; authentication and authorisation requirements (e.g. in case of remote access, two-factor authentication); password management requirements |
| 4.7.2 | CL 1 | Define and implement a process to **{Allocate/Revoke User Rights}** considering: assigning access rights to users based on what they are authorised to use (e.g. Role Based Access Control); reallocating user access rights upon change of job functions; managing user authentication and authorisation based on access control principle (e.g. need-to-know, need-to-use, least privilege, segregation of duties) and maintaining an up-to-date **[Access Control List]**; revoking access rights to information systems upon change of contractual agreements (e.g. termination of employment) |
| 4.7.3 | CL 1 | Control and restrict the allocation and use of privilege access rights |
| 4.7.4 | CL 1 | Provide multi-factor authentication for access to sensitive and critical information systems as well as for remote access |
| 4.7.5 | CL 1 | Enforce password management requirements (e.g. use of strong passwords for authentication, regular password changes, account suspension and lockouts after multiple failed login attempts) and ensure user authentication information is secured against disclosure (e.g. using encryption mechanisms during transfer) |
| 4.7.6 | CL 2 | Regularly review user identity and access rights (review frequency taking into consideration different account types, criticality of information assets) and ensure conformance to access control principles (e.g. asset owner should regularly review user access rights) |
| 4.7.7 | CL 2 | Enhance and implement the **[Requirements for Identity and Access Management]** to use tools to automate and centralise identity and access management |
| 4.7.8 | CL 2 | Use dedicated systems for tasks that require administrative access (e.g. configuration of critical systems) |
| 4.7.9 | CL 3 | Continuously measure, review and optimise the **[Requirements for Identity and Access Management]** and effectiveness of the process |

*References: ISO 27002-9.1.2, 9.2.1 through 9.2.6, 9.4.3; SANS v7.0-4.6; NCA ECC-2-2-1 through 2-2-4; NCA CSCC-2-2-1 through 2-2-3*

**4.8 — Application Whitelisting**

| Control ID | CL | Control |
|------------|-----|---------|
| 4.8.1 | CL 1 | Define and document **[Requirements for Application Whitelisting]** covering: a list of authorised software; approved application whitelisting tools |
| 4.8.2 | CL 1 | Establish and disseminate an **[Index of Authorized Software]** including software applications, software libraries (e.g. *.dll, *.ocx, *.so) and digitally signed scripts (e.g. *.ps1, *.py, macros) |
| 4.8.3 | CL 1 | Review and update the **[Index of Authorized Software]** on a regular basis |
| 4.8.4 | CL 2 | Use application whitelisting tools to ensure only authorised software executes on all information assets and ensure that the application whitelisting technology cannot be disabled or bypassed |
| 4.8.5 | CL 3 | Continuously measure, review and optimise the **[Requirements for Application Whitelisting]** |

*References: SANS v6.1-2.2 and v7.0-2.6 through 2.9; NCA CSCC-2-3-1-1*

**4.9 — Incident Management**

| Control ID | CL | Control |
|------------|-----|---------|
| 4.9.1 | CL 1 | Define and document **[Requirements for Incident Management]** covering: incident definition, identification and classification, prioritisation, and response; incident reporting structure; testing the incident response process; evidence collection; learning from information security incidents |
| 4.9.2 | CL 1 | Define and implement **{Incident Response}** process considering: incident detection by analysing reported events **[Logging and Monitoring]**; incident classification based on predefined criteria; respond to cybersecurity incidents (contain, eradicate, and recover) within organisation-defined timeframes **[Change Management]**; prepare the **[Incident Report]** and lessons learned; **report cybersecurity incidents with appropriate details to CST** |
| 4.9.3 | CL 1 | Conduct regular trainings to test the **{Incident Response}** process for its effectiveness (e.g. testing communication channels, response times) |
| 4.9.4 | CL 2 | Enhance and implement the **[Requirements for Incident Management]** to use incident management tools to automate the process and integrate with other relevant systems for increasing efficiency |
| 4.9.5 | CL 2 | Gather threat intelligence and use it during the analysis of information security events |
| 4.9.6 | CL 2 | Establish a forensic team to investigate information security incidents |
| 4.9.7 | CL 2 | Identify, collect, and preserve evidence of information security incidents; use knowledge gained to reduce probability and impact of future incidents |
| 4.9.8 | CL 3 | Continuously measure, review and optimise the **[Requirements for Incident Management]** and effectiveness of the process |

*References: ISO 27002-16.1 through 16.1.7; NIST.sp.800-53r4 – IR-1 through IR-6; NIST CSWP RS.AN-3; NCA ECC-2-13-1 through 2-13-4*

**4.10 — Malware Handling**

| Control ID | CL | Control |
|------------|-----|---------|
| 4.10.1 | CL 1 | Define and document **[Requirements for Malware Handling]** covering: detection and prevention controls to protect against malware; implementation of technical controls to safeguard information assets |
| 4.10.2 | CL 1 | Use end-point protection software, ensure it regularly updates its signature database, and implement measures to prevent this software from being deactivated or altered by users |
| 4.10.3 | CL 1 | Implement appropriate security measures to block different sources of malicious traffic (e.g. internet filters, email filters to block phishing emails, restricting download of dangerous content) **[Email & Web Browser Protection]** |
| 4.10.4 | CL 1 | Implement protective measures to safeguard removable media against malware (e.g. conduct an anti-malware scan of removable media when inserted or connected) |
| 4.10.5 | CL 2 | Implement advanced malware detection techniques (e.g. enable DNS query logging to detect hostname lookups for known malicious domains) |
| 4.10.6 | CL 2 | Use advanced logging and monitoring tools for analysing and alerting of detected malware events **[Logging and Monitoring]** |
| 4.10.7 | CL 3 | Continuously measure, review and optimise the **[Requirements for Malware Handling]** |

*References: NIST.sp.800-53r4 – SI-3; SANS v7.0-7.9, 8.1, 8.2, 8.4, 8.6, 8.7; NCA ECC-2-4-3 and 2-5-3; NCA CSCC-2-5-3*

**4.11 — Information Protection**

| Control ID | CL | Control |
|------------|-----|---------|
| 4.11.1 | CL 1 | Define and document **[Requirements for Information Protection]** covering: classification level and criteria (e.g. restricted, confidential, public) **{Asset Classification}**; privacy, ownership, protection, transmission, and retention of information; ensuring the privacy of personally identifiable information or other sensitive information **[Cybersecurity Compliance]** |
| 4.11.2 | CL 1 | Define and implement an **{Information Classification}** process considering: categorise information based on classification criteria; handle critical information according to defined criteria (e.g. business value, legal, technical, national and cross-border requirements) |
| 4.11.3 | CL 1 | Implement security mechanisms to protect information (in transit, at rest, in use) taking into account the **[Requirements for Cryptography]** and data loss prevention techniques |
| 4.11.4 | CL 1 | Prevent the transmission of information from production environment to another environment and the usage of critical systems data in test and development environments |
| 4.11.5 | CL 2 | Determine a retention period for information in accordance with organisational requirements and relevant legislations; restrict retention of critical information to necessary requirements **[Cybersecurity Compliance]** |
| 4.11.6 | CL 3 | Continuously measure, review and optimise the **[Requirements for Information Protection]** and effectiveness of the process |

*References: ISO 27002-8.2.1; SANS v6.1-13.3; NCA ECC-2-7-1 through 2-7-4; NCA CSCC-2-6-1 and 2-7-3*

**4.12 — Backup and Recovery Management**

| Control ID | CL | Control |
|------------|-----|---------|
| 4.12.1 | CL 1 | Define and document **[Requirements for Backup and Recovery Management]** covering: scope of online and offline backups including retention period; rapid recovery of information after cybersecurity incidents; periodically backup of information assets; protection of backups; availability of backups |
| 4.12.2 | CL 1 | Define and implement a **{Backup}** process considering: business requirements (e.g. Recovery Point Objective); scope of online and offline backups and their coverage of information assets (e.g. backup of complete system, through processes such as imaging) |
| 4.12.3 | CL 1 | Define and implement a **{Recovery}** process to ensure information assets are recovered within an acceptable timeframe based on criticality **[Asset Classification]** |
| 4.12.4 | CL 1 | Ensure confidentiality, integrity, and availability of backups in adverse situations (e.g. using encryption, protection of backups via physical security **[Protection of Physical Information Assets]**) |
| 4.12.5 | CL 2 | Establish an alternate storage/backup site that provides security measures equivalent to the primary site |
| 4.12.6 | CL 2 | Continuously test and review the **{Backup}** and **{Recovery}** processes to check their effectiveness |
| 4.12.7 | CL 2 | Enhance and implement the **[Requirements for Backup and Recovery Management]** to use tools to automate the **{Backup}** and **{Recovery}** processes |
| 4.12.8 | CL 3 | Continuously measure, review and optimise the **[Requirements for Backup and Recovery Management]** and effectiveness of the processes |

*References: ISO 27002-12.3.1; NIST.sp.800-53r4 – CP-6 and CP-9; NCA ECC-2-9-1 through 2-9-3; NCA CSCC-2-8-1 and 2-9-3*

**4.13 — Configuration Management and Hardening**

| Control ID | CL | Control |
|------------|-----|---------|
| 4.13.1 | CL 1 | Define and document **[Requirements for Configuration Management and Hardening]** covering: secure images and baseline configurations for information assets and used software/hardware |
| 4.13.2 | CL 1 | Implement the defined baseline configuration settings for information assets |
| 4.13.3 | CL 1 | Employ system and device hardening according to industry-recognised best practices (e.g. disable the default configurations which have been installed on the network devices) — *ICT-specific* |
| 4.13.4 | CL 1 | Restrict the use of unnecessary functions (e.g. use of unauthorised ports, services) and configure the information assets to provide only essential capabilities |
| 4.13.5 | CL 1 | Monitor and verify configuration settings against the baseline settings |
| 4.13.6 | CL 2 | Utilise a dedicated tool to monitor and verify configuration settings and alert upon unauthorised deviation from baseline configuration settings |
| 4.13.7 | CL 2 | Use dedicated tools that can automatically configure/reconfigure configuration settings **[Change Management]** on all information assets |
| 4.13.8 | CL 3 | Continuously measure, review and optimise the **[Requirements for Configuration Management and Hardening]** |

*References: NIST.sp.800-53r4 – CM-6 and CM-7; SANS v6.1-3.1 and v7.0-5.4 and v7.0-5.5 and v7.0-11.3; NCA ECC-1-6-2-2 and 1-6-3-5 and 2-5-3-5*

**4.14 — Secure Software Development**

| Control ID | CL | Control |
|------------|-----|---------|
| 4.14.1 | CL 1 | Define and document **[Requirements for Secure Software Development]** covering: utilisation of secure coding standards and practices (e.g. approved libraries, APIs); segregation and allocation of access rights to different environments; conducting tests to verify compliance of developed software with cybersecurity requirements |
| 4.14.2 | CL 1 | Ensure only authorised personnel have access to the appropriate environment **[Identity and Access Management]** |
| 4.14.3 | CL 1 | Utilise secure coding standards and practices (e.g. security-by-design principles supported via static or dynamic analysis tools) and ensure the security of integration between applications |
| 4.14.4 | CL 1 | Ensure a secure and reliable transmission of software between environments |
| 4.14.5 | CL 1 | Use only trusted and up-to-date third-party components for internally developed software |
| 4.14.6 | CL 2 | Conduct and document a security review for developed software and source code (e.g. performing error checking for all input) |
| 4.14.7 | CL 2 | Conduct security tests to verify the extent to which developed software meets cybersecurity requirements |
| 4.14.8 | CL 3 | Continuously measure, review and optimise the **[Requirements for Secure Software Development]** |

*References: ISO 27002-14.2.1; SANS v7.0-18.1 through 18.9; NIST.sp.800-53-r4 SA-15-b; NCA ECC-1-6-3; NCA CSCC-1-3-2 and 1-6-3*

**4.15 — Email & Web Browser Protection**

| Control ID | CL | Control |
|------------|-----|---------|
| 4.15.1 | CL 1 | Define and document **[Requirements for Emails and Web Browser Protection]** covering: utilisation of standardised security mechanisms for email and web browser protection |
| 4.15.2 | CL 1 | Implement the **[Requirements for Emails and Web Browser Protection]** (e.g. email filtering for spam and phishing protection, multi-factor authentication, backup and archive for emails, protection against Advanced Persistent Threats, untrusted websites) |
| 4.15.3 | CL 1 | Restrict access to unauthorised web-based email services (e.g. firewall rules, network-based URL filters) |
| 4.15.4 | CL 3 | Continuously measure, review and optimise the **[Requirements for Emails and Web Browser Protection]** |

*References: SANS v7.0-7; NCA ECC-2-5-3-3 and 2-4-1 through 2-4-4*

**4.16 — Penetration Testing**

| Control ID | CL | Control |
|------------|-----|---------|
| 4.16.1 | CL 2 | Define and document **[Requirements for Penetration Testing]** covering: purpose of penetration tests and overall objectives; defining the frequency of penetration tests |
| 4.16.2 | CL 2 | Define a **{Penetration Testing}** process consisting of the scope and frequency (e.g. at least once quarterly on critical information assets) of penetration tests using standard methodologies to identify unknown vulnerabilities (e.g. grey box testing, white box testing) |
| 4.16.3 | CL 2 | Depending on the penetration test methodology used, use the **[Vulnerabilities Report]** as an input to guide the penetration tests |
| 4.16.4 | CL 2 | Report the **[Penetration Test Report]** to the respective departments to trigger remediation actions when applicable **[Patch Management]** |
| 4.16.5 | CL 3 | Continuously measure, review and optimise the **[Requirements for Penetration Testing]** and effectiveness of the process |

*References: SANS v6.1-20.1 and v6.1-20.6; NCA ECC-2-11; NCA CSCC-2-10*

---

### Domain 5 — Physical Security

**5.1 — Protection of Physical Information Assets**

| Control ID | CL | Control |
|------------|-----|---------|
| 5.1.1 | CL 1 | Define and document **[Requirements for the Protection of Physical Information Assets]** covering: protecting physical facilities that host information assets; protecting physical information assets and physical facilities installed on offsite premises; delivery and loading areas; transportation of physical information assets; defining physical protection measures against environmental threats |
| 5.1.2 | CL 1 | Define security perimeters in order to protect physical facilities (e.g. offices, rooms, data centers, ground stations, and telecommunication processing equipment) that contain information assets |
| 5.1.3 | CL 1 | Ensure physical information assets reside within appropriate security zones and are stored in secure physical facilities during non-operational hours |
| 5.1.4 | CL 1 | Secure the delivery/loading areas that could be used by unauthorised personnel to enter the organisation's premises (e.g. segregate physically where possible incoming and outgoing shipments) |
| 5.1.5 | CL 1 | Protect physical information assets against damage from environmental threats, hazards, and unauthorised physical access, considering: protection measures against physical threats (fires, accidents, power failures, failures in supporting utilities, natural disasters); securing cables against interception, interference or damage; operating physical information assets per manufacturer requirements and controlling working atmosphere (temperature, humidity, air quality, water, light); protection against unauthorised access (e.g. surveillance through CCTV, alarm systems, motion sensors) — *ICT-specific for ground stations and telecom equipment* |
| 5.1.6 | CL 1 | Protect physical information assets during their transportation taking into consideration assessed risks and security during movement — *ICT-specific* |
| 5.1.7 | CL 3 | Continuously measure, review and optimise the **[Requirements for the Protection of Physical Information Assets]** |

*References: ISO 27002-11.1.1 through 11.2.9; ISO 27011-X.1051 TEL.11.1.7 through TEL.11.3.1; NIST.sp.800-53r4 – PE-11 through PE-17; NCA ECC-3-1 and 2-14-1 through 2-14-4*

**5.2 — Physical Access Management**

| Control ID | CL | Control |
|------------|-----|---------|
| 5.2.1 | CL 1 | Define and document **[Requirements for Physical Access Management]** covering: physical access authorisations and control; monitoring physical access |
| 5.2.2 | CL 1 | Create a **[Physical Access Control List]** of individuals with authorised access to the organisation's facilities and issue appropriate authorisation credentials |
| 5.2.3 | CL 1 | Define and implement **{Physical Access Management}** process to grant and manage access (e.g. secure keys) to physical facilities |
| 5.2.4 | CL 1 | Establish physical entry controls for visitors (e.g. provide security badges to visitors and monitor unusual activity) |
| 5.2.5 | CL 2 | Continuously review the **[Physical Access Control List]** of individuals with authorised access to facilities and remove them from the list when access is no longer required |
| 5.2.6 | CL 2 | Regularly review physical access logs for suspicious activity **[Logging and Monitoring]** |
| 5.2.7 | CL 3 | Continuously measure, review and optimise the **[Requirements for Physical Access Management]** and effectiveness of the process |

*References: ISO 27002-11.1.2; NIST.sp.800-53r4 – PE-2, PE-3, PE-6, PE-8; NCA ECC-2-14*

---

### Domain 6 — Third Party Security

**6.1 — Cloud Services**

| Control ID | CL | Control |
|------------|-----|---------|
| 6.1.1 | CL 1 | Define and document **[Requirements for Cloud Services]** covering: cybersecurity requirements expected from the cloud provider; service level agreements |
| 6.1.2 | CL 1 | Conduct a risk assessment in accordance with the **[Cybersecurity Risk Assessment]** and **[Information Protection]** prior to adopting cloud services (or in the event of changes in relevant legislative and regulatory requirements) to ensure risks related to cloud services are appropriately identified and addressed |
| 6.1.3 | CL 1 | Based on the cloud risk assessment and the **[Requirements for Asset Classification]** identify the **[Cloud Cybersecurity Requirements]** needed to protect confidentiality, integrity and availability of information assets in the cloud |
| 6.1.4 | CL 1 | Establish service level agreements (SLAs) with the cloud service provider which consider at least: **[Cloud Cybersecurity Requirements]**; incident notification and recovery obligations; making sure the cloud service can be terminated in case of non-compliance with contractual agreements; defining exit procedures covering secure deletion of data (e.g. irreversibly delete organisation's data, media destruction, returning organisation data in a usable format, data retention) |
| 6.1.5 | CL 1 | **Ensure that the hosting and storage site of the organisation's data is in the Kingdom of Saudi Arabia** |
| 6.1.6 | CL 2 | Audit, review, and monitor the cloud service provider for compliance with contractual obligations |
| 6.1.7 | CL 3 | Continuously measure, review and optimise the **[Requirements for Cloud Services]** |

*References: ISO 27002-15.1 and 15.2.1; NCA ECC-4-2-1 through 4-2-4; NCA CSCC-4-2-1 and 4-2-3*

**6.2 — Outsourcing Services**

| Control ID | CL | Control |
|------------|-----|---------|
| 6.2.1 | CL 1 | Define and document **[Requirements for Outsourcing Services]** covering: risk assessment for outsourcing information assets to a third party; addressing cybersecurity requirements expected from the third-party provider; service level agreements |
| 6.2.2 | CL 1 | Conduct a risk assessment in accordance with the **[Cybersecurity Risk Assessment]** and **[Information Protection]** prior to outsourcing any information assets to a third party provider (or in the event of changes in relevant legislative and regulatory requirements) to ensure risks related to outsourcing are appropriately addressed |
| 6.2.3 | CL 1 | Based on risk assessment, identify the **[Third-party Cybersecurity Requirements]** which the third-party provider must comply with to protect confidentiality, integrity and availability of outsourced information assets (e.g. non-disclosure clauses) |
| 6.2.4 | CL 1 | Establish service level agreements with the third-party service provider covering: **[Third-party Cybersecurity Requirements]**; communication procedure in case of cybersecurity incident; ensuring outsourced service can be terminated in case of non-compliance with contractual agreements; defining exit procedures covering secure deletion of data (e.g. media destruction, encryption) |
| 6.2.5 | CL 2 | Audit, review, and monitor the third-party provider for compliance with contractual obligations |
| 6.2.6 | CL 2 | Ensure third-party personnel are screened when contracted to work on critical systems |
| 6.2.7 | CL 3 | Continuously measure, review and optimise the **[Requirements for Outsourcing Services]** |

*References: ISO 27002-15.1 and 15.2.1; NIST CSWP – ID.SC-4 and ID.SC-5; NCA ECC-4-1-1 through 4-1-4; NCA CSCC-4-1-1 through 4-1-4*

---

## Roles and Responsibilities — Non-CNI SPs

| # | Party | Obligation |
|---|-------|-----------|
| 1 | **SP** | Full responsibility for its cybersecurity |
| 2 | **CST** | Monitors non-CNI SP compliance with defined requirements through self-assessment, field inspections, compliance workshops, proactive and incident-triggered audits |
| 3 | **CST** | Periodically reviews and updates the CRF |
| 4 | **CST** | Defines compliance requirements and sets target dates to ensure non-CNI SP compliance with the CRF |
| 5 | **SP** | Applies and implements requirements and controls in accordance with specified compliance targets |
| 6 | **SP** | Submits compliance reporting (e.g. self-assessment) or other means upon request from CST |
| 7 | **SP** | Provides information and documentation to CST when requested, in addition to defined reporting in the CRF |

---

## Key definitions (Glossary — Section 3)

| Term | CRF definition |
|------|---------------|
| Access Control | The process of granting or denying specific requests for obtaining and using information and related information processing services and to enter specific physical facilities |
| APT Protection | Protection against advanced threats that use invisible techniques to gain unauthorised access to systems and networks and stay as long as possible through circumventing detection and protection tools; viruses and zero-day malware are used |
| Asset / Information Assets | Anything tangible or intangible that has value to the organisation; includes persons, machineries, utilities, patents, software, services, information and characteristics (e.g. organisation's reputation, public image, skill and knowledge) |
| Attack | Any kind of malicious activity that attempts to achieve unauthorised access, collection, disabling, prevention, destroy or sabotage of the information system resources or information itself |
| Audit | Independent review and examination of records and activities to assess effectiveness of cybersecurity controls and ensure compliance with policies, operational procedures and relevant standard, legal and regulatory requirements |
| Availability | Ensuring timely access to and use of information, data, systems and applications |
| BYOD | Bring your own device — personally owned devices (laptops, tablets, smart phones) that personal and contractors are permitted to use to carry out business functions |
| Change Management | A service management system ensuring systematic and proactive approach using effective standard methods and procedures; helps all stakeholders move from current state to desired state and reduces impact of incidents on service |
| Cloud Computing | A model for enabling on-demand network access to a shared pool of configurable IT capabilities/resources that can be rapidly provisioned and released with minimal operation management; five characteristics: on-demand self-service, ubiquitous network access, location independent resource pooling, rapid elasticity, measured service; three delivery models: SaaS, PaaS, IaaS; four access models: Private Cloud, Community Cloud, Public Cloud, Hybrid Cloud |
| CNI — Critical National Infrastructure | Assets, facilities, systems, networks, processes, and key operators whose loss or vulnerability to security breaches may result in significant negative impact on availability, integration or delivery of basic services, including services that could result in major losses or compromise the stability or security of the ICT sector |
| Critical Systems | Systems in which breakdown, unauthorised changes, and unauthorised access lead to highly affect the availability of services, organisation's operations, economic, financial or social effects at the national level |
| Cryptography | Rules including principles, methods and means of storing and transmitting data/information in a particular form to conceal its semantic content, prevent unauthorised use or prevent undetected modification |
| Cybersecurity Incidents | A breach of a system's security policy in order to affect its integrity or availability and/or the unauthorised access or attempted access to a system or systems |
| Cybersecurity Resilience | The overall ability of organisations to withstand cyber events and, where harm is caused, recover from them |
| Cybersecurity Risks | Risks to organisational operations, assets, individuals, other organisations, or the nation due to potential unauthorised access, use, disclosure, disruption, modification, or destruction of information and/or information systems |
| Data and Information Classification | Setting the sensitivity level of data and information resulting in security controls for each level; classification is set according to predefined categories |
| Disaster Recovery | Programs, activities and plans designed to restore the organisation's critical business functions and services to an acceptable situation following exposure to cyber attacks or disruption |
| IPS | A system with intrusion detection capabilities as well as the ability to prevent and stop suspicious or potential incidents |
| Least Privilege | Basic principle in cybersecurity that aims at granting users the access privileges they need to carry out their official responsibilities only |
| LSP | Licensed Service Providers — all service providers that have requested and own a license from CST to provide services as specified in respective licences |
| Malware | A program that infects systems, usually covertly, with the intent of compromising confidentiality, integrity, or availability of the victim's data, applications, or operating system |
| MFA | Multi-Factor Authentication — a security system that verifies user identity using several separate elements: Knowledge (something only the user knows); Possession (something only owned by user e.g. OTP device, SMS); Inherent Characteristics (e.g. fingerprint) |
| Need-to-know and Need-to-use | The restriction of data, considered sensitive unless one has a specific need to know; for official business duties |
| PII | Personally identifiable information — information which can be used to distinguish or trace the identity of an individual alone, or combined with other personal or identifying information |
| Segregation of Duties | Key principle in cybersecurity that aims at minimising errors and fraud when processing specific tasks; accomplished through having several people with different privileges required to complete a task |
| SIEM | Security Information and Event Management — system that manages and analyses security events logs in real time to provide monitoring of threats, analysis of results of interrelated rules for event logs and reports on logs data, and incident response |
| Threat Intelligence | Provides organised information and analysis of recent, current and potential attacks that could pose a cyber threat to the organisation |
| Vulnerability | Any type of weakness in a computer system, software, application, set of procedures, or in anything that leaves cybersecurity exposed to a threat |
| Zero-Day Malware | Malware that is unknown before, produced/disseminated recently, and normally hard to detect by signature-based protection anti-malware applications |

---

## Compliance levels — detailed mapping

### Domain-level CL summary

| Domain | Sub-domain | Min CL for any control | Max CL required |
|--------|-----------|----------------------|----------------|
| 1 — Governance | 1.1 Cybersecurity Strategy | CL 1 (core) | CL 3 (continuous improvement) |
| 1 — Governance | 1.2 Cybersecurity Management | CL 1 (core) | CL 3 |
| 1 — Governance | 1.3 Cybersecurity Compliance | CL 1 (core) | CL 3 |
| 1 — Governance | 1.4 Cybersecurity Audit | CL 2 (all controls) | CL 3 |
| 1 — Governance | 1.5 Awareness & Training | CL 1 (core) | CL 3 |
| 1 — Governance | 1.6 Customer Cybersecurity Awareness | CL 1 (core) | CL 3 |
| 1 — Governance | 1.7 Cybersecurity in Project Mgmt | CL 1 (core) | CL 3 |
| 1 — Governance | 1.8 Cybersecurity in Human Resources | CL 1 (core) | CL 3 |
| 2 — Asset Mgmt | 2.1 Asset Discovery | CL 1 (core) | CL 3 |
| 2 — Asset Mgmt | 2.2 Asset Classification | CL 1 (core) | CL 3 |
| 2 — Asset Mgmt | 2.3 BYOD | CL 1 (core) | CL 3 |
| 2 — Asset Mgmt | 2.4 Acceptable Use | CL 1 (core) | CL 3 |
| 2 — Asset Mgmt | 2.5 Asset Maintenance | CL 2 (all controls) | CL 3 |
| 2 — Asset Mgmt | 2.6 Secure Disposal | CL 1 (core) | CL 3 |
| 3 — Risk Mgmt | 3.1 Risk Assessment | CL 1 (core) | CL 3 |
| 3 — Risk Mgmt | 3.2 Risk Treatment & Monitoring | CL 1 (core) | CL 3 |
| 4 — Logical Security | 4.1 Cryptography | CL 1 (core) | CL 3 |
| 4 — Logical Security | 4.2 Change Management | CL 1 (core) | CL 3 |
| 4 — Logical Security | 4.3 Vulnerability Management | CL 1 (core) | CL 3 |
| 4 — Logical Security | 4.4 Patch Management | CL 1 (core) | CL 3 |
| 4 — Logical Security | 4.5 Network Security | CL 1 (core) | CL 3 |
| 4 — Logical Security | 4.6 Logging and Monitoring | CL 1 (core) | CL 3 |
| 4 — Logical Security | 4.7 IAM | CL 1 (core) | CL 3 |
| 4 — Logical Security | 4.8 Application Whitelisting | CL 1 (core) | CL 3 |
| 4 — Logical Security | 4.9 Incident Management | CL 1 (core) | CL 3 |
| 4 — Logical Security | 4.10 Malware Handling | CL 1 (core) | CL 3 |
| 4 — Logical Security | 4.11 Information Protection | CL 1 (core) | CL 3 |
| 4 — Logical Security | 4.12 Backup & Recovery | CL 1 (core) | CL 3 |
| 4 — Logical Security | 4.13 Configuration Mgmt & Hardening | CL 1 (core) | CL 3 |
| 4 — Logical Security | 4.14 Secure Software Development | CL 1 (core) | CL 3 |
| 4 — Logical Security | 4.15 Email & Web Browser Protection | CL 1 (core) | CL 3 |
| 4 — Logical Security | 4.16 Penetration Testing | CL 2 (all controls) | CL 3 |
| 5 — Physical Security | 5.1 Protection of Physical Info Assets | CL 1 (core) | CL 3 |
| 5 — Physical Security | 5.2 Physical Access Management | CL 1 (core) | CL 3 |
| 6 — Third Party Security | 6.1 Cloud Services | CL 1 (core) | CL 3 |
| 6 — Third Party Security | 6.2 Outsourcing Services | CL 1 (core) | CL 3 |

> **Key observation:** Subdomain 1.4 (Cybersecurity Audit) and subdomain 4.16 (Penetration Testing) start at CL 2 — there are no CL 1 controls in these subdomains. An SP at CL 1 compliance target does not yet have formal independent audit or formal penetration testing requirements. As soon as CST sets a CL 2 target, these become binding.

---

## Audit hot spots — triage list

Ranked by frequency and regulatory exposure in CST compliance assessments:

1. **Cybersecurity strategy not approved by top management (1.1.2):** A documented strategy exists but lacks board/CEO-level approval. CST treats absence of approval as a fundamental governance failure.
2. **No customer cybersecurity awareness programme (1.6):** Unique to ICT sector; many SPs do not have any formal programme informing customers about phishing, SMishing, and similar threats. CST will raise this in customer-protection assessments.
3. **Risk register not reported to CST (3.1.2):** The CRF explicitly requires top cybersecurity risks and remediation plans to be reported to CST. This is a reporting obligation distinct from internal risk management and is commonly missed.
4. **Cloud data not hosted in KSA (6.1.5):** Explicit data-residency requirement in the CRF — organisation's data must be hosted and stored inside the Kingdom. SPs using offshore cloud storage for operational data are in breach.
5. **No formal incident reporting to CST (4.9.2):** The CRF requires cybersecurity incidents to be reported to CST. Many SPs have internal incident response procedures but no documented CST reporting channel or triggers.
6. **Log retention period undefined or too short (4.6.5):** CRF suggests 12 months as an example retention period. SPs with 30- or 90-day retention windows have a gap, especially where CST or NCA request historical log evidence.
7. **MFA not deployed for remote access and privileged accounts (4.7.4):** Required at CL 1; enforcement is rigorous; OTP via SMS alone may not satisfy CL 2 expectations.
8. **SIEM/log management absent at CL 2 (4.6.6):** Basic log collection exists (CL 1) but no SIEM with detection rules and integration — a CL 2 gap that CST increasingly expects large SPs to close.
9. **Vulnerability scans not conducted at defined frequency (4.3.2):** CRF requires monthly scans for critical systems; quarterly scans are frequently found instead. Ad-hoc scanning without documented frequency also fails.
10. **Penetration testing absent or below required quarterly frequency for critical assets (4.16.2):** At CL 2 the CRF requires at least quarterly penetration tests on critical information assets. Annual-only testing is non-compliant.
11. **No background verification for new hires in cybersecurity/critical system roles (1.8.1):** Required at CL 1 across all personnel; frequently absent for contractor and temporary staff.
12. **Third-party SLAs without cybersecurity clauses (6.2.4):** Legacy outsourcing contracts and cloud agreements without cybersecurity requirements, incident communication procedures, or exit/deletion clauses are non-compliant at CL 1.
13. **No BYOD policy or encryption on BYOD devices (2.3):** BYOD policy often exists in draft but is not enforced; encryption of organisational data on personal devices (2.3.4) is a CL 2 requirement commonly absent.
14. **Application whitelisting absent (4.8):** Many SPs manage software through anti-malware alone; a formal authorised-software index and whitelisting enforcement are separate requirements.
15. **No separation of customer network from telecom operational network (4.5.9):** ICT-specific; particularly relevant for ISPs and telecom operators — hosted customer network must be segregated from the SP's own operational network.

---

## Evidence expectations — what CST / an auditor will request

| Control area | Evidence CST / auditor will request | Control ref |
|-------------|--------------------------------------|------------|
| Cybersecurity strategy | Approved strategy document with top management signature/minute of approval; action plan with budget, timeline, and resources | 1.1.1–1.1.3 |
| Cybersecurity organisation | Org chart showing cybersecurity department; committee TOR; role descriptions with segregation-of-duties analysis | 1.2.1–1.2.4 |
| Compliance tracking | Compliance register or log; records of how new regulations are identified and tracked; evidence of regulatory change management process | 1.3.1–1.3.3 |
| Audit records | Independent audit report(s); audit schedule; records of findings and corrective actions reported to top management; log retention proof | 1.4.1–1.4.6 |
| Awareness & training | Training records with completion dates and staff names; training content; role-differentiated training matrix; phishing simulation results | 1.5.1–1.5.5 |
| Customer awareness | Customer-facing cybersecurity awareness materials (website, SMS, notifications); programme documentation; delivery evidence | 1.6.1–1.6.3 |
| HR cybersecurity | Background check records; onboarding checklist with cybersecurity elements; offboarding checklist showing access revocation evidence | 1.8.1–1.8.4 |
| Asset inventory | Up-to-date asset inventory spreadsheet or CMDB; discovery tool output; asset owner assignments | 2.1.1–2.1.3 |
| Asset classification | Classification policy; evidence that assets in the inventory carry a classification label; protection measures documented per class | 2.2.1–2.2.2 |
| BYOD | BYOD policy; MDM/MAM enrolment records; encryption proof on enrolled devices | 2.3.1–2.3.4 |
| Secure disposal | Disposal policy; certificate of destruction or secure-erase logs for disposed assets | 2.6.1–2.6.2 |
| Risk register | Risk register document with top risks identified, probability/impact assessed, treatment plans, top management approval; evidence of CST reporting | 3.1.1–3.1.2 |
| Vulnerability management | Vulnerability scan reports with dates and scope; remediation tracking tickets; evidence of critical-system monthly scanning | 4.3.1–4.3.2 |
| Patch management | Patch policy; remediation plan; evidence of pre-production testing; proof of regular patching across asset inventory | 4.4.1–4.4.5 |
| Network security | Network architecture diagram (Network Plan); firewall rule-sets; network segmentation evidence; traffic monitoring tool output | 4.5.1–4.5.9 |
| Logging & monitoring | SIEM configuration; log source list; retention setting proof (12-month); sample alerts and investigation records | 4.6.1–4.6.6 |
| IAM | Access control list; MFA configuration proof; privileged access management records; periodic review records | 4.7.1–4.7.6 |
| Incident management | Incident response procedure; records of past incident reports submitted to CST; tabletop exercise results | 4.9.1–4.9.3 |
| Malware handling | Endpoint protection tool name and version; signature update logs; scan schedule | 4.10.1–4.10.4 |
| Information protection | Data classification policy; DLP tool configuration and alert logs; evidence of production-to-test data restrictions | 4.11.1–4.11.4 |
| Backup & recovery | Backup schedule and scope documentation; recovery test results with RTOs/RPOs; evidence of encrypted backups | 4.12.1–4.12.4 |
| Configuration management | Hardening baselines (per device type); configuration scan reports; evidence of deviation alerting | 4.13.1–4.13.5 |
| Penetration testing | Penetration test report (dated within the last quarter for critical assets); scope statement; remediation actions taken | 4.16.1–4.16.4 |
| Cloud services | Cloud SLA; evidence of KSA data residency (provider confirmation or architecture diagram); cloud risk assessment | 6.1.2–6.1.5 |
| Outsourcing | Third-party contracts with cybersecurity clauses; vendor risk assessments; vendor audit reports or certifications | 6.2.1–6.2.5 |

---

## ICT-specific controls (marked in the source document)

The CRF marks certain controls as ICT-specific (telecom and ICT sector obligations not present in general cybersecurity frameworks). Key ICT-specific controls:

| Control | Obligation |
|---------|-----------|
| 4.5.2 | Document the **[Network Plan]** reflecting actual state of the network (all connections, network devices, critical servers) |
| 4.5.3 | Control incoming and outgoing traffic including SMS and voice communications |
| 4.5.8 | Secure end user data, voice and signalling information transferred through the organisation's telecommunications network (e.g. VoIP/SIP traffic, SS7) |
| 4.5.9 | Segregate hosted customer network from the organisation's telecommunications operational network |
| 4.5.10 | Cooperate with interconnected network operators to detect and block malicious acts (spam, DDoS, illegal Caller ID spoofing) |
| 4.5.11 | Secure Internet Exchange Points (e.g. securing BGP infrastructure, implementing redundancy, strong cryptography) |
| 4.5.13 | Ensure network congestion detection and load-balancing mechanisms at ICT facilities |
| 4.13.3 | Employ system and device hardening — disabling default configurations on network devices |
| 5.1.5 | Protect ground stations and telecommunications processing equipment from physical and environmental threats |
| 5.1.6 | Protect physical information assets during transportation |

---

## Common pitfalls

- **Treating CRF as a checklist rather than a maturity programme:** The three compliance levels mean that CL 1 compliance is a floor, not a ceiling. CST will communicate target compliance levels per SP category. Organisations that achieve CL 1 only and have no roadmap to CL 2/3 face escalating risk as CST raises targets.
- **Confusing the CRF with the NCA ECC:** Both may apply simultaneously (CNI SPs must comply with ECC and CRF governance obligations; non-CNI SPs may also be subject to ECC under NCA's broader mandate). Treat them as additive, not alternative.
- **Missing the CST risk-reporting obligation (3.1.2):** The requirement to report top cybersecurity risks and remediation plans to CST is explicit and distinguishes the CRF from purely internal risk management. Many compliance programmes document risks internally but never route them to CST.
- **Assuming the cloud data-residency obligation is only in CST CCSR:** CRF §6.1.5 creates a separate, standalone data-residency obligation for ICT SPs' own operational data. An SP that hosts its own systems on foreign cloud without KSA residency is in breach of the CRF even if it complies with the CCSR subscriber-data obligations.
- **Customer awareness treated as a "nice to have":** Subdomain 1.6 is mandatory. CST has enforcement interest in consumer protection. Absence of a formal customer cybersecurity awareness programme is a cited non-compliance in assessments.
- **No formal separation between hosted customer network and telecom operational network (4.5.9):** ISPs and telecoms that provision shared infrastructure without logical or physical separation between customer-facing services and their own operational/management plane are in breach at CL 1.
- **SS7 and SIP/VoIP security treated as a network operations matter, not a cybersecurity compliance matter (4.5.8):** The CRF explicitly includes voice and signalling security as a cybersecurity obligation. Network teams may not be aware of the compliance angle.
- **Penetration testing deferred to annual cycles despite CL 2 quarterly requirement for critical assets (4.16.2):** This is one of the most common gaps when SPs transition from CL 1 to CL 2.
- **No third-party cybersecurity clause in legacy outsourcing agreements (6.2.4):** Legacy contracts without exit and secure-deletion clauses are non-compliant. A remediation programme reviewing all third-party agreements against CRF Domain 6 requirements is typically needed.
- **Application whitelisting confused with anti-malware (4.8):** Anti-malware does not satisfy the whitelisting requirement. A formal, approved list of authorised software and tools to enforce it are required separately.

---

## Related frameworks

| Framework | Relationship | Reference |
|-----------|-------------|-----------|
| NCA ECC-2:2024 | CNI SPs must comply with ECC (per CRF Section 5); CRF references NCA ECC controls throughout the control tables; non-CNI SPs subject to NCA's direct designation may also need ECC | ECC-2-2024.md |
| NCA CCC-2:2024 | Cloud cybersecurity controls — applicable where the ICT SP is also a CSP or cloud tenant; CRF 6.1 adds a parallel cloud obligation | CCC-2-2024.md |
| NCA DCC-1:2022 | Data cybersecurity controls — extends ECC; applies to CNI SPs; non-CNI SPs should apply DCC principles when handling sensitive data | DCC-1-2022.md |
| CST Cloud Computing Services Provisioning Regulations (RS10, v4 2023) | Separate CST instrument covering cloud licensing, subscriber data rights, and registration categories; distinct from the CRF but may apply simultaneously to CSPs also licensed as ICT SPs | CST-Regulations.md |
| PDPL + Implementing Regulations | Applies alongside the CRF to all personal data processed by ICT SPs; CRF 4.11 requires PII protection and references cybersecurity compliance | PDPL.md |
| NDMO Data Management Standards | Data classification guidance used in CRF 2.2 and 4.11 aligns with NDMO classification framework; government-sector ICT SP data handling | NDMO-Standards.md |
| ISO/IEC 27001:2022 | Multiple CRF controls reference ISO 27002; CRF compliance programme can be designed to produce ISO 27001 ISMS artefacts with minimal additional effort | — |
| NIST CSF 2.0 | CRF control references include NIST CSWP and SP 800-53r4 throughout; cross-mapping to NIST CSF Identify/Protect/Detect/Respond/Recover is straightforward | — |

---

## Verification note

All domain names, subdomain names and numbers, control IDs, compliance levels, control text, ICT-specific control markers, glossary definitions, roles and responsibilities, annex compliance level structure, and references in this file are verified directly against the source PDF of the **Cybersecurity Regulatory Framework (CRF) for Service Providers in the Information and Communications Technology Sector**, document RT08, Second Version, October 2023, issued by CST.

**Confirmed from source PDF:**
- Document reference: RT08, Second Version, October 2023
- Previous version: First Version, September 2020 (included Postal Sector — removed in 2023 revision)
- Two SP tiers: CNI (Section 5 — ECC obligations) and non-CNI (Section 6 — full CRF control set)
- Three compliance levels: CL 1 (basic), CL 2 (advanced), CL 3 (continuous improvement)
- 6 domains, 25 subdomains for non-CNI SPs
- Full control tables for all 25 subdomains as reproduced above, with CL designations verified per-control
- All ICT-specific control markers (the ICT-specific globe icon in the source document) confirmed
- All cross-references to NCA ECC, ISO 27002, NIST, and SANS as listed in the source document's reference rows
- Glossary: all 30+ defined terms confirmed from Section 3 of the source PDF
- Annex I (Annex Scope): clarification of compliance targets and non-CNI SP structure confirmed
- Annex II (Compliance Levels): three-tier pyramid structure (CL 1/2/3) confirmed
- Annex III (Structure of controls): 6-domain/25-subdomain wheel diagram and domain/category breakdown diagram confirmed
- Roles and responsibilities for both CNI SPs (Section 5) and non-CNI SPs (Section 6, end of chapter) confirmed
- Control 6.1.5 (KSA data residency for hosting and storage) confirmed from source
- Control 3.1.2 (reporting top risks to CST) confirmed from source
- Control 4.9.2 (reporting cybersecurity incidents to CST) confirmed from source

**Items requiring separate confirmation:**
- CST-published compliance target communications (compliance level and target date per SP category communicated officially by CST — exact current targets not in the source PDF)
- "Guide for Cloud Computing Service Providers in the Kingdom of Saudi Arabia" referenced in the CST CCSR; separate from the CRF
- Any CST executive decisions issued under CRF since October 2023 supplementing or amending the CRF
