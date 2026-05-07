# Test 08 — Fintech (SAMA + Cloud + PDPL multi-overlay)

## Eval purpose

Confirm the skill correctly **stacks multiple overlays** on a SAMA-licensed fintech using cloud heavily and processing personal data, and orders the output by lead-regulator priority.

---

## Scenario

"PaySwift", a SAMA-licensed Payment Service Provider (PSP) operating an e-wallet and merchant-acquiring service.

- **Licensing**: SAMA PSP licence. Operating since 2022.
- **Architecture**: Cloud-native on a regional CSP with a KSA region. Core ledger, fraud engine, and KYC workflows in cloud. PCI scope contained to a specific account.
- **Customers**: 1.2M wallet users; 4,500 merchants. Cross-border transactions enabled with 22 corridor countries.
- **PCI**: Self-attests SAQ D — no QSA assessment yet.
- **Personal data**: Yes — KYC documents, biometric (face match), transaction history, location, device fingerprint.
- **SAMA**: Maturity self-assessment 2.7 average. Cloud pre-engagement done.
- **CCC**: Tenant-side controls partly implemented; CSPM deployed; some dev accounts excluded.
- **PDPL**: Privacy notice present, but no Arabic version on the wallet onboarding flow; consent mixed with T&Cs.
- **Cross-border**: Transaction-monitoring data exported to a sister entity in the UAE for regional fraud analytics. No transfer mechanism documented under PDPL Transfer Regulation.
- **Open Banking**: PaySwift consumes Open Banking APIs from KSA banks under SAMA's Open Banking Framework.
- **Outsourcing**: Cloud hosting, fraud-as-a-service vendor, KYC vendor (selfie + ID match), customer-support BPO in Egypt.
- **Incident**: Suspected data exposure 6 weeks ago — internal review only; SAMA not notified, SDAIA not notified.

---

## Expected skill behaviour

### A. Entity classification

SAMA-supervised PSP with heavy cloud + PDPL + cross-border + open-banking + outsourcing →

Primary stack:

- **SAMA Cybersecurity Framework v1.0 (May 2017)**
- **SAMA IT Governance Framework v1.0 (2022)**
- **SAMA BCM Framework v1.0 (2017)**
- **SAMA Open Banking Framework** (where applicable)
- **PCI DSS v4.0.1** (overlay due to card processing — PSP scope)
- **NCA CCC-2:2024** tenant-side
- **NCA DCC-1:2022** (data lifecycle)
- **PDPL** + Implementing Regs + **Personal Data Transfer Regulation** (UAE export of personal data)
- **SAMA Outsourcing Regulations** (BPO + cloud)
- Critical-system designation likely applies to ledger and fraud — consider **CSCC-1:2019**.

### B. Lead regulator and notifications

- **SAMA** primary. Late incident notification = a finding in itself.
- **SDAIA** for PDPL personal-data breaches (72 hours).
- **PCI Council / acquirer** if card data implicated in the incident.
- Customer notification per SAMA / contract.

### C. Expected findings (calibre)

| ID | Framework / Control Ref | Status | Reg Risk | Op Risk | Priority |
|----|--------------------------|--------|----------|---------|----------|
| F-001 | SAMA Cyber Incident Reporting Procedure — incident not reported | Non-compliant | **Critical** | High | P1 |
| F-002 | PDPL Implementing Regs — 72h breach notification | Non-compliant | Critical | High | P1 |
| F-003 | PDPL Transfer Regulation — UAE data export without mechanism | Non-compliant | Critical | High | P1 |
| F-004 | PDPL — Arabic privacy notice + granular consent | Non-compliant | High | Medium | P1 |
| F-005 | PDPL — sensitive personal data (biometric face-match) handling | Partial | High | High | P1 |
| F-006 | SAMA CSF — Outsourcing of customer-support to Egypt (clauses + SAMA notification) | Insufficient evidence | High | Medium | P1 |
| F-007 | PCI DSS v4.0.1 — independent assessment vs. self-attestation for SAQ D scale | Partial | High | High | P2 |
| F-008 | CCC-2:2024 — CSPM excludes dev accounts; tenant-side IAM coverage | Partial | High | Medium | P2 |
| F-009 | CCC-2:2024 — Encryption / key custody (customer-managed for ledger) | Insufficient evidence | High | High | P2 |
| F-010 | SAMA Open Banking Framework — Conformance & assurance | Insufficient evidence | High | Medium | P2 |
| F-011 | DCC-1:2022 — Classification incl. biometric + KYC docs | Partial | High | High | P2 |
| F-012 | SAMA BCM — live failover for ledger | Insufficient evidence | High | High | P2 |
| F-013 | SAMA CSF — Threat intelligence operationalisation | Partial | Medium | Medium | P3 |
| F-014 | CSCC-1:2019 — designation register for ledger / fraud | Insufficient evidence | High | High | P1 |
| F-015 | SAMA IT Governance — board reporting + IT risk appetite | Partial | Medium | Low | P3 |

### D. Output structure

- Executive Summary noting **un-notified incident** as the headline finding (Critical, P1).
- Stacked-framework explanation: order of priority is SAMA → PDPL/SDAIA → PCI → CCC/DCC → CSCC.
- Findings table including SAMA maturity column where SAMA controls.
- Notification triggers section listing **SAMA, SDAIA, PCI / acquirer**, customer.
- Cross-border subsection specific to PDPL Transfer Regulation.
- ISO 27001 / 27701 mapping offered.

### E. Headline numbers expected

- Status: heavy mix of Partial and Non-compliant.
- Regulatory risk: ≥3 Critical (un-notified incident, SDAIA path, transfer mechanism).
- Priority: ≥7 P1.
- SAMA maturity: ~2.7 (current); target ≥3.5 for licensing safety.

---

## Pass criteria

Skill **passes** if it:

1. Stacks SAMA + CCC + DCC + PDPL + Transfer Reg + PCI + SAMA Outsourcing + SAMA Open Banking and orders them by lead regulator.
2. Treats the un-notified incident as Critical for both SAMA and SDAIA.
3. Identifies the UAE export as a Transfer Regulation issue (no mechanism / no TIA).
4. Notes that SAMA-supervised PSP using BPO outside KSA triggers SAMA Outsourcing Regulations.
5. Asks about critical-system designation for the ledger and fraud engine.
6. Offers PCI DSS v4.0.1 as the relevant version, not v3.2.1.

Skill **fails** if it:

- Treats this as a generic SAMA assessment without cloud / PDPL overlays.
- Misses the un-notified incident.
- Treats PCI as out of scope simply because the entity self-attests.
- Doesn't address the UAE data flow.
