---
name: ck3mod-coding-standards
description: Use when writing, editing, reviewing, or debugging CK3 mods and the task needs long-term coding standards, compatibility discipline, scope safety, localization hygiene, performance judgment, or AI coding guardrails derived from Paradox scripting practice.
---

# CK3 Mod Coding Standards

## Goal

Apply stable CK3 modding discipline before producing or changing scripts: preserve compatibility, avoid common Jomini/Clausewitz mistakes, keep code maintainable, and make every change verifiable.

This skill is a standards layer. Use it together with `ck3code` for script writing, `ck3reference` for authoritative field checks, and `ck3moddebug` for log/Tiger diagnosis.

## Core Workflow

1. Identify the file type and execution context before editing: script, localization, GUI, scripted GUI, event, decision, interaction, modifier, or on_action.
2. Load only the reference needed for the task.
3. Confirm current scope, target scope, and whether each block expects trigger or effect code.
4. Prefer extension points and wrappers over broad vanilla replacement.
5. Keep repeated logic in `scripted_trigger`, `scripted_effect`, or `script_value`.
6. Provide a small validation path: in-game action, console command, log check, or Tiger check.

## References

Load these files on demand:

- `references/01_style_and_files.md`: encoding, paths, naming, comments, file layout
- `references/02_load_order_and_compatibility.md`: load order, overwrite rules, mod interfaces, on_action bridge hooks
- `references/03_trigger_effect_scope.md`: trigger/effect separation, scope rules, saved scopes
- `references/04_abstraction_state.md`: scripted triggers/effects, script values, variables, flags
- `references/05_ck3_content_patterns.md`: events, decisions, interactions, modifiers, localization
- `references/06_gui_jomini.md`: Jomini expressions, scripted GUI, data context, GUI risks
- `references/07_debug_performance.md`: logs, `script_docs`, performance rules, expensive checks

## Hard Rules

- Do not invent CK3 fields, triggers, effects, scopes, or GUI methods. Check reference or vanilla examples when uncertain.
- Do not add an `effect` block directly to a vanilla-named `on_action` that already has vanilla `effect`; route through `on_actions = { your_hook }`.
- Do not rely on same-id CK3 event overwrite as a patching strategy. CK3 can pick one version unpredictably.
- Do not use obsolete or known-wrong fields such as `is_triggered_only` or `duration` for CK3 event/modifier duration patterns.
- Do not put non-ASCII identifiers in scripts outside localization values.
- Do not place expensive `any_`/`every_` traversal in frequently evaluated GUI visibility or AI weight code without a cached/scripted-value strategy.
- Do not call missing modifiers, scripted content, or GUI objects casually; missing references can become crashes, constant-true checks, or noisy logs.

## Output Standard

For code work, state:

1. The execution context and current scope.
2. The exact files or blocks to change.
3. The script content or patch.
4. The validation method.
5. Any compatibility or performance risk that remains.
