# Bead: bob-cli-as.5 — Decay card Keep asks why and logs

[Bead Pages](../README.md) / [bob-cli-as](README.md) / bob-cli-as.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.55.linker.w2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.55.linker.w2.md) · **Assignee:** `bob-cli-as.5` · **Size:** medium
**Created:** 2026-10-23 08:24:13 EDT · **Closed:** 2026-10-23 10:23:22 EDT
**Plan:** [202610/rotten\_log.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/rotten_log.md)

## Description

card-keep: turn the approved-decay card's Keep into an in-card reason stage that commits stamp, increment, and Rotten Log entry as one transaction, and show the logged count and last reason on the card.

## Notes

[2026-10-23T14:22:58Z · bob-cli-as.5] Implemented card-keep in linked bob-plugins (navigation 2.54.0 -> 2.55.0): decay-card Keep swaps rows for RottenKeepReasonStage in the same modal (no close/flash, focus in field); Enter commits stamp+increment+Rotten Log entry in one applyEditorContentTransaction; Esc in stage returns to rows and refocuses Keep; second Esc writes nothing; opening Alt+F/repeat never submits; card ctx carries rottenHistory+keepsAfter and header line (N keeps logged, last date/reason; log unreadable when ambiguous); Keep row detail now say why - logs - asks again; other outcomes unchanged and never log.

[2026-10-23T14:23:02Z · bob-cli-as.5] PROPOSED FOLLOW-UP: bob-cli-6v (4 wall-clock unblocked-glyph) and bob-cli-7i (forward conversion retains BLOCKS Work_ship#^prj) reproduce identically on pristine HEAD 22ec6b2 worktree without this phases changes; unrelated to card-keep, statuses unchanged.

[2026-10-23T14:23:10Z · bob-cli-as.5] bob-cli-6w per plan: rewrote the decision-card Keep notice to Kept Nx - Rotten Log updated - next review asks and its tests (handlers now match on joined notices; new modal file covers stage). The review-journal missing-API notice (Update Bob Ledger Tools to record review stats) still fires asynchronously after applied keeps in fixtures without a stats API, so the original interference persists; bob-cli-6w status unchanged.

[2026-10-23T14:23:14Z · bob-cli-as.5] Verification: focused card/keep suites 21+21+11+94 all pass; full npm test 3500/3505 with only the 5 pre-existing clean-HEAD failures above; npm run build + build:check clean; git diff --check clean; npm run docs:check 447 passed/1 skipped; bob plugins sync deployed (3 copied). Live Obsidian check not performed: Obsidian is not running in this environment.

[2026-10-23T14:23:22Z · bob-cli-as.5] card-keep done in linked bob-plugins navigation 2.55.0: in-card Keep reason stage commits stamp+increment+entry in one undo, header shows logged keeps, Esc returns to choices. Verified: focused suites 21+21+11+94 pass; full npm test 3500/3505 with only the 5 pre-existing clean-HEAD failures (6v x4, 7i); build/docs:check/diff-check clean; plugins synced. Live Obsidian check unavailable (not running).

## Dependencies

- **Depends on:** [bob-cli-as.4](bob-cli-as.4.md) ✓ · ⧖ 2026-10-23
- **Blocks:** [bob-cli-as.6](bob-cli-as.6.md) ✓ · ⧖ 2026-10-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-as.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-as.5/README.md) | [bob-cli-as.5](bob-cli-as.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@973acea`](https://github.com/bobs-org/bob-plugins/commit/973aceafeb9c61c1ca1a61792787aa908b89b3de) | feat(navigation): decay card Keep asks why and logs Rotten Log entry | [bob-cli-as.5](bob-cli-as.5.md) | 2026-10-23 10:24:42 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-as.5][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-as.5/README.md

<!-- sase:referenced-by:end -->
