# Project Agent Guide

## Project

`{{PROJECT_NAME}}` is a `{{SYSTEM_TYPE}}` built with `{{STACK_SUMMARY}}`.

## Read Before Working

- Product overview: `docs/product/overview.md`
- Architecture map: `ARCHITECTURE.md`
- Architecture details: `docs/architecture/index.md`
- Active plans: `docs/plans/active/`
- Definition of done: `docs/quality/definition-of-done.md`
- Security principles: `docs/security/principles.md`

## Workflow

1. Read this file and the nearest `AGENTS.md` for the files you will touch.
2. Open only the relevant docs for the current task.
3. For non-trivial work, create or update a plan in `docs/plans/active/`.
4. Implement the smallest coherent change.
5. Update documentation when behavior, architecture, API, data, or decisions change.
6. Run the project's verification commands before calling work complete.

## Required Verification

Replace these placeholders with the project's real commands:

- Format: `{{FORMAT_COMMAND}}`
- Lint: `{{LINT_COMMAND}}`
- Test: `{{TEST_COMMAND}}`
- Build/typecheck: `{{BUILD_OR_TYPECHECK_COMMAND}}`
- Full validation: `{{VERIFY_COMMAND}}`

## Constraints

- Do not put product or architecture knowledge in `.codex/`.
- Do not introduce production dependencies without documenting why.
- Do not modify generated files manually.
- Do not bypass validation at HTTP, environment, auth, database, or external-service boundaries.
- Do not mark work complete while verification is failing.
- Keep secrets out of committed files.

## Definition Of Done

Implementation, verification, documentation, and acceptance criteria must agree.

