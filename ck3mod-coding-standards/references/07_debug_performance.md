# 07 Debug Performance

## Debug Sources

- `error.log` is useful for script and data errors.
- `script_docs` in CK3 developer mode can generate available triggers, effects, scopes, and actions.
- Tiger or similar validators are useful for static checks, but in-game verification is still needed for behavior.
- Startup crashes may not leave useful script logs.

## Debug Flow

1. Identify the file and entry named in the log.
2. Confirm whether the block expects trigger, effect, localization, GUI, or data.
3. Confirm current scope and target scope.
4. Check whether the referenced field/object exists.
5. Reduce to a minimal repro path.
6. Re-run the relevant check.

## Performance Rules

- Put cheap and highly selective checks first in `AND`, `OR`, `if`, AI weights, and visible/valid blocks.
- Avoid repeated `any_`/`every_` traversal inside frequently evaluated UI or AI logic.
- Cache or encapsulate expensive checks with script values or narrow scripted triggers when suitable.
- Do not run large global scans when a local scope path can answer the question.

## AI Weights

- AI weight logic should be readable and cheap.
- Start with hard gates before score modifiers.
- Use scripted triggers for repeated AI gates.
- Avoid deep nested traversal unless it is rare or pre-filtered.

## Completion Evidence

Before claiming a CK3 scripting task is complete, provide at least one of:

- exact validation command or tool result
- in-game repro path
- expected log state
- reason no direct verification was possible

