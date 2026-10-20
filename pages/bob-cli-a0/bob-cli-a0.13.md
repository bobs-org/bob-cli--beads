# Bead: bob-cli-a0.13 — llms.txt, reader tests, final sweep, and handoff

[Bead Pages](../README.md) / [bob-cli-a0](README.md) / bob-cli-a0.13

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.95](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.95.md) · **Assignee:** `bob-cli-a0.13` · **Size:** medium
**Created:** 2026-10-19 18:55:43 EDT · **Closed:** 2026-10-20 16:39:38 EDT
**Plan:** [202610/bob\_public\_docs\_site.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_public_docs_site.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | file:explicit:c447d1a8eb7915f61a1b165d | handoff for the polish phase |
| related | file:explicit:760cd5841779d1a554d08607 | attached via sase artifact create --bead |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

polish: enable llms.txt, run the agent reader test, fix label misses, do a final accessibility sweep, and file the handoff research artifact for work agents could not finish.

## Notes

[2026-10-20T20:38:56Z · 9m--1] PROPOSED FOLLOW-UP: Stranded launch-gate waiter bob-cli-a0.13--1 stayed WAITING on its own already-finished session long after the gate settled (seen WAITING at 16:04Z per plan record; it read this bead at 20:24Z and has since reached DONE on its own, so no kill was needed). A gate follow-up waiting on a finished session is a SASE runtime defect for the land agent to route, not phase work.

[2026-10-20T20:39:03Z · 9m--1] PROPOSED FOLLOW-UP: Weekly run 39475174066 (dispatched 18:29Z) failed on four HTTP 429s against github.com/bobs-org/bob-cli/edit/master/docs/... URLs (Material edit-link login redirects under rate limit), not Adobe — the landed url exclusion is working (zero Adobe failures) and per plan no new exclusion was added. Managed issue bobs-org/bobs-org.github.io#2 stays OPEN on that run. Re-dispatch gh workflow run weekly.yml --repo bobs-org/bobs-org.github.io --ref main after the backoff window; a pass closes #2. If edit-link 429s persist, fix in theme edit-link config or retry policy, never broader lychee exclusions.

[2026-10-20T20:39:16Z · 9m--1] PROPOSED FOLLOW-UP: Copy polish flagged by 3/10 blind readers (not a reader-test miss, all tasks passed): docs/guides/fix-mac-capture-bob-resolution.md:49 says the backtick ! backtick glyph returns to the bullet-b, which reads garbled. Reword to name the status indicator it actually returns to. Labels/hub-copy only, no page move.

[2026-10-20T20:39:24Z · 9m--1] PROPOSED FOLLOW-UP: Two llms.txt readers (L1, L3) reported instruction-like text inside fetched page content (a create-a-doc request and quoting rules). Verified NOT in the site: grep over docs/ and mkdocs.yml finds no claude.ai or quoting-rules text, so it came from the fetch tooling, not our pages. No site change needed; noted so future reader runs are not alarmed. If it recurs, capture the exact snippet and check the fetch path.

[2026-10-20T20:39:31Z · 9m--1] Phase handoff for land-agent triage: file:explicit:c447d1a8eb7915f61a1b165d (202610/bob_public_docs_site/bob_public_docs_site__handoff.md in bob-cli--research). Open items owned by the epic: Bryan clean-machine walkthrough, 3-5 human reader tests, dated Obsidian screenshot set, custom-domain decision, Zensical 0.1.x bump watch, 60-day schedule-inactivity watch, unwritten guide candidates. Epic notes #1, #2, #4, #5, #6 resolved this phase (commit 1513a385); epic #3 and #7 stay open.

[2026-10-20T20:39:38Z · 9m--1] Verified: commit 1513a385 on master; just docs-check green (442 passed); llms.txt HTTP 200 with 5 sections and Contracts pinned to 28 registry stems; a11y 0 violations on zensical and material; live build.json bob-cli SHA == landed commit and docs-status manifest == live; blind readers 5/5 expected-door-first on all 6 tasks for both entry points (no fix round); weekly run 39475174066 failed non-Adobe (4x 429 on github.com edit links, zero Adobe failures, no new exclusions) with issue #2 still open; handoff file:explicit:c447d1a8eb7915f61a1b165d registered and linked. Epic left open for bob-cli-a0.land.

## Dependencies

- **Depends on:** [bob-cli-a0.10](bob-cli-a0.10.md) ✓ · ⧖ 2026-10-19
- **Depends on:** [bob-cli-a0.11](bob-cli-a0.11.md) ✓ · ⧖ 2026-10-19
- **Depends on:** [bob-cli-a0.12](bob-cli-a0.12.md) ✓ · ⧖ 2026-10-19
- **Depends on:** [bob-cli-a0.5](bob-cli-a0.5.md) ✓ · ⧖ 2026-10-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-a0.13](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.13.md) | [bob-cli-a0.13](bob-cli-a0.13.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:9m--1][1] | Need phase notes for handoff step 6 | 3 |
| read-by | [agent:bob-cli-a0.13--3][2] | Verify phase closure and review recorded scope/proposals before finishing the handoff | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.9m.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.13.md

<!-- sase:referenced-by:end -->
