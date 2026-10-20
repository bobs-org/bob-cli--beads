# Bead: bob-cli-a0.2.1.7 — Finish the Bob docs toolchain landing fixes

[Bead Pages](../README.md) / [bob-cli-a0.2.1](bob-cli-a0.2.1.md) / bob-cli-a0.2.1.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-a0.2.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.2.1.land.md) · **Assignee:** `bob-cli-a0.2.1.7.land`
**Created:** 2026-10-19 21:02:59 EDT · **Closed:** 2026-10-19 22:16:19 EDT
**Plan:** [202610/docs\_toolchain\_landing\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/docs_toolchain_landing_fixes.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/docs_toolchain_landing_fixes.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 3 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/docs_toolchain_landing_fixes.md

<!-- sase:links:end -->

## Description

Fix the verified defects and acceptance gaps that the bob-cli-a0.2.1 landing audit found in bob-docs mounts, serve, lint, URL/link gates, and authoring templates, so the toolchain epic can close honestly.

## Notes

[2026-10-20T01:38:39Z · bob-cli-a0.2.1.7.land] LAND TRIAGE: Read all notes on phases bob-cli-a0.2.1.7.1, .2, and .3: no PROPOSED FOLLOW-UP entries. Also read all six parent phase beads and every note. Parent phase bob-cli-a0.2.1.1 note #1 (PDFKit public citation) was re-triaged with /sase_new_task: no duplicate task after same-type and all-type searches and the one-week sweep; corroborated the existing DISCOVERED ISSUE on active outer epic bob-cli-a0, which owns public citation follow-through. Related task bob-cli-8p is a memory decision, not the same remediation; bob-cli-85 is a rendering defect, not a citation duplicate. No task created. Parent phase bob-cli-a0.2.1.4 note #1 (HTTP-only fragment checking) remains DECLINED: its premise is false and its remediation is already part of this epic; offline lychee with --include-fragments --index-files index.html passed 3595 links with zero errors on this audit. The four remaining mount/serve defects found here are caused by this epic and will remain epic work in one medium tale; none is deferred as a task.

[2026-10-20T01:39:30Z · bob-cli-a0.2.1.7.land] LAND AUDIT at master d5c98a2a (fresh git fetch: origin/master identical). Read the epic plan, governing parent plan and inherited decisions, all three child notes and implementation commits 2c50df55/5cbfea1f/d5c98a2a, and all six parent child beads/notes. Verified the frontmatter stamp repair, symlink/stale guards, production checks, assembled-nav/exact-stamp lint, privacy/fence/ratchet fixes, widened scans, URL checks, offline fragments, templates and authoring changes. just docs-check passed: 168 tests, 27 contracts, 32 pages, 365 mentions, one curated URL, two search cases, lychee 3595 links/zero errors; live manifest gave first-publish 404 warning. just docs-build-material passed. git diff --check and tracked-tree status clean; no generated drift. No unrelated commits since this child started. Parent-era unrelated 24f43958 only changes the task-move contract (already registered and passing these gates); MIT license c7df845f agrees with decisions. Rust/check recipe and SASE memory untouched by this child. epic-symbols is empty for this epic, bob-cli-a0.2.1, and bob-cli-a0.2; symvision recipe absent. Remaining reproduced epic defects: (1) discover_repo accepts existing non-Git overrides/siblings and a Git sibling with the wrong origin, since those branches only check is_dir; the requested invalid-existing-source fixtures are absent. (2) Adding !docs/reference/plugins/guide.md after the directory ignore lets assemble write guide.md even though git check-ignore exits 1; only the synthetic probe is checked. (3) After cloning a local fixture remote, asking for branch missing emits offline/keeping cached with fatal: could not find remote ref and succeeds instead of rejecting configuration error. (4) mirror_docs_once permanently fails file-to-directory replacement with FileExistsError and reverse replacement with IsADirectoryError because it copies before deleting type conflicts. These are bounded mount/serve fixes for a medium tale, whose final step must close this epic, revalidate/close bob-cli-a0.2.1, then close phase bob-cli-a0.2 only. just check is still required after those fixes; just check-full was not run.

[2026-10-20T01:41:54Z · bob-cli-a0.2.1.7.land] REMAINING-WORK PLAN: Authored sase_plan_docs_mount_closeout.md as tier tale, size medium, covering only the four reproduced mount/serve defects and their fixtures, then combined docs-check/Material/just check verification and the full same-turn closeout. The final step explicitly closes this epic, marks plan:202610/docs_toolchain_landing_fixes.md done, revalidates and closes parent plan bob-cli-a0.2.1 and marks plan:202610/docs_toolchain.md done, then closes parent phase bob-cli-a0.2 while leaving bob-cli-a0 open. No dependency on this work own commit/push/CI and no force for successful nested landing. Follow-up triage is complete in the preceding note. Initial explained validation identified missing title/goal and inert tale parent_bead; corrected the schema and revalidated successfully.

[2026-10-20T02:16:19Z · bob-cli-a0.2.1.7.land] Verified all three phase notes and implementation, then completed source identity validation, per-output ignore checks, genuine offline cache handling, and file/directory live mirroring. just docs-check passed (185 tests, 27 contracts, 32 pages, 365 mentions, 1 curated URL, 2 search cases, lychee 3595 links/0 errors, live first-publish 404 warning). just docs-build-material passed with builder=material. sase tool run -- just check succeeded (ToolRun 7abae80366b58dd5710772574cfd5493). origin/master remained d5c98a2a with no post-start drift. Follow-up triage retained on this bead. epic-symbols empty; no just symvision recipe in this repo.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-a0.2.1.7.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.2.1.7.land.md) | [bob-cli-a0.2.1.7](bob-cli-a0.2.1.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`701dd78`](https://github.com/bobs-org/bob-cli/commit/701dd78302657dc41d807331b809977608802738) | fix(docs): validate mount sources, ignores, cache, and live mirroring | [bob-cli-a0.2.1.7](bob-cli-a0.2.1.7.md) | 2026-10-19 22:19:54 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-a0.2.1.7.1][1] | parent epic scope | 1 |
| read-by | [agent:bob-cli-a0.2.1.7.2][2] | Need governing epic decisions and phase design | 1 |
| read-by | [agent:bob-cli-a0.2.1.7.3][3] | Need parent epic DECISIONS and phase list | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.2.1.7.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.2.1.7.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.2.1.7.3/README.md

<!-- sase:referenced-by:end -->
