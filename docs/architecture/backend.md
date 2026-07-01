# Backend Architecture

## Runtime

- Language:
- Framework:
- Package manager:
- Database access:
- Authentication:

## Layers

### Domain

Responsibilities:

- Entities.
- Value objects.
- Domain errors.
- Business invariants.

Forbidden dependencies:

- HTTP frameworks.
- Database clients.
- External SDKs.

### Application / Use Cases

Responsibilities:

- Workflows.
- Ports/interfaces.
- DTOs.
- Transaction boundaries when applicable.

Forbidden dependencies:

- Concrete infrastructure.
- HTTP request/response objects.

### Infrastructure

Responsibilities:

- HTTP controllers/routes.
- Database repositories.
- External service clients.
- Background jobs.
- Runtime configuration.

## REST / API Conventions

- Success response shape:
- Error response shape:
- Pagination:
- Auth:
- Validation:

## Background Jobs

- Job ownership:
- Persistence:
- Retry policy:
- Cancellation:
- Progress reporting:

