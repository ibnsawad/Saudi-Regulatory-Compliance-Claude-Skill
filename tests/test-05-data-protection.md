# Test 05 — Personal Data Protection (PDPL + DCC + Transfer Reg)

## Eval purpose

Confirm the skill correctly applies the **privacy + data-cybersecurity** stack, distinguishes PDPL controller obligations from DCC technical obligations, and handles cross-border transfer mechanics.

---

## Scenario

"WellnessCo", a private-sector health-and-wellness platform serving KSA residents.

- **Entity type**: Private commercial; not a SAMA / CST / NCA-designated entity but processes personal data of KSA residents → in PDPL scope.
- **Data**: Account data, contact details, **biometric data** (face-scan check-in), **health-related data** (workout, vitals, dietary preferences), payment data via processor (tokenised).
- **Volume**: ~400,000 active users in KSA.
- **Storage**: Primary infrastructure on a CSP region in Ireland (`eu-west-1`). Backups in the same region. Analytics warehouse in the US for the parent company's data-science team.
- **Classification**: Internal "Public / Confidential" labels; no formal scheme; biometric and health data not specifically tagged.
- **Encryption**: TLS in transit; database encryption-at-rest at platform default keys (CSP-managed). No tokenisation / masking in non-prod.
- **DLP**: Not deployed.
- **Access**: Engineering team has broad read access to production DBs for "debugging".
- **Retention**: No documented retention schedule; user records deleted on user request only.
- **Privacy notice**: Generic global notice; no KSA-specific disclosures; no Arabic version on the KSA service.
- **Consent**: Single checkbox at sign-up covering all processing, including marketing.
- **DSR (Data Subject Rights)**: Email-based; no SLA; ad-hoc handling.
- **DPO**: Global Privacy Counsel covers; no KSA-resident DPO.
- **Sub-processors**: 11 disclosed in global notice; not disclosed to KSA users specifically.
- **Breach**: No documented 72-hour SDAIA notification path. Last suspected incident (May 2025) reviewed internally only.

---

## Expected skill behaviour

### A. Entity classification

Private commercial entity processing KSA personal data → applies:

- **PDPL** + **Implementing Regulations (Sept 2023)** + **Personal Data Transfer Regulation (Sept 2024)**
- **NCA DCC-1:2022** as the cybersecurity-of-data benchmark even though entity is not NCA-scoped — used as best-practice and as expectation if the entity becomes subject to a contract requiring it
- **NCA ECC-2:2024** *only* if NCA-scoped (likely not here) — skill should ask
- **NDMO** does not apply (not government)
- **CST CCRF** does not apply (not a CSP) — but the cloud the entity uses must be CCRF-licensed if KSA tier rules apply

### B. Lead regulator and notifications

- **SDAIA** is the privacy regulator. PDPL 72-hour breach notification + data-subject notification for high-risk breaches.
- Penalty exposure: PDPL provides for fines up to **SAR 5,000,000** (general) and up to **SAR 3,000,000** + imprisonment for sensitive-data violations.

### C. Cross-border transfer analysis

The skill should specifically address the transfers:

- **Ireland (`eu-west-1`)** — primary processing outside KSA. Requires a transfer mechanism under the Sept 2024 Personal Data Transfer Regulation (adequacy decision, appropriate safeguards, or specific exemption). EU GDPR alignment is helpful but does not equate to KSA adequacy.
- **United States (analytics warehouse)** — transfer of personal data to a non-adequate jurisdiction; needs an explicit mechanism + Transfer Impact Assessment (TIA).

The skill should require a TIA and identify whether SDAIA notification or pre-approval applies for sensitive-data transfers.

### D. Expected findings (calibre)

| ID | Framework / Control Ref | Status | Reg Risk | Op Risk | Priority |
|----|--------------------------|--------|----------|---------|----------|
| F-001 | PDPL Art. 12 [verify ref] — privacy notice (KSA-specific, Arabic) | Non-compliant | **Critical** | Medium | P1 |
| F-002 | PDPL Art. 6 [verify ref] — lawful basis & granular consent | Non-compliant | Critical | Medium | P1 |
| F-003 | PDPL — sensitive personal data (biometric, health) handling [verify ref] | Non-compliant | Critical | High | P1 |
| F-004 | PDPL Implementing Regs — DPO designation [verify ref] | Partial | High | Medium | P1 |
| F-005 | PDPL — DPIA for biometric / health processing [verify ref] | Non-compliant | High | Medium | P1 |
| F-006 | Personal Data Transfer Regulation (Sept 2024) — Ireland transfer mechanism + TIA | Non-compliant | Critical | High | P1 |
| F-007 | Personal Data Transfer Regulation — US analytics transfer; sensitive data | Non-compliant | Critical | High | P1 |
| F-008 | PDPL Implementing Regs — 72h breach notification path | Non-compliant | Critical | High | P1 |
| F-009 | PDPL — DSR workflow with SLA | Partial | High | Medium | P2 |
| F-010 | PDPL — Records of Processing | Non-compliant | High | Medium | P2 |
| F-011 | PDPL — Retention schedule | Non-compliant | High | Medium | P2 |
| F-012 | DCC-1:2022 — Classification (esp. biometric / health) | Non-compliant | High | High | P1 |
| F-013 | DCC-1:2022 — Encryption / key custody for sensitive data | Partial | High | High | P1 |
| F-014 | DCC-1:2022 — DLP, masking in non-prod, access governance | Non-compliant | Medium | High | P1 |
| F-015 | DCC-1:2022 — Sub-processor register & customer disclosure | Partial | Medium | Medium | P2 |
| F-016 | PDPL — Sub-processor agreements with PDPL clauses | Insufficient evidence | High | Medium | P2 |

### E. Output structure

- Executive Summary noting **sensitive personal data** and **cross-border** as the headline risks.
- Cross-border transfer subsection with a per-flow analysis.
- DPIA recommendation with explicit triggers (biometric, health, large-scale).
- Notification triggers section emphasising SDAIA 72-hour path.
- ISO/IEC 27701:2019 PIMS mapping offered as a structured implementation framework.

### F. Headline numbers expected

- Status: heavily Non-compliant on PDPL articles; mixed on DCC.
- Regulatory risk: ≥5 Critical (notice, consent, sensitive-data, two transfer flows, breach path).
- Priority: ≥9 P1.

---

## Pass criteria

Skill **passes** if it:

1. Treats biometric and health data as **sensitive personal data** under PDPL with stricter bases.
2. Applies the **Personal Data Transfer Regulation (Sept 2024)** explicitly and requires a TIA.
3. Cites Implementing Regulations for breach 72-hour and DPO triggers.
4. Recommends a KSA-specific Arabic privacy notice — not a translated copy of a global notice.
5. Distinguishes PDPL controller obligations from DCC technical-cybersecurity-of-data obligations and addresses both.
6. Quantifies penalty exposure with PDPL fine bands.
7. Offers ISO 27701 PIMS as an implementation scaffold.

Skill **fails** if it:

- Treats this as "GDPR with extra steps" without referencing the Transfer Regulation.
- Misses sensitive-data treatment.
- Recommends "deploy DLP" as the headline remediation while ignoring the transfer-mechanism gap.
- Doesn't tag cross-border processing as Critical.
