# Research and manual acceptance

Research date: 2026-10-03. This compares documented formats and practices, not real-project case studies. Source links support the comparisons; they are not adoption or example dependencies.

Dated validation records describe their original snapshots. Presentation changes do not extend those records to later revisions.

## Existing conventions

### Coverage and boundaries

| Convention or practice | Solves / covers | Does not prescribe for this request |
| --- | --- | --- |
| [AGENTS.md](https://agents.md/) | Predictable repository guidance, setup, tests, conventions, and context in flexible Markdown | Common work-state meanings, topic authority, publication visibility, or a task-reading contract |
| [llms.txt](https://llmstxt.org/) | Small Markdown overview of website content with annotated links and progressive retrieval | Native repository work models, completion rules, or local-versus-published state |
| [README conventions](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes) | Familiar introduction, getting started, and documentation discovery with relative links | A shared authority and state-discovery interface |
| [Architecture Decision Records](https://cognitect.com/blog/2011/11/15/documenting-architecture-decisions.html) | Decision context, status, consequences, and supersession | Current work, planning, or repository-wide navigation |
| [Tool-specific instruction files](https://code.claude.com/docs/en/memory), [context files](https://geminicli.com/docs/cli/gemini-md/), and [repository instructions](https://docs.github.com/en/copilot/how-tos/copilot-on-github/customize-copilot/add-custom-instructions/add-repository-instructions) | Persistent or scoped guidance under tool-defined mechanisms | One tool-independent discovery and work-state contract |
| [Agent Skills](https://agentskills.io/specification) | Reusable capabilities with progressive instruction/resource loading | A plain repository map independent of capability activation |

### Use in this convention

| Convention or practice | Decision |
| --- | --- |
| AGENTS.md | Complement with a map link; a context section could be an extension, but the separate map serves all readers |
| llms.txt | Borrow the curated-map principle; do not claim format compatibility or require the website convention |
| README conventions | Adopt as the recommended discovery point, using one sentence rather than duplicating the map |
| Architecture Decision Records | Accept as an optional source; decision logs, equivalents, and no formal history remain valid |
| Tool-specific instruction files, context files, and repository instructions | Existing files may link to the map; no adapter or loading behavior is required or promised |
| Agent Skills | Borrow progressive disclosure; do not package a skill or introduce activation metadata |

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

| Check / scenario | Acceptance and initial draft result |
| --- | --- |
| Core coverage | **Expected:** Root map, template, and both examples account for every topic, with sources or explicit absence. **Initial draft result:** Checked: four sections and all source-map topics present; project, work model, publication, and loading covered outside the table |
| Discovery | **Expected:** Root README exposes the map; specification states SHOULD discovery and MAY instruction-file links; no map duplication. **Initial draft result:** Checked: one discovery sentence; README contains no source map |
| Independence | **Expected:** No automatic support claim; no real-project case names or dependencies; examples require no external access. **Initial draft result:** Checked: explicit non-support statement; excluded-name scan clear; example content uses no external URLs |
| Example references | **Expected:** Every fictional path/section corresponds to an included excerpt; at most four source documents per example. **Initial draft result:** Checked: four sources each; 23 fictional links/anchors match included content |
| Six task routes | **Expected:** Both example maps cover state, review, planning, architecture, historical decisions, and evidence. **Initial draft result:** Checked: routes walked below; each selects relevant sections or identifies a gap |
| No active work | **Expected:** If a native record says no unit is active, report None; missing records alone cannot establish that. **Initial draft result:** Checked: an explicit no-active-unit variant yields None; this package's missing tracker yields Not documented |
| Multiple active units | **Expected:** Where native rules permit several, select requested units without imposing one-active-unit rules. **Initial draft result:** Checked: variant allowing parallel F2/F3 selects requested units; unchanged example retains its native single-feature rule |
| Completed "current" unit | **Expected:** Interpret its completed state under native rules; do not call it active based on its label. **Initial draft result:** Checked: a current-label/closed-state variant is not active; an unclear active-work record remains Unknown |
| Corrective release | **Expected:** A documentation correction does not change the last completed unit unless native records say so. **Initial draft result:** Checked: W2 documentation correction leaves Design completion at W1 |
| Missing decisions | **Expected:** With no maintained decision source, report Not documented; do not create ADRs or infer no decisions. **Initial draft result:** Checked: removing the maintained decision source in a reading scenario establishes a documentation gap only |
| Stale summary | **Expected:** Use declared topic authority; an outdated summary does not overrule native state records. **Initial draft result:** Checked: stale README status cannot overrule FEATURES.md lifecycle state |
| Conflicting sources | **Expected:** Apply declared authority and report disagreement that remains unresolved. **Initial draft result:** Checked: contradictory equal-authority state records leave an explicit unresolved conflict |
| Broken reference | **Expected:** Identify the unavailable context; do not silently replace it with a summary. **Initial draft result:** Checked: inaccessible design source blocks an architecture claim without erasing known feature state |
| Wrong evidence baseline | **Expected:** Earlier-unit checks cannot validate a different unit or revision. **Initial draft result:** Checked: F1/N1 results do not validate F2/N2; W1 Design checks do not close Build/W2 |
| Remote visibility | **Expected:** Describe only the retrieved published snapshot; unseen local work and unclear provenance remain Unknown. **Initial draft result:** Checked: illustrative labels establish no real publication; remote visibility and unproven supplied-file provenance stay bounded |
| Local visibility | **Expected:** Separate working changes, commits, and publication evidence; qualify cached comparisons. **Initial draft result:** Checked: clean or committed alone leaves publication unestablished; cached refs require qualification |
| Bounded loading | **Expected:** Follow task-selected sections and references, not all history, architecture, decisions, or reviews. **Initial draft result:** Checked: feature review stops at absent matching checks/review; phase planning stops at missing predecessor closure |
| Links and simplicity | **Expected:** Actual local links/anchors resolve; specification approximately <=1,200 words; generic map <=80 lines. **Initial draft result:** Checked: 25 actual local links/anchors; 1,101 specification words; 45 template lines |
| Scope and license | **Expected:** Exactly the approved eight files; original material uses CC0-1.0; no permanent tooling or publication introduced. **Initial draft result:** Checked: file inventory matches; official CC0 terms included; inspection commands leave no scripts or test framework |

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

## Phase 2 generalization validation

The original checklist and validation record above remain historical evidence for the initial draft. This separate evaluation concerns [four additional fictional models and eleven variants](../examples/generalization-validation.md), developed on local branch `phase2/generalization-validation` from baseline `addcca02beb1c97ddf1c1649868f3331ddb96925`. No real repository serves as a test target. The sole normative contract remains [SPEC.md](../SPEC.md), version 0.1; its template is unchanged.

### Four-model evaluation matrix

The manual reading exercises below use each model's included sources. A successful mapping may establish an explicit information gap; it need not establish undocumented facts. Native selectors retain their meanings, including the level of completion and each unit's baseline.

#### Sprint

| Core question | Mapping |
| --- | --- |
| Can Project be mapped? | README describes Iteration Board. |
| Can Published State be mapped? | Handoff source locates the supplied snapshot, independent of completion. |
| Can Work Model remain native? | Sprint and item states/closure rules remain distinct. |
| Can Current Work be determined? | S8 open; I4/I5 doing. |
| Can Last Completed Work be determined? | S7 for sprints; I3 for items; no invented cross-level ordering. |
| Can Planned Work be represented? | S9 plan has an unmet S8-closeout dependency. |
| Can Architecture remain native? | Board/store/filter/sorter design. |
| Can Decisions remain optional/native? | D1/D2 live in notes. |
| Can Evidence be selected by unit/baseline? | I4/SB8 differs from I3/SB7 and S7/SB6. |
| Can progressive loading avoid blanket reading? | Select item or sprint and stop at its answer/gap. |

#### Release / milestone

| Core question | Mapping |
| --- | --- |
| Can Project be mapped? | README describes Package Ledger. |
| Can Published State be mapped? | Handoff distinguishes sharing from release closure and authorization. |
| Can Work Model remain native? | Release and change rules remain distinct. |
| Can Current Work be determined? | R3 preparing; C32 validating. |
| Can Last Completed Work be determined? | R2 for releases; C31 for changes; selection is level-specific. |
| Can Planned Work be represented? | R4 plan does not authorize work or publication. |
| Can Architecture remain native? | Formatter/assembler design. |
| Can Decisions remain optional/native? | D1 lives with checks. |
| Can Evidence be selected by unit/baseline? | C32/RC32 and R3/RA3 require different evidence. |
| Can progressive loading avoid blanket reading? | Select change or assembled release and relevant checks. |

#### Experiment / research

| Core question | Mapping |
| --- | --- |
| Can Project be mapped? | README describes Sample Study. |
| Can Published State be mapped? | Notebook handoff works without a release record. |
| Can Work Model remain native? | Hypothesis outcomes and signed closure remain distinct; no implementation lifecycle. |
| Can Current Work be determined? | X5 running. |
| Can Last Completed Work be determined? | X4 is last signed, with inconclusive outcome. |
| Can Planned Work be represented? | X6 proposal requires X5 closure and a start decision. |
| Can Architecture remain native? | Study and data-flow structure; no code required. |
| Can Decisions remain optional/native? | Q1/Q2 live in method rationale without ADRs. |
| Can Evidence be selected by unit/baseline? | X5/P2/D5/A1 differs from X4 and other protocol revisions. |
| Can progressive loading avoid blanket reading? | Select investigation, protocol, and matching result. |

#### Maintenance / operations

| Core question | Mapping |
| --- | --- |
| Can Project be mapped? | README describes Queue Care. |
| Can Published State be mapped? | Documentary handoff establishes no operational deployment. |
| Can Work Model remain native? | Incident and maintenance states remain distinct. |
| Can Current Work be determined? | I1 mitigating; M1 executing. |
| Can Last Completed Work be determined? | Last ledger entry M0 is complete under maintenance rules. |
| Can Planned Work be represented? | M2 queue entry requires M1 completion; no roadmap needed. |
| Can Architecture remain native? | Queue/workers/store and relevant procedures. |
| Can Decisions remain optional/native? | D1 lives in a runbook without a formal log. |
| Can Evidence be selected by unit/baseline? | M1/MB2 differs from M0/MB1 and I1/IB2. |
| Can progressive loading avoid blanket reading? | Select incident/task and relevant runbook sections. |

| Work model | Final classification | Finding |
| --- | --- | --- |
| Sprint-based | Works as-is | Existing topic qualifiers and native selectors distinguish sprint and item completion. |
| Release / milestone-based | Works as-is | Plans, change completion, release closure, authorization, and publication remain separate. |
| Experiment / research-based | Works as-is | Native results and signed closure map without an implementation lifecycle. |
| Maintenance / operations-based | Works as-is | Concurrent heterogeneous units and a queue map without a product roadmap. |

### Six task-route results

All 24 new-model routes were walked against the included sources. The linked model sections contain the exact selection paths and reading stops; the following tables record their resulting answers or gaps. Each result is limited to the fictional records.

#### Sprint route results

[Detailed selection and stops](../examples/generalization-validation.md#sprint-task-routes).

| Route | Result |
| --- | --- |
| Current state | S8 open, I4/I5 doing; completion is level-specific. |
| Review current work | S8/SB8 review/closeout absent; I4/SB8 checks unrun. Stop at the selected gap. |
| Plan next work | S9 awaits absent S8 closeout; stop. |
| Architecture | Intended board/store/filter/sorter; stop at structural answer. |
| Historical decision | D1 superseded by accepted D2; stop at no successor. |
| Evidence audit | I4/SB8 unrun; earlier units cannot validate it. |

#### Release route results

[Detailed selection and stops](../examples/generalization-validation.md#release-task-routes).

| Route | Result |
| --- | --- |
| Current state | R3 preparing, C32 validating; no inferred publication. |
| Review current work | C32/RC32 checks unrun; stop at missing checks. |
| Plan next work | R4 awaits absent R3 closeout; stop. |
| Architecture | Intended formatter/assembler; stop at structural answer. |
| Historical decision | Accepted D1; stop at no recorded supersession. |
| Evidence audit | R3/RA3 assembled checks unrun; change checks cannot validate it. |

#### Research route results

[Detailed selection and stops](../examples/generalization-validation.md#research-task-routes).

| Route | Result |
| --- | --- |
| Current state | X5 running; X4 last signed despite inconclusive outcome. |
| Review current work | X5 matching comparison inconclusive, signoff absent; stop at those limits. |
| Plan next work | X6 awaits absent X5 signed closure; stop. |
| Architecture | Intended grouped-observation study; stop at structural answer. |
| Historical decision | Q1 superseded by accepted Q2; stop at no successor. |
| Evidence audit | X5/P2/D5/A1 inconclusive, no signoff; X4 cannot close it. |

#### Operations route results

[Detailed selection and stops](../examples/generalization-validation.md#operations-task-routes).

| Route | Result |
| --- | --- |
| Current state | I1 mitigating and M1 executing; no service-health inference. |
| Review current work | I1 probe inconclusive, resolution/review absent; stop at that gap. |
| Plan next work | M2 awaits M1 completion; stop while M1 executes. |
| Architecture | Intended queue/workers/store and procedure; stop at structural answer. |
| Historical decision | Runbook D1 accepted; stop at no recorded supersession. |
| Evidence audit | M1/MB2 unrun; M0's result cannot validate it. |

### Eleven cross-cutting cases

Each variant was read independently against the base excerpts and [variant definitions](../examples/generalization-validation.md#cross-cutting-variants). That document records sources, established facts, unknown/undocumented information, stops, and classification. Intentional missing context in E08 is a passing uncertainty-handling exercise, not a broken base-fixture reference.

| Case | Result, stop, and classification |
| --- | --- |
| E01 No active work | Explicit State absence yields None; stop at State, without treating plans as active. **Classification:** Works as-is |
| E02 Multiple active Work Units | Both sprint items and heterogeneous operational units remain active; stop at selected state, expanding only for the requested review. **Classification:** Works as-is |
| E03 No formal roadmap | Native queue covers plans; without a maintained queue, Planned Work is Not documented and actual plans Unknown. Stop at queue/absence. **Classification:** Works as-is |
| E04 No formal decision log | Equivalent rationale answers history; removing it yields Not documented, not proof of no decisions. Stop at record/absence. **Classification:** Works as-is |
| E05 No formal release record | Handoff locates a snapshot without a release log; removing it leaves the source Not documented and publication unestablished. Stop at provenance/absence. **Classification:** Works as-is |
| E06 Stale summary | Topic-authoritative operational state wins over README summary; stop at State and report discrepancy. **Classification:** Works as-is |
| E07 Conflicting sources | Equal-authority same-snapshot conflict leaves X5 state Unknown; stop at unresolved disagreement. **Classification:** Works as-is |
| E08 Missing or broken reference | Known state/baseline survives; missing selected protocol blocks method-compliance claims. Stop at the missing section. **Classification:** Works as-is |
| E09 Evidence from another baseline | Different unit or protocol revision cannot validate selected X5 baseline; stop at mismatch. **Classification:** Works as-is |
| E10 Local work newer than published snapshot | Published, local-committed, and working changes stay distinct; unseen local work/publication remains Unknown. Stop at visible provenance. **Classification:** Works as-is |
| E11 Very little formal documentation | One README covers purpose/structure/work rules; other sources are Not documented and facts Unknown. Stop at the relevant section or absence. **Classification:** Works as-is |

### Existing-example regression controls

The [feature](../examples/feature-based.md) and [phase](../examples/phase-based.md) examples were reread unchanged. All twelve control routes preserve their original native behavior; the new examples impose no parallel-work or closure rules on them.

#### Feature control

| Route | Result |
| --- | --- |
| Current state | State selects F2 active; Completions identifies F1 if needed. Stop at those records; retain one-active-feature rule. |
| Review current work | F2 contract + N2 Evidence establish unrun checks and absent review. Stop at that gap; Structure is conditional. |
| Plan next work | State/Rules + F3 scope show queued export dependent on F1; deliberate authorization remains required. Stop after applicable dependency/completion evidence. |
| Architecture | DESIGN.md Structure describes editor/store/search intention; stop without runtime claims. |
| Historical decision | D1 accepted, no recorded successor; stop. |
| Evidence audit | F2/N2 lacks checks/review; F1/N1 cannot validate it. Stop at missing matching evidence. |

#### Phase control

| Route | Result |
| --- | --- |
| Current state | State selects Build current and Design last closed. Stop at relevant State records; retain sequential phases. |
| Review current work | Build scope + W2 checks establish unrun checks and absent closeout. Stop at that gap. |
| Plan next work | State/Rules + Validate scope require Build closure; Build checks show missing closeout. Stop at unmet predecessor gate. |
| Architecture | NOTES.md Structure describes catalog/schedule intention; stop without runtime claims. |
| Historical decision | D1 accepted at Design, no recorded successor; stop. |
| Evidence audit | Build/W2 lacks checks/closeout; Design/W1 cannot close it. Stop at missing matching evidence. |

### Explanatory findings and decision gate

Three findings are **Documentation clarification only**: review scope can mean native protocol/procedure without implementation; a plan can live in notes/queues without a roadmap; container/item completion uses qualified native selectors rather than a universal latest-unit order. The new document explains these interpretations. No normative text or template field needed alteration. No finding is **Possible future extension** or **Actual Core limitation**.

1. **Does the existing v0.1 Core cover all tested work models?** Yes, for the six fictional models and stated reading exercises, including explicit gaps and uncertainty where sources cannot establish facts.
2. **Were specification changes genuinely necessary?** No. All mappings use existing topics, columns, native selection rules, and absence/uncertainty meanings.
3. **Were any findings explanatory only?** Yes, the three interpretations above; additions are examples and validation documentation.
4. **Is there evidence for formal profiles?** No. Distinct workflows are described through native sources without formal profiles.
5. **Is there evidence for a v0.2 semantic change?** No. No unrepresentable concept or incompatible structural requirement was found.
6. **Can v0.1 remain unchanged?** Yes. SPEC.md and templates/REPO_CONTEXT.md remain unchanged.

### Phase 2 validation record

Reviewed on 2026-10-03 for the local Phase 2 documentation draft: one new generalization document, this appended research section, and one README discovery link, based on the baseline named above. All 24 new-model task routes, twelve existing-example control routes, and eleven edge-case groups were checked by manual reading against their included sources and stated variants. The four-model matrix accounts for all ten Core questions. All four models and eleven edge cases are Works as-is; the three interpretation findings are Documentation clarification only.

Disposable structural inspection verified 37 actual local Markdown links/anchors and 64 fictional Markdown links/anchors across the six models, including all 41 in the new models. It also checked 72 fictional path mentions against included files/sections. Each new model has three sources besides its map; the combined document has 355 lines. All nine existing external Markdown destinations were retrieved successfully; their research comparisons were not reevaluated. E08 deliberately removes a protocol only within its variant; every base-fixture reference resolves. No permanent script, validator, schema, profile, or test framework was added.

Scope and diff review confirmed exactly the three authorized paths, one README link without copied validation details, and preservation of the original research text, both regression examples, SPEC.md, the template, root map, and license. Whitespace checks passed. The new fictional material contains no external URLs or references to real/private projects; it was authored solely from invented data, without reading or copying external-project content. All file writes and Git mutations were confined to this repository and the Phase 2 branch; no other repository was used as a test target or modified by this work. Local main, cached origin/main, and the directly queried remote main remained at the baseline; the remote Phase 2 branch was absent at inspection.

These results apply to this documentation content and the specified reading exercises. They establish neither runtime behavior, live operational observations, actual fictional publication, nor independent assistant compatibility. The local commit containing this record is not publication evidence. Recheck after material changes; the original validation record above retains its original scope.
