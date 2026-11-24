# Bead: bob-cli-px.2 — bob capture refuses unconfirmed email-task closes

[Bead Pages](../README.md) / [bob-cli-px](README.md) / bob-cli-px.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1fs](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1fs.md) · **Assignee:** `bob-cli-px.2` · **Size:** medium
**Created:** 2026-11-24 12:22:30 EST · **Closed:** 2026-11-24 14:12:42 EST
**Plan:** [202611/email\_task\_close\_confirmation.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/email_task_close_confirmation.md)

## Description

capture: last-gate post-pass that finds Gmail Tasks a capture would close, the mail_close JSON payload, the -m/--mail-close DIGEST confirmation, human output, and docs.

## Notes

[2026-11-24T19:12:29Z · bob-cli-px.2] PROPOSED FOLLOW-UP: just lint fails on clean HEAD in src/native/props/{cli.rs,contract/read.rs} (collapsible_if, for_kv_map, manual_pattern_char_comparison, map_identity) — reproduces identically on f07c2395; no existing task bead tracks it.

[2026-11-24T19:12:42Z · bob-cli-px.2] Capture last-gate refuses unconfirmed Gmail Task closes. -C/--mail-close DIGEST confirms; digest ignored when nothing is guarded. 17 CLI tests (bang, -x/-X, relation complete/cancel, x!, merge exemption, same-capture create+close, all-or-nothing, dry-run parity, human card) plus 2 unit tests and completion kinds coverage pass. capture_help_lists_options_alphabetically passes. just docs-check passed with json-outputs at the 6000-word cap; generated CLI ref lists -C/--mail-close between jump-offer and move-in. epic-symbols empty. Pre-existing props clippy on HEAD filed as PROPOSED FOLLOW-UP.

## Dependencies

- **Depends on:** [bob-cli-px.1](bob-cli-px.1.md) ✓ · ⧖ 2026-11-24
- **Blocks:** [bob-cli-px.5](bob-cli-px.5.md) ✓ · ⧖ 2026-11-24
- **Blocks:** [bob-cli-px.6](bob-cli-px.6.md) ✓ · ⧖ 2026-11-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-px.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-px.2/README.md) | [bob-cli-px.2](bob-cli-px.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`976f53b`](https://github.com/bobs-org/bob-cli/commit/976f53ba4e6f47ca80a723ac4f1f9d94495db01a) | feat(capture)!: refuse unconfirmed Gmail Task closes | [bob-cli-px.2](bob-cli-px.2.md) | 2026-11-24 14:13:52 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-px.2][1] | Need notes, remaining work, and whether earlier agents already landed capture work | 5 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-px.2/README.md

<!-- sase:referenced-by:end -->
