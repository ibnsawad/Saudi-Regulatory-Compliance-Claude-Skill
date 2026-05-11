# Test 01 — Cloud Service Provider (CST + NCA CCC)

## Eval purpose

Confirm the skill correctly identifies a CSP scenario, applies the **dual licence + cybersecurity** stack (CST CCRF + NCA CCC), and produces findings with version-cited control references.

---

## Scenario

A CSP, "NimbusKSA", offers IaaS and PaaS to commercial and government customers in Saudi Arabia.

- **Hosting**: AWS regions in Bahrain (`me-south-1`) and Frankfurt (`eu-central-1`). No KSA region. Marketed as "regional cloud".
- **CST status**: Operating commercially in KSA for 18 months. No CCRF licence on file. Founders believe they're "covered" because AWS holds a regional licence.
- **Customers**: Two government entities (data classified Confidential), one SAMA-supervised payment service provider, mid-market commercial.
- **Security**: No SIEM. CloudTrail enabled but logs only retained 90 days in the AWS account, not centralised. No alerting.
- **IAM**: Engineering team shares one root account "for emergencies"; named IAM users for daily work without MFA on five of twelve accounts. No PAM.
- **Incident response**: One-page document last updated 2023; no playbooks; no tabletop in 12 months; no SDAIA breach path.
- **Data**: No customer-data classification; no shared-responsibility matrix in customer contracts; no DPIA for the government workloads.
- **SOC**: No 24/7 monitoring. On-call rotation among 3 engineers, ad-hoc.
- **Sub-processors**: AWS, Datadog, an offshore support partner — none disclosed to customers.
- **Personal data**: Yes — customer end-user data flows through the platform.

---

## Expected skill behaviour

### A. Entity classification (must hit)

The skill should classify NimbusKSA as a **CSP operating in KSA** and apply, at minimum:

- CST CCRF (licensing class — likely Class C given government customers and Confidential data; verify against current CCRF)
- NCA CCC-2:2024 (CSP-side controls)
- NCA ECC-2:2024 (baseline)
- NCA DCC-1:2022 (data lifecycle, including customer data)
- PDPL + Implementing Regulations + Personal Data Transfer Regulation (cross-border to Bahrain / Frankfurt)
- NDMO Standards engagement noted (because government customers)
- SAMA touchpoint flagged (because PSP customer — NimbusKSA is not SAMA-supervised, but its PSP customer's SAMA obligations flow down)

### B. Lead regulator and notification triggers

Skill should identify:

- **CST** as licensing regulator (operating without CCRF licence is itself a violation).
- **SDAIA** for personal-data breach notification (72 hours).
- **NCA** for significant cyber incidents (per applicable sector).
- Customer-notification obligations under CCRF and per the PSP / government contracts.

### C. Expected findings (the skill must produce findings of this calibre)

| ID | Framework / Control Ref | Domain | Status | Reg Risk | Op Risk | Priority |
|----|--------------------------|--------|--------|----------|---------|----------|
| F-001 | CST CCRF — registration / licensing [verify class] | Licensing | Non-compliant | **Critical** | High | **P1** |
| F-002 | PDPL Personal Data Transfer Regulation (Sept 2024) | Privacy / cross-border | Non-compliant | Critical | High | P1 |
| F-003 | CCC-2:2024 — Cloud Defence — Logging & Monitoring [verify ref] | Cloud Defence | Non-compliant | High | High | P1 |
| F-004 | CCC-2:2024 — Cloud IAM / privileged access [verify ref] + ECC-2:2024 §2-x (PAM) | Cloud Defence | Non-compliant | High | High | P1 |
| F-005 | CCC-2:2024 — Incident management; PDPL Implementing Regs (72h) | Resilience | Non-compliant | Critical | High | P1 |
| F-006 | CCC-2:2024 — Shared responsibility & customer terms; CST CCRF customer-protection | Governance | Non-compliant | High | Medium | P1 |
| F-007 | DCC-1:2022 — Classification & inventory | Data Defence | Non-compliant | High | Medium | P2 |
| F-008 | CCC-2:2024 — Sub-processor disclosure & oversight | Third-Party | Non-compliant | High | Medium | P2 |
| F-009 | DCC-1:2022 — Encryption / key custody (likely customer-managed required at higher tiers) | Data Defence | Insufficient evidence | High | Medium | P2 |
| F-010 | PDPL Art. 6 / 12 (lawful basis, privacy notice) [verify ref] | Privacy | Insufficient evidence | High | Medium | P2 |

The skill **must cite versions** (CCC-2:2024, DCC-1:2022, ECC-2:2024, PDPL Sept 2024 Transfer Reg) and tag uncertain numbering with `[verify ref]`.

### D. Expected output structure

- Executive Summary (posture + headline numbers + top three exposures)
- Scope and Applicable Frameworks (with versions)
- Findings table (≥10 rows for this scenario)
- Risk Heatmap (regulatory × priority)
- Remediation Roadmap (30 / 60 / 90 days)
- Notification & Reporting Triggers (CST licence, SDAIA breach path, customer-notification obligations)
- Cross-framework Mapping (offered, not imposed)
- Assumptions and Limitations

### E. Headline numbers expected

- Status: predominantly Non-compliant; ~10–14 findings.
- Regulatory risk: ≥2 Critical, ≥4 High.
- Priority: ≥5 P1 items.
- NCA compliance level (CCC self-rating): 1–2 / 5.

### F. Maturity

CSP operates at ad-hoc / initial maturity. Expected NCA-style averages around Level 1.5 across CCC.

---

## Pass criteria for the eval

The skill **passes** Test 01 if the response:

1. Identifies CSP entity type and selects the correct framework set (CST CCRF + CCC + ECC + DCC + PDPL incl. Transfer Reg).
2. Names CST as licensing regulator and flags the unlicensed operation as Critical.
3. Cites framework versions (CCC-2:2024, DCC-1:2022, etc.) and tags uncertain control numbers.
4. Identifies the PDPL 72-hour breach notification gap.
5. Identifies the cross-border transfer issue (Bahrain / Frankfurt vs. Transfer Regulation).
6. Produces findings using the table schema in `references/finding-template.md`.
7. Applies dual risk + priority + status per `tests/scoring-model.md`.
8. Does **not** fabricate exact §-codes for controls when uncertain.

The skill **fails** if it:

- Treats this as "an AWS customer" rather than a CSP.
- Misses CST CCRF licensing entirely.
- Cites ECC-1:2018 instead of ECC-2:2024.
- Marks everything High Risk without distinguishing regulatory vs. operational.
- Recommends "deploy SIEM" and stops there without addressing licensing, residency, and breach-path.
