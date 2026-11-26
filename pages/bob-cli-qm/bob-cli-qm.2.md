# Bead: bob-cli-qm.2 — Notebook Card shell with header absorption

[Bead Pages](../README.md) / [bob-cli-qm](README.md) / bob-cli-qm.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1gr](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1gr.md) · **Assignee:** `bob-cli-qm.2` · **Size:** medium
**Created:** 2026-11-26 12:37:59 EST · **Closed:** 2026-11-26 14:12:57 EST
**Plan:** [202611/prose\_and\_notebook\_cards.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/prose_and_notebook_cards.md)

## Description

notebook-card: paint the Notebook Card's identity, title adoption, summary or Add-summary ghost, foot, drawer, fold, and editor key from local data, and replace the linked notebook header wherever the card mounts.

## Notes

[2026-11-26T19:12:38Z · bob-cli-qm.2--2] PROPOSED FOLLOW-UP: Re-triage recurring generated docs drift in docs/develop/decisions.md. npm run docs:check reports this page out of date after lint passes, and the same page drift reproduces on clean HEAD; the clean baseline also has the expected stale plugin inventory. Existing tracking bob-cli-b6 is closed as obsolete after docs-gen fixed the prior occurrence; verify the current source before filing anything new.

[2026-11-26T19:12:57Z · bob-cli-qm.2--2] Notebook Card title range fix verified; build and full npm test pass, docs inventory check passes, and bob plugins sync deployed the final plugin. docs:check still reports docs/develop/decisions.md drift reproduced on clean HEAD; follow-up noted. No epic symbols remain.

## Dependencies

- **Depends on:** [bob-cli-qm.1](bob-cli-qm.1.md) ✓ · ⧖ 2026-11-26
- **Blocks:** [bob-cli-qm.4](bob-cli-qm.4.md) ◐ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-qm.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-qm.2.md) | [bob-cli-qm.2](bob-cli-qm.2.md) | 3 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@5152f49`](https://github.com/bobs-org/bob-plugins/commit/5152f4936445123b0ab012746a63bbf01b9e9199) | feat(ledger-tools): implement notebook title card | [bob-cli-qm.2](bob-cli-qm.2.md) | 2026-11-26 13:44:08 EST |
| bob-plugins | [`bob-plugins@d190ba2`](https://github.com/bobs-org/bob-plugins/commit/d190ba210989fe288b4b679d0ffce9f9a5ff89e4) | fix(ledger-tools): remove duplicate Notebook header path declaration | [bob-cli-qm.2](bob-cli-qm.2.md) | 2026-11-26 13:49:58 EST |
| bob-plugins | [`bob-plugins@175515f`](https://github.com/bobs-org/bob-plugins/commit/175515f243e6ad0670c6d87e5fe8a7aa90314da7) | feat(ledger-tools): finish Notebook Card shell | [bob-cli-qm.2](bob-cli-qm.2.md) | 2026-11-26 14:14:20 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-qm.2--1][1] | Continue phase after monitored check; inspect scope, notes, and constraints | 1 |
| read-by | [agent:bob-cli-qm.2--2][1] | Final scope and notes review before closing the Notebook Card phase | 3 |
| read-by | [agent:research.6l.gem][2] | Inspect bob-cli-qi and bob-cli-qm phase details for parallel coordination and card architecture | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-qm.2.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.6l.gem/README.md

<!-- sase:referenced-by:end -->
