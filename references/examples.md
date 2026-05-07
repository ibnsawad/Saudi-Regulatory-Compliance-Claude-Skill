# Worked examples

Two end-to-end illustrations of how the skill should respond to common assessment requests. Use them as the gold standard for tone, structure, and depth.

---

## Example 1 — SAMA-supervised digital bank, cloud-first

### User input

> We're a SAMA-licensed digital bank using AWS for core processing. We have a SOC contract with a managed provider. Our team is 200 people, fully cloud, no on-prem datacentre. Can you do a high-level compliance review against SAMA, ECC, and PDPL? Mention any cloud licensing issues we should know about.

### Expected response shape

**Stage A — Scope.** SAMA-licensed bank → SAMA CSF, SAMA IT Governance, SAMA BCM are primary. ECC-2:2024 is not the lead framework but expectations align. PDPL applies to all customer personal data processing. Cloud use engages CST CCRF on the AWS side and CCC-2:2024 on the bank side as a Cloud Service Tenant. Critical systems likely include core banking and payment switch — designate and apply CSCC-1:2019.

**Stage B — Findings (excerpt).**

| ID | Framework / Control Ref | Domain | Finding | Status | Regulatory Risk | Priority | Owner | Remediation | Evidence Required |
|----|--------------------------|--------|---------|--------|-----------------|----------|-------|-------------|-------------------|
| F-001 | SAMA CSF — Cybersecurity Operations — IAM | Operations & Tech | Privileged access to AWS root and AWS Organizations management account is held by named individuals without PAM brokering. | Non-compliant | Critical | P1 | CISO | Move all privileged AWS access behind PAM with session recording and JIT elevation; eliminate standing root access; document break-glass. | PAM configuration export; sample recorded session; break-glass procedure with quarterly test record. |
| F-002 | CCC-2:2024 — Cloud Defence — Encryption [verify ref] | Cloud Defence | Customer KMS keys are AWS-managed; SAMA expects bank-controlled key custody for high-impact workloads. | Partial | High | P1 | CISO | Migrate critical workloads to customer-managed KMS keys with HSM backing; document key lifecycle. | Key inventory; HSM attestation; migration plan with milestones. |
| F-003 | PDPL Art. 27 (Breach notification) [verify ref] | Privacy | No documented 72-hour breach notification path to SDAIA; current procedure stops at internal escalation. | Non-compliant | High | P1 | DPO | Update incident playbook to include SDAIA notification path with template and 72-hour timer; integrate with SOC. | Updated playbook; tabletop with notification step; template letter. |
| F-004 | SAMA BCM Framework — Exercise programme | Resilience | DR tested as tabletop only; no live failover of core banking in last 24 months. | Partial | High | P1 | CIO | Schedule and execute a live failover within 12 months; document RTO/RPO achieved against targets. | Test plan, evidence of execution, post-test report. |

**Stage C — Risk and priority.** Concentration: SAMA Critical / High items dominate (PAM, key custody, BCM testing). PDPL exposure on breach process. Mark four P1 items.

**Stage D — Remediation roadmap.**

- *0–30 days*: PAM on AWS root; SDAIA breach playbook update; designate critical systems for CSCC.
- *30–60 days*: Customer-managed KMS migration plan signed off; threat-led pen test scoped.
- *60–90 days*: Live DR failover dry-run; SOC use-case gap closure; vendor remote-access tightening.

**Stage E — Output deliverables.** Findings table, executive summary, board-ready risk heatmap, regulator-ready notification triggers section, ISO 27001 / NIST CSF mapping appendix.

**Cloud licensing note.** AWS holds the relevant CST CCRF authorisations for KSA — confirm the licence covers the workload data tier the bank is using. The bank should not assume this; pull the CSP's KSA compliance attestations into the vendor file.

---

## Example 2 — Government entity migrating a citizen service to cloud

### User input

> We're a public-sector entity launching a citizen-facing service that collects national ID, mobile, and basic personal data. Hosting on a local CSP in KSA. What do we need to comply with?

### Expected response shape

**Stage A — Scope.** Government entity → ECC-2:2024 baseline + DCC-1:2022 + NDMO Standards (data management + personal data protection). Citizen service processing personal data → PDPL + Implementing Regulations + Transfer Regulation (only if any data leaves KSA). Hosting on a local CSP → CCC-2:2024 (CST/tenant side) + CST CCRF awareness for the chosen CSP. If the service is designated critical → CSCC-1:2019.

**Stage B — Pre-launch checklist.**

1. Classify the data per the four-level scheme. National ID + mobile + name = at minimum *Confidential*; if combined with sensitive attributes, escalate.
2. Run a DPIA covering the citizen flow, retention, sharing, and security controls.
3. Privacy notice on the service in plain Arabic and English with PDPL-required elements (controller identity, purposes, legal basis, recipients, retention, rights, contact, complaint route).
4. Designate a DPO or confirm coverage by the entity DPO.
5. Confirm SDAIA registration / notification status as required by the Implementing Regulations for the entity type.
6. Sign a DPA with the CSP that includes PDPL-specific clauses and security obligations aligned to CCC-2:2024.
7. Confirm CSP's CST CCRF authorisation level covers the data classification.
8. Verify residency: data, backups, logs, and admin access should remain in-KSA at the chosen tier; document any exceptions and obtain approvals.
9. Implement DCC-1:2022 obligations: classification labels in the data layer, encryption with key custody, DLP on egress paths, retention rules, secure disposal.
10. Build the breach response: 72-hour SDAIA notification and government-channel reporting per NDMO; integrate with the SOC.
11. Set up data-subject rights workflow with logged requests and 30-day SLA.
12. Conduct a pre-launch security test and a privacy review; capture sign-offs from the CISO, DPO, and Data Office.

**Stage C — Notification and ongoing reporting.**

- SDAIA: breach within 72 hours; data-subject rights periodic reporting where required.
- NCA: significant cyber incident per sectoral procedure.
- NDMO: government data incidents per the central procedure.
- Sectoral regulator: per its specific reporting channel if applicable.

**Stage D — Documents the entity should produce before go-live.**

- Service privacy notice (AR / EN)
- DPIA report
- DPA with the CSP
- Records of processing entry
- Data-flow diagram
- Classification register entry
- Retention schedule entry
- Breach playbook with SDAIA path
- DSR workflow
- Security test report
- Sign-off pack with CISO / DPO / CDO / sponsor signatures

---

## Notes on style for both examples

- Cite the framework and § / Art reference each time a claim is made about an obligation; tag `[verify ref]` if unsure.
- Findings always include status, regulatory risk, priority, owner, remediation, and required evidence.
- Do not overreach into legal advice; route to KSA-licensed counsel for novel interpretations.
- When data is missing, ask up to three pointed questions rather than guessing.
