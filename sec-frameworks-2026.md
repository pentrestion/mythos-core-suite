---
name: sec-frameworks-2026
description: Integrated 2026 cybersecurity frameworks (MITRE ATT&CK v18+, MITRE ATLAS, CTEM, NIST CSF 2.0). Use for threat-informed defense, AI red teaming, and exposure management.
model_routing:
  primary: gemini-3-flash-preview
  fallback: gemini-2.5-flash
  reasoning: Framework mapping and CVE research benefit from Flash tier's speed and web-search efficiency.
---

# 🛡️ Security Frameworks 2026 (v7.0 [JIT-INTEL] Edition)

## 🚀 How to Use (Mandatory v7.0 Intel Pulse)

Before applying any framework mapping, you MUST execute a **[WAF_PULSE]** and **[PATCH-GAP]** intel search:
1. **WAF_PULSE:** Search for "Cloudflare/Akamai rule updates April 2026" to ensure your technique isn't already dead.
2. **PATCH-GAP:** Search for "GitHub issues fixed but not released" for the target version to identify zero-day-adjacent vulnerabilities.

### 1. **MITRE ATT&CK v18+**
- **Use for:** Mapping traditional tradecraft (e.g., T1190 - Exploit Public-Facing Application).
- **v7.0 Rule:** Map the finding to the exact sub-technique but discard if it's just "Recon Noise."

### 2. **MITRE ATLAS**
- **Use for:** Red teaming AI systems. 
- **v7.0 Rule:** Prioritize "Adversarial Traffic Injection" (Skill #4) over basic prompt injections.

### 3. **CTEM (Continuous Threat Exposure Management)**
- **v7.0 Rule:** Prioritize findings by live exploitability. No [ZERO-FALSE-POSITIVE] confirmation = No CTEM ranking.

### 4. **NIST CSF 2.0**
- **v7.0 Rule:** Focus on "Trust Architecture" gaps (Sidecar/Service Mesh exploitation).

## [Capybara_Reasoning_Layer v7.0]
- **[DIFF-REGRESSION_PROTOCOL]:** Analyze the framework's history. Did a change in the standard (e.g., NIST CSF 2.0 update) expose a new gap in the target's compliance logic?
- **[ZERO-FALSE-POSITIVE]:** Never map a finding to a framework until you have performed the **Difference Analysis** (Request A/B).
