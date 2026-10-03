# Repository context

## Project

- Project: AI Repository Context; a portable Markdown context-discovery convention.
- Convention version: **0.1**.
- Description: [README](README.md).
- Work Unit: documentation change.
- Work Model: [maintaining this package](README.md#maintaining-this-package); no formal lifecycle or recorded work queue.

## Published state

Publication/handoff source: [package status](README.md#status).
Canonical published repository: [angel-wm/ai-repository-context](https://github.com/angel-wm/ai-repository-context).
Published/default handoff branch: `main`.

Describe only the snapshot available during the task. Remote readers leave unseen local work **Unknown**. Local readers distinguish working changes, commits, and publication evidence; a clean or committed checkout is not proof of publication. Qualify cached remote comparisons. Do not copy or maintain a "latest commit" value in this map; establish the visible snapshot during each task. The convention version is not a release claim.

## Source map

| Topic / purpose | Source | Authority | Read when |
| --- | --- | --- | --- |
| State / Current Work | [Status](README.md#status); active work **Not documented** in a maintained tracker | Authoritative for package status; not session or Git state | Package state or missing work records |
| Last Completed Work | **Not documented**; no native completion log | No declared completion source | Completion questions; a commit alone is insufficient |
| Planned Work | **Not documented**; no maintained roadmap | No declared planning source | Planning; obtain scope from the task |
| Architecture | [Core](SPEC.md#core); [map structure](SPEC.md#map-structure) | Authoritative for intended convention design | Meanings or map-interface questions/changes |
| Decisions | [SPEC](SPEC.md); [rationale](docs/research.md#recommendation) | SPEC is normative; research supports rationale, not formal history | Choices or proposed changes |
| Validation / Evidence | [Checklist](docs/research.md#manual-acceptance-checklist); [initial record](docs/research.md#validation-record); [Phase 2 record](docs/research.md#phase-2-validation-record); [cases](examples/generalization-validation.md) | Checklist defines scenarios; records cover stated snapshots; cases are fictional | Documentation review or evidence audit |

## Loading rules

- Read applicable guidance, this map, and task-required sources. Preserve task authorization and any native reading requirements.
- State: read README status; report undocumented work rather than inventing a queue.
- Review: use the task's selected change and scope; read affected specification sections and corresponding template/example excerpts, then relevant checklist/evidence.
- Plan: use declared task scope and README maintenance policy; plans and dependencies are undocumented unless supplied.
- Architecture: read only the relevant Core or map-structure section first.
- History: read the research recommendation and relevant comparison; formal historical decisions are not documented.
- Evidence: select the record for the documentation change and baseline; read its scope, then relevant checklist rows or generalization cases. Earlier records do not validate later revisions or publication.
- Resolve links relative to this map. Read research, templates, and examples only when the task needs them; do not follow every link.
- Prefer specification meanings over illustrative material. Report unresolved conflicts or inaccessible sources; do not silently substitute supporting material.
- Stop when sources support the answer or identify a specific gap. Keep routine state in existing sources and change this map only for changed references or reading rules.
