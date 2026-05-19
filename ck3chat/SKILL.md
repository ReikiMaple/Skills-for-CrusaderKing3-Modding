---
name: ck3chat
description: Use when the user asks about Crusader Kings III (CK3), including gameplay mechanics, mod design, script writing, debugging, or balance decisions.
---

## Goal

As the CK3 orchestration skill, first align the request, then chain the standard CK3 skills in the smallest correct flow, and finally output executable results.

Standard skill stack:

- `ck3reference` for authoritative field and mechanic checks
- `ck3code` for script writing and edits
- `ck3moddebug` for log, Tiger, or verification work
- `ck3mod-coding-standards` for non-trivial script work that needs style, compatibility, scope safety, or performance discipline

## When To Use

Enable this skill when the user request includes any of the following topics:

- CK3 gameplay, mechanics, or balance discussion
- CK3 mod design (events, decisions, cultures, religions, governments, traits, interactions, etc.)
- CK3 script writing/modification (Jomini script)
- CK3 error investigation, log analysis, or compatibility issues

## When Not To Use

Do not enable this skill in the following cases:

- General programming questions unrelated to CK3
- Pure language polishing/translation that does not involve CK3 content correctness

## Sub-skill Dispatch Rules

Default flow: identify the task type first, then call sub-skills minimally to avoid duplicate lookups.

1. Mechanic explanation / field validation: use `ck3reference`
2. Need to write or edit scripts: use `ck3code`, and add `ck3reference` when fields are uncertain
3. Need debugging/mod verification: use `ck3moddebug`, and combine with `ck3reference` to locate root cause
4. Need standards or guardrails for a non-trivial CK3 code task: use `ck3mod-coding-standards` alongside the active sub-skill

Recommended sequence:

- Writing new content: `ck3reference` -> `ck3code`
- Fixing bugs: `ck3moddebug` -> `ck3reference` -> `ck3code`
- Pure Q&A: `ck3reference` (add minimal examples only when needed)
- Non-trivial code tasks: `ck3reference` -> `ck3mod-coding-standards` -> `ck3code`

## Response Format

Try to follow this structure in each response for efficiency:

1. Conclusion: one sentence for the answer or root cause
2. Executable content: provide script/patch points/commands directly
3. Validation: how to confirm it works in-game or in logs
4. Risk notes: version differences, scope pitfalls, compatibility impact (only when necessary)

## Quality Bar

- Do not invent CK3 fields, trigger names, or effect names; check `ck3reference` when uncertain
- Any script output must be actionable and include required context (scope, conditions, effect blocks)
- For "why is this error happening", always provide repro path + fix plan + verification steps

## Quick Mapping

- "Can this trigger be used?" -> `ck3reference`
- "Help me write an event/decision" -> `ck3reference` + `ck3code`
- "How do I fix this log error?" -> `ck3moddebug` + `ck3reference` + `ck3code`
- "How should this mechanic be balanced?" -> `ck3reference` (add script suggestions if needed)
- "Need long-term CK3 coding discipline" -> `ck3mod-coding-standards` + active CK3 skill
