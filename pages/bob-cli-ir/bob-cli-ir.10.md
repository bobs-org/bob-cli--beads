# Bead: bob-cli-ir.10 — Mac Record Card and guided entry

[Bead Pages](../README.md) / [bob-cli-ir](README.md) / bob-cli-ir.10

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1a0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1a0.md) · **Assignee:** `bob-cli-ir.10` · **Size:** large
**Created:** 2026-11-08 11:06:12 EST · **Closed:** 2026-11-09 09:38:08 EST
**Plan:** [202611/record\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/record_notes.md)

## Description

mac-record-card: decode the parse record object and record contexts in Bob Mac Capture, draw the Record Card in the picker-card slot, wire Tab through missing fields and record-aware Return, and style the record spans.

## Notes

[2026-11-09T14:38:43Z · bob-cli-ir.10.1.land--2] Child epic bob-cli-ir.10.1 closed after landing-audit repairs. Parent mac-record-card acceptance is covered: Bob-authored named-field addressing (-F, assist_version 1, record.edit); Mac decode/presentation/keyboard/card surface; Tab through missing fields; record-aware Return; create-route record_target uses visible generic CompletionList; value overflow keeps selectedCompletionIndex; More rows share full-width layout; Ready is an ordinary footer hint; route emoji is a presentation overlay; schema 1, grammar gate, Cargo versions, and CHANGELOG.md preserved. No memory edits (glossary:capture belongs to other parent phases).

Final revisions: bob-cli 5e49fa5e (named-field) at HEAD 941ee724; Mac child 1e6fb18, 7933c7e, 8c13ac4, 4bca5da plus repairs c09e2bc and eded3b9 (HEAD eded3b9ca680244939ec9c69a71dac7484e4b683). Exact-tree macOS CI snapshot 13a376669befc9c140a798c5f909d43dba276edf https://github.com/bobs-org/bob-mac-capture/actions/runs/42632159176: Lint, Build, Test, Bundle, Verify plist, Launch smoke, Install passed. epic-symbols bob-cli-ir.10: none. just symvision absent from both justfiles. .4 note #4 More-row alignment declined as a separate task and fixed here; no new external follow-ups. Containing epic bob-cli-ir and plan:202611/record_notes.md left for the waiting land agent.

## Dependencies

- **Blocks:** [bob-cli-ir.11](bob-cli-ir.11.md) ◐ · ⧖ 2026-11-08
- **Depends on:** [bob-cli-ir.6](bob-cli-ir.6.md) ✓ · ⧖ 2026-11-08

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ir.10](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ir.10.md) | [bob-cli-ir.10](bob-cli-ir.10.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ir.10.1.3][1] | Need outer phase decisions and recorded completion notes governing this child epic | 1 |
| read-by | [agent:bob-cli-ir.10.1.land--2][2] | Need parent phase status after child close | 2 |
| read-by | [agent:d5][3] | Know what the shipped Mac Record Card does for the user report | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ir.10.1.3/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ir.10.1.land.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.d5/README.md

<!-- sase:referenced-by:end -->
