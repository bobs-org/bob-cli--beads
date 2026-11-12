# Bead: bob-cli-kq.3 — Web-clip network guards and image handling

[Bead Pages](../README.md) / [bob-cli-kq](README.md) / bob-cli-kq.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1bo](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1bo.md) · **Assignee:** `bob-cli-kq.3` · **Size:** medium
**Created:** 2026-11-12 05:24:40 EST · **Closed:** 2026-11-12 05:43:09 EST
**Plan:** [202611/security\_audit\_fixes\_1.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/security_audit_fixes_1.md)

## Description

web-clip-guards: re-validate the final navigation URL and redirect chain against host_is_global, block unguarded WebSocket handshakes, parse img attributes positionally so data-bob-origin query strings cannot drop images, and make the origin re.sub replacement literal.

## Notes

[2026-11-12T10:43:09Z · bob-cli-kq.3] Implemented all four web-clip-guards fixes in scripts/web_clip/: (A) post-goto re-validation of final URL + redirect chain via _private_landing_url in headless and headed paths, skipped for fixture hooks/--html; (B) per-context route_web_socket guard allowing only ws/wss to global hosts; (C) positional img src parse/rewrite (_img_attr/_set_img_src) in adapter _localize_images and render normalize_images/prefix_part_assets; (D) lambda re.sub for data-bob-origin insertion. Verified: just check-web-clip-adapter gate green (py_compile + self-test exit 0, 'ok'), new regression checks all pass, old-code failures reproduced in scratch probe, teardown noise confirmed pre-existing on base tree, no epic-symbol leftovers.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kq.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kq.3/README.md) | [bob-cli-kq.3](bob-cli-kq.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`4835680`](https://github.com/bobs-org/bob-cli/commit/4835680dc5e8a09bc9ab3d4537160f0254670a65) | feat(web-clip): add network guards and image handling | [bob-cli-kq.3](bob-cli-kq.3.md) | 2026-11-12 05:46:22 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-kd.6.1.4][1] | Identify what workspace 21 deployed over ledger-tools | 1 |
| read-by | [agent:bob-cli-kq.3][2] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.6.1.4/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kq.3/README.md

<!-- sase:referenced-by:end -->
