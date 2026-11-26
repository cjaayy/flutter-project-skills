# flutter-project-skills

Reusable AI coding agent skills (`.agents/skills/`) tailored for **Flutter + Dart** projects using **Supabase** and **Cloudflare R2**, enforcing minimalist monochrome UI, lean architecture, clean Git history, and fast surgical code edits.

Compatible with Antigravity, Cursor, Windsurf, Claude Code, Codex, and other agents supporting `.agents/skills/`.

---

## Copy Into a Flutter Project

Run from the **root of your target Flutter project**:

### Windows (PowerShell)

```powershell
git clone --depth 1 https://github.com/cjaayy/flutter-project-skills.git .tmp-skills
New-Item -ItemType Directory -Force -Path .agents/skills | Out-Null
Copy-Item -Path .tmp-skills/.agents/skills/* -Destination .agents/skills -Recurse -Force
Remove-Item -Path .tmp-skills -Recurse -Force
```

### macOS / Linux / Git Bash

```bash
git clone --depth 1 https://github.com/cjaayy/flutter-project-skills.git .tmp-skills && \
mkdir -p .agents/skills && \
cp -R .tmp-skills/.agents/skills/. .agents/skills/ && \
rm -rf .tmp-skills
```

### Manual Copy

1. Clone or download this repository as a ZIP.
2. Copy the `.agents` folder into the root directory of your Flutter project:

```text
your_flutter_app/
├── .agents/
│   └── skills/
│       ├── api-contract-validator/SKILL.md
│       ├── db-schema-rls/SKILL.md
│       ├── fast-iteration/SKILL.md
│       ├── git-ship-clean/SKILL.md
│       ├── lean-architecture/SKILL.md
│       ├── minimalist-ui/SKILL.md
│       ├── phase-planner/SKILL.md
│       ├── ponytail/SKILL.md
│       ├── project-conventions/SKILL.md
│       ├── root-cause-debugger/SKILL.md
│       └── security-hygiene/SKILL.md
├── lib/
└── pubspec.yaml
```

> **Copy a single skill only:** Copy just `.agents/skills/<skill-name>` into `your_flutter_app/.agents/skills/<skill-name>`.

---

## How to Use

1. **Automatic activation:** Once `.agents/skills/` is in your workspace root, your AI assistant automatically detects and applies the relevant skill based on your prompt (e.g., creating a screen activates `minimalist-ui` and `project-conventions`; fixing an error activates `root-cause-debugger`).
2. **Explicit trigger in chat:** Reference any skill by name or keyword in your prompt:
   - `"Use phase-planner to break down the authentication flow."`
   - `"ponytail: fix the bottom overflow on the profile card."`
   - `"Check my staged changes with git-ship-clean."`
3. **Customize for your app:** Edit `.agents/skills/project-conventions/SKILL.md` or `.agents/skills/minimalist-ui/SKILL.md` if a project uses a different backend or theme palette.

---

## Included Skills

| Skill | Purpose |
| :--- | :--- |
| `project-conventions` | Enforces Flutter + Dart stack (Supabase, Cloudflare R2), feature-first structure, and `snake_case` naming. |
| `minimalist-ui` | Monochrome grey minimalist Flutter UI, Iconoir bare grey icons, maroon-red destructive actions, and overflow-free mobile layouts. |
| `ponytail` | Minimalist senior-dev mode (`lite`, `full`, `ultra`) for the smallest working change and concise replies. |
| `fast-iteration` | Keeps code edits surgical, targeted, and fast during active development. |
| `phase-planner` | Breaks multi-file features and refactors into small, sequential, verifiable phases. |
| `lean-architecture` | Designs lean, zero/low-cost schemas, API routes, and serverless deployments. |
| `db-schema-rls` | Enforces clean database schemas, indexed query patterns, and strict Row-Level Security (RLS). |
| `api-contract-validator` | Enforces strict input validation, predictable response shapes, and clean error handling. |
| `security-hygiene` | Prevents leaked secrets, injection flaws, and exposed endpoints. |
| `root-cause-debugger` | Diagnoses and fixes bugs at their exact root cause without band-aid patches. |
| `git-ship-clean` | Keeps commits atomic, conventional (`feat:`, `fix:`, `docs:`), and free of debug leftovers or secrets. |
