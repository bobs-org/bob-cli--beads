# Bead: bob-cli-a0.2.1.4 — Protect published URLs and verify built links

[Bead Pages](../README.md) / [bob-cli-a0.2.1](bob-cli-a0.2.1.md) / bob-cli-a0.2.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-a0.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.2.md) · **Assignee:** `bob-cli-a0.2.1.4` · **Size:** medium
**Created:** 2026-10-19 19:05:38 EDT · **Closed:** 2026-10-19 19:48:02 EDT
**Plan:** [202610/docs\_toolchain.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/docs_toolchain.md)

## Description

url-links: implement built-site URL and anchor resolution, live and curated URL contracts, source mention scanning, and checksum-verified lychee acquisition and execution.

## Notes

[2026-10-19T23:47:52Z · bob-cli-a0.2.1.4] PROPOSED FOLLOW-UP: Weekly publish phase can run lychee --include-fragments over HTTP where directory-URL fragments resolve (proven over localhost); offline links gate omits it because lychee 0.24.2 reports Cannot find fragment for all 59 file:// /page/#anchor links even though every anchor exists

[2026-10-19T23:48:02Z · bob-cli-a0.2.1.4] urls+links green on strict Zensical build: 31 pages in urls.txt, 352 mentions resolved, 1 curated link, lychee 3488 links 0 errors; 74/74 pytest pass; repaired 2 broken README anchors; lychee 0.24.2 pinned with verified checksums

## Dependencies

- **Depends on:** [bob-cli-a0.2.1.2](bob-cli-a0.2.1.2.md) ✓ · ⧖ 2026-10-19
- **Blocks:** [bob-cli-a0.2.1.6](bob-cli-a0.2.1.6.md) ✓ · ⧖ 2026-10-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-a0.2.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.2.1.4/README.md) | [bob-cli-a0.2.1.4](bob-cli-a0.2.1.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`88fcca6`](https://github.com/bobs-org/bob-cli/commit/88fcca648a7c43064513a31cbdde09718da1134e) | feat(docs): protect published URLs and verify built links (bob-cli-a0.2.1.4) | [bob-cli-a0.2.1.4](bob-cli-a0.2.1.4.md) | 2026-10-19 19:49:21 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-a0.2.1.4][1] | Confirm phase bead closed | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.2.1.4/README.md

<!-- sase:referenced-by:end -->
