# Bead: bob-cli-c9.5.1 — Annotated reference overwrite on the Mac

[Bead Pages](../README.md) / [bob-cli-c9.5](bob-cli-c9.5.md) / bob-cli-c9.5.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-c9.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-c9.5.md) · **Assignee:** `bob-cli-c9.5.1.land`
**Created:** 2026-10-26 07:41:50 EDT · **Closed:** 2026-10-26 11:57:13 EDT
**Plan:** [202610/annotated\_reference\_overwrite.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/annotated_reference_overwrite.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/annotated_reference_overwrite.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 7 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/annotated_reference_overwrite.md

<!-- sase:links:end -->

## Description

Annotated reference overwrite preserves old PDFs, assets, anchors, and reading-task identity through coordinated Mac transactions, rejects unsafe hosts, and protects scans and recovery from stale editor writes.

## Notes

[2026-10-26T15:09:25Z · bob-cli-c9.5.1.land] LANDER FOLLOW-UP TRIAGE (bob-cli-c9.5.1.land): (1) bob-cli-c9.5.1.1 note #2 and (2) bob-cli-c9.5.1.3 note #1 (capture_related synthetic-vault perf gate flake) — declined as duplicates of bob-cli-ca, which 7b8c5ddb fixed (closed 2026-10-26T13:56Z); both observations predate that fix landing in the workers' trees and the landing just check on 8a1679e5 passed the full lib suite (3584 passed), so no +1/reopen. (3) Landing-discovered pre-existing CI failures (highlights_create_collection_overwrites_exact_set_with_listen pre-syncs default ~/bob; force_adopted_empty_target exit 1 vs 2) were introduced by bob-cli-c9.4.1.7 / c9.3.1.1, so per /sase_new_task they were recorded as a DISCOVERED ISSUE note on active epic bob-cli-c9, not a task. (4) Parent phase bob-cli-c9.5 note #1 (missing recapture research reference) is not a child-of-this-epic proposal; it stays for the bob-cli-c9 land agent. (5) Review findings declined without filing: open-note-task embed exemption breadth (is_embed_task_line predates this epic in c9.4; narrowing could newly refuse legacy embeds and no walker harm was demonstrated); guard I/O error aborting a whole scan and repeated per-PDF archive hashing (speculative, low impact); Linux dry-run previewing an annotated archive (intended by acceptance tests); '0 highlights' wording for assets-only/inbound-only refusals (plan-prescribed text). Epic-caused defects found in review go to the landing tale.

[2026-10-26T15:12:01Z · bob-cli-c9.5.1.land] LAND REVIEW (bob-cli-c9.5.1.land) at 92706cb4: Read epic plan, all 5 phases and notes, commits e4825208/564168f3/af416080/ca6065af/8a1679e5 and the code. just check on 8a1679e5 passed on athena (lib 3584, cli 2206). Outside commits since e4825208 (7b8c5ddb perf gate fix, 69dfd7e8/3633a10a stats, 01f7ec97 .bob walker exclusion, c7ced497 render-time code catalog, 92706cb4 completion) need no integration change; overwrite/source-store integration is owned by in-progress bob-cli-cc.5 (coordination note added there). Epic-symbols empty; no symvision recipe. Remaining epic-caused work blocks closing: (1) macOS CI red on ca6065af: /var->/private/var canonicalization (checked_vault_path canonical path stripped against non-canonical bob_dir) puts absolute .assets paths in intents and drops annotated assets; also non-cfg-gated key-on test and overwrite_web host-text asserts; (2) task_line_index/find_task_line match ^block_id by substring (^ref-x matches ^ref-x-v2); (3) recovery reverse rename coordinates the absent live path instead of the archive, falls back uncoordinated on config error, proves hashes outside the accessor, uses check-then-fs::rename, and fail-closed errors lack the required recovery hint; (4) frozen note/replacement PDF published non-atomically (partial write strands the intent); (5) earlier archives' PDFs/assets are in intent.touched and get git-checkout restored on rollback, discarding late saves; (6) ambiguous inbound #^h- links never reported and dangling ones fail verify after mutation; (7) docs list editor_active as overwrite hold, '1 highlights', link count includes self-links, frozen parent from ref_type, guard ignores digest if archived PDF missing, verbose scan omits execution-time holds, dead integrity_fingerprint check; (8) annotated failpoint sweep missing (AfterAssets never armed). Proposing a medium tale that fixes these and performs same-turn closeout of bob-cli-c9.5.1 and phase bob-cli-c9.5.

[2026-10-26T15:57:13Z · bob-cli-c9.5.1.land--1] Reviewed all five closed phases and their notes: archive, scan guard, recovery, execute, and acceptance. Landed fixes cover symlink-canonical vault-relative paths, exact task block IDs, coordinated no-clobber recovery with in-accessor ownership proof and recovery hints, atomic file publication, preservation of older archive bytes on rollback, reporting and verification of ambiguous/dangling highlight links, docs/count/parent/digest/verbose-scan fixes, and the annotated failpoint sweep.

Verification: `just check && just check-scripts && just docs-gen && just docs-check` completed with exit 0. `just check` passed formatting, lint, and tests: 3,607 library tests passed (0 failed, 1 ignored), 2,213 CLI tests passed, and all remaining integration suites passed. `just check-scripts` passed, including the Highlights acceptance kit self-test (10 checks) and install migration checks. `just docs-gen` completed. `just docs-check` passed all implemented gates: 447 passed, 1 skipped because font generation dependencies were absent. `just --list` has no symvision recipe.

Linux verified the symlinked-temp regression and platform-aware refusal/cfg behavior; macOS execution and CI were not run. Real Highlights acceptance remains Bryan manual Mac work and is pending. Reviewed outside commits 7b8c5ddb, 69dfd7e8, 3633a10a, 01f7ec97, c7ced497, 92706cb4, and newer 0bec19d8; no integration changes are needed. Source-store overwrite integration remains owned by in-progress bob-cli-cc.5; its coordination note was verified. Prior triage remains: capture_related reports were duplicates of bob-cli-ca and 7b8c5ddb resolved that issue; the two pre-existing ~/bob-dependent failures are recorded on bob-cli-c9; the other review findings were declined as documented. Parent phase bob-cli-c9.5 note #1 remains for the bob-cli-c9 land agent.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-c9.5.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-c9.5.1.land.md) | [bob-cli-c9.5.1](bob-cli-c9.5.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`38a02d7`](https://github.com/bobs-org/bob-cli/commit/38a02d7bd6342d7a431b4cebf108df53b44b12f1) | fix(highlights): resolve annotated overwrite landing findings | [bob-cli-c9.5.1](bob-cli-c9.5.1.md) | 2026-10-26 11:59:10 EDT |
| bob-cli--plans | [`bob-cli--plans@90cb827`](https://github.com/bobs-org/bob-cli--plans/commit/90cb8277caac8adcc7a12c5b0c03e43803ff5064) | docs(plan): mark annotated overwrite complete | [bob-cli-c9.5.1](bob-cli-c9.5.1.md) | 2026-10-26 12:00:17 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.land][1] | Check plan ownership overlap with batch-12 candidates | 3 |
| read-by | [agent:bob-cli-c9.5.1.1][2] | Need parent epic DECISIONS and child phase context | 1 |
| read-by | [agent:bob-cli-c9.5.1.2--1][3] | Need the parent epic DECISIONS and sibling phase coordination before implementing this phase | 1 |
| read-by | [agent:bob-cli-c9.5.1.3][4] | Need parent epic scope and decisions | 1 |
| read-by | [agent:bob-cli-c9.5.1.4][5] | Need the epic decisions governing the annotated reference overwrite phase | 1 |
| read-by | [agent:bob-cli-c9.5.1.5][6] | Need epic DECISIONS and remaining work for acceptance phase | 1 |
| read-by | [agent:bob-cli-c9.5.1.land--1][7] | Verify the landing bead scope, phase set, and prior triage before closeout | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.land.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.5.1.1/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-c9.5.1.2.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.5.1.3/README.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.5.1.4/README.md
[6]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.5.1.5/README.md
[7]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-c9.5.1.land.md

<!-- sase:referenced-by:end -->
