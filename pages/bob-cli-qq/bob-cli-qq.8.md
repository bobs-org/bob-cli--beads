# Bead: bob-cli-qq.8 — Real-Obsidian acceptance and screenshot review with the gate open

[Bead Pages](../README.md) / [bob-cli-qq](README.md) / bob-cli-qq.8

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.6m.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.6m.linker.w0.md) · **Assignee:** `bob-cli-qq.8` · **Size:** medium
**Created:** 2026-11-26 16:09:03 EST
**Plan:** [202611/property\_card\_cabinets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/property_card_cabinets.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:4e093423e907fab57e92e9db | attached via sase artifact create --bead |
| related | file:explicit:c152d5bb0c1567dc6d249e66 | attached via sase artifact create --bead |

_Plus 4 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

acceptance: build a sibling scratch-vault e2e runner. It opens the cabinets gate and every sibling species gate, and covers every species in Live Preview and Reading, the full keyboard matrix, fail-open contexts, and the passive spy. It also checks content parity and screenshots light/dark, narrow/wide, reduced-motion, and forced-colors before a GO/NO-GO.

## Notes

[2026-11-27T03:27:51Z · bob-cli-qq.8--1] PROPOSED FOLLOW-UP: Bring docs/reference/vault-format.md under the docs word limit — npm run docs:check reproduces the same 30-word overrun on the clean bob-cli base checkout, unrelated to Cabinets acceptance.

[2026-11-27T13:06:40Z · bob-cli-qq.8] VERDICT: NO-GO (attempts 18-29). Recovered attempt 17 (passed 91 checks) from athena scratch; its fixes were never committed and the workspace-12 checkout is gone. Re-applied onto bob-plugins master. The visual review found defects attempt 17 had passed, fixed in place with runner guards: Live Preview hid only the last-mounted catalog (240wg: one claim per kind), a repaint lifted the claim (240wg: leases), a dropped claim was never re-asserted (240wg), the row guard rejected bob's **Closed** row and legacy markers (240wf), heads centered or wrapped at 420px (Cabinets CSS), and open cabinets showed blank bodies because the body cache moved painted nodes between mounts (240wj/240wl). Final source (attempt 28): 94/97 checks pass, 0 exceptions, 0 passive writes/spawns; all 58 PNGs reviewed. Evidence: file:explicit:4e093423e907fab57e92e9db (review in attempt-28/acceptance-review.md); attempts 1-17: file:explicit:c152d5bb0c1567dc6d249e66. Rebased onto 56baeb9: npm test 10239 pass, 0 fail (test:perf timing passes 3/3 when rerun under load); bob-ledger-tools 1.172.5 synced (gate closed in vault).

[2026-11-27T13:06:48Z · bob-cli-qq.8] REMAINING WORK (does not fit one agent; the phase stays NO-GO): (1) Perf budget (cabinet <=2x inline, no added long task >100ms), measured in Reading by the new perf-* runner checks: 64-row Projects host 146 vs 65 ms (2.25x, 51-58 ms long tasks) and 106-record album 127-138 vs 65-69 ms (1.84-2.12x). Likely cost: the stored callout is rendered and painted before absorption hides it, and the cabinet renders a second copy. (2) Intermittent Reading card miss in the shared 240c host (attempts 10, 12, 20, 21, 24, 27, 28). Diagnostics show every tracked widget has a detached postprocessed element, no surface, and exhausted retries, while the live preview has no card. A blanket preview re-render (attempt 29) wiped Reading absorption tags and was reverted. A fix must re-render only when no host has mounted a card for that note, and never for card-less notes. Rerun obsidian-cabinets-e2e.cjs after both and record GO.

[2026-11-27T13:06:55Z · bob-cli-qq.8] PROPOSED FOLLOW-UP: Footer pick overlay clips at both ends at 420 px — the armed status-bar strip shows "abinets 1 Albums ..." and "- Properties ..." with the leading "Cabinets" and trailing "esc" cut; it should truncate one end with an ellipsis (see footer-*-narrow-armed shots in file:explicit:4e093423e907fab57e92e9db).

[2026-11-27T13:07:02Z · bob-cli-qq.8] PROPOSED FOLLOW-UP: The Areas cabinet body repeats the stored callout title row ("Areas 1 area" with its icon) directly under the header that already reads "Areas · 1 area"; the other host cabinets lift the title into the header. Drop or hide the callout title inside cabinet bodies (241al/241aj).

## Dependencies

- **Depends on:** [bob-cli-qq.5](bob-cli-qq.5.md) ✓ · ⧖ 2026-11-26
- **Depends on:** [bob-cli-qq.6](bob-cli-qq.6.md) ✓ · ⧖ 2026-11-26
- **Depends on:** [bob-cli-qq.7](bob-cli-qq.7.md) ✓ · ⧖ 2026-11-26
- **Blocks:** [bob-cli-qq.9](bob-cli-qq.9.md) ◐ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-qq.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qq.8/README.md) | [bob-cli-qq.8](bob-cli-qq.8.md) | 8 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@7e0ba56`](https://github.com/bobs-org/bob-plugins/commit/7e0ba5695e86ea88c4f103e682c38e342f43a701) | test(cabinets): add real Obsidian acceptance runner | [bob-cli-qq.8](bob-cli-qq.8.md) | 2026-11-26 22:14:41 EST |
| bob-plugins | [`bob-plugins@18e6cb9`](https://github.com/bobs-org/bob-plugins/commit/18e6cb9980eb028d04f8841fea9f0cd2ac85d207) | test(cabinets): retain failed real-Obsidian acceptance evidence | [bob-cli-qq.8](bob-cli-qq.8.md) | 2026-11-26 22:48:25 EST |
| bob-plugins | [`bob-plugins@bd1af86`](https://github.com/bobs-org/bob-plugins/commit/bd1af8607014226cc86b75845c5739032295643a) | fix(cabinets): add report fixtures and record properties stack | [bob-cli-qq.8](bob-cli-qq.8.md) | 2026-11-26 23:24:11 EST |
| bob-plugins | [`bob-plugins@66667b1`](https://github.com/bobs-org/bob-plugins/commit/66667b1c224fd2403f0ac7ceb9d46850d091441e) | test(cabinets): preserve attempt 4 report and attempt 5 launcher | [bob-cli-qq.8](bob-cli-qq.8.md) | 2026-11-26 23:38:01 EST |
| bob-plugins | [`bob-plugins@f279186`](https://github.com/bobs-org/bob-plugins/commit/f279186d37b5cad0054cec52bfb1e9b85d0e5f4e) | fix(cabinets): preserve Obsidian startup diagnostics | [bob-cli-qq.8](bob-cli-qq.8.md) | 2026-11-26 23:50:30 EST |
| bob-plugins | [`bob-plugins@e9f0c07`](https://github.com/bobs-org/bob-plugins/commit/e9f0c0703a8b10576663374883e2bb4b0ad277c2) | fix(cabinets-e2e): isolate Xvfb temporary storage | [bob-cli-qq.8](bob-cli-qq.8.md) | 2026-11-27 00:16:24 EST |
| bob-plugins | [`bob-plugins@c476086`](https://github.com/bobs-org/bob-plugins/commit/c476086a9a7135ad944993ed9ea0d715ec3fcddd) | fix(cabinets): repair acceptance fixtures and narrow bank layout | [bob-cli-qq.8](bob-cli-qq.8.md) | 2026-11-27 00:57:29 EST |
| bob-plugins | [`bob-plugins@28e7573`](https://github.com/bobs-org/bob-plugins/commit/28e7573951895c58e1917815d96e08c646b873ae) | fix(cabinets): absorb every Live Preview catalog and keep cabinet bodies painted | [bob-cli-qq.8](bob-cli-qq.8.md) | 2026-11-27 08:08:11 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-qq.7][1] | list epic children statuses | 1 |
| read-by | [agent:bob-cli-qq.8--2][2] | Resume the requested real-Obsidian Cabinets acceptance and inspect current phase obligations | 1 |
| read-by | [agent:bob-cli-qq.8--3][2] | Inspect the assigned Cabinets epic scope and its required closure workflow | 1 |
| read-by | [agent:bob-cli-qq.8--7][2] | Check assigned epic phases and notes before completing the requested acceptance closeout | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qq.7/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-qq.8.md

<!-- sase:referenced-by:end -->
