# Bead: bob-cli-fn.5 — Finish capture lists — section names with spaces, header completion, and undoable ID splices

[Bead Pages](../README.md) / [bob-cli-fn](README.md) / bob-cli-fn.5

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-fn.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-fn.land.md) · **Assignee:** `bob-cli-fn.5.land`
**Created:** 2026-11-02 07:14:36 EST
**Plan:** [202611/capture\_list\_section\_names.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_list_section_names.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/capture_list_section_names.md][1] | derived from the plan's `bead_id:` frontmatter field |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_list_section_names.md

<!-- sase:links:end -->

## Description

A list header can name any section, including one whose title has spaces (`@sase#future-work` or `@sase#"Future Work"` both reach `## Future Work`). Picking a section from the menu always inserts a selector that reaches that section. Route and section completion work on a list header even after bullets are typed below it. Accepting a block ID in Bob Mac Capture is one native Undo step. With this done, bob-cli-fn can land.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-fn.5.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fn.5.land/README.md) | [bob-cli-fn.5](bob-cli-fn.5.md) | 0 |
