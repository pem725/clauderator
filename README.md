# Clauderator

**Phase-gated task execution for Claude Code** - Stop executing before you understand.

## What is Clauderator?

Clauderator is a [Claude Code skill](https://docs.anthropic.com/en/docs/claude-code) that enforces deliberate execution through a 4-phase protocol. It prevents wasted effort from misunderstood requirements or misaligned approaches by forcing deliberation before action.

## The 4 Phases

| Phase | Purpose |
|-------|---------|
| **1. Clarifying Questions** | Understand scope, constraints, and success criteria before proposing anything |
| **2. Propose Approach** | Present the strategy and key decisions for directional approval |
| **3. Review for Alignment** | Verify the plan actually solves the user's problem |
| **4. Final Plan** | Detail concrete steps with risks, then await explicit approval |

**Core Principle:** Never execute before alignment.

## Installation

Copy the skill to your Claude Code skills directory:

```bash
# Clone the repo
git clone https://github.com/pem725/clauderator.git

# Copy to your skills directory
cp -r clauderator ~/.claude/skills/
```

Or add directly to an existing skills folder:

```bash
cd ~/.claude/skills
git clone https://github.com/pem725/clauderator.git
```

## Usage

Invoke the skill in Claude Code:

```
/clauderator
```

Then describe your task. Claude will work through each phase, waiting for your approval before executing.

### Phase Shortcuts

- **"Skip questions, just propose"** - Jump to Phase 2
- **"I trust you, just show me the plan"** - Jump to Phase 4
- **"Just do it"** - Execute (with brief confirmation)

## Development Branches

This repo is collaboratively developed with experimental branches:

| Branch | Maintainer | Description |
|--------|------------|-------------|
| [`main`](https://github.com/pem725/clauderator/tree/main) | - | Stable, merged changes |
| [`patrick`](https://github.com/pem725/clauderator/tree/patrick) | [@pem725](https://github.com/pem725) | Patrick's working branch |
| [`sean`](https://github.com/pem725/clauderator/tree/sean) | [@NVSean](https://github.com/NVSean) | Sean's working branch |

## Why This Exists

Most wasted effort in AI-assisted development comes from:
- Misunderstanding what the user actually wants
- Solving an adjacent problem instead of the real one
- Over-engineering or under-delivering
- Making assumptions that weren't validated

Clauderator fixes this by making Claude pause, ask, propose, verify, and only then execute.

## Contributing

1. Fork the repo or work on your branch
2. Make changes following the skill format
3. Test with Claude Code
4. Open a PR to `main`

## License

MIT
