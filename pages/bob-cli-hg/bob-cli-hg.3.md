# Bead: bob-cli-hg.3 — Message model and inert body renderer

[Bead Pages](../README.md) / [bob-cli-hg](README.md) / bob-cli-hg.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.cn](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.cn.md) · **Assignee:** `bob-cli-hg.3` · **Size:** large
**Created:** 2026-11-05 12:37:49 EST · **Closed:** 2026-11-05 22:17:25 EST
**Plan:** [202611/bob\_gmail.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bob_gmail.md)

## Description

mail-body: typed model of gog's thread JSON plus a pure renderer that turns each message's MIME tree into safe, readable Markdown (HTML sanitize, quote and signature folding, bulletin mode, image handling) and the mandatory inert pass.

## Notes

[2026-11-06T03:18:46Z · bob-cli-hg.3.1.land] VERIFICATION for mail-body landing (child epic bob-cli-hg.3.1 closed): typed model, inert renderer, transport integration, and acceptance evidence all complete. 96 gmail lib tests pass. just check stops on unrelated pre-existing clippy failures; gmail clippy clean, fmt clean. epic-symbols empty for both 3.1 and 3. Outer epic bob-cli-hg left for its waiting land agent.

## Dependencies

- **Blocks:** [bob-cli-hg.5](bob-cli-hg.5.md) ✓ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-hg.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-hg.3.md) | [bob-cli-hg.3](bob-cli-hg.3.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-he.land][1] | Need the child scope for the MimeInventory clippy error | 1 |
| read-by | [agent:bob-cli-hg.3.1.2][2] | Need phase decisions | 1 |
| read-by | [agent:bob-cli-hg.3.1.3][3] | Need parent phase decisions and Gmail renderer constraints | 1 |
| read-by | [agent:bob-cli-hg.3.1.4][4] | outer phase decisions | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-he.land/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.3.1.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.3.1.3/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.3.1.4/README.md

<!-- sase:referenced-by:end -->
