# Test 12 — National Cryptographic Standards Audit (NCS-1:2020)

## Scenario

A Saudi government entity is undergoing an ECC-2:2024 assessment. The IT team
has provided the following cryptographic inventory:
- Web portals: TLS 1.2 with AES-128-CBC + RSA-2048 certificates
- Internal file encryption: AES-128-ECB
- Data at rest (classified "Secret"): AES-256-GCM stored on a software key store
- Email signing: SHA-1 + RSA-1024
- Wi-Fi: WPA2-Enterprise
- VPN: IKEv1 with 3DES

## Test Prompt

```
We are a Saudi government entity. Our security team has provided this
cryptographic inventory. Please audit it against NCS-1:2020 and ECC-2:2024 §2-5,
identify all non-compliant configurations, specify whether each gap requires
MODERATE or ADVANCED level remediation, and provide a prioritised fix list.

Inventory:
- Web portals: TLS 1.2, AES-128-CBC, RSA-2048 certificates
- Internal file encryption: AES-128-ECB
- Data at rest (Secret classification): AES-256-GCM, software key store
- Email signing: SHA-1 + RSA-1024
- Wi-Fi: WPA2-Enterprise
- VPN: IKEv1 with 3DES
```

## Expected Behaviour

The skill should:
1. Reference NCS-1:2020 (MODERATE = 128-bit security; ADVANCED = 256-bit security) and ECC-2:2024 §2-5
2. Identify all non-compliant items:
   - AES-128-CBC: CBC mode prohibited → must use GCM or CCM (MODERATE non-compliant)
   - AES-128-ECB: ECB mode prohibited → non-compliant at any level
   - RSA-2048: acceptable at MODERATE but borderline; NCS recommends ≥ 3072 bits for MODERATE
   - SHA-1: explicitly prohibited by NCS-1:2020
   - RSA-1024: key length below minimum for any NCS level — critical gap
   - WPA2: NCS §4.7 requires WPA3-Enterprise once available — flag as planned upgrade
   - IKEv1 + 3DES: both prohibited; must use IKEv2 + AES
   - Secret data on software key store: ADVANCED level requires hardware cryptographic module
3. Assign MODERATE or ADVANCED requirement to each finding
4. Provide a P1/P2/P3 remediation list
5. Note that DCC-1:2022 §2-5-1 requires ADVANCED for Secret/Top Secret data

## Scoring Criteria

| Criterion | Weight |
|-----------|--------|
| Correctly identifies all prohibited algorithms/modes | 30% |
| Correctly maps each finding to MODERATE vs ADVANCED level | 20% |
| Flags hardware module requirement for Secret data | 20% |
| Provides control references (NCS section + ECC §) | 15% |
| Prioritised remediation list | 15% |

**Minimum pass score: 70%**
