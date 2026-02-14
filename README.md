# Project Name

<!-- TODO: Replace with your project name and description -->

> A project bootstrapped with the compound engineering template — AI-assisted development with compounding returns.

## What This Template Provides

This template gives you the documentation hierarchy, agent templates, hook configuration, and documentation structure to practice compound engineering from day one. It works alongside two Claude Code plugins:

- **[compound-engineering](https://github.com/augmented-dev/compound-engineering)** — Core hooks (format-on-edit, emoji commits, session cleanup) and skills (compound-review, session-summary, consolidate-memory)
- **[superpowers](https://github.com/anthropics/claude-code-superpowers)** — General-purpose skills (new-doc, update-docs, pr, commit)

The template is **stack-agnostic**. It uses TODO stubs throughout where you fill in project-specific content (your commands, your architecture, your coding standards).

## Prerequisites

1. [Claude Code](https://docs.anthropic.com/en/docs/claude-code) installed and configured
2. Install the compound-engineering plugin:
   ```bash
   claude plugin add compound-engineering
   ```
3. Install the superpowers plugin:
   ```bash
   claude plugin add superpowers
   ```

## Quick Start

### 1. Use this template

Click "Use this template" on GitHub, or clone and reinitialize:

```bash
git clone <this-repo-url> my-project
cd my-project
rm -rf .git && git init
```

### 2. Fill in CLAUDE.md

Open `CLAUDE.md` and replace the TODO stubs with your project's details:

- Project overview (2-3 sentences)
- Development commands (`npm run test`, `make build`, etc.)
- Project structure (directory map)
- Naming conventions
- Architecture patterns
- Testing requirements

### 3. Configure .compound.json

Edit `.compound.json` to match your stack:

- Update the Prettier rule's file extensions for your language
- Enable `autoTest` if you want tests to run automatically after edits
- Set `baseBranch` to your default branch name

### 4. Customize agent templates

Edit the agents in `.claude/agents/`:

- **debug-detective.md**: Fill in your platform's query commands, log locations, and config mechanisms
- **code-reviewer.md**: Fill in your coding standards, linting rules, and red flags

### 5. Set up CLAUDE.local.md

Copy the example and fill in your personal details:

```bash
cp CLAUDE.local.md.example CLAUDE.local.md
```

This file is gitignored — it's for your personal environment details and workflow preferences.

### 6. Start coding

That's it. The system improves as you use it:

- Hooks enforce formatting and linting automatically
- `/session-summary` captures learnings after each session
- `/consolidate-memory` promotes patterns to permanent docs weekly
- `/compound-review` provides multi-perspective code reviews

## Directory Structure

```
.
+-- CLAUDE.md                          # Universal project rules (customize this)
+-- CLAUDE.local.md.example            # Personal preferences template
+-- .compound.json                     # Hook and review configuration
+-- .gitignore
+-- LICENSE
+-- README.md
+-- .claude/
|   +-- agents/
|   |   +-- README.md                  # Guide to creating agents
|   |   +-- debug-detective.md         # Debugging agent template
|   |   +-- code-reviewer.md           # Code review agent template
|   +-- hooks/
|   |   +-- README.md                  # Guide to hooks
|   +-- skills/
|   |   +-- README.md                  # Guide to creating skills
|   +-- sessions/
|       +-- .gitkeep                   # Session summaries (gitignored)
+-- docs/
    +-- INDEX.md                       # Central documentation registry
    +-- compound-engineering-guide.md  # System philosophy and usage
    +-- architecture/
    |   +-- .gitkeep
    +-- plans/
    |   +-- WorkingMemory.md           # Human to-do list (gitignored)
    +-- reference/
    |   +-- known-gotchas.md           # Platform pitfalls
    +-- strategic/
        +-- .gitkeep
```

## Philosophy

Compound engineering makes every development cycle leave the codebase — and the tools around it — better than you found it. Small investments after each session accumulate into a powerful, self-improving development system.

Read the full philosophy in [docs/compound-engineering-guide.md](docs/compound-engineering-guide.md).

## Customization Guides

- [Agent creation and customization](.claude/agents/README.md)
- [Hook configuration and philosophy](.claude/hooks/README.md)
- [Skill authoring and best practices](.claude/skills/README.md)

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/my-improvement`)
3. Commit your changes using the emoji + conventional commit format
4. Push to the branch (`git push origin feature/my-improvement`)
5. Open a Pull Request

## License

[MIT](LICENSE)
