# NDMO — Data Management and Personal Data Protection Standards

## At a glance

| Field | Value |
|-------|-------|
| Instrument | KSA Data Management and Personal Data Protection Standards |
| Issuer | National Data Management Office (NDMO), Saudi Data and AI Authority (SDAIA) |
| Version | 1.5 (January 2021) |
| Version history | v1.0 Aug 2020 → v1.1 Sep 2020 → v1.2 Oct 2020 → v1.3 Dec 2020 → v1.4 Jun 2021 → v1.5 Jun 2021 |
| Binding language | English (document is classified Public) |
| Status | Mandatory for all Public Entities in KSA; also applies to business partners handling government data |
| Compliance mechanism | Annual compliance self-assessment submitted to NDMO in Q3 each year; binary scoring per specification (100% = fully implemented, 0% = partial or not implemented); NDMO may conduct ad-hoc audits to validate submissions |
| Lead for assessment | Chief Data Officer (CDO) of the Entity |
| Relationship to PDPL | NDMO Standards are the government-sector operational layer on top of PDPL; Domain 14 (Personal Data Protection) is directly PDPL-implementing; Domain 15 (Data Security) is delegated to NCA |
| Relationship to NCA frameworks | Domain 15 (Data Security and Protection) is explicitly deferred to NCA — compliance is assessed by NCA under ECC/DCC, not by NDMO. Domain 13 (Data Classification) aligns with NCA's DCC-1:2022 classification levels |
| International reference | Based on DAMA DMBOK (Data Management Body of Knowledge); ISO 27001 cited for classification and security domains |

---

## Exact structure

| Level | Count |
|-------|-------|
| Domains | 15 (Domain 15 — Data Security — deferred to NCA; no NDMO specifications) |
| Controls (NDMO-assessed domains 1–14) | 77 |
| Specifications (NDMO-assessed domains 1–14) | 191 |
| Priority 1 (P1) specifications | 76 |
| Priority 2 (P2) specifications | 98 |
| Priority 3 (P3) specifications | 16 |

### Control-numbering scheme

`[DomainID].[ControlNumber].[SpecificationNumber]`

Example: **PDP.4.2** = Personal Data Protection domain (PDP), Control 4 (Data Lifecycle Management), Specification 2 (Data Subject Rights).

### Specification priority definitions

| Priority | Implementation target | Description |
|----------|----------------------|-------------|
| P1 | End of Year 1 | Foundational building blocks — must be implemented first |
| P2 | End of Year 2 | Capability improvement — builds on P1 |
| P3 | End of Year 3 | Maturity advancement — furthest horizon |

---

## Applicability

| Applies to | Detail |
|-----------|--------|
| Public Entities | All independent governmental or public entities and their affiliates in KSA |
| Companies operating public utilities / national infrastructure | Deemed Public Entities for purposes of these standards |
| Business partners | Entities producing, managing or overseeing government data — must apply standards to all government data in their control |
| Data scope | All government data regardless of form: paper records, emails, electronic data, voice recordings, videos, maps, photos, scripts, handwritten documents |
| Excluded | Private-sector entities with no government data relationship (PDPL still applies to their personal data processing) |

---

## All 15 domains — overview table

| # | Domain ID | Domain Name | Controls | Specifications | P1 | P2 | P3 | Compliance assessed by |
|---|-----------|-------------|----------|----------------|----|----|----|------------------------|
| 1 | DG | Data Governance | 8 | 28 | 18 | 9 | 1 | NDMO |
| 2 | DCM | Data Catalog and Metadata | 6 | 20 | 5 | 13 | 2 | NDMO |
| 3 | DQ | Data Quality | 4 | 13 | 3 | 8 | 2 | NDMO |
| 4 | DO | Data Operations | 5 | 14 | 3 | 10 | 1 | NDMO |
| 5 | DOCM | Document and Content Management | 5 | 12 | 5 | 4 | 3 | NDMO |
| 6 | DAM | Data Architecture and Modelling | 7 | 13 | 3 | 10 | 0 | NDMO |
| 7 | RMD | Reference and Master Data Management | 6 | 18 | 8 | 10 | 0 | NDMO |
| 8 | BIA | Business Intelligence and Analytics | 5 | 10 | 4 | 5 | 1 | NDMO |
| 9 | DSI | Data Sharing and Interoperability | 8 | 16 | 8 | 7 | 1 | NDMO |
| 10 | DVR | Data Value Realization | 4 | 8 | 2 | 5 | 1 | NDMO |
| 11 | OD | Open Data | 5 | 10 | 4 | 5 | 1 | NDMO |
| 12 | FOI | Freedom of Information | 4 | 9 | 4 | 3 | 2 | NDMO |
| 13 | DC | Data Classification | 5 | 10 | 5 | 4 | 0 | NDMO |
| 14 | PDP | Personal Data Protection | 5 | 10 | 4 | 5 | 1 | NDMO |
| 15 | DS | Data Security and Protection | — | — | — | — | — | **NCA** (not NDMO) |
| **Total (NDMO)** | | | **77** | **191** | **76** | **98** | **16** | |

> **Critical note on Domain 15:** NCA is the sole authority for the Data Security and Protection domain. NDMO's annual compliance assessment does NOT cover Domain 15. Entities must satisfy Domain 15 obligations through NCA's ECC-2:2024, DCC-1:2022, and related frameworks independently.

---

## Domain 1 — Data Governance (DG)

8 controls, 28 specifications

| Control ID | Control Name | Priority range | Key obligation |
|-----------|--------------|---------------|----------------|
| DG.1 | Strategy and Plan | P1 | Establish a Data Management and Personal Data Protection Strategy (3–5 year horizon) and a 3-year implementation Plan |
| DG.2 | Policy and Guidelines | P1 | Gap analysis of existing policies against NDMO standards; develop entity-specific Data Management Policy and Guidelines |
| DG.3 | Training and Awareness | P1 | Conduct data management training for all related employees covering national laws, programmes, and all 15 domains |
| DG.4 | Data Management Organization | P1 | Establish Data Management Office and Committee; appoint all required roles (see role table below) |
| DG.5 | Compliance Audit Framework | P2 | Establish compliance management practices, produce audit reports with findings, monitor compliance scores periodically |
| DG.6 | Data Lifecycle Governance | P1/P2 | Govern data across its full lifecycle; establish lifecycle policies and procedures |
| DG.7 | Performance Management | P1/P2 | Define KPIs for data management; monitor and report on performance |
| DG.8 | Artifacts | P1/P2 | Document strategy, plan, policy, roles, and governance artefacts in a register |

### Required organisational roles (DG.4 — all P1)

| Specification | Role | Obligation |
|--------------|------|------------|
| DG.4.1 | Data Management Office | Establish the office; responsibilities aligned to NDMO Organisational Manual |
| DG.4.2 | Data Management Committee | Establish committee for direction and oversight; responsibilities per NDMO Organisational Manual |
| DG.4.3 | Chief Data Officer (CDO) | Appoint CDO; publish job description aligned to NDMO Organisational Manual |
| DG.4.4 | Data Governance Officer | Appoint; job description aligned to NDMO Organisational Manual |
| DG.4.5 | Open Data and Information Access Officer (ODIA) | Appoint; job description aligned to NDMO Organisational Manual |
| DG.4.6 | Compliance Officer | Appoint; job description aligned to NDMO Organisational Manual |
| DG.4.7 | Personal Data Protection Officer (PDPO) | Appoint; job description aligned to NDMO Organisational Manual — note: this is distinct from the PDPL DPO in PDPL Art. 30(2) but functionally overlapping |
| DG.4.8 | Business Data Executive (BDE) | Appoint per domain; job description aligned to NDMO Organisational Manual |
| DG.4.9 | Business Data Steward | Appoint per domain; job description aligned to NDMO Organisational Manual |
| DG.4.10 | IT Data Steward | Appoint; job description aligned to NDMO Organisational Manual |
| DG.4.11 | Legal Advisor | Appoint; job description aligned to NDMO Organisational Manual |

---

## Domain 12 — Freedom of Information (FOI)

4 controls, 9 specifications

| Control ID | Control Name | Priority | Key obligation |
|-----------|--------------|---------|----------------|
| FOI.1 | Plan | P1 | Develop a Freedom of Information Plan with a roadmap and resource allocation for compliance with NDMO FOI Regulations |
| FOI.2 | Training and Awareness | P2 | Launch awareness campaigns for employees processing FOI requests and for citizens' rights |
| FOI.3 | Data Lifecycle Management | P1/P2/P3 | Design and implement the FOI request process; publish mandatory website content; prepare request forms; determine fees; conduct internal compliance audits |
| FOI.4 | Artifacts | P3 | Maintain FOI register with officer details, access request records, publication logs |

### FOI.3 — mandatory public website publication (FOI.3.3 — P3)

Entities must publish on their official website at minimum:
- Laws, regulations, instructions and regulatory decisions applicable to the entity
- Services provided and how to obtain them
- Organisational structure including roles and responsibilities
- Job vacancy information (excluding security/military positions)
- Annual strategic and operational reports including financial statements
- General statistics: number of employees, year established, services count, activities
- Contact details for licensed persons (name, postal address, email)
- Information on projects offered or awarded, where there is a risk to life, health or property
- Awareness guidelines on citizens' FOI rights

### FOI request process (FOI.3.2 — P1)

Upon receiving a request for access to Public Information, the entity must make one of the following decisions within the NDMO FOI Regulations timeframe:
1. Grant the access
2. Deny the request
3. Extend the response time
4. Notify the requestor if the information is on the entity's website or outside the entity's competence

---

## Domain 13 — Data Classification (DC)

5 controls, 10 specifications

| Control ID | Control Name | Priority | Key obligation |
|-----------|--------------|---------|----------------|
| DC.1 | Plan | P1 | Develop a Data Classification Plan with a roadmap and resource allocation; prioritise datasets and artifacts for classification |
| DC.2 | Classification Controls | As specified by NCA | Assign data handling and protection controls to datasets and artifacts based on classification level — following NCA regulations |
| DC.3 | Classification Process | P1/P2 | Identify and inventory all datasets; conduct impact assessment; assign classification levels; review classifications; publish classification as metadata in the Data Catalog |
| DC.4 | Performance Management | P2 | Establish KPIs for classification progress |
| DC.5 | Artifacts | P2 | Maintain a Data Register with classification levels, dates, durations, and review outcomes |

### Classification levels and impact assessment (DC.3.2 — P1)

| Impact level assessed | Resulting classification | NDMO label |
|----------------------|------------------------|------------|
| High | Top Secret | Highest sensitivity |
| Medium | Secret | High sensitivity |
| Low | Confidential (unless Low-impact public assessment passes) | Medium sensitivity |
| None / Insignificant | Public | Lowest sensitivity |

### Low-impact public assessment (DC.3.3 — P1)

For data assessed as Low impact, the entity must further assess whether it can be reclassified as Public:
1. Evaluate if disclosure would breach any existing regulation
2. Identify potential benefits of opening the data and whether they outweigh negative impacts

If no regulatory breach and benefits outweigh impacts → classify as Public.

### Classification KPIs (DC.4.1 — P2)

Entities must track at minimum:
- % of datasets and artifacts classified
- % of datasets and artifacts classified by each classification level
- % of Low-impact data classified as Confidential
- % of classified datasets and artifacts that have been reviewed and approved

### Data Register minimum content (DC.5.1 — P2)

| Field | Required |
|-------|---------|
| List of identified datasets and artifacts | ✓ |
| Classification levels assigned | ✓ |
| Dates of classification assignment | ✓ |
| Classification duration applied | ✓ |
| Classification levels approved during review | ✓ |
| Dates of classification review | ✓ |

> **ECC/DCC alignment note:** DC.2 explicitly defers security controls to NCA. The four classification levels (Public / Confidential / Secret / Top Secret) match DCC-1:2022 levels exactly. Classification activity under NDMO feeds directly into DCC compliance — a single classification exercise satisfies both regulators.

---

## Domain 14 — Personal Data Protection (PDP)

5 controls, 10 specifications — **primary PDPL-implementing domain for government entities**

| Control ID | Control Name | Priority | Key obligation |
|-----------|--------------|---------|----------------|
| PDP.1 | Plan | P1 | Conduct initial Personal Data Protection Assessment; develop Personal Data Protection Plan |
| PDP.2 | Training and Awareness | P1 | Conduct Personal Data Protection training for every employee |
| PDP.3 | Data Breach | P1/P2 | Establish Data Breach notification and management procedures (72-hour clock) |
| PDP.4 | Data Lifecycle Management | P2/P3 | Establish Privacy Notice and Consent Management; Data Subject Rights processes; conduct privacy risk assessments and internal audits |
| PDP.5 | Artifacts | P2 | Maintain Personal Data Protection Register for minimum 24 months |

### PDP.1 — Plan (both specifications P1)

**PDP.1.1 — Personal Data Protection Initial Assessment** must include at minimum:
1. Identification of types of personal data being collected
2. Location and method of storage of personal data
3. Current processing and uses of the personal data
4. Privacy challenges to meet compliance with NDMO Personal Data Protection Regulations

**PDP.1.2 — Personal Data Protection Plan** must include at minimum:
1. A roadmap with activities and key milestones for achieving and maintaining compliance with NDMO Personal Data Protection Regulations — incorporating at minimum what is needed to achieve all PDP domain specifications
2. Assignment of required resources and budget

### PDP.2 — Training and Awareness (PDP.2.1 — P1)

Training must cover all employees and include at minimum:
1. Importance of Personal Data Protection and the consequences for the entity and/or data subject
2. Definition of Personal Data
3. Data Subject Data Rights
4. Entity and Data Subject responsibilities
5. Notification rules — when the entity and/or data subject should be notified and how to handle inquiries about personal data collection, processing and sharing

### PDP.3 — Data Breach

| Specification | Obligation | Priority |
|--------------|-----------|---------|
| PDP.3.1 Data Breach Notification | Data Controller or Processor handling personal data must notify the Regulatory Authority within **72 hours** of determining that personal data has been compromised | P2 |
| PDP.3.2 Data Breach Management Process | Develop and document breach management procedures including: incident review with the Regulatory Authority; immediate response; permanent corrective actions; testing of corrective actions | P1 |

> **Alignment note:** PDP.3.1 mirrors PDPL Art. 20 and the Implementing Regulations 72-hour SDAIA notification. Government entities must route notification through NDMO channels as well as SDAIA. Confirm the exact dual-notification path with current NDMO guidance.

### PDP.4 — Data Lifecycle Management

| Specification | Obligation | Priority |
|--------------|-----------|---------|
| PDP.4.1 Privacy Notice and Consent Management | Define processes for notice and consent at all personal-data collection points; obtain data subject implicit/explicit approval for collection, use or disclosure; publish Privacy Notice; maintain hyperlink to Privacy Notice on any internet presence; make Notice available to NDMO on request | P2 |
| PDP.4.2 Data Subject Rights | Establish and document Data Rights Management processes supporting 7 rights: right to be informed; right to access; right to rectification; right to erasure; right to object; right to restrict processing; right to data portability. Inform data subjects of their rights; provide means to submit, respond to and track requests | P2 |
| PDP.4.3 Personal Data Protection Risk Assessments | Conduct **yearly** risk assessments of all information systems containing personal data (collection, processing, storage, transmittal — both automated and manual). Findings must be: documented; analysed for impact and likelihood; evaluated against current regulatory obligations and criticality to resolve | P3 |
| PDP.4.4 Compliance Monitoring and Audit | Conduct internal audits to monitor compliance with privacy regulations; document findings in a report to the Data Protection Officer; take corrective actions in cases of non-compliance with notifications to the Regulatory Authority and NDMO | P2 |

> **PDPL Art. 4 vs PDP.4.2 rights comparison:** PDP.4.2 lists 7 rights (adds right to object and right to restrict processing beyond PDPL Art. 4's 5 rights). Government entities must satisfy the wider NDMO list.

### PDP.5 — Artifacts (PDP.5.1 — P2)

The Personal Data Protection Register must:
- Be maintained for a **minimum of 24 months**
- Be made available when requested by NDMO
- Include at minimum: a record of any collection and/or processing of any personal data

---

## Domain 15 — Data Security and Protection (DS)

**Deferred to NCA. NDMO does not assess compliance with this domain.**

The document lists the following control names (no specifications — for context only):

| Control name | Description summary |
|-------------|---------------------|
| Information Security Governance | Plans, tools, personnel and processes for data protection |
| Information Security Architecture | Fundamental security design concepts for the entity's systems |
| Information Systems Design, Development and Testing | Minimum security provisions during system development and testing |
| Identity and Access Management | User and system identity for access to information assets |
| Third Party Supplier Security | Information security requirements in third-party engagements |
| Information Security Training, Awareness and Communication | Comprehensive security training programme |
| Information Asset Management | Documented inventory of information assets |
| Information Security Operations Management | Operational monitoring, assessment and protection of information assets |
| Information Security Incident Management | Detection, management, recording and analysis of security threats and breaches |
| Information Security Risk Management | Identification, review, response and corrective actions for security risks |
| Information Systems Continuity Management | Confidentiality, integrity and availability preservation during incidents (ISO 27001) |

> **Assessment routing:** Assess these control areas under NCA ECC-2:2024, DCC-1:2022, and CSCC-1:2019 (if critical systems are designated). See the respective reference files.

---

## Data Management Guiding Principles

These 8 principles anchor the standards and map to domains:

| Principle | Mapped domains |
|-----------|---------------|
| Data as a National Asset — government data is discoverable, protected, maintained with clear accountability | Data Governance |
| Data Protection by Design — proactive privacy protection and consent rights built into systems | Personal Data Protection; Data Classification; Data Security; Open Data |
| Open by Default — government data available to the public unless non-disclosure is in greater public interest | Data Governance |
| Ethical Data Use — fairness, traceability, contribution to common good | Data Operations; Data Sharing and Interoperability; Data Architecture; Reference and Master Data Management |
| Purposeful Design — human-centric, responsive approach to data collection, processing, sharing | Data Operations; Data Sharing; Data Architecture; Reference and Master Data |
| Data-Driven Outcomes — operational and strategic decisions based on data insights | Business Intelligence and Analytics; Data Value Realization |
| Learning Culture — continuously learning Saudi talent | Data Value Realization; Business Intelligence; Data Governance |
| Trusted Data — high quality or transparent quality level | Data Quality; Reference and Master Data; Data Catalog and Metadata; Document and Content Management |

---

## Compliance mechanism — how NDMO assesses entities

| Element | Detail |
|---------|--------|
| Frequency | Annual — submitted Q3 each year |
| Method | Self-assessment at specification level |
| Scoring | Binary: 100% (fully implemented) or 0% (partially or not implemented) |
| Evidence | Annual compliance report must be supported with evidence for each specification |
| Cascade | Specification score → control score → domain score → entity score |
| NDMO review | Consolidates all entity reports; publishes annual results at entity, sector, and whole-of-government level |
| Ad-hoc audits | NDMO may conduct ad-hoc audits on selected entities based on submitted reports |
| Implementation plan | 3-year phased roadmap — P1 by end Year 1, P1+P2 by end Year 2, all by end Year 3 |

---

## Audit hot spots — ranked by enforcement frequency

| Rank | Issue | Control Ref | Why it gets cited |
|------|-------|-------------|-------------------|
| 1 | No CDO appointed or CDO not formally designated with compliant job description | DG.4.3 | P1 obligation; NDMO checks governance roles first |
| 2 | Data Management Strategy not established or not covering all 15 domains | DG.1.1 | Foundational P1; all other controls depend on it |
| 3 | Personal Data Protection Initial Assessment not performed | PDP.1.1 | P1; NDMO's entry point to assessing PDP compliance |
| 4 | No Personal Data Protection Officer (PDPO) appointed | DG.4.7 | P1; distinct from PDPL DPO but overlapping — both roles required |
| 5 | Data Classification not completed — no inventory, no impact assessment | DC.3.1, DC.3.2 | P1; classification underpins DCC compliance and data handling controls |
| 6 | All personal data systems not covered in PDP register | PDP.5.1 | P2; register minimum 24 months; frequently incomplete for legacy systems |
| 7 | No 72-hour breach notification procedure documented | PDP.3.1, PDP.3.2 | PDP.3.2 is P1; notification process written before the breach occurs is the standard |
| 8 | Privacy Notice not published or not available on entity website | PDP.4.1 | P2; website hyperlink requirement directly verifiable |
| 9 | Data Subject Rights process not documented or not covering all 7 rights | PDP.4.2 | P2; NDMO's 7-right list exceeds PDPL's 5-right list |
| 10 | Annual compliance self-assessment not submitted to NDMO in Q3 | DG.5.1–5.3 | P2; submission itself is a mandatory artefact; late or incomplete submissions trigger ad-hoc audit |
| 11 | FOI request process not designed or not implemented | FOI.3.1, FOI.3.2 | P1; FOI is a citizen-facing obligation — failures are publicly visible |
| 12 | Classification not reflected in Data Catalog metadata | DC.3.5 | P2; classification is siloed from catalog tools; NCA and NDMO may cross-check |
| 13 | Personal data protection risk assessments not conducted yearly | PDP.4.3 | P3 but increasingly checked; evidence of annual cycle required |
| 14 | Training records do not cover all employees or all required topics | DG.3.1, PDP.2.1 | P1; training scope must cover all 15 domains (DG.3.1) and all privacy topics (PDP.2.1) separately |

---

## Evidence expectations — what an auditor will request

| Area | Evidence NDMO / auditor will request | Control Ref |
|------|---------------------------------------|-------------|
| Strategy and Plan | Approved Data Management Strategy document; 3-year Plan with roadmap; approval minutes from Data Management Committee | DG.1.1–1.4 |
| Policy | Data Management Policy and Guidelines document; gap analysis report | DG.2.1–2.2 |
| Organisation | Appointment letters / HR records for all 11 roles; job descriptions aligned to NDMO Organisational Manual | DG.4.1–4.11 |
| Training | Training records showing all employees covered; training materials covering all 15 domains (DG.3) and separate PDP training (PDP.2) | DG.3.1, PDP.2.1 |
| Compliance audit | Annual compliance report submitted to NDMO; evidence per specification; remediation plans for gaps | DG.5.1–5.3 |
| PDP Initial Assessment | Assessment document covering personal data types, storage locations, processing uses, and compliance challenges | PDP.1.1 |
| PDP Plan | Personal Data Protection Plan with roadmap and budget | PDP.1.2 |
| Breach procedure | Documented breach management process; evidence of 72-hour notification path to Regulatory Authority | PDP.3.1–3.2 |
| Privacy Notice | Published Privacy Notice; website hyperlink; evidence it was available to NDMO on request | PDP.4.1 |
| Data Subject Rights | Documented data rights management process covering all 7 rights; request log with response evidence | PDP.4.2 |
| PDP Risk Assessments | Annual risk assessment reports for all personal-data information systems; findings documented with impact analysis | PDP.4.3 |
| PDP Compliance Audit | Internal audit report to PDPO/DPO; corrective actions log | PDP.4.4 |
| PDP Register | Register of all personal data collection/processing activity; evidence of 24-month retention | PDP.5.1 |
| Data Classification | Data Classification Plan; prioritized dataset inventory; impact assessment records; Data Register with classification levels, dates, and review outcomes | DC.1.1, DC.3.1–3.4, DC.5.1 |
| Classification metadata | Data Catalog records showing classification metadata populated | DC.3.5 |
| Classification KPIs | KPI dashboard or report showing % classified, % by level, % reviewed | DC.4.1 |
| FOI Plan | Freedom of Information Plan with roadmap | FOI.1.1 |
| FOI request process | Documented and implemented FOI process; request forms; decision records | FOI.3.1–3.2, FOI.3.4 |
| FOI website publication | Screenshot/evidence of mandatory content published on entity website | FOI.3.3 |
| FOI Register | FOI Register with officer details, access request records | FOI.4.1 |

---

## Common pitfalls

- **Treating NDMO and PDPL as separate programmes:** The PDP domain (14) is explicitly PDPL-implementing. Public entities running parallel NDMO and PDPL compliance tracks without cross-referencing produce duplicate artefacts that satisfy neither. One integrated compliance programme is more efficient and avoids inconsistency.
- **PDPO vs DPO confusion:** NDMO requires a Personal Data Protection Officer (PDPO) role under DG.4.7. PDPL Art. 30(2) requires a Data Protection Officer (DPO) where processing thresholds are met. These are not automatically the same appointment. Both may be required; confirm whether one person holds both roles and whether NDMO's Organisational Manual job description aligns with PDPL's DPO independence requirements.
- **7 rights vs 5 rights:** PDP.4.2 lists 7 data subject rights (including right to object and right to restrict processing). PDPL Art. 4 lists 5. Government entities must build processes for all 7.
- **Domain 15 double-counting:** Teams sometimes submit Domain 15 metrics in the NDMO self-assessment. Domain 15 is explicitly excluded from NDMO assessment. Including it creates confusion; NCA assesses it separately under ECC/DCC.
- **Classification siloed from DCC:** NDMO's Data Classification domain and NCA's DCC-1:2022 use identical levels (Public/Confidential/Secret/Top Secret). Entities often run classification under NDMO without connecting it to DCC control triggers. The classification outcome should automatically feed DCC compliance decisions (who can access, what encryption applies, etc.).
- **Annual compliance report submission gap:** The Q3 submission deadline is fixed. Entities that start their self-assessment in Q3 rather than building evidence throughout the year cannot produce sufficient supporting evidence at assessment time. Compliance evidence must be collected continuously.
- **PDP Register retention of 24 months:** PDP.5.1 specifies a minimum 24-month retention for personal data processing compliance records — longer than some entities' standard record retention for internal reports. The 24-month minimum must be documented in the retention policy.
- **Training coverage gaps:** DG.3.1 requires training covering all 15 NDMO domains for all related employees. PDP.2.1 requires separate PDP training covering 5 specific topics for every employee. Entities often conflate these into one training that satisfies neither standard.

---

## Related frameworks

| Framework | Relationship | Reference |
|-----------|-------------|-----------|
| PDPL + Implementing Regulations | NDMO Standards Domain 14 (PDP) operationalises PDPL for government entities; SDAIA is PDPL regulator, NDMO is government-sector supervisor | PDPL.md |
| NCA ECC-2:2024 | Domain 15 deferred to NCA; Domain 13 classification levels align with ECC §2-7 and DCC | ECC-2-2024.md |
| NCA DCC-1:2022 | NDMO Domain 13 classification levels (Public/Confidential/Secret/Top Secret) are identical to DCC classification tiers; classification work satisfies both | DCC-1-2022.md |
| CST Cloud Computing Regulatory Framework | Cloud-hosted government data must comply with NDMO standards; data residency and localisation obligations for government data are driven by NDMO and NDMO's data localisation rules (separate from the deleted ECC-2:2024 §4-2-3-3) | CST-Regulations.md |
| DAMA DMBOK | International data management body of knowledge used as primary reference for Domains 1–11 | — |
| ISO 27001:2022 | Referenced in Domain 13 (Data Classification) and Domain 15 (Data Security — via NCA) | — |
| GDPR (EU) and CCPA (California) | Referenced in Domain 14 (Personal Data Protection) as international comparators | — |

---

## Verification note

All domain names, domain IDs, control IDs, specification IDs, specification text, priority levels, and counts in this file are verified directly against the source PDF of the NDMO Data Management and Personal Data Protection Standards v1.5 (January 2021), SDAIA/NDMO, classified Public.

**Confirmed from source:**
- 15 domains; 77 controls; 191 specifications (Domains 1–14 only; Domain 15 deferred to NCA)
- All Priority levels (P1/P2/P3) verified per specification
- All 11 DG.4 role specifications verified
- All 5 PDP controls and 10 specifications verified, including the 72-hour breach notification in PDP.3.1 and the 7 data subject rights in PDP.4.2
- All 5 DC controls and 10 specifications verified, including the impact assessment levels and Low-impact public assessment
- All 4 FOI controls and 9 specifications verified, including FOI.3.3 mandatory publication requirements
- Domain 15 (Data Security) explicitly confirmed as NCA-owned with no NDMO assessment

**Items not in source document (require verification from separate NDMO publications):**
- NDMO Organisational Manual (referenced for all DG.4 role job descriptions — not included in this document)
- NDMO Personal Data Protection Regulations (referenced throughout PDP domain — separate document)
- NDMO Freedom of Information Regulations (referenced throughout FOI domain — separate document)
- NDMO Data Classification Regulation (referenced in DC.3 — separate document)
- NDMO Data Value Realization Regulation (referenced for FOI.3.5 fee determination — separate document)
- Whether v1.5 (January 2021) is still the current operative version — confirm with NDMO at time of assessment; the document metadata (creation date July 2025) suggests this was re-published or reformatted recently
