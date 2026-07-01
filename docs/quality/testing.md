# Testing Strategy

## Test Pyramid

- Unit tests for pure domain logic.
- Use-case tests for application behavior.
- Integration tests for database, HTTP, auth, and external boundaries.
- End-to-end tests for critical user workflows.

## What Must Be Tested

- Validation boundaries.
- Auth and permissions.
- Error responses.
- Data persistence.
- Background jobs and cancellation.
- External service failure modes.

## Test Data

- Use deterministic fixtures.
- Avoid real secrets.
- Avoid relying on unstable external services in CI.

