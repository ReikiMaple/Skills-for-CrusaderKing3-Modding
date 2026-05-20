# 02 Load Order And Compatibility

## Load Model

- CK3 loads vanilla, then mods by launcher order.
- Same virtual file path: later mod file replaces earlier file.
- After virtual files are chosen, many script databases read entries by file name order.
- Jomini non-GUI script entries usually use later definition wins. GUI and localization are more often first-claim behavior.

## Patch Strategy

- Prefer adding new files and new entries over copying full vanilla files.
- Prefer small wrapper entries over broad replacement.
- Use file names to control order only when the target folder actually reads entries by order.
- Do not patch CK3 events by redefining the same event id. The engine may select one version unpredictably.

## On-Action Bridge Pattern

When extending a vanilla `on_action` that already has `effect`, do not add another same-name `effect` block.

Use this pattern:

```txt
vanilla_on_action_name = {
    on_actions = {
        your_mod_hook_on_action
    }
}

your_mod_hook_on_action = {
    effect = {
        # real logic here
    }
}
```

Route multiple vanilla entry points to one shared custom hook when they should execute the same logic.

## Mod Interfaces

- For optional cross-mod integration, expose stable `scripted_trigger`, `scripted_effect`, `script_value`, on_action hook, or scripted GUI names.
- If another mod may be absent, provide placeholder entries when possible.
- Missing scripted triggers/effects can produce repeated errors and may evaluate in surprising ways. Do not use missing content as control flow unless you have verified behavior.
- Missing modifiers are especially risky in CK3 and can cause unstable startup behavior.

## Compatibility Checklist

- Does this change replace a vanilla file or entry?
- Could another mod reasonably touch the same file or entry?
- Can the logic be moved into a new scripted trigger/effect/value?
- Does the on_action change use a bridge hook?
- Are optional external references guarded or stubbed?

