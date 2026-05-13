# Test 07 — Telework / Hybrid Workforce (NCA TCC overlay)

## Eval purpose

Confirm the skill applies **TCC-1:2021** as a discrete overlay rather than folding telework into general remote-access guidance.

---

## Scenario

"ConsultEast", a Saudi consultancy. NCA-scoped (private-sector entity that has voluntarily aligned to ECC for client requirements; some clients are NCA-scoped and require flow-down).

- **Workforce**: 280 staff — 60% hybrid (3 days office / 2 days remote), 30% on client sites, 10% fully remote.
- **Devices**: Mixed — managed laptops for 75% of staff; **BYOD** for the remaining 25% (mostly contractors).
- **VPN**: Always-on VPN with split-tunnel enabled. **MFA: TOTP**.
- **EDR**: Deployed on managed laptops. Not on BYOD.
- **Posture checks**: Configured but not enforced — devices that fail still connect.
- **DLP**: Cloud DLP only (Microsoft Purview); endpoint DLP not deployed.
- **Remote screen-share / collaboration**: Teams + Zoom; no recording or watermarking on sensitive engagements.
- **Geo / anomaly**: VPN logs aggregated, but no alerting on impossible-travel or high-risk-country logins.
- **BYOD policy**: One-paragraph clause in the employee handbook; no MDM enrolment for BYOD.
- **Contractor remote access**: Contractors get full VPN access for the contract duration; not time-bound, not posture-checked.
- **Awareness**: Annual cyber awareness; no telework-specific module.
- **Sensitive client data**: Some engagements involve client personal data and Confidential government data; data downloaded to laptops for offline work.

---

## Expected skill behaviour

### A. Entity classification

NCA-aligned consultancy with significant telework + contractor population →

- **NCA TCC-1:2021** primary for the assessment lens
- **NCA ECC-2:2024** baseline
- **NCA DCC-1:2022** because client data flows through telework endpoints
- **PDPL** if personal data of staff or clients is processed
- Per client engagement, additional flow-down (e.g. SAMA bank client → SAMA controls flow into the engagement)

### B. Expected findings (calibre)

| ID | Framework / Control Ref | Status | Reg Risk | Op Risk | Priority |
|----|--------------------------|--------|----------|---------|----------|
| F-001 | TCC-1:2021 — MFA strength (TOTP for privileged remote) | Partial | High | Medium | P1 |
| F-002 | TCC-1:2021 — VPN split-tunnel for sensitive workloads | Partial | High | High | P1 |
| F-003 | TCC-1:2021 — Posture checks enforced (not just configured) | Non-compliant | High | High | P1 |
| F-004 | TCC-1:2021 — BYOD with MDM, separation of personal/work, EDR | Non-compliant | High | High | P1 |
| F-005 | TCC-1:2021 — Endpoint DLP for sensitive client data | Non-compliant | High | High | P1 |
| F-006 | TCC-1:2021 — Geo / anomaly alerting on remote logins | Non-compliant | Medium | Medium | P2 |
| F-007 | TCC-1:2021 — Contractor remote access (time-bound, posture, jump host) | Non-compliant | High | High | P1 |
| F-008 | TCC-1:2021 — Telework-specific awareness | Non-compliant | Medium | Low | P3 |
| F-009 | DCC-1:2022 — Local data on endpoints (encryption + retention) | Partial | High | High | P2 |
| F-010 | ECC-2:2024 §2-x (IAM / MFA) [verify ref] | Partial | High | Medium | P2 |
| F-011 | PDPL — client personal-data handling on endpoints | Insufficient evidence | High | Medium | P2 |

### C. Output structure

- Executive Summary calling out **BYOD without MDM** and **TOTP for privileged** as the headline risks.
- Findings split: Identity & Authentication, Endpoint & BYOD, Network & Posture, Data on Endpoints, Contractors, Awareness, Baseline overlap.
- Roadmap prioritising posture-enforce and BYOD MDM.
- Mapping to ECC-2:2024 IAM + endpoint controls offered.

### D. Headline numbers expected

- Status: predominantly Partial / Non-compliant in TCC areas.
- Regulatory risk: ~2–3 High; mostly High operational.
- Priority: ≥5 P1.

---

## Pass criteria

Skill **passes** if it:

1. Surfaces TCC-1:2021 as a discrete overlay, not as "remote access controls".
2. Treats TOTP for privileged remote access as a finding (phishing-resistant MFA expected).
3. Recommends posture **enforcement**, not just configuration.
4. Distinguishes BYOD from managed-laptop posture and applies stricter restrictions to BYOD.
5. Calls out contractor access without time-bounding or posture as P1.
6. Notes that client engagement flow-down may impose stricter controls than ConsultEast's own baseline.

Skill **fails** if it:

- Treats this as a generic ECC IAM gap.
- Misses TCC entirely.
- Doesn't ask whether contractors connect to client environments.
- Recommends "VPN is fine, just enable MFA" without addressing posture / BYOD.
