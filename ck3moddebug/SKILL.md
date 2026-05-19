---
name: ck3moddebug
description: Use when diagnosing CK3 mod errors with Tiger output, including parse errors, unknown fields, scope misuse, missing references, and repeated warning triage.
---

# CK3 Tiger Debug

## Goal

Use Tiger to quickly locate CK3 mod errors and provide a closed loop of executable fixes plus repeatable verification.

## When To Use

- The user provides Tiger error logs and needs root-cause analysis
- The mod needs a structured health check (error/warning/tips)
- Batch fixes are needed, followed by rerun verification

## When Not To Use

- Pure mechanic discussion with no logs and no errors
- Only writing new feature scripts (prefer `ck3code`)

## Resource Note (Required)

Tiger is resource-heavy. Avoid frequent reruns.  
Strategy: fix a batch of issues first, then run one consolidated retest.

## Tiger Path Initialization

Before running debug checks, read the `README.md` file in this skill directory for the current `ck3-tiger.exe` path.

- If the README already has a valid path, use it.
- If it does not exist or does not contain a usable path, ask the user for the Tiger executable location.
- After the user provides a valid path, write it back into `README.md` for future runs.

## Execution Flow

1. Run Tiger (prefer no-color output)
2. Parse the report and group by severity
3. Fix `error` first, then `warning`, then review `tips`
4. Rerun Tiger once after each fix round
5. Report remaining issues and next-round plan

## Common Commands (Windows)

Tiger binary location note:
- Prefer the path stored in `README.md`.
- If no path is available yet, follow the initialization rules above.

```powershell
# 1) Standard check (recommended)
"<ck3-tiger.exe path from README>" --no-color "path\to\descriptor.mod" > tiger_report.txt

# 2) JSON output (for programmatic processing)
"<ck3-tiger.exe path from README>" --json "path\to\descriptor.mod" > tiger_report.json

# 3) Show only new issues (requires baseline)
"<ck3-tiger.exe path from README>" --suppress baseline.json "path\to\descriptor.mod"
```

## Issue Severity Strategy

- `fatal/error`: blocks runtime or high-risk, must be fixed first
- `warning`: potential issue, recommended to handle in the same round
- `tips`: optimization guidance, handle last

## Output Standard

1. Conclusion: what is the most critical root cause now
2. Evidence: log entries, file path, line number
3. Fix: minimal-change plan (include patch snippets when needed)
4. Validation: rerun command and expected result change

## Quality Bar

- Do not just restate logs; provide executable fix actions
- Fix recommendations must match CK3 semantics; uncertain items go to `ck3reference`
- When script edits are involved, call `ck3code` to generate/correct code

## Collaboration Rules

- If semantics/fields are uncertain: call `ck3reference`
- If script changes are needed: call `ck3code`
