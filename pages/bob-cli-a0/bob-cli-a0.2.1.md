# Bead: bob-cli-a0.2.1 — Complete the Bob documentation toolchain and contract site

[Bead Pages](../README.md) / [bob-cli-a0.2](bob-cli-a0.2.md) / bob-cli-a0.2.1

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-a0.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.2.md) · **Assignee:** `bob-cli-a0.2.1.land`
**Created:** 2026-10-19 19:05:37 EDT
**Plan:** [202610/docs\_toolchain.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/docs_toolchain.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/docs_toolchain.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 6 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/docs_toolchain.md

<!-- sase:links:end -->

## Description

Finish bob-cli-a0.2 with an in-place contract site, reproducible assembly, executable documentation gates, and the authorized authoring guidance.

## Notes

[2026-10-20T00:58:02Z · bob-cli-a0.2.1.land] LAND TRIAGE (bob-cli-a0.2.1.land): (1) bob-cli-a0.2.1.1 PROPOSED FOLLOW-UP (plain-text PDFKit research mention in docs/highlights-create.md) -> recorded as a DISCOVERED ISSUE note on active outer epic bob-cli-a0. No duplicate task exists; related ready memory task bob-cli-8p could become the public citation. No new task filed. (2) bob-cli-a0.2.1.4 PROPOSED FOLLOW-UP (lychee --include-fragments only over HTTP at weekly publish) -> DECLINED as superseded and folded into this epic's remaining work. Its premise is wrong: on the landed strict build, lychee 0.24.2 run with --offline --include-fragments --index-files index.html --root-dir <site> plus the org-root remap reports 3557 links, 0 errors. The url-links phase omitted only --index-files, so offline fragment checking belongs to this epic's own links gate.

[2026-10-20T01:02:17Z · bob-cli-a0.2.1.land] LAND AUDIT (bob-cli-a0.2.1.land, master cb42d654 = origin/master). VERIFIED: all six phases closed and every phase note addressed. just docs-check green: lint, gen drift, strict Zensical, urls (32 pages, 352 mentions, 1 curated link; live /urls.txt first-publish 404 warning), offline lychee 0 errors, search smoke 2 cases, 121 pytest. The just check recipe is unchanged since 8b0f3782 and the epic made no Rust changes. Inherited decisions honored: MIT; search on; only sase/memory/docs.md added, with exact type/description, plus its generated projections. INTEGRATION: the only non-epic commit since the epic started is 24f43958 (bob-cli-9y.1.1 task-move fix, editing docs/task-move.md); docs-check passes with it, and the registry and README table need no change. c7df845f (bob-cli-a0.1 MIT license) is consistent. Mount table empty, so sibling repo drift does not apply. REMAINING EPIC WORK, all caused by this epic and verified by reading code and running probes:
- mounts: stamp_markdown drops the closing --- of existing front matter; a symlinked parent dir lets writes escape docs/ before the error; assembly never checks targets are gitignored; stale deletion is not confined to untracked ignored paths; the cache clone is never refreshed or remote-checked; serve publishes no /build.json and no live reload (it serves a one-time staged copy) despite the docs; the production JSON README example is wrong; many mounts acceptance tests are missing.
- lint: nav rules use the unexpanded authored nav and skip mount copies; source: is checked only by repo name; check_test_pins calls discover_repo (can clone, ignores production context, swallows errors); the vault-repo placeholder fails its own rule; privacy findings always report line 1; list-indented fences are not recognized; --fix and stale-ceiling detection disagree; dead code; missing negative fixtures for several budget, collision, nav, and JS-pin cases.
- urls/links: lychee runs without --include-fragments, although --index-files index.html makes offline fragments work (0 errors); the mention scan reads only *.rs and misses .lua/.tex/.json mentions; KeyError on a fragment of a non-indexed file; an empty 200 urls.txt is accepted; the post-redirect origin is unchecked; ignore-scope narrowness is enforced only for '*'; refresh runs before ignores; dead code.
- authoring: the templates lack Bob examples and the parent-required text Output .no-copy fences; writing-docs omits the concrete portability and hygiene rules.
Planned as child epic sase_plan_docs_toolchain_landing_fixes.md (parent_bead bob-cli-a0.2.1; phases mount-safety -> lint-contract, plus links-authoring in parallel). DECLINED as non-defects:
- Foundation's contract anchor slug edits (e.g. capture.md #...-with- to #...-with) were required for one strict-build slugger, and the parent plan does not freeze contract anchors.
- The mention regex matching ref/docs/... fails safe.
- console/zsh fence prompt checks are stricter than the plan, which is harmless.
- docs.md's decision-record row with no [[decisions]] link is a nit; no memory edit is authorized beyond the existing note.
epic-symbols: none for bob-cli-a0.2.1 or bob-cli-a0.2; no symvision recipe in this repo.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-a0.2.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.2.1.land.md) | [bob-cli-a0.2.1](bob-cli-a0.2.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-a0.2.1.1][1] | Need the epic decisions governing this phase | 1 |
| read-by | [agent:bob-cli-a0.2.1.2][2] | parent epic plan and decisions | 1 |
| read-by | [agent:bob-cli-a0.2.1.3][3] | Need inherited epic DECISIONS for lint phase | 1 |
| read-by | [agent:bob-cli-a0.2.1.5][4] | Need epic decisions governing authoring and approved memory edit | 1 |
| read-by | [agent:bob-cli-a0.2.1.6][5] | Need final epic decisions governing integration phase work | 1 |
| read-by | [agent:bob-cli-a0.2.1.7.3][6] | Need the toolchain epic scope, decisions, and landing notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.2.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.2.1.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.2.1.3/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.2.1.5/README.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.2.1.6/README.md
[6]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.2.1.7.3/README.md

<!-- sase:referenced-by:end -->
