# Changelog

All notable changes to the Saudi Regulatory Compliance Claude Skill are documented here.

---

## [v4.0] — 2026-05

### Added
- Expanded 4 existing reference files to compliance-grade depth from source PDFs:
  - `OSMACC-1-2021.md` — 533 lines; all 38 subcontrols verbatim, per-subdomain evidence tables, 25 audit flags, 32-point assessment checklist
  - `CGEC-1-2019.md` — 502 lines; all 21 guidelines verbatim, operator-implication layer per guideline, mandatory-vs-advisory table
  - `CGESP-1-2019.md` — 817 lines; all 34 guidelines verbatim, SoHo/SME applicability markers, regulatory mapping per guideline, mandatory obligations clearly flagged
  - `NCS-1-2020.md` — 668 lines; all algorithm/key-size requirements verbatim, MODERATE vs ADVANCED comparison table, all 8 protocol sections with accepted suites, full KLM processes table with evidence, 23 audit flags
- 4 new standalone test scenarios: social media (OSMACC), ICT SP/CST CRF RT08, NCS cryptography audit, e-commerce provider

### Fixed
- TCC identifier corrected from TCC-1:2023 to TCC-1:2021 throughout
- CGEC guideline count corrected to 21 (was 18)
- CGESP guideline count corrected to 34 (was 30)
- SKILL.md description reformatted to proper multi-line YAML block

---

## [v3.0] — 2025

### Added
- 5 new NCA framework reference files:
  - `OSMACC-1-2021.md` — Organizations' Social Media Accounts Cybersecurity Controls
  - `CST-CRF.md` — CST CRF RT08, ICT Service Provider Cybersecurity Regulatory Framework
  - `CGEC-1-2019.md` — Cybersecurity Guidelines for E-commerce Consumers
  - `CGESP-1-2019.md` — Cybersecurity Guidelines for E-commerce Service Providers
  - `NCS-1-2020.md` — National Cryptographic Standards
- SKILL.md framework table expanded to 19 entries
- Assessment workflow triage list updated
- Entity classification overlays updated for new frameworks
- `tests/README.md` coverage map updated to reflect all 15 reference files

---

## [v2.0] — 2025

### Added
- Expanded framework coverage: OTCC, TCC, NDMO Standards, SAMA IT Governance, SAMA BCM, Personal Data Transfer Regulation
- Reorganised reference notes with per-framework version dates
- Multi-axis scoring rubric (`tests/scoring-model.md`)
- Finding template (`references/finding-template.md`)
- Two worked assessment examples (`references/examples.md`)
- Nine evaluation scenarios with pass/fail criteria (tests 01–09)

---

## [v1.0] — 2024

### Added
- Initial release
- Core frameworks: ECC, CCC, DCC, CSCC, SAMA CSF, CST Regulations, PDPL
- Packaged `.skill` file for Claude upload
- Basic test scenarios
