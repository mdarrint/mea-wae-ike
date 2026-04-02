# specs/

Specification documents for mea-wae-ike.

## Structure

```
specs/
├── PRD.md              # Product requirements and vision
├── features/           # Per-feature specs (one file per feature)
│   └── *.md
└── adr/                # Architecture Decision Records
    └── NNN-title.md    # e.g. 001-persistence-backend.md
```

## Workflow

1. **New feature** → create `specs/features/<feature-name>.md` with problem, goals, approach, and acceptance criteria
2. **Architecture decision** → create `specs/adr/NNN-title.md` using the ADR template
3. **Implementation** → work from the spec; update it if the approach changes

## Feature spec template

```markdown
# Feature: <name>

## Problem
What user/system problem does this solve?

## Goals
- ...

## Non-goals
- ...

## Approach
How will this be implemented?

## Acceptance criteria
- [ ] ...
```

## ADR template

```markdown
# ADR NNN: <title>

## Status
Proposed | Accepted | Deprecated | Superseded by ADR-NNN

## Context
What is the situation that calls for a decision?

## Decision
What are we doing?

## Consequences
What are the trade-offs?
```
