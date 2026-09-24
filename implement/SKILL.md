---
name: implement
description: Implement a defined requirement, spec, issue, or plan using a living execution plan and consolidated testing after implementation. Use when the scope is ready for code changes.
---

# Implement

Carry the requested work through implementation and verification. Keep the process proportional to the task; follow explicit user constraints and applicable repository instructions.

## Execution plan

Read the relevant code and repository guidance. Before implementation, turn acceptance criteria into concrete examples of success, important boundaries, and failure behavior; identify the public interfaces to observe. Record these in the plan and derive final validation commands from project scripts, validation docs, and CI.

Use the repository's execution-plan mechanism, including its format, location, and lifecycle. An equivalent task record is sufficient. Reuse one plan for the same objective across implementation, fixes, and validation.

When no convention exists, create a short plan at `docs/exec_plans/active/YYYYMMDD-short-slug.md` containing:

- **Goal and acceptance:** intended behavior, scope boundaries, and completion criteria.
- **Approach:** relevant paths, constraints, ordered steps, and key decisions with reasons; recovery points when needed.
- **Progress:** completed work, current state, blockers, and next step.
- **Validation:** planned commands and acceptance checks, then actual results and gaps.

Keep enough context to resume without the chat history; link existing specs. Update at milestones, decisions, blockers, or handoff, not after every edit. Continue within the authorized scope without adding a plan-approval step.

## Implementation

Work through the plan to complete the requested behavior and affected documentation. Implement what the agreed behavior needs, reuse existing patterns, and avoid speculative features or abstractions.

Use the planned examples to guide implementation and test design. Once the implementation is coherent, batch necessary test additions or updates using the existing framework; reuse adequate coverage.

- Test one observable behavior per case through a public interface. Assert outcomes and contractual effects; avoid private methods, internal call sequences, or incidental structure. Behavior-preserving refactors should leave tests valid.
- Derive expected results independently from requirements or worked examples. Do not copy the implementation's algorithm into assertions or rewrite expectations merely to make a failure pass.
- Exercise real internal code paths. Use mocks or fakes at external or nondeterministic boundaries, such as remote services, clocks, or randomness, to keep tests reliable.

Do not alternate each small edit with creating and running tests. Defer routine tests, typechecking, and linting to final validation unless the user or repository explicitly requires an earlier check.

## Final validation

After implementation and test changes are complete, review the diff against acceptance criteria, then run one consolidated validation pass: the repository's full test suite and required lint, typecheck, build, and acceptance checks, including required integration or end-to-end coverage.

For bug fixes, where feasible, also run the regression test against the old behavior in an isolated copy during final validation. Confirm it fails for the expected reason and passes with the fix; record when this evidence is unavailable.

If validation fails, fix task-related failures, using focused reruns while repairing, then rerun the full validation pass against the final code. Stop once that state passes. Leave unrelated failures outside the task's scope.

If required validation is blocked or fails for an unrelated reason, record the command, evidence, and remaining gap. Report it without claiming completion or silently substituting focused tests for the full suite.

## Completion

Record results and limitations in the plan. Follow repository completion rules; with the fallback layout, move the plan to `docs/exec_plans/completed/` only when agreed work and required validation are complete. Update affected links and stable documentation.

Report what changed, the plan's location, and what validation passed, failed, or could not run. Commit, push, or publish only when requested or already authorized.
