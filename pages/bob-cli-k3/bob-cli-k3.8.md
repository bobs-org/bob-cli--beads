# Bead: bob-cli-k3.8 — Bob Mac Capture presents albums

[Bead Pages](../README.md) / [bob-cli-k3](README.md) / bob-cli-k3.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** `bbugyi200.apollo.research.43.linker.w0` · **Assignee:** `bob-cli-k3.8` · **Size:** medium
**Created:** 2026-11-11 04:56:44 EST · **Closed:** 2026-11-11 16:33:29 EST
**Plan:** [202611/album\_and\_record\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/album_and_record_notes.md)

## Description

mac-albums: show each record route's album title, owner, and summary from the additive capture-targets fields, render the bare-album refusal with its one-key `@eat/` rewrite, and name the album in record previews and success lines, gated on the exact-SHA macOS CI run.

## Notes

[2026-11-11T19:16:47Z · bob-cli-k3.8] PROPOSED FOLLOW-UP: docs-check word budgets are red at baseline (7 pages over cap, including capture-panel, capture-previews, protocol that k3.8 touched); needs a trimming pass

[2026-11-11T19:16:52Z · bob-cli-k3.8] PROPOSED FOLLOW-UP: typecheck-tests is red at baseline (CaptureModifierAliasTests and CaptureRelationEqualsAliasTests main-actor ledgerSuites errors, identical on pristine HEAD); needs a fix before the gate can go green

[2026-11-11T19:17:53Z · bob-cli-k3.8] PROPOSED FOLLOW-UP: docs-check word budgets red at baseline, tracked by bob-cli-jz (same 7 pages on pristine HEAD)

[2026-11-11T19:17:57Z · bob-cli-k3.8] PROPOSED FOLLOW-UP: typecheck-tests red at baseline, tracked by bob-cli-jy (same 4 errors on pristine HEAD)

[2026-11-11T19:24:07Z · bob-cli-k3.8] CI gate status: monitor y153j4 (macos-ci-check on the exact mac-albums tree) is staged but had not run as of 14:23 EST; no terminal verdict yet. Implementation and local gates are complete — see prior notes. Leave open until the macOS run goes green.

[2026-11-11T21:05:18Z · bob-cli-k3.8] CI gate verdict: exact-SHA run 43090193031... see next note

[2026-11-11T21:05:33Z · bob-cli-k3.8] CI GATE VERDICT (red, infra): exact-tree snapshot SHA 26aab239a0830aaa559872b2cdab78647e67fb0e ran as actions run 43093026266 (thrown-away ci/precommit branch, now deleted). Tree steps all green: Lint Swift formatting success, Build success, Test success (panel-test fix verified — 0 failures). Red step: Upload render fixtures — actions/upload-artifact@v4 got HTML error pages from the artifact service 5x over 10 min (Unexpected token <.DOCTYPE... not valid JSON), so Bundle/Verify/Launch/Install skipped. Nothing in the tree can cause that; artifact upload worked on master run 43018693025 earlier today. Bead left open: re-run the throwaway gate when the artifact service recovers; staged monitor y153j4 still pending as fallback.

[2026-11-11T21:33:29Z · bob-cli-k3.8--1] mac-albums verified: exact-SHA macOS run 43100345773 (snapshot 805d1c6f) green — Lint/Build/Test/Upload fixtures/Bundle/Verify plist/Launch smoke/Install all ok. Record route rows show album title/owner/summary, bare-album refusal renders one-key @stem/ rewrite button, previews and success lines name the album. Local: 2482 portable tests green.

## Dependencies

- **Blocks:** [bob-cli-k3.11](bob-cli-k3.11.md) ◐ · ⧖ 2026-11-11
- **Depends on:** [bob-cli-k3.4](bob-cli-k3.4.md) ✓ · ⧖ 2026-11-11

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-k3.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-k3.8.md) | [bob-cli-k3.8](bob-cli-k3.8.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-k3.5.1.3][1] | Check whether this existing follow-up tracks the unchanged docs word-budget failures | 1 |
| read-by | [agent:bob-cli-k3.8--1][2] | Need phase scope to verify close | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-k3.5.1.3/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-k3.8.md

<!-- sase:referenced-by:end -->
