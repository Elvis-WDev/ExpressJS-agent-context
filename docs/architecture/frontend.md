# Frontend Architecture

## Runtime

- Framework: Next.js.
- Language: TypeScript.
- Styling: Tailwind CSS.
- Component system: shadcn/ui.
- Icons: lucide-react.
- Form handling: React Hook Form + Zod.
- Data fetching: typed API helpers over internal backend routes.
- Charts: shadcn-compatible chart components for dashboards.

## UI Rules

- Use product screens as the first viewport for applications.
- Keep large tables paginated or virtualized.
- Keep forms validated and accessible.
- Communicate loading, success, empty, and error states.
- Do not expose server-only secrets.
- Use shadcn/ui components before creating custom primitives.
- Use icons for common actions when a familiar icon exists.
- Use tables for dense operational data, not decorative card grids.
- Keep dashboards informative: KPIs plus charts that transform data into decisions.

## State

- Server state: fetch through typed API helpers.
- Form state: React Hook Form.
- Validation state: Zod schemas.
- Local UI state: component state for transient interactions.
- URL state: filters, pagination, or deep-linkable views when useful.

## Design System

- Components: shadcn/ui.
- Icons: lucide-react.
- Charts: shadcn chart conventions.
- Motion: use sparingly for feedback and state transitions.
- Theme: CSS variables and Tailwind tokens.
