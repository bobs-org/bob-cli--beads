# Bead: bob-cli-df.2.1.4.3.3 — Repair same-payload ancestry and remaining quarantine path gaps

[Bead Pages](../README.md) / [bob-cli-df.2.1.4.3](bob-cli-df.2.1.4.3.md) / bob-cli-df.2.1.4.3.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-df.2.1.4.3.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-df.2.1.4.3.land/README.md) · **Assignee:** `bob-cli-df.2.1.4.3.3.land`
**Created:** 2026-10-28 07:11:11 EDT · **Closed:** 2026-10-28 10:31:58 EDT
**Plan:** [202610/artifact\_link\_copy\_skew\_path\_repairs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/artifact_link_copy_skew_path_repairs.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/artifact_link_copy_skew_path_repairs.md][1] | derived from the plan's `bead_id:` frontmatter field |
| related | file:explicit:ab5d6c3294bc3abbcfb7bf7b | attached via sase artifact create --bead |
| related | file:explicit:e79819a22e42975e194405f7 | attached via sase artifact create --bead |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/artifact_link_copy_skew_path_repairs.md

<!-- sase:links:end -->

## Description

Preserve earliest provable history across skewed copies and reject unsafe quarantine paths before reads or writes are accepted.

## Notes

[2026-10-28T13:27:16Z · bob-cli-df.2.1.4.3.3.land] LANDING AUDIT (bob-cli-df.2.1.4.3.3.land): Phase same-payload-ancestry verified landed as sase-core 49870f00 (origin/master tip). Its occurrence-level ancestry now includes same-digest occurrences, and the winner and runner-up share compare_surviving_selection_order. Tests cover skew/permutations/relabel, offset ties, multi-generation copies, a competitor descendant, a three-payload group basis, and a PyO3 round trip. Phase quarantine-paths is NOT landed. Continuation bob-cli-df.2.1.4.3.3.2--1 closed the phase, but its finalizer had no opened-repo obligation, so it committed only beads. sase origin/master (a1d1ea04da) still pins 00fe29d5 and lacks the staging and operation-path fixes. The stranded diff was rescued from the released workspace and stored as file:explicit:ab5d6c3294bc3abbcfb7bf7b, and finalizer evidence as file:explicit:e79819a22e42975e194405f7. Remaining work: a lander tale. FOLLOW-UP TRIAGE: (1) bob-cli-df.2.1.4.3.3.1 #1 got a +1 on bob-cli-dh (27 std::env clippy, ToolRun 7bde9693). (2) bob-cli-df.2.1.4.3.3.2 #1 got a DISCOVERED ISSUE corroboration note on causal B4 bob-cli-df (_RecoveryAssessment, KNOWN 13ea2a46). (3) bob-cli-df.2.1.4.3.3.2 #2 got a +1 on bob-cli-dg (missing plans sidecar, run c22e8134). (4) The lander's own discovery became new bug bob-cli-dn (continuation agents lose opened-repo commit obligations, size large, related to bob-cli-cv). No proposal declined. Drift: sase 87d5270573/8f75f44e92 (ACE statistics splits) and a1d1ea04da (bead sidecar publication; one-line project_key pass in _artifact_link_commit.py) are unrelated, and bob-cli and sase-core have no competing changes. A toobig split agent is RUNNING on tests/sdd/test_artifact_link_quarantine_replay_evidence.py, so new tests must go in new files. epic-symbols are empty for this epic and every ancestor.

[2026-10-28T14:31:48Z · bob-cli-df.2.1.4.3.3.land--2] LAND EVIDENCE (land--2): sase HEAD a1d1ea04da (base 49ebcc5eba, diff applies cleanly), pin sase-core-revision.txt 49870f00ec162187b46d9d50ef92446eead31388; core checkout HEAD 65546fd2 contains 49870f00 (merge-base ok). Wheel: SASE_CORE_DIR install-venv monitor w26rka5dpsfb exit 0; .venv sase_core_rs 0.43.0 matches core Cargo 0.43.0, module .../site-packages/sase_core_rs/__init__.py, has artifact_link_collision_partition(request). Focused suites vs verified wheel: quarantine-IO+copy-skew+paths+recovery 24 passed; replay-evidence+store+core+health+quarantine+projection+reconcile+publisher 51 passed; outbox-drain+outbox-io+parked+CLI-link-add+link-health-doctor+binding-validation+plan-formatting 50 passed (total 125). Governed check ToolRun a88473fd41d6305e195f74a33bc40613 exit 1 with only 2 independent failures: symvision _RecoveryAssessment KNOWN witness 13ea2a464abef73b3eab4bfee9e624d7 (file untouched by diff, owned by bob-cli-df B4); plan-links invalid-root missing sase/repos/plans (path absent, diff touches only quarantine files, owned by bob-cli-dg, prior clean-base run c22e8134/ba742b70). fmt/ruff/mypy/docs-contract green per monitor log.

[2026-10-28T14:31:58Z · bob-cli-df.2.1.4.3.3.land--2] Verified core 49870f00ec162187b46d9d50ef92446eead31388 (core HEAD 65546fd2 contains it); sase HEAD a1d1ea04da pins 49870f00 and includes staging+operation-path checks (persist validates _QUARANTINE_STAGING via _walk_quarantine_components leaf_kind=directory; _scan_quarantine_tree reports top-level non-.json as corruption; 5 load/persist IO tests + live-staging/persist-paths/read-only/recovery modules). New coverage: store copy-skew B-wins with one finding (real Git histories), every unsafe namespace/operation/leaf/staging shape rejected on load+persist with no outside write (O_CREAT probe), snapshot+doctor report blocking corruption read-only, unsafe path cannot settle/drop outbox loser and repaired path settles once across retry+restart. Suites vs verified wheel (0.43.0, artifact_link_collision_partition present): 24+51+50=125 passed. Governed check a88473fd exit 1 only known-independents: symvision _RecoveryAssessment witness 13ea2a464abef73b3eab4bfee9e624d7; plans-sidecar invalid-root owned by bob-cli-dg (run c22e8134). Follow-ups already recorded: +1 bob-cli-dh for 3.3.1 #1; DISCOVERED ISSUE on bob-cli-df for 3.3.2 #1; +1 bob-cli-dg for 3.3.2 #2; new bug bob-cli-dn for stranded commit; none declined.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-df.2.1.4.3.3.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-df.2.1.4.3.3.land.md) | [bob-cli-df.2.1.4.3.3](bob-cli-df.2.1.4.3.3.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-df.2.1.4.3.3.1--3][1] | Need the parent epic decisions governing this phase | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-df.2.1.4.3.3.1.md

<!-- sase:referenced-by:end -->
