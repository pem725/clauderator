# Clauderator

This project contains the **clauderator** skill - a phase-gated task execution protocol.

## Active Skills

- **clauderator** (`/clauderator`) - Enforces deliberate execution through 4 phases: clarifying questions, proposing approach, reviewing alignment, and presenting a final plan before acting.

## When to Use

Invoke `/clauderator` before any non-trivial task to ensure alignment before execution. Particularly useful for:

- Feature implementations with multiple valid approaches
- Refactoring where scope could creep
- Tasks where requirements feel ambiguous
- Anything that would be painful to redo

## Default Behavior

When working in this directory, Claude should default to the clauderator protocol for substantive tasks. For quick fixes or single-line changes, the protocol can be skipped.
