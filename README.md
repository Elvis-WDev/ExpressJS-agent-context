# context-eng-expressjs-nextjs

Repositorio plantilla de contexto para crear aplicaciones Express.js + Next.js con agentes de IA de forma repetible, verificable y mantenible.

Este contexto define un stack recomendado y buenas practicas para nuevos sistemas:

- **Runtime:** Node.js + TypeScript.
- **Backend:** Express.js REST API con arquitectura por capas.
- **Frontend:** Next.js + React + TypeScript.
- **Auth:** Better Auth. No reinventar login, sesiones ni hashing.
- **Base de datos:** PostgreSQL como base principal.
- **ORM:** Prisma con migraciones versionadas.
- **UI:** Tailwind CSS + shadcn/ui + iconos consistentes.
- **Formularios:** React Hook Form + Zod.
- **HTTP externo:** Axios con adaptadores tipados y tokens server-side.
- **Package manager:** pnpm via Corepack.
- **Deploy:** Docker-ready, compatible con plataformas como Dokploy.

La idea central es no convertir un prompt en una enciclopedia. El repositorio debe darle al agente:

- Un mapa corto de instrucciones permanentes.
- Documentos versionados donde buscar contexto profundo.
- Procedimientos reutilizables como skills.
- Criterios de verificacion y definicion de terminado.
- Lugares claros para registrar planes, decisiones y deuda tecnica.

Este repo no contiene codigo de aplicacion, dependencias, build, compilacion ni runtime. Solo contiene archivos Markdown y estructura de carpetas.

## Como usarlo en un proyecto nuevo

1. Copia esta estructura en la raiz del nuevo repo.
2. Edita `AGENTS.md` con el nombre del proyecto y comandos reales.
3. Completa `docs/product/overview.md` antes de implementar.
4. Crea una carpeta por feature en `docs/product/features/`.
5. Registra planes complejos en `docs/plans/active/`.
6. Mueve planes terminados a `docs/plans/completed/`.
7. Actualiza `ARCHITECTURE.md` y `docs/architecture/` cuando cambien decisiones tecnicas.
8. Convierte errores repetidos del agente en reglas, tests, linters o skills.

## Estructura

```text
.
├── AGENTS.md
├── ARCHITECTURE.md
├── CLAUDE.md
├── README.md
├── .agents/
│   └── skills/
├── .codex/
│   └── README.md
├── .github/
│   ├── copilot-instructions.md
│   └── instructions/
└── docs/
    ├── product/
    ├── architecture/
    ├── plans/
    ├── quality/
    ├── security/
    └── generated/
```

## Principios

- `AGENTS.md` es un mapa, no una enciclopedia.
- `docs/` es la fuente de verdad del proyecto.
- Las instrucciones cercanas al codigo tienen prioridad sobre las globales.
- Las decisiones importantes se versionan junto al sistema.
- Las reglas criticas deben convertirse en automatizacion cuando sea posible.
- Los procedimientos repetitivos viven como skills.
- Better Auth, PostgreSQL, Prisma, pnpm y TypeScript son decisiones base del stack.
- El frontend debe construirse con componentes reales, formularios validados y estados claros.
- El backend debe proteger boundaries: HTTP, auth, env, base de datos e integraciones externas.
