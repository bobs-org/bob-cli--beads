# Bead: bob-cli-mb.2 — bob-cli: living notes first in vault-wide \`\[\[\` link completion

[Bead Pages](../README.md) / [bob-cli-mb](README.md) / bob-cli-mb.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1cs](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1cs.md) · **Assignee:** `bob-cli-mb.2` · **Size:** small
**Created:** 2026-11-16 10:14:22 EST · **Closed:** 2026-11-16 11:35:58 EST
**Plan:** [202611/note\_goto\_followups.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/note_goto_followups.md)

## Description

cli-link-tiers: tag every `[[` note-index entry with the shared tier and order (or drop, per decision link_tiers) archive and hidden notes after living matches in `[[note`, `[[##`, `[[^^`, and record link-value suggestions, leaving target-scoped completion and link resolution unchanged.

## Notes

[2026-11-16T16:35:22Z · bob-cli-mb.2--1] Verification: `just all` passed (exit 0). Built optimized release `bob`; timed 7 live-vault `capture-complete -f json` queries each (cursor at end), medians 242.4 ms for `[[bob` and 240.3 ms for `[[2025111` versus prior release baselines 223 ms and 221 ms (+19.4 ms / +19.3 ms, about 8.7%). First `[[bob` cold-start sample was 1399.1 ms; excluded from median. Then ran `sase bead epic-symbols bob-cli-mb.2`.

[2026-11-16T16:35:58Z · bob-cli-mb.2--1] Implemented living/archive/hidden tier ordering for vault-wide link suggestions. just all passed; release timings are recorded in the bead note; epic-symbol check reported no leftovers.

## Dependencies

- **Depends on:** [bob-cli-mb.1](bob-cli-mb.1.md) ✓ · ⧖ 2026-11-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-mb.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-mb.2.md) | [bob-cli-mb.2](bob-cli-mb.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b73cf56`](https://github.com/bobs-org/bob-cli/commit/b73cf56f5fec9b4de6e95c9e326c6f6970e1d8f6) | feat(capture): prioritize living vault link suggestions | [bob-cli-mb.2](bob-cli-mb.2.md) | 2026-11-16 11:37:03 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-mb.2--1][1] | Need phase status, notes, scope, and epic decisions before closing | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-mb.2.md

<!-- sase:referenced-by:end -->
