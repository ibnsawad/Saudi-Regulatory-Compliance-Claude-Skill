# Saudi Regulatory Compliance — Claude Skill
> *"Your AI compliance assistant for Saudi Arabia's regulatory landscape."*

![Release](https://img.shields.io/badge/Release-v2.0.0-green)
![License](https://img.shields.io/badge/License-MIT-blue)
![Frameworks](https://img.shields.io/badge/Frameworks-8-orange)
![Built%20with](https://img.shields.io/badge/Built%20with-Claude-blueviolet)

> Structured, regulation-aware guidance for Saudi Arabia's regulatory landscape — powered by Claude Skills.

> This is an independent open-source project and is not affiliated with NCA, SAMA, CST, SDAIA, or any government authority.

This Claude Skill provides structured, regulation-aware guidance on Saudi Arabia's cybersecurity, cloud, and data protection regulatory frameworks. Ask questions in plain language and get regulation-specific answers — no need to read hundreds of pages of official documentation.

---

## Frameworks Covered

| Framework | Authority | Domain |
|---|---|---|
| **NCA ECC-2:2024** | National Cybersecurity Authority | Essential Cybersecurity Controls |
| **NCA CCC-2:2024** | National Cybersecurity Authority | Cloud Cybersecurity Controls |
| **NCA DCC-1:2022** | National Cybersecurity Authority | Data Cybersecurity Controls |
| **NCA CSCC-1:2019** | National Cybersecurity Authority | Cybersecurity Controls for Critical Systems |
| **SAMA-CSF** | Saudi Central Bank | Cybersecurity Framework for Financial Sector |
| **CST Regulations** | Communications, Space & Technology Commission | Cloud Computing Regulatory Framework |
| **PDPL** | NDMO / SDAIA | Personal Data Protection Law |
| **NCA TCC-1:2023** | National Cybersecurity Authority | Telecommunications Cybersecurity Controls |

---

## Installation

### Prerequisites
- Claude account (Free, Pro, Max, Team, or Enterprise)
- Code execution enabled: **Settings → Capabilities → Code execution and file creation**

### Steps

1. **Download the skill file** — Click `saudi-regulatory-compliance-v2.skill` in this repo, then click the **Download raw file** button (⬇️ icon, top right of the file view)

   Or clone the full repo:
   ```bash
   git clone https://github.com/ibnsawad/Saudi-Regulatory-Compliance-Claude-Skill.git
   ```

2. **Locate the skill file** — Use the downloaded `saudi-regulatory-compliance-v2.skill` file directly

3. **Upload to Claude**
   - Go to **Settings → Customize → Skills**
   - Click **"+"** → **"+ Create skill"** → **"Upload a skill"**
   - Select the `.skill` file
   - Toggle it **ON**

4. **Start a new chat** — The skill activates automatically. No commands needed.

---

## Example Prompts

Once installed, try these in a new Claude conversation:

```
We are a cloud service provider operating in Saudi Arabia offering IaaS 
to government and private sector clients. What NCA and CST regulations apply to us?
```

```
We are a Saudi bank. What does the SAMA Cybersecurity Framework require 
and how does it overlap with NCA ECC?
```

```
We collect personal data from Saudi residents. What are our obligations 
under the PDPL and its implementing regulations?
```

```
We operate critical national infrastructure in KSA. What cybersecurity 
controls are mandatory under ECC-2:2024?
```

---

## Testing the Skill

A `tests/` folder is included with 5 scenario-based test cases:

| Test | Scenario |
|---|---|
| `test-01-cloud-csp.md` | Cloud service provider obligations |
| `test-02-government-entity.md` | Government entity cloud compliance |
| `test-03-bank-sama.md` | Bank compliance under SAMA-CSF |
| `test-04-critical-system.md` | Critical infrastructure controls |
| `test-05-data-protection.md` | PDPL data protection obligations |

Run any test prompt in a new Claude conversation to validate the skill is working correctly. See `tests/scoring-model.md` for the evaluation rubric.

---

## Repository Structure

```
Saudi-Regulatory-Compliance-Claude-Skill/
├── SKILL.md                              # Core skill instructions
├── saudi-regulatory-compliance-v2.skill  # Packaged skill file (upload this to Claude)
├── references/
│   ├── ECC-2-2024.md                 # NCA Essential Cybersecurity Controls
│   ├── CCC-2-2024.md                 # NCA Cloud Cybersecurity Controls
│   ├── DCC-1-2022.md                 # NCA Data Cybersecurity Controls
│   ├── CSCC.md                       # Critical Systems Cybersecurity Controls
│   ├── SAMA-CSF.md                   # SAMA Cybersecurity Framework
│   ├── CST-Regulations.md            # CST Cloud Regulations
│   └── PDPL-Notes.md                 # Personal Data Protection Law
├── tests/
│   ├── scoring-model.md              # Evaluation rubric
│   ├── test-01-cloud-csp.md
│   ├── test-02-government-entity.md
│   ├── test-03-bank-sama.md
│   ├── test-04-critical-system.md
│   └── test-05-data-protection.md
├── DEMO-GUIDE.md                     # Demo walkthrough
├── DISCLAIMER.md                     # Legal disclaimer
└── README.md                         # This file
```

---

## Disclaimer

This skill is intended for informational and educational purposes only. It does not constitute legal or regulatory advice. Always consult qualified legal counsel and refer to official regulatory publications from NCA, SAMA, CST, and SDAIA for authoritative guidance.

---

## Contributing

Contributions welcome! If you spot outdated information, want to add a new framework, or improve test cases:

1. Fork the repository
2. Create a feature branch: `git checkout -b update/framework-name`
3. Submit a pull request with a clear description of changes

---

## License

MIT License — see [LICENSE](LICENSE) for details.

---

## 👤 Author

**Majid Bib Sawad** — [@ibnsawad](https://github.com/ibnsawad)

---

*If this skill helped you, consider giving it a ⭐ on GitHub!*
