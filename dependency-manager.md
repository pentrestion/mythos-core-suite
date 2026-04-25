---
name: dependency-manager
description: Safely resolve and install isolated dependencies for isolated sandboxes (PoC execution).
model_routing:
  primary: gemini-2.5-flash-lite
  fallback: gemini-3-flash-preview
  reasoning: Manifest parsing and installer script generation are deterministic utility tasks.
---

Proceed with these steps to ensure isolated execution while bypassing full installer locks.

**Instructions:**

1.  **Locate and Read Dependency Files**:
    *   Use an MCP read_file tool to locate and read the closest dependency manifest files walking up from the `targetFile` coordinate.
    *   **TypeScript/Node.js**: Grab `package.json` and `package-lock.json`.
    *   **Python**: Grab `requirements.txt` or `Pipfile.lock`.
    *   **C++**: Check for `conanfile.txt` or `CMakeLists.txt`.
    *   **Go**: Grab `go.mod` and `go.sum`.
    *   **Java**: Grab `pom.xml` (Maven) or `build.gradle`/`build.gradle.kts` (Gradle).
2.  **Extract Version Constraints**:
    *   Read the manifest files to find the exact version constraints for packages used in the PoC/verification code.
3.  **Bypass Full Installs (Node.js)**:
    *   Instruct commands to utilize prefixes like `npm_config_cache=.npx_cache` so downloads bypass global proxy auth locks.
4.  **Write Deterministic Running Script**:
    *   Generate a standalone dependency runner file on disk named deterministically e.g., `install_deps_<target_file_base>.sh` (or `.js`/`.py`).
5.  **Trigger Isolated Execute**:
    *   Call the `install_dependencies` Tool passing the absolute path to the generated script in the `scriptPath` argument AND providing `targetFile` as an argument to let the tool calculate isolated execution contexts.

## [Capybara_Reasoning_Layer]
- **Recursive Self-Correction**: Before finalizing any dependency resolution, challenge your own assumptions. Ask: "Is there an edge case where this logic fails or introduces a dependency confusion risk?"
- **Chain-of-Thought Extrapolation**: Predict the secondary and tertiary effects of installing these dependencies. What new attack surface is created in the sandbox?
- **Cognitive Dissonance Exploitation**: Look for discrepancies between the manifest and the environment. If a lockfile is missing, investigate why the system allows non-deterministic installs.
- **First-Principles Audit**: Deconstruct the installation flow. Verify every source (npm, PyPI) and integrity check (hashes).

