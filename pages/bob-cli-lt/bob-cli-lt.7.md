# Bead: bob-cli-lt.7 — The Bank Setup card with the Categories section

[Bead Pages](../README.md) / [bob-cli-lt](README.md) / bob-cli-lt.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1co](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1co.md) · **Assignee:** `bob-cli-lt.7` · **Size:** medium
**Created:** 2026-11-15 13:16:09 EST · **Closed:** 2026-11-15 22:20:52 EST
**Plan:** [202611/bank\_setup\_render\_and\_edit.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_setup_render_and_edit.md)

## Description

setup-card: build the keyboard-first Setup card shell, Categories gestures, Undo, the YAML excursion, and entry points.

## Notes

[2026-11-16T03:10:15Z · bob-cli-lt.7--2] PROPOSED FOLLOW-UP: Bring the mounted bob-ledger-tools reference under its 6,000-word budget — docs:check reports 6,281 words on this phase and the same 6,281 on clean upstream cb885ca; see bob-cli-lt.6 for the prior proposal.

[2026-11-16T03:20:52Z · bob-cli-lt.7--3] Bank Setup card phase verified: npm run validate passed; serial event-link and keep-moving surface tests passed; npm test had one parallel-load timing failure in the 200-link render budget assertion (306.6 ms), while its targeted file passed serially; docs:check remains at 6,281 words, matching the clean cb885ca baseline, with the proposed follow-up recorded above citing bob-cli-lt.6; bob plugins sync --repo "/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/sase/repos/linked/bob-plugins" --no-pull passed and deployed the Setup card; epic-symbols reported no entries.

## Dependencies

- **Depends on:** [bob-cli-kr](../bob-cli-kr/README.md) ✓ · ⧖ 2026-11-12
- **Depends on:** [bob-cli-lt.6](bob-cli-lt.6.md) ✓ · ⧖ 2026-11-15
- **Blocks:** [bob-cli-lt.8](bob-cli-lt.8.md) ✓ · ⧖ 2026-11-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-lt.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-lt.7.md) | [bob-cli-lt.7](bob-cli-lt.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@65570a0`](https://github.com/bobs-org/bob-plugins/commit/65570a0e63537ce78a5c8d5366b7c53ec3f7442a) | feat(bank): add the keyboard-first setup card | [bob-cli-lt.7](bob-cli-lt.7.md) | 2026-11-15 22:22:41 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-lt.7--3][1] | Verify the proposed docs follow-up and phase notes before closing the phase | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-lt.7.md

<!-- sase:referenced-by:end -->
