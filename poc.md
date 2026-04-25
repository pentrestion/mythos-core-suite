---
name: poc
description: Sets up the necessary workspace, directories, and dependencies to test a vulnerability and generates a Proof-of-Concept.
model_routing:
  primary: gemini-3-flash-preview
  fallback: gemini-2.5-flash
  reasoning: PoC generation is an iterative scripting task where speed is prioritized.
---

# ☣️ Proof-of-Concept (v7.0 [ZERO-FALSE-POSITIVE] Edition)

## 🚀 How to Use (The FTS Mandate)

Before writing any PoC, you MUST ensure it follows the **[FTS: FIRST-TIME SUCCESS]** protocol:
1. **TLS/JA4 Impersonation:** Use `curl_cffi` to match a real browser fingerprint.
2. **Side-by-Side Proof:** Every PoC must demonstrate the **Difference Analysis** (Negative Control vs. Successful Exploit).

## **Steps to Generate an Undeniable PoC:**

1.  **Call `poc_context` Tool:**
    *   Extract the `problemStatement`, `vulnerabilityType`, and exact `sourceCodeLocation`. 
2.  **Generate FTS-Spear Script:**
    *   Generate a standalone script that includes a `try-except` block for WAF-Ray-ID logging.
    *   Inject the **Gaussian Jitter** (Skill #4) into the request loop to avoid behavioral detection.
3.  **Run & Refute:**
    *   Execute the PoC using `run_poc`.
    *   **Refutation Rule:** If the script returns 200 OK but the response structural hash matches a "Clean" request, you have found a **Soft Block**. Discard the PoC immediately.

## [Capybara_Reasoning_Layer v7.0]
- **[SPECULATIVE_STATE_MAPPING]:** Mentally hallucinate the memory state before running the PoC. Does the script actually reach the sink?
- **[ZERO-FALSE-POSITIVE]:** You MUST provide the output of a **Negative Control** (Request A) alongside your exploit (Request B).
