# Security Principles

- Secrets are never committed.
- Provider tokens stay server-side.
- Validate input at every boundary.
- Use least-privilege credentials in production.
- Do not expose internal provider details unless users need them.
- Authentication and authorization must be explicit on protected routes.
- Avoid storing sensitive data unless there is a clear product need.

## Environment Variables

Document required variables in the app repo, not in this template.

Use placeholders only:

```text
SERVICE_API_TOKEN=replace-with-token
DATABASE_URL=replace-with-url
```

