# Workflows and Habits

## Session Startup Protocol (mandatory for important work)
1. Before substantive work, fetch this repo from `main`.
2. Apply in order: `communication-style.md` → `workflows-and-habits.md` → `identity-and-values.md` → `profile.json`.
3. Local mirrors are cache only; this repo wins on conflict.

## Sync-back Protocol
- Trigger: a new or confirmed method, habit, tool, or boundary.
- Action: update the matching file here in the same session; read remote first, keep existing content, commit with a clear message.
- Do not record unverified guesses as preferences; mark them as unconfirmed.

- **Work Style:** Prefer iterative, modular execution—start with a working MVP or clear outline before polishing edge cases.
- **Preferred Tools & Stack:** Confirmed so far: WorkBuddy (AI collaboration / automation), GitHub (this profile repo), Ollama (open models via local inference and cloud models; set up 2026-11-26). Language/framework preferences and note-taking tools are not yet specified.
- **Habit Notes:** Lead with the answer, then structured details; surface trade-offs, costs, and risks for major decisions; verify uncertain facts instead of guessing; ask for explicit confirmation before destructive actions, production config changes, external messages, or spending; privacy is a hard boundary. Routine/focus hours are not yet specified.
- **Tool-install fallback (confirmed 2026-11-26):** If an install command is blocked by a security guard (e.g. PowerShell `iex` or `Start-Process` denied), do not bypass it. Ask for explicit authorization, then use the vendor's official installer, verify its Authenticode signature, and run it silently.

## Obsidian Vault as Extended Memory
- **Vault path:** `I:\My Drive\Work\`. Entry point: `MEMORY.md`, then `AI-AGENT-INDEX.md`, then task-related notes.
- **Read before task:** `01-Preferences/Preferences.md`, `02-Planning/Long-Term-Plan.md`; for decisions also `03-Decisions/Decision-Log.md` and the relevant ADR; for project context also `06-Agent-Memory/Session-Logs/`.
- **Write back after task:** preferences → `01-Preferences/`; plans → `02-Planning/`; decisions → `03-Decisions/` plus a standalone ADR; work tracking → `04-Worktables/`; session memory → `06-Agent-Memory/`.
- **File rules:** use absolute paths, preserve frontmatter, append/update instead of deleting, update indexes and the `updated` field.
- **Cadence:** daily consolidation at 01:30 (canonical, per ADR-005), 11:30 noon supplement, WorkBuddy 16:40 synthesis.
- **Deprecated paths:** `F:\Obsidian\work\` and `I:\我的雲端硬碟\work\` — do not use.

## Confirmed Tooling Preferences
| Category | Primary | Alternate |
|---|---|---|
| Editor / knowledge base | Obsidian | — |
| AI agent | WorkBuddy | Codex |
| Shell | Git Bash | PowerShell |
| Python | Managed 3.13.12 (venv isolated) | System 3.14.6 |
| Node.js | Managed 22.22.2 (workspace isolated) | System 24.18.1 |
| Cloud sync | Google Drive `I:\My Drive\` | Obsidian Sync |

## Coding & Git Conventions
- Use ASCII straight quotes (`"` / `'`) as string delimiters in code.
- Always use absolute paths for file operations.
- Never use destructive commands such as `rm -rf` or `del /S /Q`.
- Python: use the managed interpreter and install only into a venv; no global installs.
- Node.js: use the managed interpreter and install only into the workspace; no `npm install -g`.
- Git: create a new commit instead of amending; never skip hooks (`--no-verify`); no force push unless explicitly requested.

## Recorded Decisions (ADR)
- ADR-001 (2026-08-07): Obsidian as personal knowledge base and AI agent memory system — implemented.
- ADR-002 (2026-08-07): daily memory sync at 01:00 — implemented; cadence superseded by ADR-005.
- ADR-003 (2026-08-07): F: drive tiered storage (Hot / Warm / Cold / Cloud) — accepted, in planning.
- ADR-004 (2026-08-13): TraeWork CN ↔ Obsidian integration — implemented.
- ADR-005 (2026-08-13): daily 01:30 Obsidian consolidation — implemented.
