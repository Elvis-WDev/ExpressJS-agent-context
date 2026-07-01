# Architecture Map

## System Style

Describe the dominant architecture:

- Modular monolith
- Distributed services
- Event-driven system
- API plus frontend
- CLI/tooling
- Other

## Main Components

- `{{COMPONENT_1}}`: responsibility.
- `{{COMPONENT_2}}`: responsibility.
- `docs/product/`: product specifications and domain knowledge.
- `docs/architecture/`: technical decisions and boundaries.
- `docs/plans/`: active and completed implementation plans.

## Dependency Direction

Define the allowed dependency flow.

Example:

```text
domain -> application/use-cases -> infrastructure
```

Rules:

- Domain must not depend on frameworks or databases.
- Application logic depends on ports/interfaces, not concrete infrastructure.
- Infrastructure implements ports and owns external tools.
- UI code should not know server-side secrets.

## Boundaries

Document the major boundaries:

- Authentication boundary.
- HTTP/API boundary.
- Database boundary.
- External-service boundary.
- Background-job boundary.
- Frontend/client boundary.

## Detailed Documents

- Architecture index: `docs/architecture/index.md`
- Backend: `docs/architecture/backend.md`
- Frontend: `docs/architecture/frontend.md`
- Database: `docs/architecture/database.md`
- Integrations: `docs/architecture/integrations.md`
- ADRs: `docs/architecture/adr/`

