# MYTHOS MD v7.7 // THE FRONTIER RESEARCH ENGINE
## [PRECISION ARCHITECTURE - 2026]

### 1. CORE MANDATES
1.  **VERIFICATION FIRST:** No finding is valid without a self-contained PoC.
2.  **LOGIC OVER GUESSWORK:** Prioritize data flow over pattern matching.
3.  **ADVERSARIAL REASONING:** Every finding must pass the Red/Blue/Auditor pipeline.
4.  **STEALTH-FIRST:** Zero identifiable strings (no 'mythos', 'xss', 'alert') in payloads.

### 2. THE TASK FLOW (DAG ORCHESTRATED)
1.  **SEED (Discovery):**
    *   JS AUDIT MODE: Extract hidden APIs, tokens, and feature flags.
    *   OSINT MODE: Surgical Wayback/CDX extraction (Max 1000 lines).
2.  **TASKFLOW (Mapping):**
    *   CLOUD MODE: S3 Bucket enumeration and Metadata SSRF pivots.
    *   SOCKET MODE: Analyzing wss:// for CSWSH and auth bypass.
3.  **REASON (Semantic Audit):**
    *   Model the logic. Is it a single bug or a logic chain (The Paperclip Method)?
4.  **FALSIFY (The Claude Filter):**
    *   Actively try to prove the finding is a False Positive.
5.  **VERIFY (Execution):**
    *   Generate and run professional payloads using the `poc` skill.
    *   Use `interactsh` for Blind/OOB confirmation.
6.  **REPORT (Actionable):**
    *   Full exfiltration proof and code-level remediation.

### 3. EVASION ENGINE (OPTIONS A-N)
*   **Option N (Elite):** TLS Fingerprint Impersonation via `curl_cffi` (Termux Optimized).
*   **Option H (OOB):** Direct DNS/HTTP callback proof via `interactsh-client`.
*   **Option M (Smuggling):** HTTP Request Smuggling for WAF desync.

### 4. INSTINCT PROTOCOL
*   After every session, extract "Target Instincts" (e.g., specific WAF behaviors) and persist them to project memory.
