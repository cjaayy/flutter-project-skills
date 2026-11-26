---
name: phase-planner
description: Break complex features or refactors into small, sequential, verifiable phases before writing code. Use when building new modules, multi-file features, or system migrations.
---

# Phase Planner

## Workflow
1. **Map Scope First:** List the exact files, database tables, and endpoints affected before editing anything.
2. **Split Into Sequential Phases:** Group changes into small, testable milestones (e.g., Phase 1: Schema and Types, Phase 2: Backend Logic, Phase 3: UI Integration).
3. **Complete Before Advancing:** Finish and verify the current phase cleanly before moving to the next phase.
4. **Keep Context Light:** Focus only on files relevant to the active phase.
