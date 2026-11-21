# Bead: bob-cli-o6.6.1.2 — Real-Obsidian fallback and teardown proof

[Bead Pages](../README.md) / [bob-cli-o6.6.1](bob-cli-o6.6.1.md) / bob-cli-o6.6.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-o6.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-o6.6.md) · **Assignee:** `bob-cli-o6.6.1.2` · **Size:** medium
**Created:** 2026-11-21 08:22:48 EST · **Closed:** 2026-11-21 12:17:44 EST
**Plan:** [202611/title\_block\_final\_proof.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/title_block_final_proof.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:44d1ed39ec272bcbd1055e2c | attached via sase artifact create --bead |
| related | file:explicit:482569fb7e27dee2e605a59e | attached via sase artifact create --bead |
| related | file:explicit:5e5662fc420f6fa1e25b3397 | attached via sase artifact create --bead |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

fail-open-proof: extend the shared title-block runner with native-rendering checks for Source, embeds, hover popovers, canvas, failed mounts and repaints, plugin disable, file/mode changes, and leaf teardown. Measure restoration at the first paint, preserve byte neutrality, and fix failures without weakening assertions.

## Notes

[2026-11-21T17:17:09Z · bob-cli-o6.6.1.2--b] PROPOSED FOLLOW-UP: Restore title-slot ownership after mount/repaint failure. The clean-HEAD d8dc11e run and final rerun reproduced title-slot-insert-failure-recovers (record remount timed out with localTitleOwner=false and no H1), repaint-failure-restores-native (remount timed out with localTitleOwner=false), and downstream leaf-close-clears-owner (title-card wait timed out). Do not weaken assertions. Evidence: report file:explicit:482569fb7e27dee2e605a59e; screenshot archive file:explicit:44d1ed39ec272bcbd1055e2c; visual review file:explicit:5e5662fc420f6fa1e25b3397. No new task bead created. Guarded sync dry-run and actual sync were both refused by protected deployments; zero files copied; no force used.

[2026-11-21T17:17:44Z · bob-cli-o6.6.1.2--b] Closed this phase after the final Obsidian rerun, direct review of all 23 screenshots, and epic-symbol check (no remaining entries). The walkthrough did not pass: 62 assertions passed and the same baseline failures reproduced from clean HEAD d8dc11e: title-slot-insert-failure-recovers, repaint-failure-restores-native, and downstream leaf-close-clears-owner. No assertions were weakened; the confirmed recovery defect is recorded as a PROPOSED FOLLOW-UP with report, archive, and visual-review refs on this phase. Guarded sync dry-run and actual sync were refused by protected deployments; actual result was 0 copied, 25 unchanged, 3 errors. No force was used. This close records the verification and refusal, not a walkthrough pass or successful deployment.

## Dependencies

- **Depends on:** [bob-cli-o6.6.1.1](bob-cli-o6.6.1.1.md) ✓ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-o6.6.1.3](bob-cli-o6.6.1.3.md) ✓ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-o6.6.1.5](bob-cli-o6.6.1.5.md) ◐ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-o6.6.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-o6.6.1.2.md) | [bob-cli-o6.6.1.2](bob-cli-o6.6.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@c803a4e`](https://github.com/bobs-org/bob-plugins/commit/c803a4e82ff869db4619d02adee6e1e14401d7eb) | fix(plugins): preserve title fallback after repaint failures | [bob-cli-o6.6.1.2](bob-cli-o6.6.1.2.md) | 2026-11-21 11:25:12 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-o6.6.1.2--7][1] | Need assigned epic and phase scope for the title-block fail-open verification | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-o6.6.1.2.md

<!-- sase:referenced-by:end -->
