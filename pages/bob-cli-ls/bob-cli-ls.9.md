# Bead: bob-cli-ls.9 — Record header strip and album summary card

[Bead Pages](../README.md) / [bob-cli-ls](README.md) / bob-cli-ls.9

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1cp](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1cp.md) · **Assignee:** `bob-cli-ls.9` · **Size:** medium
**Created:** 2026-11-15 13:11:22 EST · **Closed:** 2026-11-15 21:42:03 EST
**Plan:** [202611/bank\_subscriptions\_album.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_subscriptions_album.md)

## Description

surfaces: draw the per-record header strip with its charge timeline, the album summary card, and the formatted index rows on the subscriptions album.

## Notes

[2026-11-16T02:41:16Z · bob-cli-ls.9] PROPOSED FOLLOW-UP: Register scripts/test-ledger-tools-bank-subscription-linker.cjs in package.json test:unit — the linker file exists from bob-cli-ls.8 but is not in the unit list; this phase registered only test-ledger-tools-bank-subscription-surfaces.cjs.

[2026-11-16T02:41:32Z · bob-cli-ls.9] PROPOSED FOLLOW-UP: Full bob-plugins npm test 200-link Live Preview wall-clock flakes under suite load — keep-moving-marks-surface.cjs:486 took 1166.9ms (bob-cli-ki) and off-clock-link-chips.cjs:355 took 114.4ms (bob-cli-ju); isolated rerun of those files plus the surfaces tests passed 79/79. This phase did not touch those tests.

[2026-11-16T02:41:42Z · bob-cli-ls.9] PROPOSED FOLLOW-UP: npm run docs:check still fails the 6000-word cap on docs/reference/plugins/bob-ledger-tools.md (HEAD 6209, this phase 6281). Same pre-existing budget already proposed on bob-cli-ls.8.

[2026-11-16T02:42:03Z · bob-cli-ls.9] Record header strip, album summary card, and records-index pretty chrome landed in bob-ledger-tools. Surfaces read bob bank subscriptions -f json with -a; unknown bob-bank views stay quiet. Fictional Tunely/Cloudbox unit tests: 9/9 surfaces plus bank-cards/decode/source. Amber-dot CSS uses var(--color-orange) with no hex; reading-board and stats stylesheet contracts pass. Full npm test: 6785 pass, 2 skip, 2 load-flake fails (bob-cli-ki, bob-cli-ju) that pass in isolation; test:perf 5/5. docs:check still over the 6000-word cap on HEAD (6209) and this phase (6281). bob plugins sync copied main.js and styles.css without -F. subscriptions.md fence view: subscriptions sits above ## Records; bob vault-sync found a clean tree already on origin/master and pushed. sase bead epic-symbols bob-cli-ls.9 reported no leftovers.

## Dependencies

- **Blocks:** [bob-cli-ls.10](bob-cli-ls.10.md) ✓ · ⧖ 2026-11-15
- **Depends on:** [bob-cli-ls.6](bob-cli-ls.6.md) ✓ · ⧖ 2026-11-15
- **Depends on:** [bob-cli-ls.8](bob-cli-ls.8.md) ✓ · ⧖ 2026-11-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ls.9](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ls.9/README.md) | [bob-cli-ls.9](bob-cli-ls.9.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@cb885ca`](https://github.com/bobs-org/bob-plugins/commit/cb885cad16ccf013466b5b1ee8ebe89c7d75834c) | feat(bank): add subscription header strip and album summary card | [bob-cli-ls.9](bob-cli-ls.9.md) | 2026-11-15 21:43:22 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ls.9][1] | Need the phase scope, design file, and epic DECISIONS before implementing subscription surfaces | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ls.9/README.md

<!-- sase:referenced-by:end -->
