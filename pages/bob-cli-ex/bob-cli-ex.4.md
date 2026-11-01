# Bead: bob-cli-ex.4 — Mac project successor prompt

[Bead Pages](../README.md) / [bob-cli-ex](README.md) / bob-cli-ex.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bp.f0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bp.f0.md) · **Assignee:** `bob-cli-ex.4` · **Size:** medium
**Created:** 2026-10-31 12:01:12 EDT · **Closed:** 2026-10-31 19:05:11 EDT
**Plan:** [202610/project\_note\_seals.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/project_note_seals.md)

## Description

mac_offer_card: Bob Mac Capture harvests `project_note.successors` into the existing Pull-In card. The card shows a "New project" context, a folder.badge.plus glyph, and a preview row. It applies the initial-marks decision, keeps notifications free of double counts, regenerates offer-form fixtures from real bob, and updates the Mac docs.

## Notes

[2026-10-31T23:05:11Z · bob-cli-ex.4--6] Implemented the project-offer Pull-In context and preview, kept initial marks empty, avoided duplicate notification counts, added real-Bob fixture generation, and updated docs and authorized glossary entries. Verified cargo build plus fixture generation, bob-mac-capture docs-check, Athena Swift suites (1,826 tests, 0 failures), just portable-check, and git diff --check in both repos. Mac is offline; macOS targets remain unverified.

## Dependencies

- **Depends on:** [bob-cli-ex.2](bob-cli-ex.2.md) ✓ · ⧖ 2026-10-31
- **Depends on:** [bob-cli-ex.3](bob-cli-ex.3.md) ✓ · ⧖ 2026-10-31

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ex.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ex.4.md) | [bob-cli-ex.4](bob-cli-ex.4.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`e2838ac`](https://github.com/bobs-org/bob-cli/commit/e2838ac33654a440b3d9568b984ca4e39fd7129d) | docs(glossary): explain project successor offers | [bob-cli-ex.4](bob-cli-ex.4.md) | 2026-10-31 19:06:17 EDT |
| bob-mac-capture | [`bob-mac-capture@891fe11`](https://github.com/bobs-org/bob-mac-capture/commit/891fe111f61a40af9917480184e7260588bb3967) | feat(mac-capture): choose a new project's tasks in the successor card | [bob-cli-ex.4](bob-cli-ex.4.md) | 2026-10-31 19:06:46 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ex.4--6][1] | Verify the assigned phase closed after its checks passed | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ex.4.md

<!-- sase:referenced-by:end -->
