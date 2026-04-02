## Summary
- Add `xy-ai-ui` skill for desktop UI/UX and task-flow standards.

## Skill Location
- `skills/xy-ai-ui`

## Why This Skill
- Helps enforce consistent desktop UI implementation quality.
- Standardizes interaction safety for destructive and long-running operations.
- Provides concise Windows 11 visual guidance for modern desktop feel.

## Checklist
- [ ] `SKILL.md` has valid frontmatter (`name`, `description`, `license`)
- [ ] Trigger conditions are clear
- [ ] Rules are actionable and non-conflicting
- [ ] README and license included
- [ ] Installation tested via official installer script

## Test Evidence
Include command/output used for installer verification:
```bash
python "$CODEX_HOME/skills/.system/skill-installer/scripts/install-skill-from-github.py" \
  --repo <owner>/<repo> \
  --path skills/xy-ai-ui \
  --ref main
```

