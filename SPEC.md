# AI Repository Context specification

Convention version: **0.1**.

## Purpose

Provide a small repository context-discovery interface: shared meanings, references to existing sources, and rules for reading only what a task needs. Preserve the project's filenames, work model, lifecycle, and completion rules. This convention does not replace documentation, manage work, enforce approvals, create decisions, prove runtime behavior, or synchronize or publish repositories.

In this specification, **MUST** identifies a requirement, **SHOULD** a recommendation, and **MAY** an option. The specification is the sole normative definition; templates and examples illustrate it.

## Discovery

A repository adopting this convention SHOULD expose its root-level `REPO_CONTEXT.md` from a conventional entry point, preferably its root `README.md`. A single link or short sentence is sufficient. Tool-specific instruction files such as `AGENTS.md`, `CLAUDE.md`, or similar files MAY also link to it.

The README MUST NOT duplicate the context map.

```text
README.md -> discovery
REPO_CONTEXT.md -> context map
existing project documents -> authoritative information
```

This convention claims no automatic discovery or support by any assistant, coding agent, hosting platform, or other tool. Readers must encounter a link or be directed to the file. No particular tool or integration is required.

## Core

A **Work Unit** is the project's meaningful unit of work: a feature, phase, sprint, release, experiment, maintenance change, or another native concept. It is vocabulary, with no required stored object, identifier scheme, lifecycle, or formal profile.

Every map MUST account for these topics. Topics MAY share a source or table row.

| Topic | Meaning |
| --- | --- |
| Project | Repository purpose and its description source. |
| Published State | Publication or handoff source, interpreted within the visible snapshot. Publication differs from local completion and deployment. |
| Work Model | Native Work Unit terminology and working or lifecycle rules. |
| Current Work | Explicitly active work under those rules: zero, one, or multiple units. A completed unit labeled "current" is not active. |
| Last Completed Work | Most recent completion identified by native records and completion rules, not the largest identifier or most recently edited file. |
| Planned Work | Recorded future work; listing it does not authorize execution. |
| Architecture | Sources describing structure or intended architecture; distinguish intention from implementation where relevant. |
| Decisions | Recorded decisions and rationale, including status and supersession where available. |
| Validation / Evidence | Checks, reviews, observations, and limitations for identifiable work or baselines. |
| Context Loading Rules | Source selection by task and the condition for stopping. |

For missing information, distinguish **None** (the project records that no item exists), **Not documented** (no maintained source exists), and **Unknown** (available information cannot establish the answer). Missing documentation is not proof that no work or decision exists.

## Map structure

The root-level Markdown map MUST contain four sections:

1. **Project:** identity, convention version, description reference, native Work Unit term, and work-model reference or explicit absence.
2. **Published state:** publication/handoff source or explicit absence, any project-declared repository/ref, and a visibility rule.
3. **Source map:** references covering the remaining Core topics.
4. **Loading rules:** task routes, reference selection, and uncertainty handling.

The source map MUST use these columns:

| Column | Semantics |
| --- | --- |
| Topic / purpose | The question the source answers. Add a qualifier only when the topic is insufficient. |
| Source | Relative Markdown link, section reference, or explained selection rule. |
| Authority | Authoritative for the stated topic, a summary, or supporting material. |
| Read when | The task or condition requiring the source. |

Authority concerns a topic and snapshot, not universal truth. A decision record establishes a recorded decision; a report records a result for its stated baseline. Neither establishes all project behavior. A summary does not overrule its authoritative source.

Resolve links relative to the map. Resolve Work Unit selectors from native state sources before opening their documents. Explain each selector. A directory or filename pattern is a location, never an instruction to read every file. Prefer relevant sections or records in large sources.

Apply declared topic authority to conflicts; report unresolved disagreement. For broken or inaccessible references, identify the missing context and proceed only where available information supports the task. Do not silently substitute a summary for missing authoritative information.

Update the map when locations, authority, or reading rules change. Routine status updates belong in existing sources. No frontmatter, rigid schema, per-source version fields, timestamps, or authority scores are required.

## Progressive loading

Start with applicable repository guidance, the map, and task-required sources. Preserve the project's reading requirements and approval rules.

| Task | Initial reading | Expand when necessary |
| --- | --- | --- |
| Understand current state | State source and relevant work records | Latest completion summary |
| Review current work | Selected unit's contract, implementation scope, and evidence | Affected architecture, decisions, and code |
| Plan next work | State, planned work, and work-model rules | Required predecessor closeout and dependencies |
| Answer an architecture question | Relevant architecture section | Supporting code, specifications, or decisions |
| Investigate a historical decision | Decision index or targeted search | Selected decision and supersession chain |
| Audit evidence | Evidence for the selected unit and baseline | Referenced reports, reviews, and observations |

Stop when relevant sources support an answer or establish a specific unresolved gap. Do not recursively load links, all history, completed units, decisions, reviews, or architecture unless the project or task requires them.

## Publication visibility

A remote reader MUST describe only the published snapshot actually retrieved and treat unseen local work as **Unknown**. A supplied archive or pasted file with unclear provenance is not confirmed published state. A snapshot is not necessarily the latest remote state, default branch, release, or deployment.

A local reader MUST distinguish working changes, commits, and publication evidence. A clean checkout or local commit alone does not prove publication. Qualify comparisons using cached remote references. Readers identify the snapshot/ref they can establish during their task; the map MUST NOT maintain a copied "latest published commit" or release value. A handoff reference locates information but does not prove that a checkout matches it.

## Versioning and boundaries

Declare **0.1** in maps and this specification. Editorial corrections may use `0.1.x`; incompatible semantic or structural changes require `0.2` and a short explanation here. Updating project references does not change the convention version.

Version 0.1 requires only Markdown and the filesystem. No formal profiles, scripts, schemas, agents, RAG, CI, generators, validators, services, automatic decisions, or automatic publication are part of it.
