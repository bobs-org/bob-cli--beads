# Bead: bob-cli-qq.10.1 — Bring the Reading cabinet paint within the 2x inline budget

[Bead Pages](../README.md) / [bob-cli-qq.10](bob-cli-qq.10.md) / bob-cli-qq.10.1

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.g7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.g7.md) · **Assignee:** `bob-cli-qq.10.1` · **Size:** medium
**Created:** 2026-11-27 09:12:20 EST
**Plan:** [202611/finish\_property\_card\_cabinets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/finish_property_card_cabinets.md)

## Description

perf: profile the gate-open Reading paint of the 106-record album and the 64-row Projects host. Remove the double render and paint the breakdown confirms, without weakening fail-open or parity. Prove both perf checks pass in two athena runner runs.

## Notes

[2026-11-27T14:21:40Z · bob-cli-qq.10.1] perf profile breakdown (code inspection + attempt-28 runner medians), recorded before choosing the fix.

Gate-open Reading paint path for a catalog host (projects 64 rows; records 106 rows):
1. Obsidian renders the stored callout natively (unavoidable; the gate-closed inline baseline pays this too).
2. The kind's inline Reading painter decorates the native callout synchronously in its
   Markdown postprocessor (priorities 51-53: albums 51, records 52, projects 53, areas similar).
   Cost scales with row count (per-row DOM work over 64/106 rows).
3. The property-card host postprocessor (priority 46/47) batches via setTimeout(0), then
   paintReading mounts the card synchronously: foot build + propertyCardCabinetsAssemble
   (provider applies checks are sync, cached reports) + onMounted claims + Reading
   absorption hides the native callout.
4. The default-open body builds async: propertyCardCabinetRenderCatalog runs a SECOND
   full MarkdownRenderer.render of the same region source plus the same painter again,
   then binds links/hover. The body cache never helps across opens (a body inside another
   mount's container is not orphaned, so the fresh mount re-renders).
5. measureCatalogPaint stops the clock when cabinet-body li rows exist.

Attempt-28 medians (gate open vs inline): Projects 146-147ms vs 65-70ms (2.1-2.25x);
album 127-138ms vs 65-69ms (1.84-2.12x). Cabinet ~= inline + (inline painter + card
mount/stack + body re-render + body paint). The inline painter pass (step 2) is pure
waste under an open gate: its output is hidden by absorption in the same frame (each
painter already paint-then-strips when it sees a mounted stack). Removing it shortens
the measured window by the full painter cost with no new work added.

Chosen fix (plan candidate 1): defer the inline Reading painter for the measured kinds
(projects, records) when the gate is open on an eligible Reading surface. Skip the
synchronous paint; keep widget tracking; one bounded fallback timer (150ms, max 3
re-arms) paints the native callout only if no cabinet absorption covers it by then
(never-claimed, claim failed/released, card never mounted). Live Preview untouched.
Fail-open preserved: every path that shows the stored section paints it exactly as
today, only slightly later; plus 240wj failure branches now call a repaintNative hook
threaded from the kind providers (existing schedule*Refresh loops) so a failed body
still leaves today's painted catalog visible. No 240c surface/retry changes
(reading-miss owns that); no stored-byte or vault-format changes.

## Dependencies

- **Blocks:** [bob-cli-qq.10.4](bob-cli-qq.10.4.md) ◐ · ⧖ 2026-11-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-qq.10.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qq.10.1/README.md) | [bob-cli-qq.10.1](bob-cli-qq.10.1.md) | 0 |
