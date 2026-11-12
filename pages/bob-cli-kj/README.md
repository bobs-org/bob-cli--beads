# Bead: bob-cli-kj — Fix the impact-ranked open task beads

[Bead Pages](../README.md) / bob-cli-kj

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1bm](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1bm.md) · **Assignee:** `bob-cli-kj.land`
**Created:** 2026-11-11 17:20:03 EST · **Closed:** 2026-11-11 19:52:12 EST
**Plan:** [202611/impact\_ranked\_bead\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/impact_ranked_bead_fixes.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/impact_ranked_bead_fixes.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/impact_ranked_bead_fixes.md

<!-- sase:links:end -->

## Description

The three red verification gates every landing re-triages (macOS CI, bob-cli docs-check, the bob-plugins wikilink perf budgets) are green again and the two diagnosed user-facing bugs are fixed, so beads bob-cli-jx, -jy, -h9, -jz, -jr, -k8, -f8, and -hp can be closed with verified evidence.

## Notes

[2026-11-12T00:26:07Z · bob-cli-kj.land] LANDING TRIAGE (bob-cli-kj.land). Verified: jr (3ba40fc5), k8 (04cba0fa), hp (2a37f8ce) via full just check at 3ba40fc5 (exit 0; lib 6658, cli 3592) plus live repros; jx, jy via bob-mac-capture master 7fceb52 exact-SHA run 43117124821 fully green (Test 4750/0 failures, Bundle, Launch smoke, Install); h9, jz via bob-cli just docs-check lint ok + drift ok and bob-plugins docs:check lint ok. Closed jx, jy, h9, jz, jr, k8, hp. Integration: post-start commits bc3983d3, 6352824b, 300a6e81 (bob-cli), 7fceb52 (mac-capture), e8a776e, d532aad (bob-plugins) add no timestamp-helper or HomesEngine resolver users and do not conflict. REMAINING EPIC WORK: bob-cli-f8 - warm snapshot+order budget still fails inside full bob-plugins npm test 3/3 (63.5-68.5 ms vs 50) though it passes in isolation; planned as a tale. FOLLOW-UPS: (1) strict Zensical link warnings (kj.2 #3, kj.6 #2) -> +1 bob-cli-kk; validation.md->bob-vim-yank-flash already a DISCOVERED ISSUE on active epic bob-cli-kb. (2) subprocess_runner detached-grandchild drain flake (kj.3 #2) -> NEW bob-cli-kl (flake, large; tests from closed epic kf). (3) 25 ms ledger mark budgets under full-suite load (kj.6 #2) -> +1 bob-cli-ki (own repro 402.4 ms), +1 bob-cli-io (frees-marks 90 ms), +1 bob-cli-ju (off-clock 39.5 ms), NEW bob-cli-km for event-link-times (427.6 ms; flake, small). (4) cold-index last-yield basename-rebuild tail 16-28 ms (kj.6 #2) -> NEW bob-cli-kn (bug, medium). (5) CaptureDotRouteAliasTests fast-double-dot 1-vs-2 asks (kj.5) -> NEW bob-cli-ko (flake, small, related jb); separator unchanged-alias test -> +1 bob-cli-jc. DECLINED: edit-before-reply sigilEdited (kj.5) - fixed by bob-cli-ka.5 7fceb52, passes on green run 43117124821; notebook/drawer trio (kj.5) - owned and fixed by ka.5 7fceb52, passes on that run; second-eligible-sigil (kj.5) - already tracked by bob-cli-jk with no new failure evidence (passed on every observed run); docs:check word-budget overruns (kj.6 #2) - resolved by kj.2 (lint ok). No --epic-symbol entries for bob-cli-kj.

[2026-11-12T00:52:12Z · bob-cli-kj.land] Landing verification already on this epic (kj.land note #1): jx, jy, h9, jz, jr, k8, hp closed on evidence; integration reviewed; follow-up triage recorded in the LANDING TRIAGE note.

This tale finished bob-cli-f8. Cause: process.cpuUsage helper-thread inflation under parallel node --test allocation-heavy siblings (isolated main-thread snapshot 14–24 ms; in-wave process CPU 54+ ms). Fix: serial test:perf stage after test:unit; budgets unchanged. Isolated TAP 5/5×3. Full npm test wikilink file 5/5×3 consecutive (run 1 whole suite 6183+5 pass; runs 2–3 left allowed ledger flakes bob-cli-ki/km and Chromium timeout bob-cli-fz). Scratch regression still fails at 4×/8× decorate (51.5 / 77.1 ms). Artifacts file:explicit:3d550e65cc62b734faea3798 file:explicit:1e174e03afca3ba6c01d2d2f.

epic-symbols: none. just symvision: unavailable (no recipe on bob-cli). sibling_timing_tests=leave. Plan status set to done.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-kj.1](bob-cli-kj.1.md) | Isolation-correct alias test teardowns | ✓ closed | small | 2026-11-11 | 1 | 1 |
| [bob-cli-kj.2](bob-cli-kj.2.md) | Mounted reference pages back under the word cap | ✓ closed | medium | 2026-11-11 | 1 | 2 |
| [bob-cli-kj.3](bob-cli-kj.3.md) | Stats RefCell double-borrow panic | ✓ closed | small | 2026-11-11 | 1 | 1 |
| [bob-cli-kj.4](bob-cli-kj.4.md) | Configured-timezone created stamps | ✓ closed | small | 2026-11-11 | 1 | 1 |
| [bob-cli-kj.5](bob-cli-kj.5.md) | Deterministic alias-tip CI timeouts | ✓ closed | large | 2026-11-11 | 1 | 0 |
| [bob-cli-kj.6](bob-cli-kj.6.md) | Task-wikilink CPU budget investigation | ✓ closed | large | 2026-11-11 | 1 | 1 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-kj: Fix the impact-ranked open task beads [closed]"]
    n1["bob-cli-kj.1: Isolation-correct alias test teardowns [closed]"]
    n2["bob-cli-kj.2: Mounted reference pages back under the word cap [closed]"]
    n3["bob-cli-kj.3: Stats RefCell double-borrow panic [closed]"]
    n4["bob-cli-kj.4: Configured-timezone created stamps [closed]"]
    n5["bob-cli-kj.5: Deterministic alias-tip CI timeouts [closed]"]
    n6["bob-cli-kj.6: Task-wikilink CPU budget investigation [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n0 --> n6
    n1 -.-> n5
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kj.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kj.1/README.md) | [bob-cli-kj.1](bob-cli-kj.1.md) | 1 |
| [bbugyi200.athena.bob-cli-kj.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kj.2.md) | [bob-cli-kj.2](bob-cli-kj.2.md) | 2 |
| [bbugyi200.athena.bob-cli-kj.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kj.3.md) | [bob-cli-kj.3](bob-cli-kj.3.md) | 1 |
| [bbugyi200.athena.bob-cli-kj.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kj.4/README.md) | [bob-cli-kj.4](bob-cli-kj.4.md) | 1 |
| [bbugyi200.athena.bob-cli-kj.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kj.5.md) | [bob-cli-kj.5](bob-cli-kj.5.md) | 0 |
| [bbugyi200.athena.bob-cli-kj.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kj.6.md) | [bob-cli-kj.6](bob-cli-kj.6.md) | 1 |
| [bbugyi200.athena.bob-cli-kj.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kj.land.md) | [bob-cli-kj](README.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@1e83c03`](https://github.com/bobs-org/bob-mac-capture/commit/1e83c032217a9d6c90827ee467e5c60b57069d88) | fix(tests): isolate alias ledger teardown on main actor | [bob-cli-kj.1](bob-cli-kj.1.md) | 2026-11-11 17:32:23 EST |
| bob-mac-capture | [`bob-mac-capture@2007294`](https://github.com/bobs-org/bob-mac-capture/commit/2007294cdc29ef379f6959ef2f05b87d75681e45) | docs: trim mounted reference pages back under the word cap | [bob-cli-kj.2](bob-cli-kj.2.md) | 2026-11-11 17:54:54 EST |
| bob-plugins | [`bob-plugins@cb32d8d`](https://github.com/bobs-org/bob-plugins/commit/cb32d8d3ad06971bf352710224046c30dfca7566) | docs: trim navigation-hotkeys page back under the word cap | [bob-cli-kj.2](bob-cli-kj.2.md) | 2026-11-11 17:55:26 EST |
| bob-cli | [`04cba0f`](https://github.com/bobs-org/bob-cli/commit/04cba0fad559471e17415f71811e21c8baf8f740) | fix(capture): stamp created/captured in the configured timezone | [bob-cli-kj.4](bob-cli-kj.4.md) | 2026-11-11 18:09:34 EST |
| bob-plugins | [`bob-plugins@70408bf`](https://github.com/bobs-org/bob-plugins/commit/70408bf815ce899ca2e5965e9fca8c1d8703ceee) | fix(block-id-prompt): restore task-wikilink snapshot and rank CPU budgets | [bob-cli-kj.6](bob-cli-kj.6.md) | 2026-11-11 18:16:41 EST |
| bob-cli | [`3ba40fc`](https://github.com/bobs-org/bob-cli/commit/3ba40fc5444e0b593f5805d9af6742bfd989b953) | fix(stats): drop HomesEngine resolver borrow before remember | [bob-cli-kj.3](bob-cli-kj.3.md) | 2026-11-11 18:42:28 EST |
| bob-plugins | [`bob-plugins@d94c6bb`](https://github.com/bobs-org/bob-plugins/commit/d94c6bb4346fc9b02bfd6e70e826564a7e368fd0) | test: run wikilink CPU budgets in a serial npm test stage | [bob-cli-kj](README.md) | 2026-11-11 19:53:37 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-kj.2][1] | epic scope | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kj.2.md

<!-- sase:referenced-by:end -->
