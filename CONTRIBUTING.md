# Contributing to AI Soul Operating System

Thank you for your interest in contributing! This project aims to turn any AI agent into a J.A.R.V.I.S-class cognitive partner. Contributions of all kinds are welcome.

## Ways to Contribute

### 🐛 Report Bugs
- Open an [issue](https://github.com/FrankHu-HK/ai-soul-os/issues) with:
  - A clear title and description
  - Steps to reproduce (if applicable)
  - Expected vs. actual behavior

### 💡 Suggest Improvements
- Open an issue with the `enhancement` label
- Describe the use case, not just the feature ("I want X" is weaker than "I need X for Y scenario")

### ✏️ Improve Documentation
- Fix typos, clarify wording, add examples
- Add translations (Chinese/English parity is a project goal)

### 🧩 Add New Modules
- New soul modules (e.g., a "Negotiation" expert mode) are welcome
- Follow the progressive-disclosure pattern: main `SKILL.md` = navigation only; density goes into `references/`
- Keep the TRACE-aligned design: Trust, Reliability, Adaptability, Convention, Effectiveness

## Development Workflow

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/your-feature`
3. Make your changes
4. Verify:
   - Main document stays lean (navigation + quick reference only)
   - New depth content lives in `references/`
   - Changelog entry added (never mention score changes)
   - Version bumped for behavior changes
5. Commit with a clear message
6. Open a Pull Request

## Style Guidelines

- **Language**: English for this repository (the SkillHub release is Chinese — keep both in sync)
- **Format**: Markdown, tables for structured comparisons, code blocks for templates
- **Tone**: Precise, actionable, no fluff — matching the soul framework's own communication principles

## Code of Conduct

Please review and follow our [Code of Conduct](CODE_OF_CONDUCT.md).

## Questions?

Open an issue or reach out via the repository. We're happy to help you get started.
