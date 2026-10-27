# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.1 — Give Linux-launched agents a bounded precommit macOS CI check

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.1` · **Size:** large
**Created:** 2026-10-27 06:23:58 EDT · **Closed:** 2026-10-27 08:29:29 EDT
**Plan:** [202610/backlog\_batch17\_macos\_gate\_source\_backfill\_hook\_dedupe\_dirty\_scans\_swift\_format.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch17_macos_gate_source_backfill_hook_dedupe_dirty_scans_swift_format.md)

## Description

macos-precommit-gate: resolve bob-cli-by per the macos_gate decision with a scratch-branch macOS CI check for bob-cli and bob-mac-capture that never moves the checkout and always deletes its branch.

## Notes

[2026-10-27T11:11:16Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.1] Implementation (offline, pre-live-proof): identical stdlib Python gates at bob-cli scripts/dev/macos-ci-check and bob-mac-capture Scripts/macos-ci-check (byte-identical, with matching test_macos_ci_check.py copies). Profiles: bobs-org/bob-cli job "test (macos-latest)" required Lint macOS-only targets / Run tests / Run archive-move presenter cases; bobs-org/bob-mac-capture job "macOS 26 SwiftPM" required Lint Swift formatting, Build, Test, Bundle, Verify plist and signature, Launch smoke test, Install and reinstall. Snapshot uses a temp GIT_INDEX_FILE (read-tree HEAD, add -A, write-tree, commit-tree -p HEAD) and a create-only push to refs/heads/ci/precommit/<id>; origin is git config --get-all remote.origin.pushurl then .url. Offline unittest 35/35 in both repos; just check-scripts both; bob-cli just check green; Mac Capture just portable-check 1695 tests passed; BOB_DOCS_BOB_MAC_CAPTURE_DIR just docs-check 173 pages, 447 pytest passed + 1 skip. Mac Capture CI on.push.branches includes ci/** and a Check scripts step before Swift. Live-proof base HEADs: bob-cli c2b6908913d8350cbefa9115da676499259e9f50, bob-mac-capture 0e7eba439a5c59b2fecc67917b8f36dcf479e2f1. Index sha256: bob-cli 6304fbdc85f1d596637d447df78eed6a8e1d30f2dc265c42e3dd46591595877c, bob-mac-capture 705afe664462510804b4e49db350e4e2e69162ba2e16c37c789c5d928a07213c. Live proof of one scratch CI run per repo (including uncommitted gate files) is in progress via sase monitor; the follow-up records run URLs, every macOS step, process exits, HEAD/index/worktree before-vs-after, and independent remote-ref absence.

PROPOSED FOLLOW-UP: incorporate macos-ci-check into agent guidance — after the lander obtains memory authorization, update sase.md (and related agent instructions) so Linux-launched agents run the packaged precommit macOS gate (scripts/dev/macos-ci-check / Scripts/macos-ci-check) through /sase_monitor before landing Mac/AppKit work, and still watch GitHub Actions to completion. Cites existing memory task bob-cli-1x. This phase must not edit AGENTS.md or memory notes.

[2026-10-27T12:29:29Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.1--4] Verified one live scratch CI run per repo with macos-ci-check on the leftover-command-budget-fixed tree (monitor 1gkqm0pkk6zz, combined exit 0, 15m 26s). Script copies remain byte-identical (scripts/dev/macos-ci-check == Scripts/macos-ci-check; matching test_macos_ci_check.py copies). Offline tests after the leftover-budget fix: python3 -B scripts/dev/test_macos_ci_check.py 40 OK; Mac Capture copy 40 OK; Scripts/test_docs_scripts.py 8 OK.

bob-cli (exit 0):
- repository bobs-org/bob-cli
- base SHA c2b6908913d8350cbefa9115da676499259e9f50
- snapshot SHA 9ba368a23e6856dfe652cac2f7c6079ee75c79db
- remote branch ci/precommit/0a6429e2c177c80c665c6b86e1935740 (deleted after the run)
- run URL https://github.com/bobs-org/bob-cli/actions/runs/40501382150 (independent gh run view: conclusion success, event push, headSha 9ba368a23e6856dfe652cac2f7c6079ee75c79db; jobs package/lint/test (ubuntu-latest)/test (macos-latest) all success)
- macOS job test (macos-latest) steps: Set up job ok; Check out ok; Install pinned toolchain ok; Cache Rust ok; Install just ok; Install uv ok; Install macOS bash 5 ok; Install full-test tools skipped; Lint macOS-only targets ok; Run tests ok; Run archive-move presenter cases ok; Post Install uv ok; Post Cache Rust ok; Post Check out ok; Complete job ok
- failed_non_macos_jobs: none
- HEAD/index/worktree before vs after unchanged: HEAD c2b6908913d8350cbefa9115da676499259e9f50; .git/index sha256 6304fbdc85f1d596637d447df78eed6a8e1d30f2dc265c42e3dd46591595877c; status still M docs/develop/ci.md, M justfile, ?? scripts/dev/macos-ci-check, ?? scripts/dev/test_macos_ci_check.py
- independent git ls-remote origin refs/heads/ci/precommit/* after the proof: empty (our hash-named scratch branch is gone)

bob-mac-capture (exit 0):
- repository bobs-org/bob-mac-capture
- base SHA 0e7eba439a5c59b2fecc67917b8f36dcf479e2f1
- snapshot SHA be1413e3d382d48ba374a096d61496d23cb7e6bf
- remote branch ci/precommit/5ce91e97c3bcc48be5b0e260fd76f79c (deleted after the run)
- run URL https://github.com/bobs-org/bob-mac-capture/actions/runs/40501379782 (independent gh run view: conclusion success, event push, headSha be1413e3d382d48ba374a096d61496d23cb7e6bf; job macOS 26 SwiftPM success)
- macOS job macOS 26 SwiftPM steps: Set up job ok; Check out repository ok; Check scripts ok; Show toolchain ok; Lint Swift formatting ok; Build ok; Test ok; Upload render fixtures ok; Upload test hang samples skipped; Bundle ok; Verify plist and signature ok; Launch smoke test ok; Upload launch smoke test diagnostics skipped; Install and reinstall ok; Post Check out repository ok; Complete job ok
- failed_non_macos_jobs: none
- HEAD/index/worktree before vs after unchanged: HEAD 0e7eba439a5c59b2fecc67917b8f36dcf479e2f1; .git/index sha256 705afe664462510804b4e49db350e4e2e69162ba2e16c37c789c5d928a07213c; status still M .github/workflows/ci.yml, M Scripts/test_docs_scripts.py, M docs/develop/ci.md, M justfile, ?? Scripts/macos-ci-check, ?? Scripts/test_macos_ci_check.py
- independent git ls-remote origin refs/heads/ci/precommit/* after the proof: our hash-named scratch branch is gone. A concurrent unrelated ref refs/heads/ci/precommit/per-pdf-dirty-scan-20261027T122338Z-4063044 (created after this proof finished at 12:23:23Z) was left untouched.

Prior live proofs that found and fixed gate defects (not clean-base CI failures):
1. monitor ep13g3g1by5y exit 2 in 7.8s: gh 2.103 colorized empty JSON under CLICOLOR_FORCE=1. Fix: colorless child env + parse_json strips ANSI.
2. monitor qcyqvpke5ypj: bob-cli exit 0 on run 40496091203; bob-mac-capture exit 1 on run 40496089258 because Check scripts compared Path(__file__).resolve() (/private/var/folders) to git rev-parse --show-toplevel (/var/folders). Fix: resolve git toplevel before containment, Path.relative_to, resolve temp-index path, test_logical_checkout_path_is_resolved.
3. monitor kcsgq0ync1rs: bob-cli exit 0 on run 40498141069; bob-mac-capture exit 1 on run 40498140327 because leftover discovery started gh run list with a 0.1s timeout that macOS CI spawn exceeded. Fix: command_timeout refuses leftover below min(1s, command cap); wait_for_matching_run reports no matching instead of timed out; short discovery overrides removed.

PROPOSED FOLLOW-UP already on this phase cites existing memory task bob-cli-1x to incorporate macos-ci-check into agent guidance after the lander obtains memory authorization. AGENTS.md and memory were not edited. bob-cli-by, bob-cli-1x, the parent epic, and ancestor plan beads are left for the lander. epic-symbols: no leftover --epic-symbol entries for this phase.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.1.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.1](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`79b2859`](https://github.com/bobs-org/bob-cli/commit/79b2859d6fcb4b3efee5a908d048377e58f3eba9) | feat(ci): add macos-ci-check scratch-branch precommit gate | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.1](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.1.md) | 2026-10-27 08:30:41 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.1--4][1] | Need current phase notes, PROPOSED FOLLOW-UP, and status before recording live-proof evidence and closing | 1 |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.land][2] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.1.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.land.md

<!-- sase:referenced-by:end -->
