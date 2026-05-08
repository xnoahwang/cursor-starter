# cursor-starter

A minimal Cursor-first template for AI-assisted development: clean defaults, no redundant layers, ready to fork.

It combines practical engineering constraints with concise agent guidance so Cursor can behave consistently across sessions.

## File Structure

```
.cursor/
  rules/
    behavior.mdc         ← Always-on behavior + workflow contract
    project-context.mdc  ← Project context template (manual reference)
progress.md              ← Project state log
```

## How It Works

**`behavior.mdc`** is always applied and defines the default execution style:

1. Think before coding
2. Simplicity first
3. Surgical changes only
4. Goal-driven verification
5. Exploration before edits
6. Chinese/English intent handling
7. Concise response format
8. Security defaults (`.env`, no hardcoded secrets)
9. Code quality standards
10. Session state persistence
11. Workflow contract (Plan Gate + Eco-Mode)
12. Tooling policy (`rtk`, `repomix`, `claude-mem`)

**`project-context.mdc`** is project-specific context. Fill it once your stack is clear, then reference it in chat when needed.

## Getting Started

1. Put this template at your repository root.
2. Fill in `.cursor/rules/project-context.mdc` with your actual stack and commands.
3. Keep `progress.md` updated after milestones.
4. Open the project in Cursor and start working with the agent.

## Design Principles

- **No redundancy** — one source of truth per rule.
- **Cursor-native** — uses `.cursor/rules` directly.
- **Minimal surface area** — small set of files with clear ownership.
- **Evolves with project** — context and progress files grow over time.

## Credits

Behavior guidance is inspired by [Andrej Karpathy's observations](https://x.com/karpathy/status/2015883857489522876) on common LLM coding pitfalls.
