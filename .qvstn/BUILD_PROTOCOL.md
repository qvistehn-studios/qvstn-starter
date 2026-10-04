# QVSTN Build Protocol

Version: 0.1

## Core principles

Repository documentation is the source of truth.

Main must represent a known-good state.

Never implement directly on `main`.

Every implementation change must happen on an appropriately scoped branch.

Work only within the current milestone unless explicitly instructed to update project planning.

Completed milestones establish contracts that later work must respect.

Do not silently redesign completed work.

Prefer the smallest correct implementation.

Prefer explicit, understandable solutions over clever solutions.

Project reality and documentation must remain synchronized.

## Before implementation

Before modifying code:

1. Read repository instructions.
2. Read project documentation.
3. Read the current milestone specification.
4. Read relevant architecture decisions.
5. Inspect the existing implementation.
6. Inspect Git status.
7. Verify the current branch.
8. Ensure implementation will not happen directly on `main`.
9. Identify the exact milestone scope.
10. Identify assumptions or unresolved constraints.

If repository documentation contradicts implementation, do not guess.

Determine whether:

- documentation is stale
- implementation is incorrect
- an undocumented architectural change occurred

Resolve the inconsistency explicitly.

## During implementation

Implement only what is required by the current milestone.

Avoid unrelated refactoring.

Avoid speculative features.

Avoid abstractions for hypothetical future requirements.

Preserve existing behaviour unless changing it is explicitly part of the current milestone.

Keep the repository runnable throughout development when practical.

Add or update tests for meaningful behaviour.

Document architectural decisions that materially affect future development.

## Completed milestones

A completed milestone represents an established project contract.

Later work must not silently alter its guarantees.

If changing a completed contract becomes necessary:

1. identify the affected milestone
2. explain why the change is necessary
3. document the architectural decision
4. identify migration or compatibility concerns
5. update affected documentation
6. validate the new behaviour

## Source of truth hierarchy

When determining current project state, prefer:

1. current repository implementation
2. current repository documentation
3. architecture decision records
4. milestone specifications
5. external conversation context

Conversation history and model memory must never override repository state.

## End of work

Work is not complete merely because code has been written.

Completion requires:

- implementation review
- appropriate validation
- documentation updates
- current milestone status update
- repository status update
- explicit identification of deferred work

Stop when the requested milestone or scoped task is complete.

Do not automatically continue into future milestones.