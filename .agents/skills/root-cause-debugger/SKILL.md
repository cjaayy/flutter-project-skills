---
name: root-cause-debugger
description: Diagnose and fix bugs at their exact root cause without guesswork or band-aid patches. Use when troubleshooting runtime errors, failed builds, broken UI states, or API failures.
---

# Root-Cause Debugger

## Diagnostic Steps
1. **Reproduce & Isolate:** Identify the exact input, state, or environment condition triggering the failure.
2. **Trace Data Flow:** Follow the execution path from entry point (UI event or request) through state/logic down to the database or external call.
3. **Fix the Source:** Patch the underlying defect directly. Do not mask errors with empty try/catch blocks or arbitrary timeouts.
4. **Verify Side Effects:** Confirm the fix resolves the issue without breaking adjacent flows.
