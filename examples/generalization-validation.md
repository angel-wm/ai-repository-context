# Generalization validation: fictional work models

These four invented projects test the existing [v0.1 Core](../SPEC.md#core). All sources, baselines, results, and snapshots are illustrative. No application, external repository, real publication, or underlying report exists. Each model includes its map and all three fictional sources; links inside fences refer only to that model's excerpts. The variants below replace stated excerpts for a reading exercise, not files in another repository.

Reading paths: [sprint](#sprint-task-routes), [release](#release-task-routes), [research](#research-task-routes), [operations](#operations-task-routes), and [edge cases](#cross-cutting-variants).

## Shared reading contract

The four sample maps use the existing sections and columns, without profiles or new fields. Preserve native rules; select units from native state before opening their evidence. A topic qualifier distinguishes container and item questions where needed; it introduces no universal hierarchy or ordering. Interpret review scope as the unit's native contract, protocol, or procedure; there need not be an implementation.

Read applicable guidance, the map, and task-selected sections. Apply declared topic authority, report unresolved conflicts, and identify unavailable references without replacing them with summaries. Stop at a supported answer or a specific gap. No directory, link chain, or evidence index requires blanket reading. All routes below apply this contract; their stops exclude unrelated records unless the task requires expansion.

The handoff sources describe supplied fictional snapshots, not actual publication. Remote readers leave unseen local work **Unknown**. Local readers distinguish working changes, commits, and publication evidence, qualifying cached remote comparisons. A clean checkout, a completion, or a handoff reference alone proves no publication. Missing maintained sources are **Not documented**; recorded absence is **None**; an answer not established by available information is **Unknown**.

## Sprint-based

### Sprint map

```markdown
# Repository context

## Project

- Project: Iteration Board; a fictional task board.
- Convention version: **0.1**.
- Description: [Project](README.md#project).
- Work Unit: sprint; its items retain their own native rules.
- Work Model: [Rules](ITERATIONS.md#rules).

## Published state

Handoff: [Handoff](README.md#handoff). Repository/ref: **Not
documented**; no remote exists. Describe the supplied snapshot; unseen
local work is Unknown. Distinguish local changes, commits, and
publication evidence; qualify cached comparisons.

## Source map

| Topic / purpose | Source | Authority | Read when |
| --- | --- | --- | --- |
| Current Work / sprint and items | [State](ITERATIONS.md#state); select open sprints and doing items | Native work state | State or unit selection |
| Last Completed Work / sprint or item | [Completions](ITERATIONS.md#completions); select the last entry in the requested ledger | Completion at that level | Latest completion matters |
| Planned Work | [State](ITERATIONS.md#state); select planned sprints or backlog items | Plans, not start permission | Planning |
| Architecture | [Structure](NOTES.md#structure) | Intended structure | Structure questions or affected scope |
| Decisions | [Decisions](NOTES.md#decisions); select D1 or D2 and its successor | Recorded rationale | Decision history |
| Validation / Evidence | [Evidence](NOTES.md#evidence); match sprint or item and baseline selected from state/completions | Results for that unit/baseline | Review or evidence audit |

## Loading rules

- State: State, then the requested completion ledger if relevant.
  Review: Rules, selected sprint/item scope in State, then matching
  Evidence.
- Plan: State and Rules, then required completion/evidence.
  Architecture: Structure, expanding only for an affected decision.
- History: selected decision and successor. Evidence: selected
  unit/baseline and its record. Apply the shared reading contract; stop
  at an answer or gap.
```

### Sprint task routes

| Task | Selected sources, result, and stop |
| --- | --- |
| Current state | Rules + State establish S8 open and I4/I5 doing. Completions gives S7 or I3 when the requested level matters; stop without inventing a global latest unit. |
| Review current work | Select S8 or I4 from State; read Rules, that scope, and matching Evidence. S8/SB8 lacks review/closeout; I4/SB8 checks are NOT RUN. Stop at the selected gap; Structure is needed only for a design question. |
| Plan next work | State + Rules select S9 and require S8 closeout. Completions establishes that closeout is absent; stop there. Neither item completion nor the plan permits starting S9. |
| Architecture | Structure describes store/filter/sorter intention; stop for that question. Actual implementation and runtime behavior remain unestablished. |
| Historical decision | Decisions selects D1, follows D2, and establishes the changed rationale and D2's accepted status; stop at no recorded successor. |
| Evidence audit | State selects I4/SB8; Evidence records unrun checks. Stop at that gap; I3/SB7 and S7/SB6 cannot validate I4. |

### Sprint sources

#### README.md

```markdown
# Iteration Board

## Project

A fictional board for grouping tasks into iterations. Context:
[map](REPO_CONTEXT.md).

## Handoff

The shared illustrative snapshot SB8 includes the state below. No actual
publication is asserted; completing an item or sprint is independent of
sharing a snapshot.
```

#### ITERATIONS.md

```markdown
# Iterations

## Rules

Sprints are planned, open, or closed; items are backlog, doing, or done.
Open sprints and doing items are active; several items may be doing.
Item completion requires a passing check and a completion entry. Sprint
closure requires its own recorded review and closeout, even if all items
are done. Start planned work only after a deliberate start decision.

## State

S8: open, baseline SB8, scope label filtering and sort retention.

I3: done, baseline SB7, scope save board title.

I4: doing, baseline SB8, scope filter by label.

I5: doing, baseline SB8, scope retain sort choice.

S9: planned, scope archive a board, requires S8 closeout. No start
decision for S9 is recorded.

## Completions

Sprint ledger: last entry S7, baseline SB6, review and closeout
recorded.

Item ledger: last entry I3, baseline SB7, completion recorded. No S8
closeout exists. The ledgers do not declare an ordering across levels.
```

#### NOTES.md

```markdown
# Notes

## Structure

Intended structure: a board store supplies items to a filter and sorter;
this is design, not runtime evidence.

## Decisions

D1, superseded by D2: use one board-wide sort order for simplicity. D2,
accepted: retain a user's chosen sort order to avoid repeated setup. No
successor to D2 is recorded.

## Evidence

S7/SB6: illustrative review accepted and closeout recorded.

S8/SB8: sprint review and closeout NOT RECORDED.

I3/SB7: title check PASS. I4/SB8 and I5/SB8: checks NOT RUN. These are
excerpted fictional records, not executable checks.
```

## Release / milestone-based

### Release map

```markdown
# Repository context

## Project

- Project: Package Ledger; a fictional document-package generator.
- Convention version: **0.1**.
- Description: [Project](README.md#project).
- Work Unit: release/milestone; changes retain separate completion
  rules.
- Work Model: [Rules](MILESTONES.md#rules).

## Published state

Handoff: [Handoff](README.md#handoff). Repository/ref: **Not
documented**; no remote exists. Describe the supplied snapshot; unseen
local work is Unknown. Distinguish local changes, commits, and
publication evidence; qualify cached comparisons.

## Source map

| Topic / purpose | Source | Authority | Read when |
| --- | --- | --- | --- |
| Current Work / release and changes | [State](MILESTONES.md#state); select preparing releases and validating changes | Native work state | State or unit selection |
| Last Completed Work / release or change | [Completions](MILESTONES.md#completions); select the requested level's last closure | Native completion | Latest completion matters |
| Planned Work | [State](MILESTONES.md#state); select planned releases or queued changes | Plans, not execution/publication permission | Planning |
| Architecture | [Structure](README.md#structure) | Intended structure | Structure questions or affected scope |
| Decisions | [Decisions](CHECKS.md#decisions); select D1 | Recorded rationale | Decision history |
| Validation / Evidence | [Evidence](CHECKS.md#evidence); select change baseline or assembled-release baseline from state/completions | Results for that scope/baseline | Review or evidence audit |

## Loading rules

- State: Rules and State; add the requested completion level only if
  needed. Review: selected scope and matching Evidence.
- Plan: State, Rules, and required release closeout. Architecture:
  Structure, expanding for affected decisions only.
- History: selected decision and any successor. Evidence: selected
  change or assembled release and its baseline. Apply the shared reading
  contract; stop at an answer or gap.
```

### Release task routes

| Task | Selected sources, result, and stop |
| --- | --- |
| Current state | Rules + State establish R3 preparing and C32 validating; Completions supplies R2 or C31 if asked. Stop before inferring release closure, authorization, or publication from change completion. |
| Review current work | State selects C32/RC32 and its index scope; Rules + Evidence establish checks NOT RUN. Stop at the missing checks; do not require unrelated release history. |
| Plan next work | State + Rules select R4, dependent on R3 closeout. Completions establishes no R3 closure; stop. Planned R4 and completed C31 grant no start/publication permission. |
| Architecture | Structure establishes formatter/assembler intention; stop. Implementation and deployment remain unestablished. |
| Historical decision | Decisions establishes D1's accepted rationale and no recorded supersession; stop. |
| Evidence audit | State selects R3/RA3; Evidence establishes unrun assembled checks and absent closeout/publication. Stop at these gaps; C31's checks cannot validate RA3. |

### Release sources

#### README.md

```markdown
# Package Ledger

## Project

A fictional generator that assembles document packages. Context:
[map](REPO_CONTEXT.md).

## Handoff

Illustrative shared snapshot RP2 includes R2's signed closure and R3's
preparation records. No real publication exists. A release plan, signed
closure, or completed change alone does not authorize publication.

## Structure

Intended structure: a formatter supplies documents to an assembler. This
states design, not implemented behavior or deployment.
```

#### MILESTONES.md

```markdown
# Milestones

## Rules

Releases/milestones are planned, preparing, or closed. Changes are
queued, validating, or complete. Preparing releases and validating
changes are active. A change closes with its checks and completion
entry. A release closes with assembled-package checks and a signed
closeout. Publication separately requires authorization and a
publication record. Starting planned work requires a deliberate start
decision.

## State

R3: preparing, assembled baseline RA3.

C31: complete, baseline RC31, scope format headings.

C32: validating, baseline RC32, scope assemble an index.

R4: planned, scope add package metadata, requires R3 closeout; no start
decision recorded. R3 publication authorization is NOT RECORDED.

## Completions

Last release closure: R2/RA2, signed closeout.

Last change completion: C31/RC31. No R3 closeout is recorded; no global
ordering across the two levels is declared.
```

#### CHECKS.md

```markdown
# Checks

## Decisions

D1, accepted: assemble one package to keep documents together at
handoff. No superseding decision is recorded.

## Evidence

R2/RA2: assembled checks PASS, signed closeout recorded.

C31/RC31: heading checks PASS, completion recorded.

C32/RC32: index checks NOT RUN.

R3/RA3: assembled checks NOT RUN; closeout and publication NOT RECORDED.
Change checks do not establish assembled-package validity. All results
are fictional.
```

## Experiment / research-based

### Research map

```markdown
# Repository context

## Project

- Project: Sample Study; a fictional sampling investigation.
- Convention version: **0.1**.
- Description: [Project](README.md#project).
- Work Unit: investigation of a hypothesis; no implementation lifecycle.
- Work Model: [Rules](NOTEBOOK.md#rules).

## Published state

Handoff: [Handoff](README.md#handoff); no formal release record.
Repository/ref: **Not documented**; no remote exists. Describe the
supplied snapshot; unseen local work is Unknown. Distinguish local
changes, commits, and publication evidence; qualify cached comparisons.

## Source map

| Topic / purpose | Source | Authority | Read when |
| --- | --- | --- | --- |
| Current Work | [Investigations](NOTEBOOK.md#investigations); select running investigations | Native investigation state | State or unit selection |
| Last Completed Work | [Closures](NOTEBOOK.md#closures); select the last signed entry, not a favorable result | Native closure | Latest completion matters |
| Planned Work | [Investigations](NOTEBOOK.md#investigations); select proposed investigations | Proposals, not permission | Planning |
| Architecture | [Structure](METHOD.md#structure) | Intended study/data structure | Method structure questions |
| Decisions | [Rationale](METHOD.md#rationale); select Q1/Q2 and successor | Recorded methodological decisions | Decision history |
| Validation / Evidence | [Evidence](NOTEBOOK.md#evidence); match investigation and its protocol/data/analysis baseline; [Protocol](METHOD.md#protocol) when method review needs it | Recorded observations and limitations | Review or evidence audit |

## Loading rules

- State: Rules and Investigations; add Closures if needed. Review:
  selected hypothesis, scope, Protocol, and matching Evidence.
- Plan: Investigations and Rules, then required predecessor closure.
  Architecture: Structure, expanding for affected protocol/rationale
  only.
- History: selected rationale and successor. Evidence: investigation and
  matching baseline record. Apply the shared reading contract; stop at
  an answer or gap.
```

### Research task routes

| Task | Selected sources, result, and stop |
| --- | --- |
| Current state | Rules + Investigations select X5 running; Closures identifies X4 as last completed despite its inconclusive result. Stop; outcome and signed closure answer different questions. |
| Review current work | Investigations selects X5's hypothesis, scope, and P2/D5/A1; Protocol + matching Evidence establish an inconclusive comparison and absent signoff. Stop at those limits; no implementation artifact is required. |
| Plan next work | Investigations + Rules select X6 and require X5 closure. Closures establishes no signed X5 entry; stop. A proposal does not permit starting. |
| Architecture | Structure describes grouped observations, sampling, and analysis; stop for that structural question. Actual measurement validity needs the selected protocol/evidence. |
| Historical decision | Rationale selects Q1, follows Q2, and establishes supersession and accepted group-wise comparison; stop at no recorded successor. |
| Evidence audit | Investigations selects X5/P2/D5/A1; Evidence records an inconclusive result and missing signoff. Stop there; X4's signed result cannot close X5. |

### Research sources

#### README.md

```markdown
# Sample Study

## Project

A fictional comparison of sampling strategies. Context:
[map](REPO_CONTEXT.md).

## Handoff

Illustrative shared notebook snapshot RP2 contains X5 running. No formal
release record is maintained; this handoff note locates the supplied
snapshot. No actual publication is asserted.
```

#### NOTEBOOK.md

```markdown
# Notebook

## Rules

Investigations are proposed, running, or closed; running investigations
are active. Results may be accepted, rejected, inconclusive, or
superseded. These describe a hypothesis outcome or replacement; none
alone closes work. Closure requires a result and signed entry. Starting
a proposal requires a deliberate start decision. No implementation
lifecycle applies.

## Investigations

X1 through X4 are closed.

X5: running, hypothesis stratified sampling reduces uneven coverage;
scope compare group coverage; baseline P2/D5/A1
(protocol/data/analysis).

X6: proposed, scope extend the sample interval; requires X5 signed
closure; no start decision recorded.

## Closures

Entry 1: X1/P1/D1/A1, accepted, signed.

Entry 2: X2/P1/D2/A1, rejected, signed.

Entry 3: X3/P1/D3/A1, superseded by X4, signed.

Entry 4 (last): X4/P2/D4/A1, inconclusive, signed. X5 has no signed
closure. Closure order is recorded, not inferred from identifiers.

## Evidence

X4/P2/D4/A1: inconclusive coverage result, signed closure.

X5/P2/D5/A1: coverage comparison INCONCLUSIVE; insufficient observations
to resolve the hypothesis; signoff NOT RECORDED. These are fictional
records, not measurements or proof of X5 closure.
```

#### METHOD.md

```markdown
# Method

## Protocol

P2 compares coverage within each group using the selected dataset and
analysis revision; record insufficient observations as inconclusive,
without treating that outcome as permission to close.

## Structure

Intended study structure: grouped observations feed sampling and
coverage analysis. This is methodological architecture; no software
implementation is asserted.

## Rationale

Q1, superseded by Q2: pool observations to simplify analysis. Q2,
accepted: compare groups separately to expose uneven coverage. No
successor to Q2 is recorded. This is an equivalent decision source, not
a formal ADR log.
```

## Maintenance / operations-based

### Operations map

```markdown
# Repository context

## Project

- Project: Queue Care; a fictional queued-job processor.
- Convention version: **0.1**.
- Description: [Project](README.md#project).
- Work Unit: incident or maintenance task, preserving their different
  states.
- Work Model: [Rules](OPS.md#rules).

## Published state

Handoff: [Handoff](README.md#handoff). Repository/ref: **Not
documented**; no remote exists. Describe the supplied snapshot; unseen
local work is Unknown. Distinguish local changes, commits, and
publication evidence; qualify cached comparisons. A handoff proves no
operational deployment.

## Source map

| Topic / purpose | Source | Authority | Read when |
| --- | --- | --- | --- |
| Current Work | [State](OPS.md#state); select mitigating/resolved incidents and executing maintenance | Native operational work state | State or unit selection |
| Last Completed Work | [Closures](OPS.md#closures); select last ledger entry under its unit's rules | Native closure | Latest completion matters |
| Planned Work | [Queue](OPS.md#queue); select scheduled tasks | Queue, not permission; no formal roadmap | Planning |
| Architecture | [Structure](RUNBOOK.md#structure) | Intended structure/procedure | Structure questions or affected work |
| Decisions | [Rationale](RUNBOOK.md#rationale); select D1 | Equivalent recorded rationale; no formal decision log | Decision history |
| Validation / Evidence | [Evidence](RUNBOOK.md#evidence); match selected incident/task and baseline from State/Closures | Observations/checks for that unit/baseline | Review or evidence audit |

## Loading rules

- State: Rules and State; add Closures if useful. Review: selected
  procedure/scope and matching Evidence.
- Plan: Queue and Rules, then required completion. Architecture:
  Structure, expanding for affected procedure/rationale only.
- History: selected rationale and successor if any. Evidence: selected
  unit/baseline only. Apply the shared reading contract; stop at an
  answer or gap.
```

### Operations task routes

| Task | Selected sources, result, and stop |
| --- | --- |
| Current state | Rules + State establish I1 mitigating and M1 executing; Closures identifies M0 when asked. Stop without normalizing incident and maintenance states or inferring live service health. |
| Review current work | State selects I1/IB2 and lease inspection; Rules + relevant Structure procedure + matching Evidence establish an inconclusive probe and missing resolution/review. Stop at that gap. |
| Plan next work | Queue + Rules select M2, dependent on M1 completion. State shows M1 executing; stop at unmet completion. No formal roadmap or start permission is inferred. |
| Architecture | Structure describes queue/workers/store and the relevant procedure; stop. Deployment and service health remain unestablished. |
| Historical decision | Rationale establishes D1's accepted retry-bound choice and no recorded supersession; stop. A formal decision log is unnecessary. |
| Evidence audit | State selects M1/MB2; Evidence records checks NOT RUN. Stop at that gap; M0/MB1 cannot validate M1. |

### Operations sources

#### README.md

```markdown
# Queue Care

## Project

A fictional processor for queued jobs. Context: [map](REPO_CONTEXT.md).

## Handoff

Use illustrative shared snapshot OP2 for documentary handoff. No actual
remote, release, or deployment is asserted; operational work state comes
from OPS.md.
```

#### OPS.md

```markdown
# Operations

## Rules

Incidents are mitigating, resolved, or closed; closure requires recorded
resolution and response review. Mitigating/resolved incidents remain
active until closed. Maintenance is scheduled, executing, or complete;
executing tasks are active, and completion requires passing checks and a
completion entry. Several units may be active. Scheduling alone does not
authorize execution; a deliberate start decision is required. No product
roadmap exists.

## State

I1: mitigating, baseline IB2, scope restore dequeuing; selected
procedure inspect queue leases in RUNBOOK.md#structure.

M1: executing, baseline MB2, scope bound retry count. An incident's
resolved label alone is not closed.

## Closures

Entry 1: I0/IB1, resolution and response review recorded, closed.

Entry 2 (last): M0/MB1, passing checks and completion recorded,
complete.

## Queue

M2: scheduled, scope add queue metrics, depends on M1 completion; no
start decision recorded. This queue is not a formal roadmap.
```

#### RUNBOOK.md

```markdown
# Runbook

## Structure

Intended structure: a queue feeds workers and a result store. Lease
inspection reads the selected queue's lease records; a retry bound
limits repeated processing. These procedures establish no deployment or
observed service health.

## Rationale

D1, accepted: bound retries so old jobs do not starve new work. No
supersession is recorded. No formal decision log is maintained.

## Evidence

I0/IB1: fictional resolution and accepted response review.

M0/MB1: checks PASS and completion recorded.

I1/IB2: mock queue probe INCONCLUSIVE; resolution and response review
NOT RECORDED.

M1/MB2: retry checks NOT RUN. No live operational observations exist.
```

## Cross-cutting variants

Each variant is a separate, self-contained modification of the named fixture; unchanged excerpts and map rules still apply. Deliberately unavailable references in E08 are the tested gap, not unresolved links in the base fixtures. The shared contract bounds runtime, publication, and unseen-work claims in every case.

### E01 No active work

**Sources and variant:** Sprint Rules + State: replace open/doing entries with `No sprint or item is active`; retain completions and plans.

**Established:** Current Work is **None**, explicitly recorded.

**Unknown or undocumented:** Unseen local activity is Unknown; plans do not establish activity.

**Reading stop:** State; completion history is unnecessary for this question.

**Classification:** Works as-is

### E02 Multiple active Work Units

**Sources and variant:** Sprint Rules/State retain I4/I5 doing; Operations Rules/State retain I1 mitigating and M1 executing.

**Established:** Several units are active under distinct native rules; select the requested one or report the set.

**Unknown or undocumented:** Neither set establishes completion or valid checks.

**Reading stop:** Selected state; review expands only for selected units.

**Classification:** Works as-is

### E03 No formal roadmap

**Sources and variant:** Operations Rules + Queue retain M2. Second variant removes Queue and declares its Planned Work source Not documented.

**Established:** M2 is a recorded plan without a roadmap; in the second variant, no maintained plan source exists.

**Unknown or undocumented:** Actual future work in the second variant is Unknown, not None.

**Reading stop:** Queue in the first variant; explicit source absence in the second.

**Classification:** Works as-is

### E04 No formal decision log

**Sources and variant:** Operations Rationale provides D1 without a log. Second variant removes Rationale and declares Decisions Not documented.

**Established:** Equivalent rationale answers D1's history; second variant establishes only a documentation gap.

**Unknown or undocumented:** Unrecorded decisions/supersession remain Unknown; absence of a log is not absence of decisions.

**Reading stop:** D1 and its recorded supersession limit, or declared source absence.

**Classification:** Works as-is

### E05 No formal release record

**Sources and variant:** Research Handoff exists without a release log. Second variant removes Handoff and declares publication/handoff source Not documented.

**Established:** A handoff source can locate the supplied snapshot without a release record.

**Unknown or undocumented:** Real publication is unestablished; second variant has no maintained publication source.

**Reading stop:** Handoff and visible provenance, or explicit source absence.

**Classification:** Works as-is

### E06 Stale summary

**Sources and variant:** Add `I1 is closed` to Operations README as a summary; OPS.md State remains authoritative and says mitigating at IB2.

**Established:** I1 is mitigating; the summary conflicts with native state and cannot overrule it.

**Unknown or undocumented:** Resolution/review remain unestablished by the summary.

**Reading stop:** Rules + authoritative State; report stale summary without loading unrelated history.

**Classification:** Works as-is

### E07 Conflicting sources

**Sources and variant:** Research Investigations contains two equally authoritative state records for the same snapshot: `X5 running` and `X5 closed`; no precedence is declared.

**Established:** A state conflict exists.

**Unknown or undocumented:** X5's work state is **Unknown**; neither the larger identifier nor edit recency resolves it.

**Reading stop:** Conflicting records and authority declaration; report unresolved disagreement.

**Classification:** Works as-is

### E08 Missing or broken reference

**Sources and variant:** Remove Research METHOD.md Protocol while the map retains METHOD.md#protocol; Investigations and Evidence remain available.

**Established:** X5 is running and its baseline is P2/D5/A1; the selected protocol reference is unavailable.

**Unknown or undocumented:** Method compliance cannot be established; earlier protocol/results cannot substitute.

**Reading stop:** Identify the missing Protocol section; answer only supported state/evidence questions.

**Classification:** Works as-is

### E09 Evidence from another baseline

**Sources and variant:** Research Investigations keeps X5/P2/D5/A1. Replace X5's evidence with `X5/P1/D5/A1: PASS`; retain X4/P2/D4/A1 signed evidence.

**Established:** Available evidence concerns another protocol revision or another investigation.

**Unknown or undocumented:** X5/P2/D5/A1 validation is **Unknown**; matching evidence is unavailable.

**Reading stop:** Baseline selector + Evidence; stop at mismatch without importing earlier success.

**Classification:** Works as-is

### E10 Local work newer than published snapshot

**Sources and variant:** Research Handoff + supplied published RP2 say X5 running at P2/D5/A1. A stipulated descendant local commit records X5 accepted/signed at P2/D5/A2; an uncommitted edit proposes X7. These are fictional provenance facts for this exercise only.

**Established:** Published-only reader sees running X5. Local reader separates the published record, committed closure, and uncommitted proposal.

**Unknown or undocumented:** Published-only reader cannot infer local closure/X7; publication of local changes is Unknown. Cached refs alone do not confirm current remote state.

**Reading stop:** Each reader's available snapshot/provenance; no inference about inaccessible local/remote content.

**Classification:** Works as-is

### E11 Very little formal documentation

**Sources and variant:** Replace Operations sources with the sparse README below; map Project/Architecture/Work Model to its sections and missing data sources to Not documented. Route tasks to those sections or declared absence; retain the shared loading/visibility rules.

**Established:** Purpose, intended structure, and ad hoc working rules are available with one source.

**Unknown or undocumented:** Current/last-completed/planned work, decisions, evidence, and publication sources are Not documented; corresponding real facts remain Unknown.

**Reading stop:** Relevant README section or declared absence; no invented tracker or blanket repository search.

**Classification:** Works as-is

### E11 sparse README excerpt

```markdown
# Queue Care

## Project

A fictional queued-job processor.

## Structure

Intended structure: a queue feeds workers.

## Working

Ad hoc fixes; no formal lifecycle. No maintained sources for work state,
completions, plans, decisions, evidence, or publication/handoff exist in
this fixture.
```

## Interpretation findings

All four model mappings and eleven variants work under v0.1. The shared reading contract explains three potentially narrow readings: a unit's review scope may be a protocol/procedure rather than implementation; plans may live in notes rather than a roadmap; container and item completions need level-specific selectors. These findings are **Documentation clarification only**. No required new field, universal status, ordering, profile, or semantic change was found. No finding is classified **Possible future extension** or **Actual Core limitation**.

The [Phase 2 record](../docs/research.md#phase-2-generalization-validation) records the evaluation and existing-example regression controls. These exercises demonstrate document mapping and bounded reading, not application execution, actual publication, or automatic assistant compatibility.
