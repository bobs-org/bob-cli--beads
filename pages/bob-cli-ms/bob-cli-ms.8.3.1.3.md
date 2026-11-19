# Bead: bob-cli-ms.8.3.1.3 — Verify live record coverage and the final deployed build

[Bead Pages](../README.md) / [bob-cli-ms.8.3.1](bob-cli-ms.8.3.1.md) / bob-cli-ms.8.3.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ms.8.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ms.8.3.md) · **Assignee:** `bob-cli-ms.8.3.1.3` · **Size:** medium
**Created:** 2026-11-18 08:59:24 EST · **Closed:** 2026-11-19 07:03:14 EST
**Plan:** [202611/record\_card\_obsidian\_proof.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/record_card_obsidian_proof.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:0f30e6da56a61167008fb26b | attached via sase artifact create --bead |
| related | file:explicit:1989925b303385554af4b7ee | attached via sase artifact create --bead |
| related | file:explicit:6c29e2ed7ad7cd9f4e9a88db | attached via sase artifact create --bead |
| related | file:explicit:8e1f53f2d73873a2908568ea | attached via sase artifact create --bead |
| related | file:explicit:925b70926af44650172dea5b | attached via sase artifact create --bead |
| related | file:explicit:d49f87761753c59199815bbc | attached via sase artifact create --bead |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

coverage-release: add and run the read-only per-record coverage audit, run the complete walkthrough and repository gates against the final tree, deploy without force, and publish the final acceptance and deployment evidence.

## Notes

[2026-11-19T09:20:59Z · bob-cli-ms.8.3.1.3] Implemented the reusable read-only audit in opened bob-plugins scripts/record-card-vault-coverage.py with registered Node offline wrapper and 23 Python tests, all passing. Uses installed PyYAML SafeLoader composition, preserves duplicate-key evidence, rejects malformed/non-string/merge/custom/cyclic structures explicitly, handles nested/quoted values, independently scans all non-hidden Markdown plus album-folder occupants and cross-checks bob albums list. Only albums list and records show are executed; report must be outside vault, subprocesses bounded, each authored key requires exactly one home, absent schema rows are separate, findings require exact path/code/field rationale with stale entries refused. Whole-Markdown before/after hashes detect concurrent edits and retry at most twice without falsely claiming original neutrality. No product behavior/version/memory edits. Source bases fetched/ff-checked: bob-cli e07a26bf and bob-plugins b88bc46; installed Bob 0.5.0 already contains prerequisite literal-value repair. Current read-only albums listing reports 193 records across six albums (104 eat,12 movies,15 podcasts,11 sase_blog_zettel,28 subscriptions,23 tv); this is preliminary and not yet independent coverage proof. Prior phase accepted all144 assertions at run16 and deployed 1.140.0/2.88.0/0.2.0; audited final evidence file:explicit:c7152b287d5c14283393fafe. No epic-symbol entries on this phase. Local .build/record-coverage/verify.py reuses inspected orchestration from this same workspace, isolates both Cargo target and build dirs, runs current/base gates, newly built-binary live audit, exact-source remote full walkthrough and captures provenance/logs/screenshots. Long verification must run through sase_monitor next. Remaining bounded work: inspect every new log/report and PNG, investigate live findings explicitly (never blanket allowlist or mutate vault), repair only new attributable failures, register final artifacts, refresh/rebuild before explicit --repo opened-linked --no-pull non-force sync, mandatory isolated deployed-vault startup smoke/all31 managed hashes including ledger-tools/navigation/command-mode, then close ONLY this phase. Existing .build/record-workflows/postsync16.py documents the previously successful fixed-command loopback reverse-tunnel smoke transport; adapt paths/run identity, never borrow old evidence as new. Preserve known baseline-identical date-sensitive tick failures and timing reds honestly; new followups only via PROPOSED FOLLOW-UP on this bead. No new beads or ancestor closure. This is a verification checkpoint with the audit coding complete, not abandonment; monitor successor can finish the remaining evidence/deployment work.

[2026-11-19T10:46:11Z · bob-cli-ms.8.3.1.3--1] PROPOSED FOLLOW-UP: Fix the ownership of sase_blog_zettel/sase_is_too_complex.md — independent live audit discovers 193 records but this record has parent pointing to the vault root instead of its album. Current e07a26bf binary and clean-base 3617c2ea binary both exit 2 with record_parent_mismatch on unchanged SHA256 af803e16edf35f44a53576a0efd44f0ad673aedc41b30b0caec088e2dfb6d3ca. Seven authored keys remain unverified by records show. Live Markdown was not mutated and no warning allowlist masks this failure. Evidence file:explicit:925b70926af44650172dea5b; classification is an existing data rejection under the phase baseline-identical-failure policy.

[2026-11-19T10:46:26Z · bob-cli-ms.8.3.1.3--1] PROPOSED FOLLOW-UP: Corroboration for existing bob-cli-nf — the new run-20261119-092200 has the same 12 tick:: failures and identical normalized assertion bodies under just check on current e07a26bf and clean 3617c2ea; both fixed-date BOB_NOW=2026-11-18 12:00:00 tick-only controls pass all 19 cases. Preserve the full raw failures and cli-failure-comparison.json. No new tick implementation work in this phase; land agent should attach the evidence to bob-cli-nf, not duplicate it.

[2026-11-19T10:49:06Z · bob-cli-ms.8.3.1.3--1] Review checkpoint: run-20261119-092200 full CDP proof passes all 144 assertions, no skips or console exceptions. All 25 new PNGs were viewed directly and exact-hash verdicts saved in screenshot-review.json; retained native identity/other rows are intentional, initial wide capture is actually 1024px, and dense Schema Card footer/plain URL input are recorded honestly. Full gate/baseline logs indexed in gate-review.json; two timing-budget reds reproduce on clean plugin base and 12 tick failures reproduce identically on clean CLI base (tracked bob-cli-nf). Audit discovered 193 canonical records/1989 keys: 192 reads succeed and one existing parent mismatch leaves seven keys unverified, now separately documented with baseline evidence and PROPOSED FOLLOW-UP. Original global churn failure is repaired with conservative per-invocation reuse: all paths/frontmatter/album/record bytes are dependencies; only ordinary body changes can reuse successful reads, rejected reads always retry, and a full final snapshot must settle. All 28 offline cases pass. No live Markdown, product behavior, versions or memory changed. Final upstream fetch currently shows no new commits. Staging .build/record-coverage/reverify.py through sase_monitor for affected gates, fresh live audit and full UI, final refresh/rebuild, explicit non-force dry-run/sync, isolated pre/post smoke and all31 managed hashes; adapted .build/record-coverage/postsync.py uses the previously verified fixed-command loopback reverse-tunnel transport. Successor must inspect every NEW release PNG, publish all evidence and accepted exceptions, run epic-symbols and close ONLY this phase. This is a normal bounded verification continuation, not a new planning task.

[2026-11-19T11:33:34Z · bob-cli-ms.8.3.1.3--2] Release-20261119-105232 stopped before UI, smoke or deployment: raw live audit again enumerated193 records/1989 keys, with192 successful reads and1982 covered keys. The same unchanged parent mismatch leaves7 keys uncovered; the only other failure is unstable whole-vault snapshots across all3 attempts (all193 reads reran each time). No new record findings, live Markdown changes or new PNGs. Full current plugin suite has only the baseline-proven frees timing red; build, validate, docs generation and docs check passed. Failure audit, all raw gate logs, source hashes, orchestration and investigation are preserved at file:explicit:8e1f53f2d73873a2908568ea. Repaired audit runtime with bounded8 read-only subprocesses, serial result/cache collection, route deduplication without dropping discovered records, unchanged conservative dependency invalidation and stable-final-snapshot requirement.31offline cases plus registered Node wrapper pass;8 real read-only probes completed in2.675s. Staging reverify.py with --workers8 --retries5 for all affected gates and full acceptance/deployment. Remains in progress; successor must inspect every NEW PNG, publish final acceptance with raw exceptions, verify pre/post isolated startup and all31 deployed hashes, run epic-symbols and close ONLY this phase. No new beads, ancestor closures or memory edits.

[2026-11-19T12:03:14Z · bob-cli-ms.8.3.1.3--3] Accepted coverage-release after review of release-20261119-113453 (monitor 5w47echahe5x, tool run 39be9acc44fd917fdc237d94390f97c3). Full evidence: file:explicit:1989925b303385554af4b7ee; archive SHA256 0d36013369ed13acacc9f2accdc286ece68f70e8cd24cc862ec73b2a8e4614a5, 127 files plus nested 69-file prior evidence. All raw reports, commands/exits, baseline logs, source manifest/archive, CLI bundle, orchestration copies and new PNGs are retained. Standalone final acceptance report: file:explicit:6c29e2ed7ad7cd9f4e9a88db.

Implemented read-only independent coverage audit in bob-plugins using PyYAML, eight bounded subprocesses, dependency-checked reuse and a required stable final full snapshot. All 31 offline cases and registered Node wrapper pass. Final scan counted 6931 Markdown files and 193 canonical records across six albums; 192 reads succeeded and 1982/1989 authored keys have exactly one home. Attempts 1 and 2 observed daily-note body edits; attempt 3 settled with equal full before/after hashes. This is not an entire-run byte-neutral claim. Raw audit remains exit 1/pass false: unchanged sase_blog_zettel/sase_is_too_complex.md, SHA256 af803e16edf35f44a53576a0efd44f0ad673aedc41b30b0caec088e2dfb6d3ca, is rejected with exit 2/record_parent_mismatch on parent by both final and pristine-base binaries. Seven keys remain uncovered: claim, created, parent, section, status, title, type. Existing PROPOSED FOLLOW-UP and file:explicit:925b70926af44650172dea5b remain authoritative. No live Markdown writes or blanket allowlist.

Fresh real Obsidian full CDP run passes 144/144 assertions with zero skips or console exceptions. Directly viewed every one of the 25 new PNGs using view_image; screenshot-review.json records exact SHA256/dimensions and individual observations. Initial wide captures are actually 1024px; dense Schema Card footer and plain URL input are recorded limitations. Scratch write/undo/refusal byte evidence and passive note hashes pass.

Final exact CLI source e07a26bf86b93fe12df571ac6cb00f8b71d28cca, no source patch; Bob 0.5.0 binary SHA256 0c43504dad27a160cc4ce311e090d2c9e591d29f93834f08014699904734b639. Plugin base b88bc46423e08851fb97ba6dfa7115fb1370a547 plus five audit/test/docs changed files; 1412-file manifest SHA256 8f5edc7472eb7b258e365905d64f25580494e0e43f7e4204d7ee7161aae0e7b1 matches current and transported source. npm build/docs:gen/validate/docs:check and cargo build pass. Full npm test retains only the same two clean-base timing failures (event-link-times and frees-marks); unit counts 7377 pass/2 fail/3 skip, separate perf 5/5. Exact unchanged CLI just check evidence remains exit 101 with the same 12 normalized tick failures as clean 3617c2ea, tracked bob-cli-nf; both fixed-date controls pass 19/19. Raw nonzero exits and

… and 1362 more characters

## Dependencies

- **Depends on:** [bob-cli-ms.8.3.1.2](bob-cli-ms.8.3.1.2.md) ✓ · ⧖ 2026-11-18

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ms.8.3.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ms.8.3.1.3.md) | [bob-cli-ms.8.3.1.3](bob-cli-ms.8.3.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@36d4801`](https://github.com/bobs-org/bob-plugins/commit/36d48017f9a16edaf21346fb0276c530836e08f4) | test(records): add read-only live vault coverage audit | [bob-cli-ms.8.3.1.3](bob-cli-ms.8.3.1.3.md) | 2026-11-19 07:04:44 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-n7.land][1] | Check whether its date-sensitive tick failure note already tracks the tick fixture defect | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-n7.land/README.md

<!-- sase:referenced-by:end -->
