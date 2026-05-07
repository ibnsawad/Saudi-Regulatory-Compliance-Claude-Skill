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
| 01 | `test-01-cloud-csp.md` | CSP licensing + cloud cyber + cross-border | CST CCRF, CCC-2:2024, ECC-2:2024, DCC-1:2022, PDPL + Transfer Reg |
| 02 | `test-02-government-entity.md` | Government overlay (NDMO + privacy) | ECC-2:2024, DCC-1:2022, NDMO Standards, PDPL, partial CCC |
| 03 | `test-03-bank-sama.md` | SAMA primary + cloud overlay | SAMA CSF, SAMA IT Gov, SAMA BCM, CCC-2:2024, CSCC-1:2019, PDPL, DCC |
| 04 | `test-04-critical-system.md` | CSCC + OTCC overlay; designation discipline | CSCC-1:2019, OTCC-1:2022, ECC-2:2024, DCC, PDPL |
| 05 | `test-05-data-protection.md` | PDPL + DCC + Transfer Reg; sensitive data | PDPL + Implementing Regs + Transfer Reg, DCC-1:2022 |
| 06 | `test-06-ot-energy.md` | OT/ICS — Purdue, vendor remote, safety patching | OTCC-1:2022, ECC-2:2024, CSCC-1:2019, IEC 62443 mapping |
| 07 | `test-07-telework.md` | Hybrid workforce + BYOD + contractor remote | TCC-1:2023, ECC-2:2024, DCC-1:2022, PDPL |
| 08 | `test-08-fintech-multi-overlay.md` | SAMA + cloud + PCI + PDPL + cross-border | SAMA CSF / IT Gov / BCM / Outsourcing / Open Banking, PCI DSS v4.0.1, CCC-2:2024, DCC-1:2022, PDPL + Transfer Reg, CSCC |
| 09 | `test-09-incident-notification.md` | Notification routing across regulators | PDPL Implementing Regs, SAMA CIRP, CST CCRF, NCA sectoral, NDMO |

---

## Coverage map

The nine tests collectively exercise every framework in `references/`:

- ECC-2:2024 — every test (baseline)
- CCC-2:2024 — Tests 01, 02, 03, 08
- DCC-1:2022 — Tests 01, 02, 03, 04, 05, 07, 08
- CSCC-1:2019 — Tests 03, 04, 06, 08
- OTCC-1:2022 — Tests 04, 06
- TCC-1:2023 — Test 07
- SAMA CSF / IT Gov / BCM — Tests 03, 08
- CST CCRF — Tests 01, 09
- PDPL + Implementing Regs — Tests 01, 02, 05, 07, 08
- Personal Data Transfer Regulation — Tests 01, 05, 08
- NDMO Standards — Tests 02, 09
- PCI DSS v4.0.1 — Test 08
- Notification routing — Test 09 (focused), Tests 03 / 05 / 08 (embedded)

If a future framework is added to the skill (e.g. SAMA Open Banking dedicated reference), add a test here that exercises it specifically.

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
