# Demo Guide — Saudi Regulatory Compliance Skill

A walk-through for trying the skill end-to-end. Useful for first-time users, demos to colleagues or clients, and as a sanity check before publishing changes.

---

## Objective

By the end of this guide you will have:

1. Run the skill against a representative scenario.
2. Produced a structured compliance assessment.
3. Scored the output against the multi-axis rubric.
4. Compared the result to the test's pass / fail criteria.

The demo takes 15–25 minutes per scenario.

---

## Audience

- Cybersecurity and GRC professionals evaluating the skill.
- Cloud security teams testing it on representative architectures.
- Internal auditors planning to use it for readiness reviews.
- Educators and learners.

---

## Prerequisites

Before starting:

1. **Install the skill.** Drop the `saudi-regulatory-compliance.skill` archive into your skills folder, or unpack the directory directly. Confirm the skill is listed and triggerable.
2. **Read the entry point.** Open `SKILL.md`. The framework table (§2) and entity classification (§4) are the parts you'll see reflected in every output.
3. **Skim the scoring model.** Open `tests/scoring-model.md`. Understand the dual risk axes and the priority matrix before reading any output — the skill's findings only make sense against that rubric.
4. **Pick a scenario.** Browse `tests/`. The catalogue in `tests/README.md` shows which frameworks each scenario exercises.

---

## Step 1 — Pick a test scenario

The nine scenarios cover increasing complexity:

| If you want to demo… | Use this test |
|----------------------|---------------|
| Cloud Service Provider obligations + cross-border | `test-01-cloud-csp.md` |
| Government entity with personal data | `test-02-government-entity.md` |
| SAMA-supervised bank with cloud overlay | `test-03-bank-sama.md` |
| Critical system / CSCC overlay discipline | `test-04-critical-system.md` |
| PDPL + DCC + Personal Data Transfer Regulation | `test-05-data-protection.md` |
| OT / ICS in petrochemical or utility | `test-06-ot-energy.md` |
| Hybrid workforce, BYOD, contractor remote access | `test-07-telework.md` |
| Fintech with stacked overlays (SAMA + cloud + PCI + PDPL) | `test-08-fintech-multi-overlay.md` |
| Incident & breach notification routing | `test-09-incident-notification.md` |

For a first demo, **test-03-bank-sama** or **test-08-fintech-multi-overlay** show the skill at its most representative.

---

## Step 2 — Copy the scenario

Open the test file. Copy only the **Scenario** section (not the "Expected skill behaviour" or "Pass criteria" — those are for scoring afterwards).

---

## Step 3 — Run the skill

In your AI client, start a fresh session and use a prompt like:

> Please run a Saudi regulatory compliance assessment on the following entity. Use your full workflow — entity classification, framework selection, findings table, risk + priority scoring, notification triggers, remediation roadmap.
>
> [Paste Scenario here]

The skill should:

1. Restate scope and selected frameworks (with versions).
2. Optionally ask up to three clarifying questions if the scenario leaves something ambiguous (e.g. critical-system designation, OT in scope, telework in use).
3. Produce a findings table per `references/finding-template.md`.
4. Produce a risk heatmap, remediation roadmap, notification triggers, and (optional) cross-mapping to ISO / NIST.

If the skill jumps straight into recommendations without classifying the entity or citing framework versions, that is a first-pass quality issue worth flagging.

---

## Step 4 — Review the output structure

Check that the output contains:

- **Executive Summary** — posture statement, top three exposures, headline numbers.
- **Scope and Applicable Frameworks** — version-cited.
- **Findings table** — with Status, Regulatory Risk, Operational Risk, Priority, Owner, Remediation, Evidence Required.
- **Risk Heatmap** — count by regulatory risk × priority.
- **Remediation Roadmap** — 30 / 60 / 90-day grouping.
- **Notification & Reporting Triggers** — separate section, not buried.
- **Cross-Framework Mapping** — offered, not imposed.
- **Assumptions and Limitations** — honest about what was assumed and what evidence was missing.

A response missing the Notification section is a frequent failure mode — flag it.

---

## Step 5 — Apply the scoring model

Walk through `tests/scoring-model.md` with the output in front of you:

- **Status** — Compliant / Partial / Non-compliant / Not applicable / Insufficient evidence. Is the distribution sensible?
- **Regulatory risk vs. Operational risk** — are they distinct, or has the skill collapsed them into one severity?
- **Priority (P1–P4)** — does the priority follow the matrix, with statutory-notification gaps escalated to P1?
- **NCA compliance level** (1–5) — present where NCA frameworks apply?
- **SAMA maturity** (0–5) — present where SAMA frameworks apply, with current vs. target?

A common failure: every finding marked "High Risk / Critical / P1". That defeats the purpose of the rubric.

---

## Step 6 — Compare to the test's pass / fail criteria

Open the test file and read the **Pass criteria** section. Score the output against each criterion. Typical examples:

- Did the skill cite framework versions (e.g. "ECC-2:2024" not "ECC")?
- Did it tag uncertain control numbers with `[verify ref]` rather than fabricate?
- Did it identify the lead regulator correctly (SAMA-supervised entity → SAMA primary)?
- Did it apply the right overlays (CSCC for designated critical, OTCC for OT, TCC for telework)?
- Did it surface the 72-hour PDPL breach notification path?
- Did it produce sensible remediation owners (CISO / DPO / CIO / Vendor Manager) rather than generic "the team"?

Note pass / fail per criterion. A short review log is enough.

---

## Step 7 — Iterate and broaden

After your first run:

- **Tweak the scenario.** Add a sub-processor in a non-adequate jurisdiction, or designate a system as critical, and re-run. The skill should recompute the framework set.
- **Run a second test from a different category.** Move from a SAMA scenario to an OT scenario to confirm the skill changes posture.
- **Try a notification-routing question** (test-09 vignettes). Time-pressured questions are where users most need the skill.

---

## Common failure modes to watch for

- Citing **ECC-1:2018** instead of **ECC-2:2024**.
- Missing **PDPL Personal Data Transfer Regulation (Sept 2024)** when cross-border processing is described.
- Treating SAMA-supervised entities under ECC primary rather than SAMA primary.
- Applying CSCC across an entire estate without insisting on a critical-system **designation register**.
- Lumping OT into ECC instead of applying **OTCC-1:2022**.
- Single-axis severity (e.g. everything "High Risk") rather than dual regulatory + operational risk.
- Recommending "deploy SIEM" as a universal remediation while skipping licensing, residency, and breach-path issues.
- Confidently stating exact reporting timelines (e.g. "SAMA written report within 7 days") that should be verified rather than asserted.

---

## What the demo is good for

- Compliance training and onboarding.
- Internal readiness reviews ahead of an audit cycle.
- Cloud security evaluations of new services.
- Education on the Saudi regulatory stack for international teams.
- Vendor questionnaires and pre-engagement screening.

## What the demo is not for

- Formal regulatory submissions or attestations.
- Replacing QSA, accredited assessor, or auditor work.
- Live system telemetry analysis.
- Legal advice — this is compliance-engineering analysis only.

---

## Disclaimer

This guide and the skill are for educational and professional reference. They are not affiliated with NCA, SAMA, CST, SDAIA, NDMO, or any other regulator. Always refer to official regulator publications for the controlling text. See `DISCLAIMER.md` for full terms.
