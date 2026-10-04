# QVSTN Repository Instructions

This repository follows the QVSTN Build Protocol.

Repository documentation is the source of truth.

Before planning, modifying or implementing code, read:

1. `.qvstn/BUILD_PROTOCOL.md`
2. `.qvstn/ENGINEERING.md`
3. `.qvstn/GIT_WORKFLOW.md`
4. `.qvstn/MILESTONE_PROCESS.md`
5. `.qvstn/COMPLETION_CHECKLIST.md`
6. `docs/PROJECT.md`
7. `docs/ARCHITECTURE.md`
8. `docs/ROADMAP.md`
9. `docs/STATUS.md`
10. the specification for the current milestone
11. relevant files under `docs/decisions/`

## Mandatory workflow

Never implement directly on `main`.

Before implementation:

- inspect the repository
- inspect Git status
- determine the current branch
- determine the current milestone
- verify milestone scope
- create or use an appropriately scoped non-main branch

Do not implement work belonging to future milestones.

Completed milestones represent established project contracts. Do not silently change those contracts.

If a completed architectural decision must change:

- explain why
- identify affected behaviour
- document the decision
- update relevant architecture documentation
- add migration work when required

## Validation

Before declaring implementation complete, run the validation appropriate to the repository.

This normally includes:

- lint
- type checking
- tests
- production build

Do not bypass failing validation.

Do not weaken tests merely to make an implementation pass.

## Completion

When work is complete:

- review the diff
- remove temporary/debug code
- run validation
- update documentation
- update milestone state
- update `docs/STATUS.md`
- summarize implemented work
- identify deferred work
- stop when current milestone scope is complete

Do not automatically begin the next milestone.