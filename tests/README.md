# Tests — saudi-regulatory-compliance skill

A test (or "eval") in this folder is a scenario the skill should handle correctly. Each test gives:

- A scenario the user might bring.
- The framework set the skill should apply.
- The findings the skill should produce (with calibre, not exact text).
- Pass / fail criteria so a reviewer can score the skill's output objectively.

Use these tests when:

- Updating the skill — run all nine before publishing changes.
- Onboarding a new contributor — the tests make the skill's expected behaviour concrete.
- Debugging a real client output that didn't match expectations — find the closest test and compare.

---

## How to run a test

1. Open a fresh session (no carry-over context).
2. Paste the **Scenario** section from the test file as if you were the user.
3. Capture the skill's output.
4. Score against the **Pass criteria** in the test file.
5. Note any deviation in a short review log.

Optional: use the `skill-creator` skill's eval tooling to automate runs across multiple Claude models.

---

## Scoring

All tests use the scoring approach defined in `scoring-model.md`:

- Status (Compliant / Partial / Non-compliant / N/A / Insufficient evidence)
- Regulatory risk (Critical / High / Medium / Low)
- Operational risk (High / Medium / Low)
- Priority (P1 / P2 / P3 / P4)
- NCA compliance level (1–5) where NCA frameworks apply
- SAMA maturity (0–5) where SAMA frameworks apply

A skill response should reflect this multi-axis scoring, not a single severity label.

---

## Test catalogue

| # | File | Coverage focus | Frameworks exercised |
|---|------|----------------|----------------------|
| 01 | `test-01-cloud-csp.md` | CSP licensing + cloud cyber + cross-border | CST CCRF, CST CRF RT08 (if ICT SP), CCC-2:2024, ECC-2:2024, DCC-1:2022, NCS-1:2020, PDPL + Transfer Reg |
| 02 | `test-02-government-entity.md` | Government overlay (NDMO + privacy) | ECC-2:2024, DCC-1:2022, NDMO Standards, PDPL, partial CCC, NCS-1:2020 |
| 03 | `test-03-bank-sama.md` | SAMA primary + cloud overlay | SAMA CSF, SAMA IT Gov, SAMA BCM, CCC-2:2024, CSCC-1:2019, PDPL, DCC, NCS-1:2020 |
| 04 | `test-04-critical-system.md` | CSCC + OTCC overlay; designation discipline | CSCC-1:2019, OTCC-1:2022, ECC-2:2024, DCC, PDPL, NCS-1:2020 |
| 05 | `test-05-data-protection.md` | PDPL + DCC + Transfer Reg; sensitive data | PDPL + Implementing Regs + Transfer Reg, DCC-1:2022, NCS-1:2020 |
| 06 | `test-06-ot-energy.md` | OT/ICS — Purdue, vendor remote, safety patching | OTCC-1:2022, ECC-2:2024, CSCC-1:2019, NCS-1:2020 (lightweight crypto for constrained OT), IEC 62443 mapping |
| 07 | `test-07-telework.md` | Hybrid workforce + BYOD + contractor remote | TCC-1:2023, ECC-2:2024, DCC-1:2022, PDPL, NCS-1:2020 |
| 08 | `test-08-fintech-multi-overlay.md` | SAMA + cloud + PCI + PDPL + cross-border | SAMA CSF / IT Gov / BCM / Outsourcing / Open Banking, PCI DSS v4.0.1, CCC-2:2024, DCC-1:2022, PDPL + Transfer Reg, CSCC, NCS-1:2020, CGESP-1:2019 (e-commerce channel) |
| 09 | `test-09-incident-notification.md` | Notification routing across regulators | PDPL Implementing Regs, SAMA CIRP, CST CCRF, CST CRF RT08, NCA sectoral, NDMO |

---

## Coverage map

The nine tests collectively exercise the following frameworks from `references/`. Frameworks marked *(background)* are applied as baseline or cross-reference rather than as the primary assessment lens.

| Framework | Reference file | Tests |
|-----------|---------------|-------|
| ECC-2:2024 | `ECC-2-2024.md` | All tests (baseline) |
| CCC-2:2024 | `CCC-2-2024.md` | 01, 02, 03, 08 |
| DCC-1:2022 | `DCC-1-2022.md` | 01, 02, 03, 04, 05, 07, 08 |
| CSCC-1:2019 | `CSCC-1-2019.md` | 03, 04, 06, 08 |
| OTCC-1:2022 | `OTCC-1-2022.md` | 04, 06 |
| TCC-1:2023 | `TCC-1-2023.md` | 07 |
| OSMACC-1:2021 | `OSMACC-1-2021.md` | 08 *(background — e-wallet social media channel)* |
| SAMA CSF / IT Gov / BCM | `SAMA-CSF.md` | 03, 08 |
| CST CCRF (RS10) | `CST-Regulations.md` | 01, 09 |
| CST CRF RT08 | `CST-CRF.md` | 01 *(if entity is also an ICT SP)*, 09 |
| PDPL + Implementing Regs | `PDPL.md` | 01, 02, 05, 07, 08 |
| Personal Data Transfer Regulation | `PDPL.md` | 01, 05, 08 |
| NDMO Standards | `NDMO-Standards.md` | 02, 09 |
| NCS-1:2020 | `NCS-1-2020.md` | All tests *(background — cryptographic standard underlying ECC §2-5 and DCC §2-5-1)*; foregrounded in 03, 04, 05, 08 where ADVANCED level is likely required |
| CGEC-1:2019 | `CGEC-1-2019.md` | 08 *(background — e-wallet consumer-facing obligations)* |
| CGESP-1:2019 | `CGESP-1-2019.md` | 08 *(background — e-commerce service provider good-practice)* |
| PCI DSS v4.0.1 | *(cross-mapping)* | 08 |
| Notification routing | Multiple | Test 09 (focused), Tests 03 / 05 / 08 (embedded) |

**Frameworks with no dedicated test scenario yet** (coverage is background-only):
- OSMACC-1:2021 — no standalone social-media-account assessment test; embedded in 08.
- CST CRF RT08 — no standalone ICT Service Provider test; embedded in 01 and 09.
- CGEC-1:2019 / CGESP-1:2019 — no standalone e-commerce SME or consumer-protection test.
- NCS-1:2020 — no standalone cryptographic-standards audit test.

If any of these become a common client request, add a dedicated test here that exercises it as the primary lens.

---

## What "good" looks like

A passing skill response on these tests should:

1. Pick the right framework set on first read.
2. Cite framework versions explicitly.
3. Tag uncertain control numbers with `[verify ref]` rather than fabricate.
4. Use the multi-axis scoring from `scoring-model.md`.
5. Produce a findings table per `references/finding-template.md`.
6. Surface notification triggers as a discrete section.
7. Offer (not impose) cross-mapping to ISO / NIST.
8. Note assumptions and limitations honestly.

A failing response typically:

- Treats every gap as "High Risk".
- Cites ECC-1:2018 instead of ECC-2:2024.
- Misses the lead regulator.
- Skips PDPL when personal data is involved.
- Recommends "deploy SIEM" as a universal remediation.
