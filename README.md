# CK3 MCP Skills

## Overview

- `ck3chat`: Main CK3 entry point. Dispatches requests to the right skill by task type.
- `ck3reference`: Looks up CK3 mechanics, fields, syntax, official notes, and reference material.
- `ck3code`: Writes or edits CK3 scripts, decisions, events, localization, and related mod files.
- `ck3mod-coding-standards`: Applies CK3 coding standards for compatibility, scope safety, maintainability, and performance.
- `ck3moddebug`: Diagnoses Tiger logs, locates errors, and verifies fixes.

## Typical Flow

- Mechanics question: `ck3reference`
- Code writing: `ck3reference` -> `ck3code`
- Error diagnosis: `ck3moddebug` -> `ck3reference` -> `ck3code`
- Non-trivial code task: `ck3reference` -> `ck3mod-coding-standards` -> `ck3code`

## Notes

- `ck3moddebug` reads the Tiger executable path from the `README.md` file in its own skill directory.
- These skills are intended for CK3 mod development, not general programming questions.

