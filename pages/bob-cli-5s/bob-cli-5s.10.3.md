# Bead: bob-cli-5s.10.3 — Search binding, open-error re-show, unavailable rows, refresh triggers, and live settings

[Bead Pages](../README.md) / [bob-cli-5s.10](bob-cli-5s.10.md) / bob-cli-5s.10.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** `bbugyi200.apollo.bob-cli-5s.land` · **Assignee:** `bob-cli-5s.10.3` · **Size:** medium
**Created:** 2026-10-09 08:04:27 EDT · **Closed:** 2026-10-09 10:06:29 EDT
**Plan:** [202610/bob\_refs\_land\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_refs_land_fixes.md)

## Description

refs-model-fixes: in bob-mac-capture, send typed text to the model, re-show the panel after an open error without resetting it and through BobPanelCoordinator, render unavailable rows per spec §5.5, refresh on wake, Today on every open, git dates in their own lane, ⌘R and Recheck Bob refreshes that re-rank, and live settings re-registration that reads the new value; with tests.

## Notes

[2026-10-09T14:06:29Z · bob-cli-5s.10.3] refs-model-fixes verified: all 9 items implemented with tests in bob-mac-capture (search binding via setQuery, error re-show through coordinator represent path for both open targets, unavailable rows with last-known titles and open refusal, wake on workspace center, Today on every open, -g on own lane after publish, deferred Rerank on R/Retry keeping selection, Recheck .recheck, labeled Today reasons, live settings from received values, Copy Diagnostic via injected pasteboard); README Updates/Opening updated; CI green on 9979d36 (run 37940264190, https://github.com/bobs-org/bob-mac-capture/actions/runs/37940264190); epic-symbols clean; no memory edits. Notes for 10.4: model.panelPresenter is now wired but uncalled in production (error paths use panelRepresenter); no unavailable-row render fixture exists so visual review of the inspector title+message stays with 10.4; the RefsCaption lint hoist repaired 10.2-originated parse errors that gated all CI verification.

## Dependencies

- **Depends on:** [bob-cli-5s.10.2](bob-cli-5s.10.2.md) ✓ · ⧖ 2026-10-09
- **Blocks:** [bob-cli-5s.10.4](bob-cli-5s.10.4.md) ◐ · ⧖ 2026-10-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-5s.10.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5s.10.3/README.md) | [bob-cli-5s.10.3](bob-cli-5s.10.3.md) | 5 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@85720a2`](https://github.com/bobs-org/bob-mac-capture/commit/85720a2810ceae383e413e13c366be822d422ec6) | fix(refs): search binding, error re-show, refresh lanes, live settings | [bob-cli-5s.10.3](bob-cli-5s.10.3.md) | 2026-10-09 09:19:28 EDT |
| bob-mac-capture | [`bob-mac-capture@9c46702`](https://github.com/bobs-org/bob-mac-capture/commit/9c46702b0d6ed13a6ef3e9499396cdb64ca35442) | fix(refs): hoist multiline calls out of caption interpolations | [bob-cli-5s.10.3](bob-cli-5s.10.3.md) | 2026-10-09 09:32:47 EDT |
| bob-mac-capture | [`bob-mac-capture@cf0c8b1`](https://github.com/bobs-org/bob-mac-capture/commit/cf0c8b16e11d7eab78205f333ea5a295c49aaac1) | fix(refs): last-known title cache and test compile fixes | [bob-cli-5s.10.3](bob-cli-5s.10.3.md) | 2026-10-09 09:36:57 EDT |
| bob-mac-capture | [`bob-mac-capture@4dcd5f0`](https://github.com/bobs-org/bob-mac-capture/commit/4dcd5f0bed0867abb0b27be108f04143e657e490) | fix(refs): settle the git lane before the wake-test baseline | [bob-cli-5s.10.3](bob-cli-5s.10.3.md) | 2026-10-09 09:43:30 EDT |
| bob-mac-capture | [`bob-mac-capture@9979d36`](https://github.com/bobs-org/bob-mac-capture/commit/9979d36b37fa92c8d3402bc91a829e8b14fe10f0) | fix(refs): wait for the git-lane invocation in its test | [bob-cli-5s.10.3](bob-cli-5s.10.3.md) | 2026-10-09 09:54:42 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-5s.10.3][1] | Need the phase scope and design file | 2 |
| read-by | [agent:bob-cli-5s.10.4][2] | Need predecessor INTERFACE CHANGE notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5s.10.3/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5s.10.4/README.md

<!-- sase:referenced-by:end -->
