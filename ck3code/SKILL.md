---
name: ck3code
description: Use when writing, editing, or reviewing CK3 mod scripts (Jomini), especially for event/decision/interaction logic, scope handling, trigger/effect correctness, script-level bug fixes, and AI-coded CK3 mod implementation.
---

# CK3 Script Coding

## Goal

For CK3 scripting tasks, produce Jomini/Clausewitz code that is runnable, verifiable, compatible, and maintainable.

## When To Use

Enable this skill for:

- Writing or modifying CK3 events, decisions, interactions, traits, modifiers, scripted triggers/effects/values, on_actions, localization-linked script, or scripted GUI.
- Fixing script errors, invalid triggers, invalid effects, invalid fields, or scope issues.
- Reviewing existing CK3 scripts for correctness, compatibility, performance, and hidden logic risks.

## Standards Layer

For any non-trivial CK3 mod code task, also apply `ck3mod-coding-standards`.

At minimum, load its references when the task touches:

- vanilla extension or mod compatibility: `ck3mod-coding-standards/references/02_load_order_and_compatibility.md`
- scope-heavy code: `ck3mod-coding-standards/references/03_trigger_effect_scope.md`
- repeated logic or AI weights: `ck3mod-coding-standards/references/04_abstraction_state.md`
- event/decision/interaction/modifier/localization patterns: `ck3mod-coding-standards/references/05_ck3_content_patterns.md`
- GUI or scripted GUI: `ck3mod-coding-standards/references/06_gui_jomini.md`
- debugging or performance work: `ck3mod-coding-standards/references/07_debug_performance.md`

## Load Reference On Demand

Do not load all docs by default. Load only the minimum set required for the current task:

- `reference/rules.md`: CK3 quick guardrails and local rule index.
- `reference/script.md`: base syntax and block structure.
- `reference/scopes.md`: scope switching, `root/prev/this/scope:name`.
- `reference/effect.md`: effect statements.
- `reference/trigger.md`: trigger statements.
- `reference/variables.md`: variable statements.

If any field or syntax is uncertain, check reference or vanilla examples first. Do not guess from memory.

## Execution Flow

1. Identify task type: new feature, bug fix, review, compatibility patch, or refactor.
2. Identify file type and expected block type: trigger, effect, localization, GUI, or data.
3. Identify current scope and target scope.
4. Load the minimum required reference.
5. Produce actionable script or patch, not pseudocode.
6. Provide validation steps through console, log, Tiger, or in-game repro.

## Quality Bar

- Do not output guessed fields that only look like CK3 syntax.
- When scope is involved, explicitly state the current context.
- Clearly distinguish trigger checks from effect changes.
- Do not directly add `effect` to vanilla on_actions that already have vanilla `effect`; use a bridge hook.
- Do not rely on same-id event overwrite as a patching strategy.
- Keep expensive traversals out of hot GUI/AI paths unless justified.
- For bug fixes, provide root cause, fix point, and validation path.

## Output Standard

1. Conclusion: one sentence on change goal or root cause.
2. Context: current scope and affected file/block.
3. Script or patch: include required surrounding structure.
4. Validation: how to confirm it works or the error is gone.
5. Risk note: only when version, compatibility, or performance matters.

## Collaboration With Other Skills

- Need long-term coding standards or compatibility discipline: use `ck3mod-coding-standards`.
- Need authoritative mechanic/field confirmation: use `ck3reference`.
- Need tooling-based error diagnosis: use `ck3moddebug`.

