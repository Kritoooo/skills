---
name: folio
description: Draft or refine issue trees from conversations, ideas, requirements, and plans, and publish them when requested. Use when organizing work into trackable implementation tasks with explicit scope, acceptance, and dependencies.
---

# Folio

Shape ideas into actionable issue trees. This skill organizes work; it does not execute the resulting tasks.

## Structure

Use up to three levels, with one issue per node:

| Level | Meaning | Acceptance |
| --- | --- | --- |
| **Epic** | A bounded overall objective. | The intended overall state is achieved. |
| **Canto** | An independently valuable outcome within an Epic. | The capability or result works as a whole. |
| **Verse** | A self-contained development or implementation task. | The implemented change passes observable checks. |

- Every leaf is a Verse. Verses may stand alone; Epics may contain Canto or Verse nodes; Canto nodes contain Verses. Skip unnecessary levels and duplicate containers.
- Separate objectives with independent success criteria into different trees; keep contributions to one objective together.
- Each node must be understandable without the original conversation, with its own scope and observable acceptance. Parent acceptance verifies the combined outcome, beyond counting closed children.
- Give siblings distinct responsibilities and independently verifiable results. Prefer complete, narrow behavior over implementation layers.

## Shape the work

Use the supplied sources, relevant existing issues, and project state to identify remaining work. Distinguish confirmed requirements from alternatives, rejected ideas, and your suggestions; suggestions do not automatically become scope.

Reuse issues with matching outcomes, preserving identities and history through revisions or regrouping. Avoid duplicating completed work. Keep essential context in each issue; link supporting detail.

Check coverage, overlapping responsibilities, acceptance, and dependency cycles. Present the tree and new or revised bodies, distinguishing additions, changes, and unresolved scope. Use descriptive linked titles and stable identifiers.

### Exploration belongs to implementation

Put research, prototyping, and design decisions in the relevant Verse's **Preparation** section. For example, investigating expiry semantics belongs inside implementing expiring share links. Exploration is never a standalone issue or sufficient acceptance for a Verse.

Assign shared exploration to the implementation task that first needs it; others reference its findings. Do not merge unrelated implementation goals to house research.

Unbounded work stays in the nearest parent's **Pending** notes, or draft notes if no tree exists. Ask about missing scope, acceptance, or decisions requiring user input. Do not invent tasks or publish empty branches.

### Relationships

- **Parent:** at most one immediate parent.
- **Blocked by:** a genuine prerequisite; state the required result. Hierarchy and preferred order alone are not blockers.
- **Related:** useful context without a blocking dependency.

Allow cross-tree links; keep shared work in one canonical issue. Independent acceptance does not require simultaneous execution.

## Destination and publication

Resolve the destination from user instruction, project conventions, then repository and tool context, in that order. Reference URLs are sources unless designated as targets. Verify the project and issue availability; do not guess between forks, upstream, or multiple projects.

If the destination is unclear or inaccessible, retain Markdown drafts and explain what publication needs. Ask for a destination only when needed to publish; do not silently switch an explicitly chosen target.

Publish or update tracker issues only when requested, honoring existing authorization. Create missing nodes, then link them by real identifiers. Prefer native relationships; otherwise use named links in bodies. Report verified links and partial completion. Pause on uncertain write results and reconcile before retrying.

For requested local files, use one file per issue with stable identifiers and relative links, following project conventions.

## Node template

Omit optional sections and unused relationships. Add **Pending** to parents as needed. Follow the user's or project's language; retain the level names.

```markdown
# <Outcome-oriented title>

**Level:** Epic | Canto | Verse

## Context
Necessary background, sources, and established constraints.

## Scope
The result to deliver and its boundaries.

## Preparation
Optional: questions or investigations needed to implement this Verse.

## Acceptance
- [ ] Observable result and how to verify it.

## Relationships
- Parent: <title and reference>
- Blocked by: <title and reference> — <required result>
- Related: <title and reference>
```
