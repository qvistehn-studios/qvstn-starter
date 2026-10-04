# QVSTN Starter

Reusable engineering baseline for QVSTN software projects.

This repository is a GitHub template. New QVSTN projects should be created from this template rather than initialized from scratch.

## Purpose

The template establishes a consistent development process across AI-assisted and human development.

It defines:

- repository documentation
- milestone-driven development
- Git workflow
- engineering principles
- validation requirements
- architecture decision records
- AI-agent instructions
- definition of done

The same repository should be usable from different development environments, including OpenAI/Codex and Claude Code.

## Source of truth

Repository documentation is authoritative.

The current state of the project must be represented by:

- `docs/PROJECT.md`
- `docs/ARCHITECTURE.md`
- `docs/ROADMAP.md`
- `docs/STATUS.md`
- current milestone specification
- relevant architecture decision records

Conversation history, model memory and previous chat sessions must not be treated as authoritative project state.

## QVSTN protocol

Development rules are stored under:

`.qvstn/`

Read these before implementation:

1. `BUILD_PROTOCOL.md`
2. `ENGINEERING.md`
3. `GIT_WORKFLOW.md`
4. `MILESTONE_PROCESS.md`
5. `COMPLETION_CHECKLIST.md`

## Starting a new project

Create the repository from this GitHub template.

Then complete:

- `docs/PROJECT.md`
- `docs/ARCHITECTURE.md`
- `docs/ROADMAP.md`
- `docs/STATUS.md`
- the first milestone specification

Do not begin product implementation until the project foundation is documented.

## Version

QVSTN Build Protocol v0.1