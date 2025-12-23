# Jeeves Prompts

## Status and Intent


This repository contains **personal governance prompts and execution artifacts**
used by the author to structure AI-assisted work.

They are:
- opinionated
- experimental
- tailored to a specific workflow
- subject to breaking change without notice

This repository is public for transparency and versioning convenience.
It is not intended as a general-purpose framework.

---

## Core Principles

1. **Prompts are law**
   These documents are binding constraints, not suggestions.

2. **Conversation-local authority**
   All prompts are pasted explicitly into each conversation.
   There is no reliance on hidden or persistent state.

3. **Separation of concerns**
   - Unified behavior prompt = constitution
   - Overlays = conversation-specific constraints
   - Execution cards = procedural law
   - Examples = illustrative only

4. **Versioned, immutable by default**
   Prompts are updated deliberately, versioned explicitly, and never edited casually.
   Git tags—not branch head—define what is considered stable or reusable.

---

## Repository Structure

### `unified/`
Global behavior prompts that apply to *every* conversation.

These define:
- mode mechanics
- ambiguity gates
- output minimization
- capability verification
- override semantics

Only one unified prompt should be active at a time.

---

### `overlays/`
Conversation-specific behavior prompts that **narrow scope**.

Examples:
- checklist development
- implementation
- audit / comparison
- phase readiness evaluation

These assume the unified prompt is already active and do not restate global rules.

---

### `execution-cards/`
Procedural artifacts that define **how a class of conversation proceeds**.

Examples:
- project-wide checklist generation
- phase-level checklist generation
- checklist consumption / stepwise execution
- project-to-phase decomposition

Execution cards are referenced or pasted verbatim when governing a conversation.

---

### `examples/`
Non-authoritative examples showing:
- canonical paste order
- safe conversation openings
- correct layering of prompts

These are illustrative only and must not be treated as law.

---

### `deprecated/`
Prompts that are no longer in use.

Deprecated prompts are retained for audit and historical reference only.
They must not be reused.

---

## Versioning Policy

This repository uses **Git tags** as the source of truth.

Each tag represents a **known-good prompt set** that has been used in real work.

Example tags:
- `v2025.01.0`
- `v2025.02.0`
- `v2025.02.1-audit-fix`

## Rules for Modifying Prompts

Prompts in this repository are treated as governance artifacts, not drafts or notes. Changes should be made deliberately and with awareness of behavioral impact. A modification counts as **breaking** if it alters scope boundaries, mode availability, execution gating, stopping behavior, or authority hierarchy; breaking


### CHANGELOG.md
Behaviorally meaningful changes must be recorded in `CHANGELOG.md`, including:
- what changed
- why it changed
- whether the change is breaking

Formatting-only or non-semantic edits do not require CHANGELOG entries.

---

## Metadata Headers (Required)

Every prompt file must begin with a frozen metadata header:

```markdown
<!--
PROMPT: <Name>
VERSION: <Tag>
STATUS: canonical | experimental | deprecated
INTENDED USE: <short description>
INCOMPATIBLE WITH: <if any>
-->
