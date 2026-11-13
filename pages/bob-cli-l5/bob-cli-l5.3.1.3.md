# Bead: bob-cli-l5.3.1.3 — Implement the one-key review session

[Bead Pages](../README.md) / [bob-cli-l5.3.1](bob-cli-l5.3.1.md) / bob-cli-l5.3.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-l5.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-l5.3.md) · **Assignee:** `bob-cli-l5.3.1.3` · **Size:** medium
**Created:** 2026-11-12 20:43:26 EST · **Closed:** 2026-11-13 00:37:29 EST
**Plan:** [202611/gcal\_ack\_cli.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gcal_ack_cli.md)

## Description

terminal: finish the bare-TTY ack session using a scoped libc termios guard and shared note services, all approved keys, per-answer saves, repeat protection, recurring scope defaults, queue recomputation, and disjoint summaries. Test piped keys and real PTY terminal restoration.

## Notes

[2026-11-13T05:30:13Z · bob-cli-l5.3.1.3] PROPOSED FOLLOW-UP: lib test native::gcal::cli::tests::sync_args_read_last_n_days_aliases_and_default_to_none fails identically on clean base HEAD 1863b39b (expected ["today", "tomorrow"], got ["tomorrow"]); existing owner per plan notes is bob-cli-l2, not this phase.

[2026-11-13T05:30:24Z · bob-cli-l5.3.1.3] PROPOSED FOLLOW-UP: just docs-check fails identically on clean base HEAD 1863b39b with "generated drift" plus sase/memory/glossary/event-ack.md having no front matter; strand repair is owned by bob-cli-l5.4, not this phase.

[2026-11-13T05:37:29Z · bob-cli-l5.3.1.3] Implemented the one-key ack review session: scoped libc termios guard (sigaction SIGINT, no SA_RESTART), unbuffered key/line input, keys a/n/e/s/q/Esc/Ctrl-C/?/o/conditional-A, per-answer persistence with recomputation and disjoint summaries, All-events default for ack scope and This-event default for note/editor/adopt, 80-column cards from shared previews. Added save_session_note/note_text_for to note/write.rs; spawn_opener is now pub(crate). Verified: 29 gcal_ack tests (20 new), 5 real-PTY tests (quit/Ctrl-C raw+cooked/transitions/error restoration), 4 guard/drain unit tests, all other gcal suites green, just lint and fmt clean. Two identical clean-base failures filed as PROPOSED FOLLOW-UP (sync day-alias unit test, docs-check event-ack strand). Two subprocess_runner timing tests flaked once under load and pass in isolation.

## Dependencies

- **Depends on:** [bob-cli-l5.3.1.2](bob-cli-l5.3.1.2.md) ✓ · ⧖ 2026-11-12
- **Blocks:** [bob-cli-l5.3.1.4](bob-cli-l5.3.1.4.md) ✓ · ⧖ 2026-11-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-l5.3.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-l5.3.1.3/README.md) | [bob-cli-l5.3.1.3](bob-cli-l5.3.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`307616a`](https://github.com/bobs-org/bob-cli/commit/307616aea9167577805a8e525dc4dd0ea0f9190d) | feat(gcal): add one-key ack review session \[bob-cli-l5.3.1.3\] | [bob-cli-l5.3.1.3](bob-cli-l5.3.1.3.md) | 2026-11-13 00:41:28 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-l5.3.1.3][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-l5.3.1.3/README.md

<!-- sase:referenced-by:end -->
