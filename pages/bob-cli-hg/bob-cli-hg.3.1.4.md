# Bead: bob-cli-hg.3.1.4 — Complete the pure message renderer and its acceptance corpus

[Bead Pages](../README.md) / [bob-cli-hg.3.1](bob-cli-hg.3.1.md) / bob-cli-hg.3.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-hg.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-hg.3.md) · **Assignee:** `bob-cli-hg.3.1.4` · **Size:** medium
**Created:** 2026-11-05 13:16:21 EST · **Closed:** 2026-11-05 21:02:13 EST
**Plan:** [202611/gmail\_mail\_body.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_mail_body.md)

## Description

body-integration: assemble the public RenderedBody interface, plain-text reply splitting, HTML/plain/snippet selection, and fetched-body retry behavior. Complete all parent acceptance fixtures, entry-point property tests, documentation, and downstream consumer examples described in section 6.

## Notes

[2026-11-06T01:58:22Z · bob-cli-hg.3.1.4] PROPOSED FOLLOW-UP: just-check clippy gate fails on unused const TODAY in tests/cli/capture/merge_in.rs:8 (landed in 53c1d1ad, zero uses in its file, fails identically on clean base)

[2026-11-06T01:58:28Z · bob-cli-hg.3.1.4] PROPOSED FOLLOW-UP: four tests fail identically on clean base: help root snapshot misses the landed gmail line, catalog protocol count 73 vs 72, catalog leaves and completion kinds both flag a duplicate clipboard entry

[2026-11-06T01:58:34Z · bob-cli-hg.3.1.4] PROPOSED FOLLOW-UP: just docs-check lychee fails on pre-existing broken fragment #merging-tasks-into-a-new-task-with linked from docs/capture.md (heading carries a trailing < that changes the anchor)

[2026-11-06T02:02:13Z · bob-cli-hg.3.1.4] render_message assembled with plain.rs segmentation and render.rs selection; 24 new tests pass (77 gmail lib tests green), fmt clean, full clippy gate clean except pre-existing TODAY deny recorded as follow-up; 5 unrelated failures + docs-check fragment reproduced on clean base and recorded; docs-gen regenerated drifted CLI refs; no epic-symbols left

## Dependencies

- **Depends on:** [bob-cli-hg.3.1.3](bob-cli-hg.3.1.3.md) ✓ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-hg.3.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.3.1.4/README.md) | [bob-cli-hg.3.1.4](bob-cli-hg.3.1.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`45118e1`](https://github.com/bobs-org/bob-cli/commit/45118e1b197b3c1c604c837d3b73a27d5e813aa8) | feat(gmail): complete the pure message renderer and its acceptance corpus | [bob-cli-hg.3.1.4](bob-cli-hg.3.1.4.md) | 2026-11-05 21:03:30 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hg.3.1.4][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.3.1.4/README.md

<!-- sase:referenced-by:end -->
