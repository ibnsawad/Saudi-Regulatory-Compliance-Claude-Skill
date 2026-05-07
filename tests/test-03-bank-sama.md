# Test 03 — SAMA-Supervised Bank

## Eval purpose

Confirm the skill knows that SAMA-supervised entities use **SAMA CSF + IT Governance + BCM** as primary, applies the SAMA 0–5 maturity model, and surfaces SAMA-specific notification expectations.

---

## Scenario

"NajdBank", a mid-sized retail bank licensed by SAMA.

- **Supervision**: SAMA-supervised since founding. Last SAMA cyber maturity self-assessment: 2 years ago, average maturity 2.4.
- **Environment**: Hybrid — core banking on-prem at primary site in Riyadh, DR site in Jeddah; digital channels and analytics workloads on AWS (KSA region).
- **CISO**: Reports to CIO. No direct line to board cybersecurity committee.
- **SOC**: Internal SOC 24/7. SIEM ingests core banking, AD, and AWS CloudTrail; not yet ingesting endpoint EDR or some payment middleware. ~70% use-case coverage by SAMA's expected catalogue.
- **PAM**: Deployed for on-prem privileged access; **AWS root and AWS Organizations management account** held by named cloud engineers without PAM brokering. No JIT.
- **MFA**: TOTP for staff; **SMS OTP** for some privileged remote access.
- **Threat intel**: Subscriptions consumed but not feeding SOC use cases.
- **Vendor management**: Vendor inventory exists; only 60% have SAMA-aligned cyber clauses; remote-access by core-banking vendor via shared VPN credentials.
- **BCM**: BIA done in 2022. RTO/RPO defined. **Live failover not exercised in 24 months** — only tabletop.
- **IT Governance**: Steering committee meets quarterly; minutes thin; no documented IT risk appetite; KPIs reported only on availability.
- **Cloud governance**: SAMA pre-engagement on cloud documented; AWS-specific risk acceptance signed. CCC-2:2024 tenant-side controls partially implemented.
- **Personal data**: Yes — customer KYC, transaction history, biometrics for some channels.
- **Incident reporting**: One major incident in last 12 months; reported to SAMA CTI within 4 hours (good); written report submitted late.

---

## Expected skill behaviour

### A. Entity classification

SAMA Member Organisation → primary stack:

- **SAMA CSF v1.0 (May 2017)**
- **SAMA IT Governance Framework v1.0 (2022)**
- **SAMA Business Continuity Management Framework v1.0 (2017)**
- **PDPL** + Implementing Regs (customer personal data)
- **NCA CCC-2:2024 (CST/tenant side)** for AWS workloads
- **CST CCRF awareness** — confirm AWS CCRF compliance, but bank itself is not licensed under CCRF
- **Critical-system designation** — core banking and payment switch likely critical; trigger CSCC-1:2019 overlay

ECC-2:2024 is not the lead framework but expectations broadly map; the skill should align to SAMA primary.

### B. Lead regulator and notifications

- **SAMA** is the primary supervisor. Cyber Incident Reporting Procedure: verbal first, then written within stipulated window — flag the late written report from the recent incident as a finding.
- **SDAIA** for PDPL personal-data breaches: 72 hours.
- **NCA** for significant cyber incidents per sectoral procedure.

### C. Expected findings (calibre, with SAMA maturity ratings)

| ID | Framework / Control Ref | Status | Maturity (current → target) | Reg Risk | Priority |
|----|--------------------------|--------|------------------------------|----------|----------|
| F-001 | SAMA CSF — Operations & Tech — IAM & PAM | Non-compliant | 2 → 4 | **Critical** | **P1** |
| F-002 | SAMA CSF — Authentication / MFA (SMS OTP for privileged) | Partial | 2 → 4 | High | P1 |
| F-003 | CCC-2:2024 — Cloud IAM (AWS root not in PAM) | Non-compliant | — | Critical | P1 |
| F-004 | SAMA BCM — live failover programme | Partial | 2 → 4 | High | P1 |
| F-005 | SAMA CSF — Logging & Monitoring (use-case coverage gaps) | Partial | 3 → 4 | High | P2 |
| F-006 | SAMA CSF — Threat intelligence operationalisation | Partial | 2 → 3 | Medium | P2 |
| F-007 | SAMA CSF — Third-Party Cybersecurity (vendor clauses, vendor remote access) | Partial | 2 → 4 | High | P1 |
| F-008 | SAMA IT Governance — Board-level reporting & IT risk appetite | Partial | 2 → 4 | High | P2 |
| F-009 | SAMA CSF — Leadership & Governance (CISO reporting line) | Partial | 2 → 4 | High | P2 |
| F-010 | SAMA Cyber Incident Reporting Procedure — written report timeliness | Non-compliant | — | High | P1 |
| F-011 | CSCC-1:2019 — designation register (core banking & payment switch) | Insufficient evidence | — | High | P1 |
| F-012 | PDPL Implementing Regs — 72h breach notification path | Insufficient evidence | — | Critical | P1 |
| F-013 | DCC-1:2022 — encryption / key custody for cloud workloads | Partial | — | High | P2 |

### D. Expected output

- Executive Summary noting maturity drift since last self-assessment.
- SAMA scorecard: maturity per subdomain (current vs. target), with average.
- Findings table including SAMA maturity column (current → target).
- BCM gap called out separately (live failover deficit is a recurring SAMA concern).
- Cloud overlay (CCC-2:2024) findings tied back to SAMA's third-party / cloud expectations.
- Notification triggers section: SAMA, SDAIA, NCA, customer.
- ISO 27001:2022 + ISO 22301 mapping (offered).

### E. Headline numbers expected

- Status: mostly Partial with several Non-compliant in IAM/PAM/BCM.
- SAMA maturity average: ~2.4 (current); target 3.5.
- Priority: ≥6 P1.
- Regulatory risk: ≥3 Critical, ≥5 High.

---

## Pass criteria

Skill **passes** if it:

1. Treats SAMA frameworks as primary; ECC as secondary alignment only.
2. Applies SAMA 0–5 maturity model and reports current vs. target.
3. Identifies the **AWS root not in PAM** as Critical regulatory risk.
4. Flags **SMS OTP for privileged remote access** as a SAMA finding (phishing-resistant MFA expected for privileged).
5. Surfaces the **BCM live-failover** gap as P1 — this is a known SAMA hot spot.
6. Notes the late written incident report as a separate, distinct finding.
7. Asks (or assumes with justification) about critical-system designation and applies CSCC overlay if confirmed.
8. References SAMA CSF v1.0 May 2017 explicitly.

Skill **fails** if it:

- Recommends ECC-2:2024 as the primary framework.
- Skips SAMA maturity scoring.
- Treats AWS-side issues as out of scope.
- Misses the BCM live-failover or incident-report timeliness finding.
