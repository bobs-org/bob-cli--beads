# Bead: bob-cli-go.10.1 — Capture transfer grammar and execution

[Bead Pages](../README.md) / [bob-cli-go.10](bob-cli-go.10.md) / bob-cli-go.10.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-go.10](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-go.10.md) · **Assignee:** `bob-cli-go.10.1.land`
**Created:** 2026-11-04 01:50:44 EST · **Closed:** 2026-11-04 08:36:08 EST
**Plan:** [202611/capture\_transfer.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_transfer.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/capture_transfer.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 5 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_transfer.md

<!-- sase:links:end -->

## Description

Complete bob-cli-go.10 with one-item capture transfers that move to notes or merge into tasks, drawers, and sections, preserving atomicity, editor contracts, offers, shell safety, and existing capture behavior.

## Notes

[2026-11-04T13:36:08Z · bob-cli-go.10.1.land] Landing verified all five phases (e00f9074 lexer+shell guard, 706eab67 resolvers+single grammar bump 9->10 with feat(capture)!/BREAKING CHANGE, b9fe9d0c staged moves, dad9e660 staged explicit merges/offers, d25080e1 docs). Read source: shared scan_transfer_line claims before target-run fan-out in draft.rs and editor_parse.rs; CaptureKind::Transfer + capture-parse transfer object/spans/needs; capture/transfer.rs resolves against staged snapshots, refuses resolved duplicates/overlap/destination-is-source, moves via apply_batch_move in typed order, merges via plan_task_merge (MergeGesture::Explicit, first merge label else 'merged into') with staged write order, read guards, draft-level pull_in offers; moves[]/merges[]/repaired_files[]; shell_ate_transfer_arrow guard cfg-gated Linux/macOS; no transfer_execution_unavailable left; no memory/Cargo version/CHANGELOG edits; Mac gate is grammar>=5 so revision 10 stays compatible. LANDING FIX (epic-caused, mislabelled 'clean-base' by phases .3/.4/.5): the glued-arrow scan claimed any '>' anywhere ('=>', '<https://...>'), breaking 4 capture_language lib tests and cli capture_bracketed_url_queues_without_brackets; restricted try_glued_arrow to near-transfer shapes (source-like run glued to '>' or '>@dest' right after the run) with 9 new Unclaimed vectors; and the test-only parse_capture_text_with_options had been switched to target-run fan-out (breaking terminal_extraction_crosses_the_run) - split parse_transfer_claim out so the singleton helper claims transfers but keeps ordinary items unfanned. Results: just check rc=0 (fmt, clippy, all workspace tests incl. 549 capture_language, 4942 lib, 3071 cli); git diff --check clean; scratch-vault smoke with just-built bob: worked example -> grammar 10 task_merge drawer transfer, '=>'/bracketed URL ordinary/ref, '@a+x> @c' transfer_arrow_spacing. just docs-check: lint ok, generated drift exits 2 on sase/memory/glossary/task-merge.md missing front matter (reproduced identically on pre-epic 3741ce2e; owned by bob-cli-go memory closeout). Integration: no non-epic commits landed since 3741ce2e (HEAD == origin/master). FOLLOW-UP TRIAGE: .1#1/.2#1/.3#1 MergeContext successor_labels compile break on 3741ce2e - declined, already fixed in b9fe9d0c with correct configured successor_labels wiring; .3#2, .3#3, .4#1 arrow false positives - epic-caused, fixed in this landing; .4#2/#3 stale capture CLI reference - declined, resolved by d25080e1 docs-gen (docs_reference test passes); .5#1 token-coverage '@route+id @route+id' literal gap - pre-existing (fails on 3741ce2e), corroborated duplicate bob-cli-fo via +1; .5#2 contracts drift test / glossary task-merge front matter - pre-existing, causally owned by active epic bob-cli-go (aac3947c), recorded as DISCOVERED ISSUE corroboration note on bob-cli-go. epic-symbols: none for bob-cli-go.10.1 or bob-cli-go.10. No just symvision recipe exists in this repo.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-go.10.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-go.10.1.land/README.md) | [bob-cli-go.10.1](bob-cli-go.10.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`cb9dd8f`](https://github.com/bobs-org/bob-cli/commit/cb9dd8f9a956f8845724c0c428acd3d0c377a6a7) | fix(capture): stop transfer lexer claiming non-transfer arrows | [bob-cli-go.10.1](bob-cli-go.10.1.md) | 2026-11-04 08:37:35 EST |
| bob-cli--plans | [`bob-cli--plans@5f0c598`](https://github.com/bobs-org/bob-cli--plans/commit/5f0c5981216fe917e17be092453f3c9b0798ad4c) | chore(plans): mark capture\_transfer epic plan done | [bob-cli-go.10.1](bob-cli-go.10.1.md) | 2026-11-04 08:38:21 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-go.10.1.1][1] | Need parent epic scope and DECISIONS | 1 |
| read-by | [agent:bob-cli-go.10.1.2][2] | Need the epic decisions governing this phase | 1 |
| read-by | [agent:bob-cli-go.10.1.3][3] | Need epic DECISIONS and scope for phase work | 1 |
| read-by | [agent:bob-cli-go.10.1.4--1][4] | Confirm binding epic decisions while closing only transfer-merges | 1 |
| read-by | [agent:bob-cli-go.10.1.5][5] | Need child epic DECISIONS and closeout scope | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-go.10.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-go.10.1.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-go.10.1.3/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-go.10.1.4.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-go.10.1.5/README.md

<!-- sase:referenced-by:end -->
