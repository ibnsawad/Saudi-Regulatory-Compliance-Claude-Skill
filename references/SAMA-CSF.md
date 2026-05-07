# SAMA — Cybersecurity Framework + IT Governance + Business Continuity

This file covers three SAMA frameworks that apply together to SAMA-supervised "Member Organisations".

## Issuer

Saudi Central Bank (SAMA — Saudi Arabian Monetary Agency, formally renamed Saudi Central Bank in 2020).

## Member Organisations (in-scope entities)

- All licensed banks
- Finance companies
- Insurance and reinsurance companies
- Payment service providers and electronic money institutions
- Exchange houses
- Credit information companies
- Fintechs licensed by SAMA (including those in the Regulatory Sandbox post-licensing)

Outsourced service providers and subsidiaries can fall in scope through contractual flow-down.

---

## SAMA Cybersecurity Framework (CSF) v1.0, May 2017

### Structure

Four main domains, each broken into subdomains and controls. Each control has a defined maturity expectation.

1. **Cybersecurity Leadership and Governance**
   - Cyber strategy
   - Cybersecurity policy
   - Cybersecurity roles and responsibilities (incl. CISO independence)
   - Cyber risk management
   - Compliance with regulatory requirements
   - Cybersecurity reviews and audits
   - Awareness

2. **Cybersecurity Risk Management and Compliance**
   - Cyber risk-management process
   - Information asset classification
   - Cyber risk assessment
   - Compliance with cyber regulations and standards

3. **Cybersecurity Operations and Technology**
   - HR security
   - Physical security
   - Asset management
   - Cybersecurity architecture
   - IAM
   - Application and system security
   - Change management
   - Configuration and patch management
   - Cryptography
   - Vulnerability management
   - Network security
   - Mobile and BYOD
   - Backup and recovery
   - Logging and monitoring
   - Incident management
   - Threat intelligence

4. **Third-Party Cybersecurity**
   - Cybersecurity in the procurement process
   - Cybersecurity in vendor management
   - Cyber requirements in outsourcing
   - Cloud computing requirements

### Maturity model

SAMA CSF uses a five-level maturity model. Each subdomain and control is assessed against this scale:

| Level | Label | Meaning |
|-------|-------|---------|
| 0 | Non-existent | No control |
| 1 | Ad-hoc | Reactive, not formalised |
| 2 | Repeatable but informal | Performed but not standardised |
| 3 | Structured and formalised | Documented, approved, in operation |
| 4 | Managed and measurable | Metrics, KPIs, periodic review |
| 5 | Adaptive | Continuously improving with industry leadership |

SAMA expects Member Organisations to define a target maturity per control (typically Level 3 or 4) and to demonstrate progression. Compliance reporting to SAMA includes maturity scoring.

### Reporting and notifications

- Annual cyber maturity self-assessment to SAMA
- Periodic regulatory reporting via the SAMA portal
- **Cyber Incident Reporting**: SAMA's *Cyber Incident Reporting Procedure* requires notification of major cyber incidents to the SAMA Cybersecurity Threat Intelligence Unit. Verbal notification first, then written report within stipulated timelines. Confirm exact timelines against the version of the procedure currently in force.
- Threat intelligence sharing through the Banking Cybersecurity Committee channels.

### Audit hot spots

- CISO not independent from IT operations
- Risk-management methodology generic, not cyber-tailored
- Threat intelligence consumed but not actioned
- Outsourcing contracts without SAMA-required clauses
- Cloud-use without SAMA pre-engagement (where required)
- Maturity self-attested but not evidenced on inspection

---

## SAMA IT Governance Framework (v1.0, 2022)

Applies to Member Organisations alongside CSF. Focuses on IT-strategy alignment, value delivery, IT risk, IT performance, and resource management. Structured around governance and management practices similar to COBIT. Common gap: IT governance committee in name only, without documented charter, decision rights, or board reporting cadence.

Key elements typically assessed:

- IT governance committee structure and charter
- IT strategy aligned to business strategy
- IT risk management integrated with enterprise risk
- IT performance management with KPIs
- IT investment governance
- IT compliance management

---

## SAMA Business Continuity Management Framework (v1.0, 2017)

Applies alongside CSF. Sets out BCM expectations: BIA, RTO/RPO discipline, BCM strategy, BC and DR plans, exercise programme, crisis management, board reporting.

Key elements:

- BCM policy approved by the board
- Documented BIA covering all critical business processes
- RTO and RPO defined and agreed at process level
- BC plans for each critical process, with assigned roles
- DR plans for each critical IT system
- Annual exercise programme with full-scope tests at defined intervals
- Crisis-management arrangements integrated with regulatory communications
- Periodic management and board reporting

Common gaps: BIA outdated, RTO/RPO defined but not technically achievable, exercises run as tabletop only, no end-to-end live failover.

---

## Cross-references

- SAMA-supervised entities also subject to PDPL where personal data is processed
- Cloud-use by SAMA Member Organisations engages CST CCRF licensing of the chosen CSP and SAMA's specific cloud-use rules — coordinate before adopting public cloud
- Mapping to ISO/IEC 27001:2022, ISO 22301 (BCM), ISO 38500 (IT governance), and NIST CSF 2.0 is straightforward and worth offering for institutions with international parents

## Verification note

Maturity numbering and domain titles above are accurate to the published SAMA CSF v1.0. Specific subdomain references are not transcribed verbatim — cite the SAMA document directly for exact wording. Where reporting timelines matter (incident notification windows in particular), check the latest version of SAMA's Cyber Incident Reporting Procedure rather than relying on memory.
