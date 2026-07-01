# Architecture Index

## Read Order

1. `ARCHITECTURE.md`
2. `docs/architecture/stack.md`
3. `docs/architecture/bootstrap.md`
4. `docs/architecture/backend.md`
5. `docs/architecture/frontend.md`
6. `docs/architecture/authentication.md`
7. `docs/architecture/database.md`
8. `docs/architecture/integrations.md`
9. `docs/architecture/deployment.md`
10. `docs/architecture/adr/`

## Architecture Rules

- Document boundaries explicitly.
- Keep dependency direction enforceable.
- Prefer tests or lint rules for critical constraints.
- Record irreversible or costly decisions as ADRs.
- Use the default stack unless an ADR explains why a project deviates.
