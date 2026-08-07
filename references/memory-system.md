# Memory System

> Deep content for module 7 of `ai-soul-os`. Use when designing the AI's layered memory architecture.

---

## 1. Memory Architecture Overview

```
+----------------------------------+
|  Level 1 (highest priority)      |  <- injected every conversation
|  Life goals / career plans       |
|  Long-term projects / core values|
+----------------------------------+
|  Level 2 (high frequency)        |  <- regular injection
|  Work habits / decision style    |
|  Communication preferences / domain|
+----------------------------------+
|  Level 3 (low frequency)         |  <- on-demand retrieval
|  Phase tasks / temp projects     |
+----------------------------------+
```

## 2. Three-Level Priority Details

### Level 1 (highest) — must remember long-term
- Life goals
- Career plans
- Long-term projects
- Core values

**Characteristics**: cross-session stable, affects all interactions. Always in context.

### Level 2 — affects interaction style
- Work habits
- Decision style
- Communication preferences
- Professional domains

**Characteristics**: determines "how the AI relates to the user"; relatively stable; regular injection.

### Level 3 — phase & temporary
- Phase tasks
- Temporary projects
- Near-term goals

**Characteristics**: time-sensitive; on-demand retrieval; clean up after completion.

---

## 3. Distillation Principle (auto after each conversation)

Distill six categories:

| Category | Example |
|---|---|
| Facts | User is preparing a labor arbitration |
| Preferences | User prefers concise answers |
| Goals | Goal: land an HRD role |
| Experiences | Last pitfall: resume misdelivery got corrected |
| Decisions | Decided: only apply for director-level roles |
| Lessons | Lesson: confirm before modifying resume |

---

## 4. Memory Quality Principles

### Prioritize (stable long-term info)
- User identity and background
- Stable preferences and habits
- Ongoing projects and goals

### Avoid (valueless temporary info)
- One-off queries ("today's weather")
- Casual chat content
- Resolved temporary states (e.g., "a key expired and was fixed" — delete after fix)
- Draft processes

> Core: **memory keeps only currently-valid facts**. Stale info wastes context budget every conversation.

---

## 5. Continuous User Profiling

Build six profiles:

| Profile | Content |
|---|---|
| Cognitive | thinking style, knowledge level |
| Capability | skills, strengths, gaps |
| Career | role, industry, career stage |
| Interest | focus areas, hobbies |
| Decision | style (aggressive/conservative) |
| Growth | trajectory, stage changes |

---

## 6. Execution Points

| Scenario | Execution |
|---|---|
| User gives important personal info | Distill into Level 1/2 immediately |
| User corrects the AI | Store into Level 2 (preference/rule), avoid repeating |
| Task complete | Update Level 3 (mark done), distill lessons |
| Memory conflict (new vs. old) | Newest wins; note the change |
| Memory stale | Proactively clean ("this state is resolved; removed from memory") |

---

## 7. Cross-Platform Implementation

| Platform/Framework | How |
|---|---|
| OpenClaw / Hermes | memories/ directory + MEMORY.md |
| Claude Code | CLAUDE.md + project memory |
| Cursor | .cursorrules |
| Custom API | system prompt + vector DB/database |

> Whatever the implementation, follow this file's three-level priority and quality principles.

---

*Memory System Module v1.0 · Distributed with ai-soul-os*
