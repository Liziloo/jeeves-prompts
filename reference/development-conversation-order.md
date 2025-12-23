Canonical Order of Operations (Overlay-Centric Model)

This document defines the authoritative order in which prompts and inputs are introduced when conducting AI-assisted development conversations.

This system assumes that conversation-specific overlays are self-governing and internally complete.

1. Unified Behavior Prompt (Constitution) — FIRST

What is pasted

The Unified Behavior Prompt

Purpose

Establish global law before any intent, scope, or artifact is known.

Defines

Mode system

Ambiguity gate

Capability verification

Output minimization

Override semantics

Invariant

If this does not come first, all subsequent control is unreliable.

2. Overlay Selection (Human decision)

What happens

The human selects exactly one overlay appropriate to the task.

Examples:

Phase-level checklist generation

Project-wide checklist generation

Project-to-phase decomposition

Checklist-state audit

Checklist consumption & execution

This step is conceptual, not textual — it determines what is pasted next.

3. Conversation-Specific Overlay (Pasted verbatim)

What is pasted

One complete overlay document, unmodified

Purpose

Define the entire operational envelope for the conversation.

Each overlay already contains:

Scope declaration

Active modes

Hard rules

Required inputs

Internal protocol

Confirmation gates

Invariant

Only one overlay may be active.

Overlays do not restate constitutional rules.

If an overlay omits an Active Modes declaration, the Unified Behavior Prompt’s default mode applies.

4. Required Inputs for That Overlay (User-provided)

What is provided

Exactly — and only — the inputs listed in the overlay’s
REQUIRED INPUTS section.

Examples:

Phase charter + minimal architecture context

Authoritative checklist + project state

Locked checklist + codebase reference

Rule

If a required input is missing, the assistant must ask one clarifying question and stop (as defined by the overlay).

5. Overlay-Governed Interaction

From this point on:

The overlay governs everything

No external “steps” are injected

No implicit transitions occur

Depending on overlay type:

Planning overlays → produce governance artifacts

Audit overlays → classify only

Execution overlays → stepwise GO/WAIT execution

6. Overlay-Defined Closure

The conversation ends according to the overlay’s own rules:

Confirmation gate

Explicit WAIT token

Closure summary

No continuation is implied.