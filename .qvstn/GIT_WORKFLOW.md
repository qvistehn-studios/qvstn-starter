# QVSTN Git Workflow

## Main branch

`main` represents the latest known-good state of the project.

Never perform implementation directly on `main`.

Do not force push `main`.

Do not rewrite shared history without an explicit and justified reason.

## Before starting work

Before implementation:

1. inspect `git status`
2. ensure unrelated local changes are understood
3. fetch current remote state
4. ensure the intended base is current
5. create or switch to an appropriately scoped branch

Do not discard unknown local changes.

## Branch naming

Use one of:

- `feature/<description>`
- `fix/<description>`
- `refactor/<description>`
- `docs/<description>`
- `chore/<description>`

Milestone work may use:

`feature/m<number>-<description>`

Examples:

`feature/m1-foundation`

`feature/m3-site-crawler`

`fix/url-normalization`

`refactor/page-repository`

## Branch scope

A branch should contain one coherent piece of work.

Do not mix unrelated changes into the same branch.

Do not perform opportunistic cleanup unrelated to the task.

If unrelated work is discovered, document or defer it.

## Commits

Prefer small, coherent commits.

Commit messages should communicate intent.

Avoid meaningless messages such as:

`stuff`

`changes`

`fix`

Do not knowingly commit:

- credentials
- local environment secrets
- temporary debugging output
- generated junk files
- unrelated changes

## Pull requests

Changes to `main` should be merged through a pull request.

Before marking a PR ready:

- validation passes
- scope is understood
- diff has been reviewed
- documentation is current
- no known blocking issue remains

## Forbidden shortcuts

Do not:

- bypass hooks with `--no-verify` merely to force a commit through
- disable failing tests to make CI green
- force push `main`
- knowingly merge failing code
- knowingly commit secrets
- hide validation failures

## After merge

Delete branches that are no longer needed.

Start future work from the current known-good base.