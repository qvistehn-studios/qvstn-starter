# QVSTN Milestone Process

Milestones divide project development into explicit, reviewable contracts.

## Every milestone must define

- goal
- scope
- non-goals
- requirements
- acceptance criteria
- validation expectations
- documentation impact

## Before milestone implementation

Read:

- `docs/PROJECT.md`
- `docs/ARCHITECTURE.md`
- `docs/ROADMAP.md`
- `docs/STATUS.md`
- relevant architecture decisions
- the milestone specification

Then inspect the implementation.

Do not assume documentation perfectly reflects reality without verification.

## Scope discipline

Only implement work required by the current milestone.

A milestone must not absorb future features merely because they appear convenient.

If future work becomes necessary to complete the milestone, update the milestone explicitly before implementing it.

## Architecture changes

If implementation requires a meaningful architectural decision that will influence future work, create an ADR.

Examples include:

- database choice
- authentication model
- canonical domain model
- external-service strategy
- major framework choice
- persistence strategy
- queue architecture
- security model

Do not create ADRs for trivial implementation details.

## Completion

A milestone may be marked complete only when:

- requirements are implemented
- acceptance criteria are satisfied
- required tests exist
- validation passes
- documentation reflects reality
- `docs/STATUS.md` is updated
- `docs/ROADMAP.md` reflects milestone state

## After completion

Stop.

Do not begin implementation of the next milestone unless explicitly requested.