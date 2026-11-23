# Bead: bob-cli-on.10.1.6 — Contract section, cross-plugin e2e, and ship

[Bead Pages](../README.md) / [bob-cli-on.10.1](bob-cli-on.10.1.md) / bob-cli-on.10.1.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-on.10](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.10.md) · **Assignee:** `bob-cli-on.10.1.6` · **Size:** small
**Created:** 2026-11-21 14:10:17 EST · **Closed:** 2026-11-21 22:07:56 EST
**Plan:** [202611/obsidian\_req\_gestures.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/obsidian_req_gestures.md)

## Description

gestures-contract-and-e2e: document the shipped Obsidian gestures in bob-cli docs/task-requirements.md, extend the real-Obsidian e2e to every gesture across the three plugins, run the full plugin and docs gates, and sync the three plugins.

## Notes

[2026-11-22T03:07:35Z · bob-cli-on.10.1.6] PROPOSED FOLLOW-UP: docs-check published-URLs gate fails on clean tree too — src/native/highlights_ref/podcast/feed.rs:70 links docs/1.0.md to /1.0/ with no built page; unrelated to obsidian-gestures, needs its own fix

[2026-11-22T03:07:43Z · bob-cli-on.10.1.6] PROPOSED FOLLOW-UP: consider having bob-ledger-tools adopt the full RQ twin (it still carries a display-only RQ subset without path/subtree_end/note ranges/row keys)

[2026-11-22T03:07:56Z · bob-cli-on.10.1.6] Contract section added to docs/task-requirements.md §5 (gesture table with exact copy, one-undo rule, Ctrl+Shift+T carve-out) and §10 (byte-identical RQ/RL/RW twins note), linking the three plugin reference pages. Real-Obsidian e2e extended to 41 scenarios: Alt+[ drop with reason then Undo, Alt+[ Esc, Alt+] restore, Alt+] pending refusal, Ctrl+Enter / Ctrl+Shift+] / Alt+N / Alt+F refusals, Ctrl+Shift+Enter carried-stub refusal with link kept, Ctrl+Shift+P owner Task Card (cursor on owner, card titled, clean close) — full run green under xvfb-run on athena. npm test 8568 pass 0 fail; npm run docs:check and just docs-check pass except one pre-existing published-URLs break (feed.rs docs/1.0.md -> /1.0/) that fails identically on the clean tree (recorded as PROPOSED FOLLOW-UP, as is the ledger-tools full-RQ-twin idea). All three plugins sync up to date; vault manifest.json/main.js byte-identical to repo. No commits made; two e2e scripts + task-requirements.md left uncommitted for the land agent.

## Dependencies

- **Depends on:** [bob-cli-on.10.1.4](bob-cli-on.10.1.4.md) ✓ · ⧖ 2026-11-21
- **Depends on:** [bob-cli-on.10.1.5](bob-cli-on.10.1.5.md) ✓ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.10.1.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.10.1.6/README.md) | [bob-cli-on.10.1.6](bob-cli-on.10.1.6.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`e5ee4a8`](https://github.com/bobs-org/bob-cli/commit/e5ee4a8d9e942b7bbd9478ac1fa66a52d5c70ddf) | docs(task-reqs): add §5 Obsidian gestures table with exact copy and undo rule | [bob-cli-on.10.1.6](bob-cli-on.10.1.6.md) | 2026-11-21 22:08:54 EST |
| bob-plugins | [`bob-plugins@7b96dce`](https://github.com/bobs-org/bob-plugins/commit/7b96dced3a85eea7ebeca5f911b0fb05c0d7bf3c) | test(e2e): add real-Obsidian task-reqs scenarios across three plugins | [bob-cli-on.10.1.6](bob-cli-on.10.1.6.md) | 2026-11-21 22:09:33 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-on.10.1.6][1] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-os.land][2] | Check whether test_contracts registry fix is in this phase scope | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.10.1.6/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-os.land/README.md

<!-- sase:referenced-by:end -->
