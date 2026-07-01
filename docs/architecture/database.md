# Database Architecture

## Primary Database

- Engine:
- ORM/query layer:
- Migration strategy:

## Data Ownership

| Table/Collection | Owner | Notes |
| --- | --- | --- |
| `{{TABLE}}` | `{{MODULE}}` | Description. |

## Migration Rules

- Schema changes require a migration.
- Generated database docs must be refreshed after migrations.
- Destructive migrations require an explicit data plan.
- Production migration credentials should be limited after initial provisioning.

## Indexing

- List critical queries.
- Map each critical query to an index.

