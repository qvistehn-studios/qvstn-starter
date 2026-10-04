# QVSTN Engineering Principles

## General philosophy

Prefer simple solutions over clever solutions.

Prefer explicit behaviour over hidden magic.

Prefer maintainability over short-term convenience.

Avoid premature optimization.

Avoid premature abstraction.

Do not create architecture for requirements that do not yet exist.

## Code structure

Keep modules and functions focused.

Use clear, descriptive names.

Separate domain logic from infrastructure where practical.

Keep configuration separate from business logic.

Follow existing project conventions before introducing new patterns.

Do not refactor unrelated code during scoped feature work.

## Type safety

Use strong typing when supported by the language.

Avoid unsafe casts unless unavoidable and justified.

Represent invalid states explicitly when practical.

Do not use broad escape hatches merely to silence compiler or type errors.

## Error handling

Handle expected failures explicitly.

Never silently swallow meaningful errors.

Provide useful internal context when errors occur.

Do not expose secrets, credentials or sensitive implementation details in user-facing errors.

## Input and boundaries

Treat external input as untrusted.

Validate data entering the system.

Validate responses from external services when correctness depends on their shape.

Keep trust boundaries explicit.

## Dependencies

Before adding a dependency:

1. determine whether the platform or existing stack already provides the functionality
2. confirm the dependency provides meaningful value
3. prefer mature and actively maintained packages
4. avoid dependencies for trivial functionality
5. avoid adding a new framework or major architectural pattern solely for convenience

Remove unused dependencies.

## Testing

Test meaningful behaviour, not implementation trivia.

Bug fixes should normally include regression coverage.

Do not remove or weaken tests merely to make new code pass.

When a test fails, first determine whether:

- the implementation is wrong
- the test is wrong
- the expected behaviour has intentionally changed

Behavioural changes must be documented.

## Security

Never commit credentials or secrets.

Use environment variables or approved secret-management mechanisms.

How to handle secrets:

- Store real values in the hosting provider's settings (for example Cloudflare, Supabase or Vercel) or in a local `.env` file.
- `.env`, `.env.*` and other local secret files are gitignored. Do not remove these rules.
- Document every required variable in `.env.example`, with names only and no values.
- Values exposed to the browser (for example `VITE_*` or `NEXT_PUBLIC_*`) are public. Never put a secret in them.
- If a secret is committed, treat it as leaked: rotate it at the provider first, then remove it from the repository.

Apply least privilege to external services.

Validate authorization separately from authentication.

Do not trust client-side validation for security-sensitive behaviour.

Avoid logging sensitive information.

Keep dependencies reasonably current and review meaningful security warnings.

## Generated and AI-assisted code

AI-generated code is held to the same standard as human-written code.

Generated code must be:

- understood
- reviewed
- validated
- consistent with project architecture

Code must not be accepted solely because it compiles or appears plausible.