# Saudi Regulatory Compliance Skill

A structured, AI-driven advisor for cybersecurity, cloud, OT, and data-protection compliance in the Kingdom of Saudi Arabia.

---

## About

This is an independent, open-source project that explores how AI can support cybersecurity and privacy compliance assessments under Saudi regulation. It is not affiliated with NCA, SAMA, CST, SDAIA, or NDMO and is not an official assessment tool. It is built for educational and professional use by compliance teams, CISOs, internal auditors, and consultants.

---

## Why this project

Saudi Arabia has one of the most layered regulatory environments in the region. A single organisation may simultaneously be in scope for NCA cybersecurity controls, sector-specific SAMA or CST regulation, NDMO data-management standards, and PDPL privacy obligations — each with its own structure, language, and assessment methodology. This skill tries to:

- Apply the right framework set on the first read by classifying entity type before assessing.
- Produce findings that cite specific framework versions and controls (rather than generic recommendations).
- Use a multi-axis scoring approach that distinguishes regulatory risk from operational risk.
- Surface notification and reporting obligations alongside control findings.
- Map to international frameworks (ISO/IEC 27001:2022, ISO/IEC 27701:2019, NIST CSF 2.0) where useful.

---

## Target audience

- Cybersecurity professionals and CISOs operating in KSA.
- GRC and compliance practitioners.
- Cloud security teams, including CSPs and Cloud Service Tenants.
- OT / ICS security leads in critical national infrastructure.
- Internal and external auditors preparing for or responding to regulator inspections.
- Researchers and students studying GCC regulatory frameworks.

---

## Supported frameworks (v4.0)

### National Cybersecurity Authority (NCA)
- Essential Cybersecurity Controls — **ECC-2:2024**
- Cloud Cybersecurity Controls — **CCC-2:2024**
- Data Cybersecurity Controls — **DCC-1:2022**
- Critical Systems Cybersecurity Controls — **CSCC-1:2019**
- Operational Technology Cybersecurity Controls — **OTCC-1:2022**
- Telework Cybersecurity Controls — **TCC-1:2021**
- Organizations' Social Media Accounts Cybersecurity Controls — **OSMACC-1:2021**
- Cybersecurity Guidelines for E-commerce Consumers — **CGEC-1:2019**
- Cybersecurity Guidelines for E-commerce Service Providers — **CGESP-1:2019**
- National Cryptographic Standards — **NCS-1:2020**

### Saudi Central Bank (SAMA)
- Cybersecurity Framework — **CSF v1.0 (May 2017)**
- IT Governance Framework — **v1.0 (2022)**
- Business Continuity Management Framework — **v1.0 (2017)**

### Communications, Space and Technology Commission (CST)
- Cloud Computing Regulatory Framework — **CCRF v2 (2023)** — licence classes, customer-data tiers, customer protection
- Cybersecurity Regulatory Framework for ICT Service Providers — **CRF RT08, Second Version (October 2023)** — telecom operators, ISPs, managed service providers; 6 domains, 25 subdomains, 3 compliance levels

### Saudi Data and AI Authority (SDAIA) and National Data Management Office (NDMO)
- Personal Data Protection Law — **PDPL** (Royal Decree M/19, 2021; amended 2023; effective 14 Sept 2023; full enforcement 14 Sept 2024)
- **PDPL Implementing Regulations (Sept 2023)**
- **Personal Data Transfer Regulation (Sept 2024)**
- **NDMO Data Management & Personal Data Protection Standards** (v1.5, 2022)

### Cross-mappings offered
- ISO/IEC 27001:2022 + Annex A
- ISO/IEC 27701:2019 (PIMS overlay for PDPL)
- ISO/IEC 27017 / 27018 (cloud / cloud-PII)
- NIST CSF 2.0 functions (Govern, Identify, Protect, Detect, Respond, Recover)
- NIST SP 800-53 Rev 5 / SP 800-82 Rev 3 (for CSCC / OTCC depth)
- IEC 62443 (for OT / ICS)
- PCI DSS v4.0.1 (where card processing is in scope)

---

## Key capabilities

- **Entity classification** — selects the right framework set before assessing.
- **Multi-framework gap analysis** with version-cited control references.
- **Multi-axis scoring** — status, regulatory risk, operational risk, priority (P1–P4), with NCA compliance levels (1–5) and SAMA maturity (0–5) where applicable.
- **Cloud assessments** for both CSP-side and Cloud Service Tenant-side obligations.
- **OT / ICS coverage** under OTCC with Purdue-model and IEC 62443 mapping.
- **Privacy assessments** under PDPL with sensitive-data and cross-border treatment.
- **Notification and reporting routing** across SAMA, SDAIA, NCA, CST, and NDMO.
- **Audit-ready outputs** with finding-table format, risk heatmap, and remediation roadmap.
- **Cross-framework mapping** to ISO and NIST.

---

## Use cases

- Pre-audit readiness for NCA / SAMA / CST inspections.
- Cloud licensing preparation under CST CCRF.
- Critical-system designation and CSCC overlay assessments.
- OT / ICS cybersecurity readiness for utilities, energy, water, and manufacturing.
- PDPL implementation and Transfer Regulation reviews.
- Vendor and third-party security questionnaires.
- Board and management compliance reporting.
- Training and uplift for compliance teams.

---

## How it works

The user provides:

- An entity description (sector, licensing posture, lead regulator, system architecture).
- Security controls, governance documents, or audit findings already in place.
- The compliance scope or specific question.

The skill:

1. **Classifies** the entity and selects the framework set.
2. **Asks** up to three clarifying questions if scope is unclear.
3. **Evaluates** against each applicable framework using the per-framework reference notes in `references/`.
4. **Scores** findings on the multi-axis model in `tests/scoring-model.md`.
5. **Produces** a structured assessment using the format in `references/finding-template.md`.
6. **Calls out** notification and reporting triggers separately.
7. **Maps** to ISO and NIST when offered.

---

## Architecture

```
saudi-regulatory-compliance/
├── SKILL.md                     # Entry point with role, framework table, workflow
├── README.md                    # This file
├── DEMO-GUIDE.md                # Walk-through for trying the skill
├── CHANGELOG.md                     # Full version history
├── DISCLAIMER.md                # Limitations and intended use
├── LICENSE                      # MIT licence
├── references/
│   ├── ECC-2-2024.md            # NCA Essential Cybersecurity Controls
│   ├── CCC-2-2024.md            # NCA Cloud Cybersecurity Controls
│   ├── DCC-1-2022.md            # NCA Data Cybersecurity Controls
│   ├── CSCC-1-2019.md           # NCA Critical Systems Cybersecurity Controls
│   ├── OTCC-1-2022.md           # NCA Operational Technology Cybersecurity Controls
│   ├── TCC-1-2021.md            # NCA Telework Cybersecurity Controls
│   ├── OSMACC-1-2021.md         # NCA Organizations' Social Media Accounts Controls
│   ├── CGEC-1-2019.md           # NCA Cybersecurity Guidelines for E-commerce Consumers
│   ├── CGESP-1-2019.md          # NCA Cybersecurity Guidelines for E-commerce Service Providers
│   ├── NCS-1-2020.md            # NCA National Cryptographic Standards
│   ├── SAMA-CSF.md              # SAMA CSF + IT Governance + BCM
│   ├── CST-Regulations.md       # CCRF (RS10), licence classes, customer-data tiers
│   ├── CST-CRF.md               # CST Cybersecurity Regulatory Framework RT08 for ICT SPs
│   ├── PDPL.md                  # PDPL + Implementing Regs + Transfer Reg
│   ├── NDMO-Standards.md        # NDMO Data Management & PDP Standards
│   ├── finding-template.md      # Finding-row template and field guidance
│   └── examples.md              # Two end-to-end worked examples
└── tests/
    ├── README.md                # Eval index with coverage map
    ├── scoring-model.md         # Multi-axis scoring rubric
    ├── test-01-cloud-csp.md
    ├── test-02-government-entity.md
    ├── test-03-bank-sama.md
    ├── test-04-critical-system.md
    ├── test-05-data-protection.md
    ├── test-06-ot-energy.md
    ├── test-07-telework.md
    ├── test-08-fintech-multi-overlay.md
    ├── test-09-incident-notification.md
    ├── test-10-social-media.md
    ├── test-11-ict-cst-crf.md
    ├── test-12-cryptography-ncs.md
    └── test-13-ecommerce-provider.md
```

---

## Design principles

- **Saudi-first**, with international mapping as overlay rather than substitute.
- **Cite versions** — every framework reference is dated.
- **Don't fabricate control numbers** — uncertain references are tagged for verification.
- **Two risk axes, not one** — regulatory risk and operational risk are separate dimensions.
- **Notification matters** — incident- and breach-reporting paths are first-class output.
- **Engineering, not legal** — this skill produces compliance-engineering analysis, not legal opinions.
- **Evidence-oriented** — every finding has an "evidence required" field aligned to what an assessor will ask for.

---

## Limitations

- Not a substitute for formal audits, QSA assessments, or accredited assessor reviews.
- Does not connect to live systems, evidence repositories, or regulator portals.
- Quality of output depends on completeness of input.
- Saudi regulations evolve; framework versions and reporting timelines must be re-checked against current published documents.
- Sectoral overlays beyond the listed frameworks (Aramco IPSCS, Ministry of Health programmes, etc.) are not modelled in detail.
- The skill flags uncertain control numbers rather than fabricating them — exact §-codes should be confirmed against official documents before formal use.

---

## Roadmap

Candidates for future iterations:

- Dedicated reference for **SAMA Open Banking Framework**, **SAMA Outsourcing Regulations**, and **SAMA Counter-Fraud Framework**.
- Reference for **PCI DSS v4.0.1** as a first-class reference file (currently cross-mapping only).
- Reference for **CST IoT Regulatory Framework**.
- Dedicated test scenario for **NCS-1:2020** cryptographic standards audit (standalone, not background).
- Dedicated test scenario for **OSMACC-1:2021** social-media account assessment.
- Dedicated test scenario for **CST CRF RT08** ICT Service Provider assessment.
- Dedicated test scenario for **CGESP-1:2019** SME/SoHo e-commerce operator.
- A Statement of Applicability spreadsheet template (per framework).
- A control-by-control catalogue for ECC-2:2024 with NIST CSF 2.0 + ISO/IEC 27001:2022 mappings.
- Sample executive and audit-committee report templates.
- Optional language pack with Arabic terminology for Arabic-language outputs.
- Companion eval harness using the `skill-creator` tooling.
- NCS update once NCA publishes post-quantum cryptography guidance aligned to NIST FIPS 203/204/205 (August 2024 standards).

Suggestions and contributions welcome — see DISCLAIMER for use limits.

---

## Version

**Current: v4.0** — See [CHANGELOG.md](CHANGELOG.md) for full version history.

---

## Official Sources

Links to the authoritative publications this skill is based on:

| Authority | Resource | Link |
|-----------|----------|-------|
| NCA | All published frameworks (ECC, CCC, DCC, OSMACC, NCS, etc.) | [nca.gov.sa](https://nca.gov.sa/en/pages/regulations.html) |
| SAMA | Cybersecurity Framework and related regulations | [sama.gov.sa — Regulatory Sandbox & Rules](https://www.sama.gov.sa/en-US/Rules/Pages/Regulatory-Rules.aspx) |
| CST | Cloud Computing Regulatory Framework, CRF RT08 | [cst.gov.sa — Regulations](https://www.cst.gov.sa/en/regulations/regulations) |
| SDAIA / NDMO | PDPL, Implementing Regulations, Data Transfer Regulation | [sdaia.gov.sa](https://sdaia.gov.sa/en/) |
| NDMO | Data Management and Personal Data Protection Standards | [ndmo.gov.sa](https://ndmo.gov.sa/en) |

> Always verify you are using the latest published version before a formal assessment. Regulations are updated periodically without advance notice.

---

## Author

**Majid Bin Sawad** — [@ibnsawad](https://github.com/ibnsawad)
Cybersecurity Director
