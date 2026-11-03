# Bead: bob-cli-gn — Image zoom remembers where images came from

[Bead Pages](../README.md) / bob-cli-gn

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.17n](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.17n.md) · **Assignee:** `bob-cli-gn.land`
**Created:** 2026-11-03 14:53:40 EST
**Plan:** [202611/image\_zoom\_origins.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/image_zoom_origins.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/image_zoom_origins.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/image_zoom_origins.md

<!-- sase:links:end -->

## Description

Every image bob copies into the vault remembers its original file path. The `Z` viewer can copy that path (`y`) or turn the link back into it (`r`), and `Z` on a bullet holding only an image path imports it the way `%c` does. One beautiful, undoable loop: path → embed → path.

## Notes

[2026-11-03T22:32:13Z · bob-cli-gh.land] DISCOVERED ISSUE: bob-cli-gh.land's just check on master 0b4cebdf (+ unrelated period fixes) fails exactly two tests: native::catalog::tests::document_shape (src/native/catalog/tests.rs:395, left 69 right 67) and catalog::protocol_1_parses_with_schema_version_one (tests/cli/catalog.rs:42, 69 vs 67). gn.1 commit 0b4cebdf added the attachments-import and attachments-origin catalog entries in src/native/catalog/table.rs without updating both entry-count assertions (67 -> 69; same pattern as closed bob-cli-de). Every other lib (4789) and CLI (2970) test passes. Please update both counts during gn integration. Separately FYI: bob-cli_18's uncommitted deploy (22:10Z) of bob-ledger-tools and bob-navigation-hotkeys to athena's vault makes bob plugins sync refuse the gh landing's deploy; gh.land did not force it.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-gn.1](bob-cli-gn.1.md) | bob records attachment origins and ships \`bob attachments\` | ✓ closed | medium | 2026-11-03 | 1 | 1 |
| [bob-cli-gn.2](bob-cli-gn.2.md) | Viewer shows the origin, copies it with \`y\`, restores it with \`r\` | ✓ closed | medium | 2026-11-03 | 1 | 1 |
| [bob-cli-gn.3](bob-cli-gn.3.md) | \`Z\` on an image-path bullet imports it | ✓ closed | small | 2026-11-03 | 1 | 1 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-gn: Image zoom remembers where images came from [in_progress]"]
    n1["bob-cli-gn.1: bob records attachment origins and ships `bob attachments` [closed]"]
    n2["bob-cli-gn.2: Viewer shows the origin, copies it with `y`, restores it with `r` [closed]"]
    n3["bob-cli-gn.3: `Z` on an image-path bullet imports it [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n1 -.-> n2
    n1 -.-> n3
    n2 -.-> n3
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-gn.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-gn.1.md) | [bob-cli-gn.1](bob-cli-gn.1.md) | 1 |
| [bbugyi200.athena.bob-cli-gn.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gn.2/README.md) | [bob-cli-gn.2](bob-cli-gn.2.md) | 1 |
| [bbugyi200.athena.bob-cli-gn.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gn.3/README.md) | [bob-cli-gn.3](bob-cli-gn.3.md) | 1 |
| [bbugyi200.athena.bob-cli-gn.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gn.land/README.md) | [bob-cli-gn](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`0b4cebd`](https://github.com/bobs-org/bob-cli/commit/0b4cebdf90cdd8fb8bb69ed60e07b2936c480906) | feat(attachments): record attachment origins and ship bob attachments | [bob-cli-gn.1](bob-cli-gn.1.md) | 2026-11-03 16:32:51 EST |
| bob-plugins | [`bob-plugins@1a2b572`](https://github.com/bobs-org/bob-plugins/commit/1a2b5720c2db468709858d498f04259e71bb1b23) | feat(image-zoom): add attachment origin actions | [bob-cli-gn.2](bob-cli-gn.2.md) | 2026-11-03 17:16:17 EST |
| bob-plugins | [`bob-plugins@7ad20f5`](https://github.com/bobs-org/bob-plugins/commit/7ad20f50c8eb784d827ea41248a0d47ec8d2eb0d) | feat(image-zoom): Z on an image-path bullet imports it | [bob-cli-gn.3](bob-cli-gn.3.md) | 2026-11-03 18:03:13 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-gh.land][1] | Check whether the gn epic already notes the catalog entry-count test failures from its phase 1 commit 0b4cebdf | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gh.land/README.md

<!-- sase:referenced-by:end -->
