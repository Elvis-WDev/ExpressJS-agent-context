# Definition Of Done

A change is done only when:

- The implementation matches the relevant product specification.
- Acceptance criteria are satisfied or explicitly updated.
- Verification commands pass.
- API, database, architecture, security, or user workflow docs are updated when behavior changes.
- New dependencies are justified.
- Generated files are produced by scripts or documented sources, not manually edited.
- No secrets are committed.
- pnpm/Corepack commands were used.
- Stack decisions remain aligned with `docs/architecture/stack.md` or an ADR explains the deviation.

For backend work:

- Use cases do not import infrastructure.
- Domain code remains framework-free.
- HTTP validation and error handling are explicit.
- Protected endpoints use documented auth middleware.
- Better Auth owns auth behavior.
- Prisma migrations exist for schema changes.
- PostgreSQL behavior is considered for production.

For frontend work:

- Loading, empty, success, and error states are handled.
- Forms use validation.
- Large lists are paginated or virtualized.
- Text and controls fit on supported viewports.
- shadcn/ui conventions are followed.
- Authenticated and unauthenticated states are handled.
