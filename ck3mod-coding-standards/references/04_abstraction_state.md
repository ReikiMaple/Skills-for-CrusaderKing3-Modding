# 04 Abstraction State

## Scripted Triggers

Use `common/scripted_triggers` for repeated conditions.

Good uses:

- eligibility checks
- expensive condition groups
- compatibility guards
- AI permission gates

Keep the trigger name explicit and prefix it with the mod id.

## Scripted Effects

Use `common/scripted_effects` for repeated state changes.

Good uses:

- shared event consequences
- repeated cleanup logic
- setup blocks used by several on_actions

Do not hide important scope assumptions. Name parameters clearly and document required scope when non-obvious.

## Parameters

- Fill every `$PARAM$` expected by a scripted trigger/effect call.
- Prefer uppercase parameter names such as `$TARGET$` or `$TITLE$`.
- When parameter behavior is uncertain, verify against an existing vanilla example or generated script docs.

## Script Values

- Use `common/script_values` for reusable numeric logic and AI weighting.
- Script values are often better than variables for derived calculations.
- In CK3, be careful about script value scope. Evaluate from the local/current scope unless verified otherwise.
- Avoid script values that read data being mutated inside the same execution chain.

## Variables

- Variables belong to a scope or global storage.
- Confirm the variable host scope before setting or reading.
- Use `flag:` prefix for flag-typed variable values when required.
- Prefer script values for derived numeric results; use variables for persistent state.

## Flags

- Flags are simple named state markers, optionally timed.
- In newer CK3 logic, variables often replace flags when a value or target must be stored.
- Use stable prefixes to avoid collisions.

