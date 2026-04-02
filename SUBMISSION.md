# xy-ai-ui Submission Pack

This repository is prepared for submitting `xy-ai-ui` to the public skills catalog workflow.

## Skill Path
- `skills/xy-ai-ui`

## What This Skill Solves
- Standardizes desktop UI/UX implementation and interaction flows.
- Emphasizes visual consistency, alignment symmetry, and predictable task-state behavior.
- Provides Windows 11 style guidance (Mica/Acrylic, Segoe UI, blue-neutral palette, smooth motion).

## Scope
- Primary: Electron desktop apps.
- Secondary: desktop webview-style apps with similar architecture.

## Quality Checklist
- [x] Frontmatter exists in `SKILL.md` (`name`, `description`, `metadata.short-description`, `license`)
- [x] `README.md` exists under `skills/xy-ai-ui`
- [x] `LICENSE.txt` exists under `skills/xy-ai-ui`
- [x] Trigger conditions are explicit
- [x] Non-goals and boundaries are explicit
- [x] Actionable checklist included
- [x] Examples included in `skills/xy-ai-ui/EXAMPLES.md`

## Install Test (Official Installer)
```bash
python "$CODEX_HOME/skills/.system/skill-installer/scripts/install-skill-from-github.py" \
  --repo lishengxuan212-code/LSX-AI-Skill- \
  --path skills/xy-ai-ui \
  --ref main
```

Expected output:
- `Installed xy-ai-ui to <CODEX_HOME>/skills/xy-ai-ui`

## Suggested Upstream PR Target
- `openai/skills`
- likely path: `skills/.curated/xy-ai-ui` (or maintainer-requested location)

