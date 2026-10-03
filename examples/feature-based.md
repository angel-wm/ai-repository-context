# Fictional feature-based example: Pocket Notes

Pocket Notes is an invented software project. All sources and results below are illustrative; no repository, executable application, real report, or remote exists. The excerpts are sufficient for every sample-map reference. Relative links inside fenced blocks describe files in the fictional repository, not files to fetch from this reference package.

## Fictional layout

```text
README.md
REPO_CONTEXT.md
FEATURES.md
docs/DESIGN.md
docs/EVIDENCE.md
```

There are four source documents besides the map. Read the [sample map](#sample-map), then only the relevant [source excerpts](#included-source-excerpts).

## Sample map

```markdown
# Repository context

## Project

- Project: Pocket Notes.
- Convention version: **0.1**.
- Description: [README](README.md#project).
- Work Unit: feature.
- Work Model: [feature rules](FEATURES.md#rules).

## Published state

Handoff source: [README handoff](README.md#handoff); native state:
[feature state](FEATURES.md#state).
Canonical repository/ref: **Not documented**; this fixture has no
remote.
Describe the supplied illustrative snapshot; remote readers cannot infer
unseen local work. Local completion does not establish publication. A
real reader must identify the visible snapshot and distinguish changes,
commits, and publication evidence.

## Source map

| Topic / purpose | Source | Authority | Read when |
| --- | --- | --- | --- |
| State / Current Work | [Feature state](FEATURES.md#state); select the feature explicitly marked active | Authoritative for feature lifecycle state | Understanding state or selecting current work |
| Last Completed Work | [Completions](FEATURES.md#completions); select the latest recorded completion | Authoritative for native completion | Latest completion matters |
| Planned Work | [Feature state](FEATURES.md#state); select queued features in recorded order | Authoritative for the queue, not execution permission | Planning next work |
| Architecture | [Structure](docs/DESIGN.md#structure) | Authoritative for intended structure, not runtime proof | Architecture questions or affected changes |
| Decisions | [Decisions](docs/DESIGN.md#decisions); select the relevant decision ID | Authoritative for recorded decisions | Explaining a choice or its history |
| Validation / Evidence | [Evidence](docs/EVIDENCE.md#evidence); select the feature ID and matching baseline | Records checks and reviews for that feature/baseline only | Reviewing a feature or auditing evidence |

## Loading rules

- Read applicable guidance and preserve the feature rules.
- State: read feature state; add the latest completion only if it
  explains the answer.
- Review: select the active feature; read its contract, relevant
  evidence, and affected design sections.
- Plan: read state and rules; then the queued feature's contract and
  dependencies. Queued is not authorized.
- Architecture: read Structure; follow only relevant decision or
  contract references.
- History: select a decision ID; follow its supersession references if
  present.
- Evidence: select feature and baseline; other checks or reviews do not
  establish its validity.
- Resolve links relative to this map. Patterns and headings are
  selectors, not bulk-reading instructions.
- Apply topic authority; report unresolved conflicts, missing
  references, and unknown information. Stop when the answer is supported
  or a specific gap is established.
```

## Included source excerpts

### README.md

```markdown
# Pocket Notes

## Project

A simple application for creating and finding personal notes.
For project context and task-specific reading guidance, see
[REPO_CONTEXT.md](REPO_CONTEXT.md).

## Handoff

Use the shared snapshot supplied for the handoff. Feature completion
requires the feature rules, independently of publication. These excerpts
represent illustrative snapshot N2; no actual publication is asserted
and no remote is declared.
```

### FEATURES.md

```markdown
# Features

## Rules

Use states queued, active, and done. Work on one active feature at a
time. Deliberately select and authorize queued work before starting.
Mark a feature done only after its contract is satisfied and passing
checks plus an independent review are recorded for its completion
baseline.

## State

| ID | Feature | State | Contract |
| --- | --- | --- | --- |
| F1 | Create notes | done | Save a note and retrieve its text. |
| F2 | Search notes | active | Return notes containing the query text; depends on F1. |
| F3 | Export notes | queued | Export all note text; depends on F1. |

## Completions

Completion 1: F1 completed at baseline N1; matching checks and review
are in docs/EVIDENCE.md. No other completion is recorded.
```

### docs/DESIGN.md

```markdown
# Design

## Structure

Intended structure: a note editor calls a note store. Search reads that
store and returns matching text. This describes the design, not measured
runtime behavior.

## Decisions

D1, accepted: store notes locally to support use without a connection.
No superseding decision is recorded. The consequence is that
multi-device synchronization is not part of the current design.
```

### docs/EVIDENCE.md

```markdown
# Evidence

## Evidence

F1, baseline N1: illustrative save/retrieve check PASS; independent
review ACCEPTED. Both concern only F1's contract at N1.
F2, baseline N2: search checks NOT RUN; review NOT RECORDED. F1's
results do not validate F2. These fictional excerpts contain no
executable code or underlying reports.
```

## Reading walkthrough

For "review current work":

1. Select F2 from feature state.
2. Read its search contract and N2 evidence: checks have not run and no review is recorded.
3. Read Structure only if evaluating the proposed search design.
4. Stop at the specific evidence gap. F1's completion checks cannot validate F2; F3's contract and unrelated history need not be loaded.

The fixture cannot substantiate implementation behavior or unseen local progress.
