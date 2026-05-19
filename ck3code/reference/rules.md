# CK3 Code Quick Rules

This is the quick guardrail index for `ck3code`. For fuller standards, use `ck3mod-coding-standards`.

## Must Check Before Writing

- What file type is this: script, localization, GUI, scripted GUI, data, event, decision, interaction, on_action?
- Does the current block expect trigger code or effect code?
- What is the current scope? What is the target scope?
- Is this replacing vanilla content or extending it?
- Is any field, trigger, effect, scope, method, or modifier uncertain?

## Hard Rules

- Do not guess CK3 field names. Check local reference, generated `script_docs`, CK3 vanilla files, or `ck3reference`.
- Do not use `is_triggered_only` in CK3 events.
- Do not use `duration` as a guessed duration field; use valid CK3 syntax such as `years =`, `months =`, or `days =` where accepted.
- Do not directly add `effect` to a vanilla-named on_action that already has vanilla `effect`; append through `on_actions = { your_hook }`.
- Do not patch CK3 events by redefining the same event id and relying on load order.
- Do not use non-ASCII identifiers outside localization values.
- Do not call missing modifiers casually; missing CK3 modifiers can become crash risks.

## Trigger And Effect

- Trigger blocks check conditions and return yes/no.
- Effect blocks change state.
- `trigger`, `limit`, `is_shown`, `is_valid`, and AI gates usually expect triggers.
- `effect`, `immediate`, `after`, options, and on_action effects usually expect effects.
- If an `if` has `limit = { ... }`, the `limit` block is trigger code and the body is effect code.

## Scope

- `root` is the root of the current execution context, not automatically the player.
- `this` is the current block scope.
- `prev` is the previous scope after a scope switch.
- `scope:name` must have been saved earlier.
- Dot-chain jumps like `root.holder.culture` require every hop to be valid and should not be used for one-to-many relations or `prev`.

## Compatibility

- Prefer new files and new entries over full vanilla file replacement.
- Prefer `scripted_trigger`, `scripted_effect`, and `script_value` for repeated logic.
- Use bridge hooks for vanilla on_actions.
- Guard optional cross-mod calls with placeholders or verified existence checks.

## Performance

- Put cheap checks before expensive checks.
- Avoid `any_`/`every_` scans in hot `is_shown`, GUI, and AI weight paths.
- Use script values or narrow scripted triggers for repeated expensive logic.

## Reference Map

- General standards: `ck3mod-coding-standards/references/01_style_and_files.md`
- Compatibility and on_actions: `ck3mod-coding-standards/references/02_load_order_and_compatibility.md`
- Trigger/effect/scope: `ck3mod-coding-standards/references/03_trigger_effect_scope.md`
- Abstractions/state: `ck3mod-coding-standards/references/04_abstraction_state.md`
- CK3 content patterns: `ck3mod-coding-standards/references/05_ck3_content_patterns.md`
- GUI/Jomini: `ck3mod-coding-standards/references/06_gui_jomini.md`
- Debug/performance: `ck3mod-coding-standards/references/07_debug_performance.md`

