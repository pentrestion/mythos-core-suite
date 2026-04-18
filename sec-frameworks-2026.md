---
name: sec-frameworks-2026
description: Integrated 2026 cybersecurity frameworks (MITRE ATT&CK v18+, MITRE ATLAS, CTEM, NIST CSF 2.0). Use for threat-informed defense, AI red teaming, and exposure management.
model_routing:
  primary: gemini-3-flash-preview
  fallback: gemini-2.5-flash
  reasoning: Framework mapping and CVE research benefit from Flash tier's speed and web-search efficiency.
---

# 🛡️ Security Frameworks 2026

This skill integrates the most critical cybersecurity frameworks of 2026 to provide a "threat-informed defense."

## 🚀 How to Use

When the user asks for a security analysis, red team plan, or framework mapping, use the following references:

### 1. **MITRE ATT&CK v18+**
- **Use for:** Behavioral detection, analyst precision scoring, and mapping traditional tradecraft.
- **Reference:** [attack_v18.md](references/attack_v18.md)

### 2. **MITRE ATLAS**
- **Use for:** Red teaming AI systems, defending against prompt injection, and model safety.
- **Reference:** [atlas_ai.md](references/atlas_ai.md)

### 3. **CTEM (Continuous Threat Exposure Management)**
- **Use for:** Prioritizing vulnerabilities by business risk and live exploitability.
- **Reference:** [ctem_ops.md](references/ctem_ops.md)

### 4. **NIST CSF 2.0**
- **Use for:** Governance, "Trust Architecture," and overall risk management.
- **Reference:** [nist_csf_2.0.md](references/nist_csf_2.0.md)

## 🛠️ Mapping Example

1. **Identify** the asset (NIST CSF ID).
2. **Scope** the threat using CTEM (Scoping).
3. **Map** the technique to MITRE ATT&CK or ATLAS (e.g., Prompt Injection).
4. **Prioritize** based on live exploitability (CTEM Prioritization).
5. **Detect** using v18+ analytics (MITRE ATT&CK Detection).
