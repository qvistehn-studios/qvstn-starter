# QVSTN Completion Checklist

Before declaring scoped implementation complete, verify the following.

## Scope

- [ ] Work matches the requested milestone or task.
- [ ] No unrelated feature work was added.
- [ ] Deferred work is explicitly identified.

## Git

- [ ] Work was not implemented directly on `main`.
- [ ] Branch scope is coherent.
- [ ] No unexpected files are included.
- [ ] No credentials or secrets are included.
- [ ] New environment variables are documented in `.env.example`.

## Implementation

- [ ] Diff has been reviewed.
- [ ] Temporary/debug code has been removed.
- [ ] Error handling is appropriate.
- [ ] External input is validated where needed.
- [ ] Existing conventions are followed.
- [ ] No unnecessary dependencies were introduced.

## Validation

Run all checks applicable to the repository.

Typical checks:

- [ ] lint
- [ ] typecheck
- [ ] tests
- [ ] production build

Do not claim a check passed unless it was actually run successfully.

If a check cannot be run, state why.

## Documentation

- [ ] `docs/STATUS.md` reflects current reality.
- [ ] `docs/ROADMAP.md` reflects milestone state.
- [ ] Architecture documentation was updated when necessary.
- [ ] ADR created when a meaningful architecture decision was made.
- [ ] Current milestone specification reflects completion state.

## Completion report

Report:

- branch
- implemented changes
- validation performed
- documentation updated
- deferred work
- milestone state
- readiness for PR

Stop after completion.