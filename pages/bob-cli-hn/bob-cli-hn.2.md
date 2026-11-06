# Bead: bob-cli-hn.2 — Rust offer-close engine and per-row close descriptors

[Bead Pages](../README.md) / [bob-cli-hn](README.md) / bob-cli-hn.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.191](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.191/README.md) · **Assignee:** `bob-cli-hn.2` · **Size:** medium
**Created:** 2026-11-05 18:41:46 EST · **Closed:** 2026-11-05 20:18:24 EST
**Plan:** [202611/successor\_card\_verdicts.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/successor_card_verdicts.md)

## Description

engine: build the pure Rust offer-close engine (eligibility, root-only Done, Task-Card-parity Cancel, recover-only cascade, consequence copy), attach a `close` descriptor to every capture offer row, and publish tests/fixtures/offer_close/vectors.json.

## Notes

[2026-11-06T01:17:40Z · bob-cli-hn.2] PROPOSED FOLLOW-UP: reconcile memory_verdict_record=no with memory_offers_supersede=yes before superseding decisions:unblocked-tasks-are-offered; the required target strand is absent, and bob-cli-hn.1 already records this authorization collision.

[2026-11-06T01:17:45Z · bob-cli-hn.2] PROPOSED FOLLOW-UP: remove the duplicate clipboard catalog and completion-kind registrations; both native::catalog::tests::public_leaves_are_entries_or_excluded and native::completion::kinds::tests::every_table_entry_matches_the_tree fail on clean base 723af324. Existing task bob-cli-hp tracks the exact failures; bob-cli-hj.4 also records them.

[2026-11-06T01:17:49Z · bob-cli-hn.2] PROPOSED FOLLOW-UP: document BOB_GMAIL_GOG, BOB_GMAIL_BROWSER, BOB_GMAIL_ASSUME_TTY, and BOB_GMAIL_CONSENT_SECS from src/native/google/profile.rs so just docs-check passes; this is already reproduced on clean HEAD and recorded in bob-cli-hl.1, with no matching task bead found.

[2026-11-06T01:18:24Z · bob-cli-hn.2] Implemented the pure offer-close engine, shared descriptors on every surviving capture offer via the final staged batch post-pass, and the SV1–SV16 fixture. Verified focused tests (9 passed), just lint, and git diff --check. Full lib suite: 5190 passed, 2 ignored; the two clipboard registration failures reproduce on clean base 723af324 and are tracked by bob-cli-hp. just docs-check has four clean-base BOB_GMAIL_* documentation errors tracked by bob-cli-hl.1. epic-symbols is clean. Recorded the memory authorization collision as a proposed follow-up; no memory note changed.

## Dependencies

- **Depends on:** [bob-cli-hn.1](bob-cli-hn.1.md) ✓ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-hn.3](bob-cli-hn.3.md) ✓ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-hn.6](bob-cli-hn.6.md) ◐ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-hn.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hn.2/README.md) | [bob-cli-hn.2](bob-cli-hn.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`53f9c2c`](https://github.com/bobs-org/bob-cli/commit/53f9c2c758653cb54fbb1fd4d4339d18ae23d459) | feat(capture): add staged offer close descriptors | [bob-cli-hn.2](bob-cli-hn.2.md) | 2026-11-05 20:19:35 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hn.2][1] | Checking prior phase notes before continuing | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hn.2/README.md

<!-- sase:referenced-by:end -->
