# Bead: bob-cli-e8.6 — Mention rows, pills, quotes, and jump-to-mention

[Bead Pages](../README.md) / [bob-cli-e8](README.md) / bob-cli-e8.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2v.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2v.linker.w0.md) · **Assignee:** `bob-cli-e8.6` · **Size:** medium
**Created:** 2026-10-29 17:20:22 EDT · **Closed:** 2026-10-29 19:16:41 EDT
**Plan:** [202610/inline\_task\_mentions.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/inline_task_mentions.md)

## Description

plugin-rows: render mention entries in Live Preview and Reading view with grouping, pills, quote lines, no ×, mixed-pair markers, density limits, stale styling, and click-to-mention.

## Notes

[2026-10-29T23:15:38Z · bob-cli-e8.6] Fake DOM snapshot (Live Preview shared row renderer; chip internals abbreviated):
<span class="bob-dep-row bob-relation-row is-incoming is-labelled" aria-label="Tasks linking here · relations and 💬 text mentions · live" role="group" title="Tasks linking here · relations and 💬 text mentions · live"><span class="bob-dep-label bob-relation-label" aria-hidden="true">"🪢 linked from"</span><span class="bob-relation-group bob-relation-link-group"><span class="bob-relation-entry"><span class="bob-relation-pill">"followed up by"</span><span class="bob-dep-chip bob-relation-chip is-todo" aria-label="Fix flaky capture retries · followed up by" data-state="todo" role="link" tabindex="0" title="Fix flaky capture retries — sources.md — Todo">…</span><span class="bob-relation-mixed-marker" aria-label="Also mentioned in its text" title="Also mentioned in its text">"💬"</span></span></span><span class="bob-relation-divider" aria-hidden="true"></span><span class="bob-relation-group bob-relation-mention-group"><span class="bob-relation-entry is-mention"><span class="bob-relation-pill is-mention" aria-haspopup="dialog" aria-label="Why is this here? Add support for hidden, superseded mem… mentions this task in its text" role="button" tabindex="0">"💬 mentioned in"</span><span class="bob-dep-chip bob-relation-chip is-todo is-mention" aria-label="Add support for hidden, superseded mem… · mentioned in its text" role="link" tabindex="0">…</span><span class="bob-mention-quote">"“OBSOLETE: See "<span class="bob-mention-quote-target">"this task"</span>"!”"</span></span></span></span>
Reading view equivalent is covered by test "Reading view groups mention rows, renders the quote, omits ×, and jumps to the source occurrence".

[2026-10-29T23:15:46Z · bob-cli-e8.6] PROPOSED FOLLOW-UP: Reconcile navigation Task Card theme tests — the same five failures reproduce in unchanged navigation files after this phase (four missing theme helper exports and one hue-muted assertion); already tracked in bob-cli-e8.5 note #1 from the clean base test run.

[2026-10-29T23:16:41Z · bob-cli-e8.6] Rendered mention rows in Live Preview and Reading view; fake DOM snapshot recorded in phase notes. Focused relation/mention tests pass 24/24, build and build:check pass, docs:check passes 447 with 1 skip, and bob-ledger-tools main.js/manifest/styles match deployed bytes. Full npm test has 5 unrelated navigation Task Card theme failures, reproduced unchanged and tracked in bob-cli-e8.5 note #1. epic-symbols reports none.

## Dependencies

- **Depends on:** [bob-cli-e8.5](bob-cli-e8.5.md) ✓ · ⧖ 2026-10-29
- **Blocks:** [bob-cli-e8.7](bob-cli-e8.7.md) ○ · ⧖ 2026-10-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-e8.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-e8.6/README.md) | [bob-cli-e8.6](bob-cli-e8.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@d096507`](https://github.com/bobs-org/bob-plugins/commit/d0965076319fadb8d5ab826710e915c54ab99e1d) | feat(ledger-tools): render task mention rows | [bob-cli-e8.6](bob-cli-e8.6.md) | 2026-10-29 19:17:29 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-e8.6][1] | Check this phase's existing notes and remaining work before completion | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-e8.6/README.md

<!-- sase:referenced-by:end -->
