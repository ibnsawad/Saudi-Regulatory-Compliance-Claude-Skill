# Test 02 — Government Entity (NCA ECC + DCC + NDMO + PDPL)

## Eval purpose

Confirm the skill correctly routes a government scenario through the **government overlay stack** (NDMO Standards alongside NCA controls) and treats classification + open-data + citizen privacy as first-class concerns.

---

## Scenario

A ministry-level entity, "MinistryX", launching a citizen-facing services portal.

- **Environment**: Mostly on-prem in two data centres in Riyadh; partial migration of non-sensitive workloads to a local CSP underway.
- **Network**: Perimeter firewall (legacy NGFW), no segmentation between corporate and citizen-service zones.
- **Logging**: Each system logs locally; no centralised SIEM. Some servers retain logs 30 days.
- **SOC**: None. Tickets handled by a 5-person ops team during business hours.
- **Governance**: No board-approved cybersecurity policy. CISO role exists but reports into IT operations director.
- **Risk management**: No formal cyber risk register; risk treatment ad-hoc.
- **Vendor management**: No vendor security clauses; no inventory of third-party access.
- **Data**: Citizen personal data collected (national ID, mobile, email, family details) for service eligibility. No documented classification scheme. No data catalogue. No data-flow diagrams.
- **Open Data**: Ministry publishes some open datasets but without a central pipeline; one dataset withdrawn last year after PII appeared.
- **Privacy**: No privacy notice on the portal. No DPO appointed. No DPIA for the new service.
- **DR / BCM**: BCP exists but tested only as tabletop in 2023.
- **Awareness**: Annual training completed by ~60% of staff.

---

## Expected skill behaviour

### A. Entity classification

Government entity → applies:

- **NCA ECC-2:2024** (baseline)
- **NCA DCC-1:2022** (data lifecycle, including citizen data)
- **NDMO Data Management & Personal Data Protection Standards** (government overlay)
- **PDPL** + **Implementing Regulations** (citizen personal data)
- **NCA CCC-2:2024** (CST/tenant side, partial migration)
- **CSCC-1:2019** *if any system is designated critical* — skill should ask, not assume
- **NCA TCC-1:2021** if telework is in use — skill should ask

### B. Lead regulator and notifications

- **NCA** for cyber controls oversight (typical sectoral-regulator coordination).
- **SDAIA / NDMO** for personal data and government data management; PDPL 72-hour breach notification + government-channel reporting.
- **CST** awareness for the local CSP relationship (the CSP must be properly licensed; ministry need not licence).

### C. Expected findings (calibre)

| ID | Framework / Control Ref | Status | Reg Risk | Op Risk | Priority |
|----|--------------------------|--------|----------|---------|----------|
| F-001 | ECC-2:2024 §1-x (Cybersecurity Governance — strategy & policy) [verify ref] | Non-compliant | High | Medium | P1 |
| F-002 | ECC-2:2024 §2-x (Logging & Monitoring) [verify ref] — no centralised SIEM | Non-compliant | High | High | P1 |
| F-003 | ECC-2:2024 §1-x (Risk management) [verify ref] | Non-compliant | High | Medium | P2 |
| F-004 | ECC-2:2024 §4-x (Third-Party Cybersecurity) [verify ref] | Non-compliant | High | Medium | P2 |
| F-005 | DCC-1:2022 — Classification + inventory | Non-compliant | High | High | P1 |
| F-006 | NDMO Standards — Data Catalogue & Metadata | Non-compliant | High | Medium | P2 |
| F-007 | NDMO PDP Standards — privacy notices on citizen services | Non-compliant | **Critical** | High | P1 |
| F-008 | PDPL Art. 12 (Privacy notice) [verify ref] | Non-compliant | Critical | High | P1 |
| F-009 | PDPL — DPO designation [verify ref] | Non-compliant | High | Medium | P1 |
| F-010 | PDPL — DPIA for high-risk processing [verify ref] | Non-compliant | High | Medium | P1 |
| F-011 | PDPL Implementing Regs — 72h breach notification path | Non-compliant | Critical | High | P1 |
| F-012 | ECC-2:2024 §3-x (Resilience — BC tested) [verify ref] | Partial | Medium | Medium | P2 |
| F-013 | ECC-2:2024 §1-x (Awareness) [verify ref] — coverage 60% | Partial | Medium | Low | P3 |
| F-014 | NDMO — Open Data review pipeline (PII leak history) | Partial | High | Medium | P2 |

### D. Required clarifying questions

Before producing the assessment, skill should ask up to three of:

1. Are any systems in this entity formally designated as **critical** by NCA / sectoral regulator? (drives CSCC)
2. Is OT in scope (building management, physical security)? (drives OTCC)
3. Is staff working remotely / hybrid? (drives TCC)

### E. Expected output structure

Same as Test 01: Executive Summary, Scope, Findings, Risk Heatmap, Roadmap, Notification Triggers, Mapping (offered), Limitations.

### F. Headline numbers expected

- Status: heavily Non-compliant; ~12–18 findings.
- Regulatory risk: ≥3 Critical (privacy notice, DPO/DPIA absent, breach path missing), ≥5 High.
- Priority: ≥7 P1.
- NCA compliance level (ECC self-rating): ~1.5 / 5.

---

## Pass criteria

Skill **passes** if it:

1. Selects the government overlay stack (ECC + DCC + NDMO + PDPL) and asks the three clarifying questions before locking scope.
2. Treats the missing privacy notice and DPO as Critical regulatory risk (not just security weakness).
3. Cites versions and uses `[verify ref]` for uncertain numbering.
4. Lists NDMO Standards explicitly, not just NCA frameworks.
5. Routes breach notification through both SDAIA (PDPL) and NDMO (government channel).
6. Produces a remediation roadmap that begins with governance + privacy notices, not just SIEM.

Skill **fails** if it:

- Treats the entity as a generic NCA-scoped private company.
- Skips NDMO entirely.
- Recommends only "deploy SIEM" without addressing privacy obligations.
- Marks privacy notices as Low or Medium regulatory risk.
