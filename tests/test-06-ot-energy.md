# Test 06 — OT / Energy Operator (NCA OTCC overlay)

## Eval purpose

Confirm the skill recognises OT / ICS scope and applies **OTCC-1:2022** rather than treating OT as a generic IT problem. Verify it handles Purdue-model segmentation, vendor remote access, and safety-coordinated patching.

---

## Scenario

"NorthRefinery", a downstream petrochemical operator. The user asks for an OT cybersecurity readiness assessment.

- **Architecture**: Process automation across DCS (level 1–2), HMIs and engineering workstations (level 2), historian and patch server (level 3). One **shared corporate-OT firewall** between level 3 and level 4. No formal IDMZ at level 3.5.
- **Asset inventory**: Spreadsheet in OT engineering; ~70% accurate; not reconciled with the IT CMDB.
- **Engineering workstations**: Internet-capable for vendor downloads.
- **Removable media**: Used regularly to move firmware and project files; no scanning kiosk; some scans on individual laptops.
- **Vendor remote access**: OEM connects via a vendor-managed jump host; **shared credentials** across OEM staff; sessions not recorded.
- **Patching**: OT patches deferred; many controllers more than 36 months out of date; no documented exception register.
- **Antivirus / EDR**: Antivirus on engineering workstations and historian (signatures up to date in most cases). EDR not feasible on legacy controllers.
- **Monitoring**: No passive ICS monitoring (Claroty / Nozomi / Dragos). IT SIEM does not receive OT logs.
- **Backup**: Controller logic and HMI projects backed up quarterly; backups not restore-tested.
- **Incident response**: OT-specific runbook not written. Safety integration with cyber playbooks absent.
- **Designation**: Refinery is treated as critical infrastructure by the parent group, but no formal NCA designation register on file.

---

## Expected skill behaviour

### A. Entity classification

OT-heavy critical infrastructure → applies:

- **NCA OTCC-1:2022** primary for OT
- **NCA ECC-2:2024** baseline
- **NCA CSCC-1:2019** if the refinery is designated critical
- **NCA DCC-1:2022** for engineering and operational data
- **TCC-1:2023** if OEM / contractors connect remotely
- **PDPL** if any personnel personal data flows through OT systems (rare, but check biometric access)
- Sectoral overlays: parent-group / Aramco-style standards if applicable; IEC 62443 mapping offered

### B. First-step requirement

Skill should:

1. Ask whether NCA designation exists.
2. Ask whether the entity is in the parent's IPSCS / critical-infrastructure programme.
3. Ask which IEC 62443 zones / conduits are documented.

### C. Expected findings (calibre)

| ID | Framework / Control Ref | Status | Reg Risk | Op Risk | Priority |
|----|--------------------------|--------|----------|---------|----------|
| F-001 | OTCC-1:2022 — IT/OT segmentation, IDMZ at level 3.5 | Non-compliant | High | **High** | P1 |
| F-002 | OTCC-1:2022 — Engineering workstation hardening (no internet) | Non-compliant | High | High | P1 |
| F-003 | OTCC-1:2022 — Removable media controls + scanning kiosk | Non-compliant | High | High | P1 |
| F-004 | OTCC-1:2022 — Vendor remote access (jump, MFA, recording, individualised creds) | Non-compliant | High | High | P1 |
| F-005 | OTCC-1:2022 — OT asset inventory completeness | Partial | Medium | High | P2 |
| F-006 | OTCC-1:2022 — OT monitoring (passive sensing) + log feed to SOC | Non-compliant | High | High | P1 |
| F-007 | OTCC-1:2022 — Patching strategy with safety-coordinated windows; exception register | Partial | High | High | P2 |
| F-008 | OTCC-1:2022 — Backup of controller logic + HMI projects with restore tests | Partial | High | High | P2 |
| F-009 | OTCC-1:2022 — OT incident-response runbook with safety integration | Non-compliant | High | High | P1 |
| F-010 | CSCC-1:2019 — designation register | Insufficient evidence | High | Medium | P1 |
| F-011 | ECC-2:2024 §3-x (Resilience — DR for OT) [verify ref] | Insufficient evidence | High | High | P2 |
| F-012 | DCC-1:2022 — engineering data protection | Insufficient evidence | Medium | Medium | P3 |

### D. Output structure

- Executive Summary calling out **safety integration** and **vendor remote access** as the headline risks.
- Findings split: Architecture & Segmentation, Endpoints & Removable Media, Vendor Access, Asset Inventory, Monitoring, Patching, Backup, IR, Designation, Baseline.
- Roadmap with **safety-aware** milestones — recognise that OT changes need outage windows.
- Cross-mapping to IEC 62443 series and NIST SP 800-82 Rev 3 offered.
- Notification triggers: NCA + sectoral regulator (energy / petrochemical) + parent-group reporting.

### E. Headline numbers expected

- Operational risk: dominantly High.
- Regulatory risk: ≥1 Critical possible if designation gap is severe; multiple High.
- Priority: ≥6 P1.

---

## Pass criteria

Skill **passes** if it:

1. Recognises OT scope and reaches for OTCC-1:2022, not just ECC.
2. Insists on Purdue-model / IDMZ at level 3.5 and treats the corporate-OT firewall alone as inadequate.
3. Treats vendor remote access (shared OEM credentials) as **multi-framework** finding (OTCC + CSCC + ECC).
4. Recognises EDR is not always supportable on legacy controllers and recommends compensating controls (whitelisting, monitoring, segmentation).
5. Differentiates OT patching cadence from IT cadence and demands an exception register.
6. Offers IEC 62443 zone-and-conduit mapping.
7. Asks about NCA designation before applying CSCC.

Skill **fails** if it:

- Applies "ECC + EDR everywhere" thinking.
- Recommends active scanning of OT networks without caveats.
- Treats removable-media as an awareness issue only.
- Misses the safety-integration requirement in IR.
