---
name: ck3reference
description: Use when answering CK3/CK3 mod questions that require authoritative field names, valid script entries, game-mechanic rules, or source-backed explanations before coding or debugging.
---

# CK3 Reference Retrieval

## Goal

Before CK3 Q&A, scripting, script changes, or debugging, extract verifiable evidence from local references first, so you do not output incorrect fields or mechanics from memory.

## When To Use

- The user asks CK3 mechanic details, field validity, or syntax availability
- You need to confirm concrete entries such as trigger/effect/scope/modifier/on_action
- You need evidence for "why this should be written this way"
- A `ck3code` or `ck3moddebug` task has uncertain fields

## When Not To Use

- Pure creative discussion that does not require field correctness
- Topics unrelated to CK3

## Data Sources And Lookup Rules

Search with "authority first + minimum cost":

1. `skills/ck3code_reference/Reference/script_docs/` (field validity first)
2. `skills/ck3code_reference/Reference/info/` (official/developer-oriented structure notes; now hierarchical mirror of `game/`)
3. `skills/ck3code_reference/Reference/ck3modwiki/` (experience/tutorial supplements)

Do not load the full library at once. Open only files directly related to the current question.

## Minimal Mapping From Task To Docs

- Check trigger/effect: `script_docs/triggers.txt`, `script_docs/effects.txt`
- Check event scope/target: `script_docs/event_scopes.txt`, `script_docs/event_targets.txt`
- Check on_actions: `script_docs/on_actions.txt`
- Check modifiers: `script_docs/modifiers.txt`
- Check localization scripting: `script_docs/custom_localization.txt`
- Check event/decision/interaction structure: `info/events/_events.md`, `info/common/decisions/_decisions.md`, `info/common/character_interactions/_character_interactions.md`
- Check mechanic gameplay context: prefer `info/**/*.md` (or `info/INDEX.md` for navigation), then add `ck3modwiki/*.md` only if needed

## Output Standard

1. Start with conclusion: is the field usable, does the mechanic hold
2. Provide evidence: source file path and key entry name
3. Provide action advice: what to write/change/test next
4. If uncertain, explicitly mark as "inference" and explain the gap

## Quality Bar

- Do not fabricate entry names or "guess a similar field"
- Every conclusion must be traceable to specific files
- If sources conflict, prefer `script_docs` and explain the conflict
- Keep citations minimal; avoid large pasted blocks

## Collaboration Rules

- For `ck3code`: return usable fields + context constraints (scope/location)
- For `ck3moddebug`: return legal alternatives/fix direction for reported errors
