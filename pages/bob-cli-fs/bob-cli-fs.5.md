# Bead: bob-cli-fs.5 — Capture unlink hand-offs (v1.1)

[Bead Pages](../README.md) / [bob-cli-fs](README.md) / bob-cli-fs.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5m.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5m.linker.w0.md) · **Assignee:** `bob-cli-fs.5` · **Size:** medium
**Created:** 2026-11-02 05:57:12 EST · **Closed:** 2026-11-02 19:35:16 EST
**Plan:** [202611/starts\_after\_relation.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/starts_after_relation.md)

## Description

capture_unlink: raise a parked event when capture's @route+id! toggle unlinks a Pending task, offering its starts-after sources at the link's former slot.

## Notes

[2026-11-03T00:35:16Z · bob-cli-fs.5--1] Pending unlink via @route+id! raises a parked relation event and offers starts-after sources at the removed-link slot (SA31); Next and Ready unlinks stay silent (SA32). CLI tests cover dry-run/real JSON parity and relink. just check passed (tool 79486eafd8b28e77501e7e0342cd89f0, exit 0). No leftover --epic-symbol entries. Glossary already covers parking/successor-offer.

## Dependencies

- **Blocks:** [bob-cli-fs.10](bob-cli-fs.10.md) ◐ · ⧖ 2026-11-02
- **Depends on:** [bob-cli-fs.4](bob-cli-fs.4.md) ✓ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-fs.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-fs.5.md) | [bob-cli-fs.5](bob-cli-fs.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`71907da`](https://github.com/bobs-org/bob-cli/commit/71907dab7ceb7dab45a401a700e7069cd767bc24) | feat(capture): offer relation successors on Pending unlink | [bob-cli-fs.5](bob-cli-fs.5.md) | 2026-11-02 19:36:19 EST |
