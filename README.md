# context-eng-expressjs-nextjs

Repositorio plantilla para trabajar sistemas Express.js + Next.js con agentes de IA de forma repetible, verificable y mantenible.

La idea central es no convertir un prompt en una enciclopedia. El repositorio debe darle al agente:

- Un mapa corto de instrucciones permanentes.
- Documentos versionados donde buscar contexto profundo.
- Procedimientos reutilizables como skills.
- Criterios de verificacion y definicion de terminado.
- Lugares claros para registrar planes, decisiones y deuda tecnica.

Este repo no contiene codigo de aplicacion, dependencias, build, compilacion ni runtime. Solo contiene archivos Markdown y estructura de carpetas.

## Como usarlo en un proyecto nuevo

1. Copia esta estructura en la raiz del nuevo repo.
2. Edita `AGENTS.md` con el nombre del proyecto, stack y comandos reales.
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
