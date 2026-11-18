# Bead: bob-cli-ms.8.1 — Record sheet shows the title and mounts on H1-less records

[Bead Pages](../README.md) / [bob-cli-ms.8](bob-cli-ms.8.md) / bob-cli-ms.8.1

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ms.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ms.land.md) · **Assignee:** `bob-cli-ms.8.1` · **Size:** medium
**Created:** 2026-11-17 22:26:14 EST
**Plan:** [202611/record\_card\_title\_and\_proof.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/record_card_title_and_proof.md)

## Description

sheet-title: in bob-ledger-tools, render the record title at the top of the record sheet with page-title styling, mount the sheet at the top of H1-less records (including frontmatter-only notes) in Live Preview and Reading, make the title's one home the sheet, pin the rollover test's clock, update docs, bump, and deploy.

## Notes

[2026-11-18T04:02:05Z · bob-cli-ms.8.1--1] PROPOSED FOLLOW-UP: Stabilize four known full-suite 25 ms timing flakes — monitor yktc8xcfr9as reported event-link-times at 37.0 ms (bob-cli-km), frees-marks at 94 ms (bob-cli-io), keep-moving-marks-surface at 2124 ms (bob-cli-ki), and off-clock-link-chips at 81.4 ms (bob-cli-ju); npm run validate passed. These match the existing READY flake beads and the epic land evidence records the same failures on this epic with clean-base/isolation passes and no Record Card involvement.

[2026-11-18T04:09:38Z · bob-cli-ms.8.1--1] DEPLOY BLOCKED: bob plugins sync --repo <linked bob-plugins checkout> --no-pull --dry-run refused because the vault has bob-ledger-tools 1.133.0 deployed from an uncommitted build in another checkout (f8a8619); git fetch found no upstream path commit and sase agent list shows no agent on that checkout. Docs require asking Bryan before replacing an unlanded abandoned deploy. User instruction forbids -F, so deployment and phase close await a non-force recovery path.

## Dependencies

- **Blocks:** [bob-cli-ms.8.2](bob-cli-ms.8.2.md) ◐ · ⧖ 2026-11-17
- **Blocks:** [bob-cli-ms.8.3](bob-cli-ms.8.3.md) ◐ · ⧖ 2026-11-17

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ms.8.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ms.8.1.md) | [bob-cli-ms.8.1](bob-cli-ms.8.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@9ad471d`](https://github.com/bobs-org/bob-plugins/commit/9ad471d8a7ebcdc193cffda8eeb8ba99b4c87332) | feat(bob-ledger-tools): render record titles in the sheet | [bob-cli-ms.8.1](bob-cli-ms.8.1.md) | 2026-11-17 23:12:55 EST |
