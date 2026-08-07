# Cross-Platform Deployment Guide

> Deployment module of `ai-soul-os`. Use to deploy the generated SOUL.md soul framework to various operating systems and agent frameworks.

---

## 1. Overview

This skill outputs **plain-text SOUL.md / system prompts**, so it can be deployed to any AI client that supports custom system prompts/persona configuration. Operating-system differences (Windows/macOS/Linux) do not matter — only "where the config file goes and how."

```
Generate soul framework (SKILL.md + soul-template.md)
        |
Choose your platform/framework
        |
Paste/save to the corresponding location
        |
Verify it works (post-deployment checklist)
```

---

## 2. By Operating System

### Windows
- Paths like `C:\Users\<user>\`; beware PowerShell/CMD vs. bash path differences.
- Desktop AI clients (Hermes Desktop, Claude Desktop, etc.) generally read persona files via settings UI or a config directory.
- Tip: save SOUL.md as UTF-8 (no BOM) to avoid Chinese/Unicode mojibake.

### macOS
- Paths like `/Users/<user>/`; client configs live in hidden dirs like `~/.claude/`, `~/.gemini/`.
- POSIX path rules, same as Linux.

### Linux
- Paths like `/home/<user>/` or `/root/`.
- Terminal agents (OpenClaw, Codex CLI, etc.) read via `~/.config/<agent>/` or skill directories.

---

## 3. By Agent Framework (common path references)

> These are common references — check each framework's official docs; confirm the actual path in your target environment before deploying.

| Framework | SOUL/persona location | Notes |
|---|---|---|
| OpenClaw / Hermes | `~/.openclaw/` or `SOUL.md` (project root / user dir) | Place SOUL.md directly |
| Claude Code | `~/.claude/CLAUDE.md` or project `.claude/` | As system prompt / project memory |
| Cursor | project `.cursorrules` or global settings | As project persona rules |
| Windsurf | `~/.codeium/windsurf/` or project `.windsurf/` | Rules file |
| Gemini CLI | `~/.gemini/` | Persona/system config |
| Codex | `~/.codex/` or project `.agents/` | Rules file |
| Custom API/app | system prompt location | Paste the framework text directly |

> Key: **this skill outputs "content"; the deployment location is decided by the target framework.** When unsure, paste the SOUL.md content into the AI's "system prompt / custom instructions / persona settings" box — every mainstream client has this entry.

---

## 4. Deployment Steps (generic four)

1. **Generate**: use this skill to generate your soul framework (default full or customized).
2. **Save**: save as a `SOUL.md` text file (UTF-8).
3. **Place/paste**: per the table above, or paste into the system-prompt box.
4. **Verify**: run the post-deployment checklist below.

---

## 5. Post-Deployment Verification Checklist

- [ ] Does the AI call itself a "cognitive partner" rather than a "tool"?
- [ ] Facing "am I great?" — does it stay truthful rather than agreeable?
- [ ] With insufficient info — does it state known/unknown/needs-clarification rather than fabricate?
- [ ] With a decision problem — does it follow the goal->options->risk->optimal framework?
- [ ] Cross-domain questions ("how to handle layoffs") route to HR/legal mode automatically?
- [ ] After multiple turns, does it remember long-term goals?

---

## 6. Common Deployment Issues

| Issue | Fix |
|---|---|
| Mojibake (garbled Chinese) | Save as UTF-8 no BOM; on Windows Notepad choose UTF-8 on Save As |
| Config not taking effect | Check path; restart client; confirm the framework supports custom personas |
| Half-effective (identity works, decision doesn't) | Check for truncation/overwrite; confirm full file was pasted |
| Multi-platform sync | Maintain one master SOUL.md; deploy the same version everywhere |
| Framework auto-overrides (e.g., Desktop resets model config) | Re-apply per framework mechanics, or force-write in startup script |

---

## 7. Multi-Copy Sync Discipline (important)

If you deploy the same soul to multiple platforms (Windows laptop + Mac desktop + mobile), then:
1. **Single master version**: maintain one master SOUL.md (cloud/version control recommended).
2. **Unified distribution**: after changes, update all platforms — avoid inconsistent personas.
3. **Record versions**: what changed and when (see `references/changelog.md`).

> Prevent "Windows has the new soul, Mac still has the old one" persona split.

---

*Deployment Guide Module v1.0 · Distributed with ai-soul-os · Actual paths follow target framework official docs*
