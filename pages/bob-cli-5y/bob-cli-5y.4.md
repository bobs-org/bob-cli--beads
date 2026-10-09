# Bead: bob-cli-5y.4 — Live alias, install, and the hook passes -P

[Bead Pages](../README.md) / [bob-cli-5y](README.md) / bob-cli-5y.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0z0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0z0.md) · **Assignee:** `bob-cli-5y.4` · **Size:** small
**Created:** 2026-10-09 12:29:34 EDT · **Closed:** 2026-10-09 13:11:38 EDT
**Plan:** [202610/ref\_tasks\_live\_with\_parent.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_tasks_live_with_parent.md)

## Description

hook-config: install bob, add project_name_aliases to bob.md, confirm the live sase exports the variable, then switch the chezmoi hook command to pass -P.

## Notes

[2026-10-09T17:07:30Z · bob-cli-5y.4] PROPOSED FOLLOW-UP: Add decisions strand decisions:ref-tasks-live-with-their-parent recording that ref tasks live with their parent note (skipped per epic auto-decision memory_ref_parent_decision=no)

[2026-10-09T17:07:33Z · bob-cli-5y.4] PROPOSED FOLLOW-UP: Update glossary strands glossary:reference-task, glossary:reference-note, and glossary:area-note for the parent-resident ref-task model (skipped per epic auto-decision memory_glossary_ref_terms=no)

[2026-10-09T17:11:38Z · bob-cli-5y.4] hook-config done: just install ok; project_name_aliases [bob-cli] on live bob.md (vault-sync pushed); capture-targets shows alias, -P bob-cli resolves to parent bob via alias and -P sase by stem (dry-run); live sase primary checkout pulled ff-only to 6f6754f97d incl. 5y.1 export commit, runner verified via live interpreter (exports project, unset when missing/empty/unknown); chezmoi research-highlights hook now 'bob ref create --include-id -P $SASE_FILE_HOOK_PROJECT', committed (fd85c856), applied, live sase file-hook list confirms, chezmoi update -a --force clean; just check exit 0; no epic-symbol leftovers

## Dependencies

- **Depends on:** [bob-cli-5y.1](bob-cli-5y.1.md) ✓ · ⧖ 2026-10-09
- **Blocks:** [bob-cli-5y.13](bob-cli-5y.13.md) ◐ · ⧖ 2026-10-09
- **Depends on:** [bob-cli-5y.2](bob-cli-5y.2.md) ✓ · ⧖ 2026-10-09
- **Blocks:** [bob-cli-5y.9](bob-cli-5y.9.md) ✓ · ⧖ 2026-10-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-5y.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5y.4/README.md) | [bob-cli-5y.4](bob-cli-5y.4.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-5y.4][1] | Need the phase scope and design file | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5y.4/README.md

<!-- sase:referenced-by:end -->
