# Fictional phase-based example: Workshop Planner

Workshop Planner is an invented project for organizing workshop sessions. All sources and results below are illustrative; no external repository, live ref, real reports, or runtime exists. Every sample-map reference has an excerpt here. Relative links inside fenced blocks describe fictional files, not external reading dependencies.

## Fictional layout

```text
README.md
REPO_CONTEXT.md
CURRENT_STATE.md
ROADMAP.md
NOTES.md
```

There are four source documents besides the map. Read the [sample map](#sample-map), then only the relevant [source excerpts](#included-source-excerpts).

## Sample map

```markdown
# Repository context

## Project

- Project: Workshop Planner.
- Convention version: **0.1**.
- Description: [README](README.md#project).
- Work Unit: phase.
- Work Model: [roadmap rules](ROADMAP.md#rules).

## Published state

Handoff source: [README handoff](README.md#handoff) and [state](CURRENT_STATE.md#state).
Canonical repository/ref: **Not documented**; no actual remote exists in this fixture.
These excerpts depict a supplied illustrative published snapshot. Remote readers leave unseen local work Unknown. In a real project, report the retrieved snapshot and distinguish local changes, commits, and publication evidence; clean or committed is not proof of publication.

## Source map

| Topic / purpose | Source | Authority | Read when |
| --- | --- | --- | --- |
| State / Current Work | [State](CURRENT_STATE.md#state); select the phase explicitly current under roadmap rules | Authoritative for recorded phase state | Understanding state or selecting current work |
| Last Completed Work | [State](CURRENT_STATE.md#state), then the named closeout in NOTES.md | State selects the last closed phase; closeout records its exit evidence | Latest completion or predecessor handoff matters |
| Planned Work | [Plan](ROADMAP.md#plan); select the next planned phase | Authoritative for phase order and plans, not execution permission | Planning next work |
| Architecture | [Structure](NOTES.md#structure) | Authoritative for intended project structure | Architecture questions or affected work |
| Decisions | [Decisions](NOTES.md#decisions); select the relevant decision ID | Authoritative for recorded decisions | Rationale or decision history matters |
| Validation / Evidence | [Closeout](NOTES.md#design-closeout) or [current checks](NOTES.md#build-checks), selected by phase and baseline from state | Records phase checks and closure evidence at the named baseline | Reviewing a phase or auditing evidence |

## Loading rules

- Read applicable guidance and preserve roadmap rules and handoff requirements.
- State: read State; load the last closeout only when relevant.
- Review: select the current phase; read its roadmap scope and matching checks, then affected structure or decisions.
- Plan: read state, roadmap rules, and the next phase's scope. Include required predecessor closeout and dependencies; a plan does not authorize starting.
- Architecture: read Structure first; add relevant decisions or phase scopes only as needed.
- History: select a decision ID and any recorded supersession chain.
- Evidence: select phase and baseline; closed-phase results do not establish current-phase validity.
- Resolve links relative to this map. Select the named closeout section, not every historical section.
- Apply topic authority; report unresolved conflicts, unavailable evidence, and unknowns. Stop when the answer is supported or a specific gap is established.
```

## Included source excerpts

### README.md

```markdown
# Workshop Planner

## Project

Organize session topics and their available time slots.
For project context and task-specific reading guidance, see [REPO_CONTEXT.md](REPO_CONTEXT.md).

## Handoff

Use the shared published snapshot for phase handoff. All excerpts depict illustrative snapshot W2, including the earlier Design closeout from W1. A phase closes only after its exit checks, closeout, and publication condition in the roadmap are satisfied. No actual remote or publication exists outside this fictional example.
```

### CURRENT_STATE.md

```markdown
# Current state

## State

Current phase: Build; state current; baseline W2.
Last closed phase: Design, at W1; closeout: NOTES.md#design-closeout.
Next planned phase: Validate; scope and dependencies: ROADMAP.md#plan.
A wording correction to the shared documentation in W2 did not close Build or alter Design's completion baseline W1.
```

### ROADMAP.md

```markdown
# Roadmap

## Rules

Use phases sequentially, with states planned, current, and closed. Start a phase only after deliberate authorization and predecessor closure. Closure requires recorded passing exit checks, a closeout, and inclusion in the shared published snapshot. Phase handoff requires the predecessor closeout; additional structure/decisions are read when they affect the next phase.

## Plan

| Phase | Scope | Dependency |
| --- | --- | --- |
| Design | Define session and time-slot records. | None |
| Build | Implement the records and scheduling view. | Design closed |
| Validate | Check scheduling conflicts and usability. | Build closed |
```

### NOTES.md

```markdown
# Project notes

## Structure

Intended structure: a session catalog supplies topics; a schedule associates sessions with time slots. Runtime behavior is not demonstrated here.

## Decisions

D1, accepted at Design: use one shared schedule to avoid conflicting parallel copies. No superseding decision is recorded.

## Design closeout

Design, baseline W1: illustrative record-definition checks PASS; closeout accepted and included in the shared published fixture. Design is closed under roadmap rules. This evidence establishes no Build or Validate result.

## Build checks

Build, baseline W2: scheduling checks NOT RUN; no Build closeout or closure publication recorded. No executable implementation or underlying reports are included in these excerpts.
```

## Reading walkthrough

For "plan next work," read State and roadmap rules, then Validate's scope and dependency. Build is current and lacks exit checks and closeout, so Validate cannot start under the native rules. Follow the required predecessor selection to Build checks; the missing Build closeout is a specific gap. Design's closed state and the documentation correction do not satisfy Build's exit gate. Unrelated decision history and the full structure need not be loaded unless they affect planning. Unseen local progress remains unknown.
