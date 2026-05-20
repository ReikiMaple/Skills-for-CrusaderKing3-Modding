# 01 Style And Files

## File Format

- Inspect encoding, newline style, and structure before reading or editing.
- CK3 script files are normally `.txt`; GUI files are `.gui`; localization files are `.yml`.
- CK3 tolerates LF and CRLF in practice. Preserve the existing newline style when editing.
- Prefer UTF-8 for skill/reference docs. For CK3 localization, preserve the file's existing encoding and header style.

## Paths

- The engine recognizes files by specific folders. Events belong in `events/`; decisions in `common/decisions`; scripted triggers in `common/scripted_triggers`; scripted effects in `common/scripted_effects`; on_actions in `common/on_action`.
- Some `common/` paths have engine-significant second-level folders, such as `common/artifacts/`. Do not assume every subfolder is only for organization.
- Prefer `/` inside script paths. Windows `\` also works in many places but can be confused with escaping.

## Naming

- Pick a stable mod prefix and use it on files, namespaces, scripted objects, variables, flags, and localization keys.
- Use ASCII identifiers outside localization values: letters, numbers, and `_`; do not start with a number.
- Prefer descriptive suffixes such as `_events.txt`, `_triggers.txt`, `_effects.txt`, `_values.txt`, `_l_simp_chinese.yml`.
- Avoid vanilla-looking names unless intentionally extending a vanilla entry through a safe hook.

## Formatting

- Use consistent indentation. Four spaces are easy to read; preserving local file style is more important than reformatting unrelated code.
- Use comments for complex logic, compatibility notes, and intentional vanilla hooks.
- Keep comments useful: explain why a block exists or what compatibility contract it protects.

