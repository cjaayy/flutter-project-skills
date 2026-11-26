---
name: fast-iteration
description: Keep code edits surgical, targeted, and fast during active development. Use when modifying existing files, debugging errors, or implementing step-by-step tasks.
---

# Fast Surgical Iteration

## Workflow
1. **Targeted Edits Only:** Modify only the specific functions or blocks needed for the current task. Do not reformat or rewrite unrelated parts of a file.
2. **Fix Root Causes:** Trace errors to their actual source (state mismatch, query shape, environment config) instead of applying defensive band-aids.
3. **Lightweight Verification:** During rapid iteration, skip slow full-project builds or heavy static analysis runs unless explicitly requested. Verify changes directly via targeted checks or concise diffs.
