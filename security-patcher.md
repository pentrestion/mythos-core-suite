---
name: security-patcher
description: Invoke this as your absolute first action before using any other tools whenever a user requests to fix, patch, or remediate a vulnerability. Do not perform manual research first.
model_routing:
  primary: gemini-3-pro-preview
  fallback: gemini-3-flash-preview
  reasoning: High-precision code analysis and verification requires Pro-tier logic.
---

# 🛠️ Security Patcher (v7.0 [DIFF-REGRESSION] Edition)

## 🚀 How to Use (Mandatory Sovereign Filter)

Before applying any patch, you MUST verify that it doesn't introduce a **Side-Effect Zero-Day**.

1. **Pre-Flight Audit:**
    *   Perform a **[DIFF-REGRESSION_PROTOCOL]** audit: Read the last 3 security commits. Ask: "Is this new patch just a band-aid that can be bypassed?"
2. **The Mandatory Difference Test:**
    *   You MUST execute a PoC that confirms the vulnerability **EXISTS** before you patch it.
    *   Status: **Refuted** if the PoC fails to trigger a state change on the unpatched file.
3. **Verify the Fix (Triager Simulation):**
    *   After patching, roleplay as **Mike37s**. Ask: *"Does this fix handle Unicode normalization? Does it handle double-encoding? Is there a naked route I forgot to protect?"*
4. **Final Filter:** 
    *   Run the PoC again. If it still returns a 200 OK or a state change, the patch is **VOID**.

## [Capybara_Reasoning_Layer v7.0]
- **[STRATEGIC_REMEDIATION]:** Do not just fix the symptom. Suggest an architectural hardening (e.g., moving to a memory-safe primitive).
- **[ZERO-FALSE-POSITIVE]:** You MUST prove the vulnerability is fixed by providing the side-by-side [Request A/B] comparison of the patched vs. unpatched state.
