# Test 04 — Critical System (NCA CSCC overlay)

## Eval purpose

Confirm the skill correctly distinguishes a **critical system overlay** from baseline ECC, demands a designation step, and applies stricter expectations (PAM, segmentation, 24/7 SOC, tested DR, vendor restrictions) only to the in-scope critical systems.

---

## Scenario

A national-utility entity, "GridCo", operating a public-facing customer billing portal, customer outage-reporting service, and an internal asset-management platform that interfaces with SCADA. The user has asked for an assessment of "the critical system".

- **Designation**: No formal critical-system designation register exists. The entity *believes* the SCADA-adjacent asset-management platform is critical but has no signed-off list.
- **Architecture**: Public-facing portal in DMZ, asset-management platform in the corporate VLAN, SCADA on a separate physical network with a partial firewall between corporate and SCADA.
- **Segmentation**: Corporate network is largely flat L2; jump host exists for SCADA access but several engineers know shared admin credentials and bypass it.
- **Endpoint**: Antivirus on all laptops; **EDR/XDR not deployed**.
- **PAM**: Selected privileged accounts vaulted; many domain admin accounts and SCADA-engineering accounts not vaulted; no session recording.
- **MFA**: Phishing-resistant MFA for some staff; **none** for vendors.
- **Monitoring**: SIEM ingests perimeter and AD logs; no SCADA-network monitoring; no use cases tuned for ICS-relevant threats.
- **SOC**: Outsourced 24/7 — but contracted scope excludes the OT side.
- **Patching**: Corporate patch SLAs OK; SCADA patches deferred indefinitely citing vendor support.
- **DR**: Designed but **not tested in 3 years**.
- **Vendor remote access**: SCADA OEM connects via vendor-managed VPN with shared credentials. No session recording.
- **Incident response**: Plan exists; no tabletop in 18 months; no OT-specific playbook.

---

## Expected skill behaviour

### A. Entity classification

Critical national infrastructure context →

- **NCA ECC-2:2024** baseline
- **NCA CSCC-1:2019** overlay on designated critical systems
- **NCA OTCC-1:2022** for the OT/SCADA portion
- **NCA DCC-1:2022** for billing and customer data
- **PDPL** for customer personal data
- **TCC-1:2023** if telework into corporate or jump-host paths

The skill **must demand a designation step** before applying CSCC. Apply OTCC immediately to the SCADA boundary.

### B. Required first step

Before assessing, skill should run a designation exercise:

- Identify candidate critical systems (asset-management platform with SCADA interface, SCADA itself, billing platform if outage would affect critical service delivery).
- State that designation is the entity's responsibility in coordination with NCA / sectoral regulator.
- Tag the absence of a designation register as **Finding F-001 (Critical regulatory risk)**.

### C. Expected findings (calibre)

| ID | Framework / Control Ref | Status | Reg Risk | Op Risk | Priority |
|----|--------------------------|--------|----------|---------|----------|
| F-001 | CSCC-1:2019 — Designation register / sign-off | Non-compliant | **Critical** | High | P1 |
| F-002 | OTCC-1:2022 — IT/OT segmentation, IDMZ, conduit control | Non-compliant | High | **High** | P1 |
| F-003 | CSCC-1:2019 / OTCC-1:2022 — Vendor remote access (shared creds, no session recording) | Non-compliant | High | High | P1 |
| F-004 | CSCC-1:2019 — Privileged Access Management (vault + JIT) | Non-compliant | High | High | P1 |
| F-005 | CSCC-1:2019 — MFA (phishing-resistant for privileged + vendor) | Non-compliant | High | High | P1 |
| F-006 | CSCC-1:2019 — 24/7 SOC scope including OT | Non-compliant | High | High | P1 |
| F-007 | OTCC-1:2022 — OT network monitoring (passive sensing) | Non-compliant | High | High | P1 |
| F-008 | CSCC-1:2019 — Tested DR for critical systems (3 years) | Non-compliant | High | High | P1 |
| F-009 | OTCC-1:2022 — Configuration backup of controllers | Insufficient evidence | High | High | P2 |
| F-010 | CSCC-1:2019 — EDR/XDR on critical-adjacent endpoints | Non-compliant | Medium | High | P2 |
| F-011 | OTCC-1:2022 — Patching strategy with safety-coordinated windows | Partial | High | High | P2 |
| F-012 | ECC-2:2024 §3-x (Resilience — BC tested) [verify ref] | Non-compliant | High | High | P1 |
| F-013 | DCC-1:2022 — Customer data encryption / classification | Insufficient evidence | Medium | Medium | P2 |
| F-014 | PDPL Art. 12 / DPO designation [verify ref] | Insufficient evidence | High | Medium | P2 |

### D. Output structure

- Executive Summary explicitly stating CSCC and OTCC overlays.
- Designation step recommendation up-front.
- Findings split into: Designation, Critical-System Controls (CSCC), OT Controls (OTCC), Baseline (ECC), Data & Privacy (DCC + PDPL).
- Roadmap with clear separation between **safety-impacting OT remediations** (slower planning) and **IT remediations** (faster).
- Notification triggers: NCA significant cyber incident; sectoral regulator (energy / water etc.); CST if telecom-adjacent; SDAIA for personal data.
- IEC 62443 mapping offered for OT.

### E. Headline numbers expected

- Status: dominantly Non-compliant.
- Regulatory risk: ≥1 Critical (designation), ≥6 High.
- Priority: ≥7 P1.
- Operational risk: ≥7 High (this is the key axis for critical systems).

---

## Pass criteria

Skill **passes** if it:

1. Refuses to apply CSCC across the whole entity; insists on designation.
2. Applies OTCC overlay to the SCADA boundary.
3. Differentiates **OT** patching/change cadence from IT cadence (safety constraint).
4. Treats vendor remote access with shared credentials as a major finding for both CSCC and OTCC.
5. Calls out SOC scope excluding OT as a CSCC + OTCC failure.
6. Tags the 3-year-old DR test as P1.
7. Offers IEC 62443 mapping for the OT side.

Skill **fails** if it:

- Applies CSCC to the entire estate without designation.
- Treats SCADA segmentation as a basic firewall question only.
- Ignores OTCC and lumps OT into ECC.
- Recommends "just deploy EDR on SCADA" without recognising platform/safety constraints.
