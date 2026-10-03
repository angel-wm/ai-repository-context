# Research and manual acceptance

Research date: 2026-10-03. This compares documented formats and practices, not real-project case studies. Source links support the comparisons; they are not adoption or example dependencies.

## Existing conventions

| Convention or practice | Solves / covers | Does not prescribe for this request | Decision |
| --- | --- | --- | --- |
| [AGENTS.md](https://agents.md/) | Predictable repository guidance, setup, tests, conventions, and context in flexible Markdown | Common work-state meanings, topic authority, publication visibility, or a task-reading contract | Complement with a map link; a context section could be an extension, but the separate map serves all readers |
| [llms.txt](https://llmstxt.org/) | Small Markdown overview of website content with annotated links and progressive retrieval | Native repository work models, completion rules, or local-versus-published state | Borrow the curated-map principle; do not claim format compatibility or require the website convention |
| [README conventions](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes) | Familiar introduction, getting started, and documentation discovery with relative links | A shared authority and state-discovery interface | Adopt as the recommended discovery point, using one sentence rather than duplicating the map |
| [Architecture Decision Records](https://cognitect.com/blog/2011/11/15/documenting-architecture-decisions.html) | Decision context, status, consequences, and supersession | Current work, planning, or repository-wide navigation | Accept as an optional source; decision logs, equivalents, and no formal history remain valid |
| [Tool-specific instruction files](https://code.claude.com/docs/en/memory), [context files](https://geminicli.com/docs/cli/gemini-md/), and [repository instructions](https://docs.github.com/en/copilot/how-tos/copilot-on-github/customize-copilot/add-custom-instructions/add-repository-instructions) | Persistent or scoped guidance under tool-defined mechanisms | One tool-independent discovery and work-state contract | Existing files may link to the map; no adapter or loading behavior is required or promised |
| [Agent Skills](https://agentskills.io/specification) | Reusable capabilities with progressive instruction/resource loading | A plain repository map independent of capability activation | Borrow progressive disclosure; do not package a skill or introduce activation metadata |

Generated code maps address code structure and symbols, a different navigation layer from work-state, completion, and evidence sources. They may coexist with this convention but are neither required nor implemented. This is a scope distinction, not a claim to have evaluated every code-mapping tool.

## Recommendation

Define a narrow Markdown context-discovery convention that combines familiar discovery and link-based documentation with explicit meanings for authority, work, and visibility. The reviewed formats can host much of it; their documented contracts do not prescribe this entire combination. That is a finding about the reviewed sources, not proof that no other proposal exists.

The map introduces no replacement state store. Root README discovery leads to `REPO_CONTEXT.md`, which leads to existing authoritative sources. A separate map keeps the interface available to humans and tools without adopting an agent instruction file as the required entry point. It does not gain automatic tool support from its name.

One universal Core and a generic Work Unit term are sufficient for v0.1. The [feature](../examples/feature-based.md) and [phase](../examples/phase-based.md) examples contain all their fictional sources and demonstrate mapping differences without profiles. Explicit absence/uncertainty distinguishes missing information from recorded lack of work. Topic authority prevents a summary from silently becoming lifecycle truth.

This rationale supports [the specification](../SPEC.md); it is not an independent normative contract or a formal decision-history log.

## Deliberately excluded

No formal profiles or inheritance, universal statuses, copied work-state summaries, publication-hash maintenance, mandatory ADRs, session archives, frontmatter, schemas, tools, scripts, validators, generators, agents, RAG, CI, services, or automatic publication. No real-project case studies or dependencies appear in the published examples. Optional sources and instruction-file links do not create required tooling.

## Manual acceptance checklist

Review the current documentation snapshot after material changes. Use the included fictional excerpts for scenarios; do not access any external example repository. These are manual reading exercises, not executable tests. Mark a result only after checking it. Structural scans may be run as disposable inspection commands; no permanent tooling belongs in the package.

| Check / scenario | Expected result | Initial draft result |
| --- | --- | --- |
| Core coverage | Root map, template, and both examples account for every topic, with sources or explicit absence | Checked: four sections and all source-map topics present; project, work model, publication, and loading covered outside the table |
| Discovery | Root README exposes the map; specification states SHOULD discovery and MAY instruction-file links; no map duplication | Checked: one discovery sentence; README contains no source map |
| Independence | No automatic support claim; no real-project case names or dependencies; examples require no external access | Checked: explicit non-support statement; excluded-name scan clear; example content uses no external URLs |
| Example references | Every fictional path/section corresponds to an included excerpt; at most four source documents per example | Checked: four sources each; 23 fictional links/anchors match included content |
| Six task routes | Both example maps cover state, review, planning, architecture, historical decisions, and evidence | Checked: routes walked below; each selects relevant sections or identifies a gap |
| No active work | If a native record says no unit is active, report None; missing records alone cannot establish that | Checked: an explicit no-active-unit variant yields None; this package's missing tracker yields Not documented |
| Multiple active units | Where native rules permit several, select requested units without imposing one-active-unit rules | Checked: variant allowing parallel F2/F3 selects requested units; unchanged example retains its native single-feature rule |
| Completed "current" unit | Interpret its completed state under native rules; do not call it active based on its label | Checked: a current-label/closed-state variant is not active; an unclear active-work record remains Unknown |
| Corrective release | A documentation correction does not change the last completed unit unless native records say so | Checked: W2 documentation correction leaves Design completion at W1 |
| Missing decisions | With no maintained decision source, report Not documented; do not create ADRs or infer no decisions | Checked: removing the maintained decision source in a reading scenario establishes a documentation gap only |
| Stale summary | Use declared topic authority; an outdated summary does not overrule native state records | Checked: stale README status cannot overrule FEATURES.md lifecycle state |
| Conflicting sources | Apply declared authority and report disagreement that remains unresolved | Checked: contradictory equal-authority state records leave an explicit unresolved conflict |
| Broken reference | Identify the unavailable context; do not silently replace it with a summary | Checked: inaccessible design source blocks an architecture claim without erasing known feature state |
| Wrong evidence baseline | Earlier-unit checks cannot validate a different unit or revision | Checked: F1/N1 results do not validate F2/N2; W1 Design checks do not close Build/W2 |
| Remote visibility | Describe only the retrieved published snapshot; unseen local work and unclear provenance remain Unknown | Checked: illustrative labels establish no real publication; remote visibility and unproven supplied-file provenance stay bounded |
| Local visibility | Separate working changes, commits, and publication evidence; qualify cached comparisons | Checked: clean or committed alone leaves publication unestablished; cached refs require qualification |
| Bounded loading | Follow task-selected sections and references, not all history, architecture, decisions, or reviews | Checked: feature review stops at absent matching checks/review; phase planning stops at missing predecessor closure |
| Links and simplicity | Actual local links/anchors resolve; specification approximately <=1,200 words; generic map <=80 lines | Checked: 25 actual local links/anchors; 1,101 specification words; 45 template lines |
| Scope and license | Exactly the approved eight files; original material uses CC0-1.0; no permanent tooling or publication introduced | Checked: file inventory matches; official CC0 terms included; inspection commands leave no scripts or test framework |

### Task-route walkthroughs

These outcomes come from reading the included fictional sources. Edge-case rows above also use hypothetical textual variants; the example excerpts remain unchanged. No application tests, independent agent evaluations, or external publication checks were performed.

| Task | Feature example | Phase example |
| --- | --- | --- |
| State | FEATURES.md State selects F2 active; Completions selects F1 only if needed | CURRENT_STATE.md State selects Build current and Design last closed |
| Review | F2 contract and N2 evidence identify unrun checks and absent review; Structure is conditional | Build scope and W2 checks identify unrun checks and missing closeout |
| Plan | F3 is queued and depends on F1; starting still needs deliberate authorization | Validate depends on Build closure; required predecessor closeout is missing, so it cannot start |
| Architecture | DESIGN.md Structure describes editor/store/search intention; it proves no runtime behavior | NOTES.md Structure describes catalog/schedule intention; it proves no runtime behavior |
| Historical decision | D1 is accepted and has no recorded supersession; no other history is needed | D1 is accepted at Design and has no recorded supersession |
| Evidence | Match F1/N1 or F2/N2; passing earlier checks establish no current-unit validity | Match Design/W1 or Build/W2; earlier closure establishes no Build result |

## Validation record

Reviewed on 2026-10-03 for the initial local v0.1 documentation draft, comprising the specification, README, root map, template, two examples, this research/checklist document, and license. All 19 checklist rows were checked through document inspection, manual reading walkthroughs, and disposable structural inspection commands. The inspection found 25 actual local links/anchors and 23 fictional links/anchors matching their included sources. Size checks found 1,101 specification words and 45 template lines. Whitespace and file-scope checks passed.

Results apply only to this local documentation draft and the stated reading scenarios. They do not establish a published release, later revision, example runtime behavior, or automatic assistant compatibility. Recheck after material changes. This record is supporting evidence, not a work tracker or publication record.
