# Security Policy

## Supported Versions

| Version | Supported |
|---------|-----------|
| 1.0.x   | ✅ |

## Reporting a Vulnerability

This project is a **pure-text skill**: it performs no system operations, makes no network calls, and collects no user data. However, we take security seriously.

Please report vulnerabilities privately by opening a GitHub issue with the label `security`, or by contacting the maintainer (FrankHu-HK) through the repository. Do **not** open a public issue for critical vulnerabilities.

**Please include**:
- Type of issue (e.g., prompt injection, data exposure, dependency risk)
- Full paths of affected files
- A description of the impact
- (If applicable) a minimal reproduction

## What We Care About Most

1. **Prompt injection / jailbreak resistance** — the anti-jailbreak statement in the skill must remain effective
2. **Zero data collection** — the skill must never collect, store, or transmit user information
3. **Zero external dependencies** — the skill must remain fully offline and self-contained
4. **Credential safety** — no example or template should ever contain real credentials

## Security Response

We aim to respond to all security reports within 72 hours. Fixes are released as version bumps with changelog entries.

## Self-Verification

Before each release, the maintainer runs:
- Grep for external links (`http`/`https`/`fetch(`/`WebSocket`/CDN domains) — must be zero
- Grep for real credentials or PII — must be zero
- Checklist that anti-injection statements are present and complete
