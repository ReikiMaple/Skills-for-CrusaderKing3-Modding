# 03 Trigger Effect Scope

## Trigger Vs Effect

- Trigger code checks truth and returns yes/no.
- Effect code changes state or performs actions.
- `limit = { ... }`, `trigger = { ... }`, `is_shown = { ... }`, and `is_valid = { ... }` normally expect triggers.
- `effect = { ... }`, `immediate = { ... }`, `after = { ... }`, `on_accept = { ... }`, and event options normally expect effects.
- Empty trigger blocks usually pass. Empty effect blocks do nothing.

## Scope Discipline

- Most CK3 triggers and effects are valid only on specific scope types.
- Always identify current scope before writing code: character, title, county, province, culture, faith, dynasty, house, activity, scheme, etc.
- `root` is not "the player"; it is the root scope of the current execution context.
- `this` is the current scope inside the current block.
- `prev` is the previous scope after a scope switch.
- `scope:name` is a saved scope explicitly created earlier in the chain.

## Safe Scope Checks

- Use `always = <scope>` to check whether a scope exists when the syntax supports it.
- Do not assume chained jumps always exist. If an intermediate scope is absent, the chain can silently fail.
- Dot-chain syntax such as `root.holder.culture` is useful, but each jump must be legal.
- Do not use dot chains for one-to-many relationships or `prev`.

## Saved Scopes

- Use `save_scope_as` or `save_temporary_scope_as` when later logic needs a stable target.
- Temporary saved scopes are scoped to the current evaluation area and can disappear after the block ends.
- Prefer clear names with the mod prefix when the saved scope becomes part of a larger event chain.

## Review Questions

- What is `root` here?
- What is `this` here?
- Does the trigger/effect support the current scope type?
- Could the target scope be missing?
- Is a saved scope needed to avoid fragile `prev` logic?

