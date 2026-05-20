# 05 CK3 Content Patterns

## Events

- CK3/Jomini events use event ids as top-level entries.
- Use a namespace and a stable mod prefix.
- Do not rely on same-id event replacement for compatibility patches.
- Confirm event root scope before writing triggers or effects.
- If an event is hidden, it should not require player-facing title/desc behavior.

## Decisions

- `is_shown` controls whether the decision appears.
- `is_valid` controls whether it can be taken.
- `effect` performs the actual action.
- Keep expensive checks out of `is_shown` when possible.
- Put repeated eligibility logic in scripted triggers.

## Interactions

- Confirm actor and recipient scopes. CK3 interaction contexts often differ from event contexts.
- Keep AI acceptance and AI willingness logic readable and cheap.
- Put shared actor/recipient checks in scripted triggers.

## Modifiers

- Confirm referenced modifiers exist before use.
- Use correct duration syntax for CK3 modifier application, such as `years =`, `months =`, or `days =` where valid.
- Avoid obsolete or guessed fields such as `duration`.

## Localization

- Localization keys should be stable and prefixed.
- Keep script identifiers ASCII; Chinese belongs in localization values.
- Preserve the localization file's header and encoding style.
- Avoid renaming localization keys casually; old keys may be referenced by events, decisions, GUI, or scripted loc.

## Common Anti-Patterns

- Copying a large vanilla file to change one entry.
- Embedding the same long eligibility check in many places.
- Writing effect code inside trigger blocks.
- Assuming `root` means the player character.
- Adding direct `effect` to vanilla on_action entries.

