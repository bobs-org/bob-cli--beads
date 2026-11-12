# Bead: bob-cli-kd.4.1 — Weekly bank import with deterministic matching and one guarded commit

[Bead Pages](../README.md) / [bob-cli-kd.4](bob-cli-kd.4.md) / bob-cli-kd.4.1

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-kd.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kd.4.md) · **Assignee:** `bob-cli-kd.4.1.land`
**Created:** 2026-11-11 14:24:04 EST
**Plan:** [202611/bank\_import.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_import.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/bank_import.md][1] | derived from the plan's `bead_id:` frontmatter field |
| related | file:explicit:0f0772d7cfd9fab573bd4a19 | attached via sase artifact create --bead |
| related | file:explicit:f1a42eafbd40c70d5d0a8f74 | attached via sase artifact create --bead |

_Plus 7 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_import.md

<!-- sase:links:end -->

## Description

Complete bob-cli-kd.4: import posted Wells Fargo QFX/OFX and CSV transactions once, preserve typed rows and edits, journal private identities, and install the Monday PRE chore after the command is verified.

## Notes

[2026-11-12T01:48:43Z · bob-cli-kd.4.1.land] FOLLOW-UP TRIAGE (complete before repair proposal): kd.4.1.1 #1 and kd.4.1.2 #2 (vault_git items_after_test_module) are resolved by 6e3d8837; source order is fixed, so declined a new task. kd.4.1.2 #1 and kd.4.1.3 #1 were corroborated on bob-cli-g8 (+1), with coordination evidence on active bob-cli-3j (existing note #15). Declined a separate date-aging task: tests/cli/capture/complete_themes.rs::command explicitly pins BOB_NOW=2026-10-24 08:00:00; the late-date explanation is unsupported, while the 150ms deadline omission remains. kd.4.1.4 #1 splits into the two existing anchor defects, corroborated on bob-cli-kk (+1), and the yank-flash mounted-link defect, noted on active bob-cli-kb after reading kb.1. No duplicate task created. kd.4.1.4 #2 (live bank journal allowlist/union gap) remains import-epic integration work and is retained in the repair plan, not filed separately. Corrected its claimed consequence: ob::commit_paths explicitly git-adds the journal and host_catalog::txn rolls both append and rows back on staging failure; code does not silently omit the journal. Recent all-status task sweep and all 16 active epic scopes were checked. These corroborations relay independent phase evidence, not a fresh full-suite/docs-check reproduction.

[2026-11-12T01:53:30Z · bob-cli-kd.4.1.land] LANDING AUDIT / NOT READY: Read the epic (no prior notes), all four children and all ten child notes, original plan:202611/bank_import.md, parent phase kd.4 and final checking-only/discretionary-subscriptions/glossary-only-outer-wrap-up DECISIONS. Reviewed source and commits bffbf36b, ee2d2cbf, d9f0539f, b8c71181. Hashes, account resolution, journal masking/fold/read guards, exact-cent/window typed matching, ordered append plus scoped commit/rollback, dispatch/catalog/completion, additive JSON, docs, and unchanged-row ownership are implemented. Fresh cargo test --lib native::bank:: passes 92/92; host_catalog::txn:: passes 13/13. No fresh just check or docs-check in this audit-only turn; phase green gates are historical evidence. Never ran check-full. Live read-only bob query confirms exactly one Bank import task in gtd_daily, #gtd #pre, repeat every week on Monday when done, scheduled 2026-11-16; no chore mutation.

Synthetic installed-CLI probes plus source inspection confirm remaining defects: (1) truncated/misnested OFX aggregate containers accepted and missing STMTTRN close swallows the next transaction; (2) same alias/FITID with conflicting money across files is silently seen, with equivalent unchecked existing-journal shortcut; (3) duplicated unjournaled bank IDs create a third financial row; (4) new day headings reparent trailing prose/checklists; (5) registry eat->restaurants emits an eat/ link and guards the wrong directory; (6) merchant keys omit cleaning, so SQ * versus TST* defeats learned payees. Journal setup reported in .4 #2 also remains. Retained as epic work in medium tale sase_plan_bank_import_landing_repairs.md, not follow-up tasks. Script file:explicit:f1a42eafbd40c70d5d0a8f74; output file:explicit:0f0772d7cfd9fab573bd4a19. The current tests include false assurances: duplicate_ids expects the third row and BOM/prose test checks substring survival rather than day ownership.

INTEGRATION: fetched origin/master and reviewed non-epic history from bffbf36b parent through 0d2f433d (HEAD equals fetched base). Albums index/catalog and record writes now use the shared transaction; appends=[] and new ReadDependencies::extend retain all dependency kinds. Preserve those in repairs. Newer 03a0aba2 fixed ensure cursor-after-children, not whole-day ownership; parent kd already tracks that defect, and a coordination note there records this import reproduction. 04cba0fa configured-timezone timestamps are compatible with import now_stamp. Script/glob/sync, plugin deploy, notebook capture menu, Keep-moving, and stats fixes introduce no additional bank consumer requiring edits. Restaurant registry path propagation is the concrete integration gap. No production integration edit made in this planning turn.

SYMBOLS/CLOSEOUT: epic-symbols kd.4.1 and kd.4 both empty; no symvision recipe. Do not close yet or mark original plan done. Validated tale ends with fresh verification, exact symbol cleanup, normal kd.4.1 close, optional symvision, original plan 202611/bank_import.md status done, and normal close of phase kd.4 only. Outer kd remains for its waiting land agent. No closeout dependency on the repair commit SHA/push/CI. All follow-up outcomes are in the preceding TRIAGE note and must be carried into the eventual close note.

[2026-11-12T02:52:29Z · bob-cli-kd.4.1.land] LANDING REPAIRS IMPLEMENTED; LIVE VAULT SETUP BLOCKED. Added aggregate-boundary refusal, immutable money identity checks, duplicate unjournaled-ID refusal, whole-day section placement, configured restaurant paths/dependencies, cleaned merchant learning, and real-apply ignored-journal refusal with regressions and docs. Fresh results: native::bank 106/106, host_catalog::txn 13/13, notebooks 49/49, albums 65/65; just docs-gen passed. just docs-check passed lint and generated drift but strict build reports three known broken references (bob-vim-yank-flash.md#verification, task-dependencies.md#1217-lp---leaf-vector, gcal.md#events). Required just check is handed to monitor for observed result. Concrete blocker: supported SASE project/repo inventory has no brokerable live Bob vault reference, so the required .bob/bank/*.jsonl .gitignore allowlist and union .gitattributes rule could not be applied or verified with check-ignore/check-attr; do not bypass by accessing ~/bob. Keep this epic open until the narrow live-vault policy step is completed. epic-symbols returned no entries for this epic or kd.4; Justfile has no symvision recipe.

[2026-11-12T03:07:29Z · bob-cli-kd.4.1.land--1] REQUIRED GATE RESULT: monitored `just check` (ToolRun 5a7d51346f33f6981050349b553e722d; monitor afdtjmdcq2b4) failed, exit 101, started 2026-11-12T02:53:05.505430-05:00, finished 2026-11-12T03:00:06.858520Z, elapsed 6m 5s. Two unrelated test failures: `bob-obsidian --lib` 6693 passed / 1 failed / 3 ignored in 30.01s: `native::subprocess_runner::tests::run_bounds_pipe_drain_when_detached_grandchild_holds_output`, `src/native/subprocess_runner.rs:462`, `output.stderr.contains("output truncated")` was false. `bob-obsidian --test cli` 3603 passed / 1 failed in 84.34s: `capture::complete_themes::configured_shell_describes_never_used_and_unconfigured_create`, `tests/cli/capture/complete_themes.rs:308`, expected the `your type · never used` hint but captured stdout was empty. These source/test files are unchanged and outside the bank repair diff; no bank code failed. The capture failure matches the pre-existing completion-test deadline omission recorded in the prior triage note. Treat this as an unrelated baseline/environment-sensitive red gate, not a bank-import regression. Keep this epic open: live Bob vault `.gitignore` allowlist and `.gitattributes` union rule remain unverified because no supported SASE inventory reference brokers that repo; do not access `~/bob`.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kd.4.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kd.4.1.land.md) | [bob-cli-kd.4.1](bob-cli-kd.4.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`ae6a28d`](https://github.com/bobs-org/bob-cli/commit/ae6a28d07c023ab7ee8bd518d0fcff26739e4178) | fix(bank): harden import planning and recovery | [bob-cli-kd.4.1](bob-cli-kd.4.1.md) | 2026-11-11 22:08:28 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-kd.4.1.1][1] | Need parent epic DECISIONS and remaining work notes | 1 |
| read-by | [agent:bob-cli-kd.4.1.4][2] | check child epic phases status | 1 |
| read-by | [agent:research.49.cld][3] | research: user guide for first-time bank ack and e2e test of bob-cli-kd | 1 |
| read-by | [agent:research.49.final][4] | Check sub-phase state and any notes for the consolidated kd e2e test gating | 1 |
| read-by | [agent:research.49.gem][5] | Understand phase 4.1 import implementation status | 1 |
| read-by | [agent:research.49.grk][6] | Need import child-epic phase list so the e2e scorecard is accurate | 1 |
| read-by | [agent:research.49.mus][7] | kd import child epic status for guide | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.4.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.4.1.4/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.49.cld/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.49.final/README.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.49.gem/README.md
[6]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.49.grk/README.md
[7]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.49.mus/README.md

<!-- sase:referenced-by:end -->
