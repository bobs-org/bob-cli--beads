# Bead: bob-cli-da.4.1.1 — Move embedded payloads and verify both Cargo packages

[Bead Pages](../README.md) / [bob-cli-da.4.1](bob-cli-da.4.1.md) / bob-cli-da.4.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-da.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-da.4.md) · **Assignee:** `bob-cli-da.4.1.1` · **Size:** medium
**Created:** 2026-10-27 16:43:43 EDT · **Closed:** 2026-10-27 17:11:20 EDT
**Plan:** [202610/embedded\_assets\_split.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/embedded_assets_split.md)

## Description

assets-and-packages: create the bob-obsidian-assets workspace crate, move the existing font and vendor payloads without changing their bytes, preserve installed and source tree consumers, and extend package-check to verify both archives with their own license and size budgets; add unique release tags with the new member. Follow the assets-and-packages section below.

## Notes

[2026-10-27T21:11:20Z · bob-cli-da.4.1.1] Assets split landed: root 3,217,453B (3.07MiB) + assets 5,004,750B (4.77MiB), both below 8MiB warning (headroom 5.17/3.38MiB) vs baseline 8,220,034B. Verified: byte-identical moves (24 git renames, sampled SHA match), shared-font tests (3), note-snapshot fonts (6), check-release-tools (82), check-web-clip-adapter source+installed ok, docs-check (448), full package-check with verification, pinned release-plz 0.3.173 parses unique tags v and bob-obsidian-assets-v. No epic-symbols.

## Dependencies

- **Blocks:** [bob-cli-da.4.1.2](bob-cli-da.4.1.2.md) ◐ · ⧖ 2026-10-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-da.4.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-da.4.1.1/README.md) | [bob-cli-da.4.1.1](bob-cli-da.4.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b63e5a0`](https://github.com/bobs-org/bob-cli/commit/b63e5a046f4d03de6aa38ce080b015447ad305c5) | feat(assets)!: split embedded payloads into bob-obsidian-assets crate | [bob-cli-da.4.1.1](bob-cli-da.4.1.1.md) | 2026-10-27 17:12:31 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-da.4.1.1][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-da.4.1.1/README.md

<!-- sase:referenced-by:end -->
