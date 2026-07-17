# agent-ready-app-context

Repositorio de contexto para construir aplicaciones modernas con agentes de IA de forma repetible, verificable y mantenible.

`agent-ready-app-context` no es un starter de codigo. Es una base documental y operativa para que un desarrollador o agente de IA pueda iniciar cualquier aplicacion con una arquitectura clara, un stack recomendado y reglas de trabajo consistentes.

Su proposito es evitar empezar cada proyecto desde cero en decisiones fundamentales como autenticacion, base de datos, estructura, documentacion, calidad, seguridad y flujo de trabajo con IA.

## Para que sirve

Sirve para crear nuevos sistemas con un contexto inicial robusto:

- Define el stack tecnico recomendado.
- Explica las buenas practicas base.
- Organiza la documentacion del producto y arquitectura.
- Da instrucciones a agentes como Codex, Claude o GitHub Copilot.
- Incluye skills reutilizables para implementar features, crear migraciones, revisar codigo y actualizar documentacion.
- Ayuda a que cada cambio tenga plan, implementacion, verificacion y documentacion.
- Evita que el agente dependa de conversaciones pasadas o contexto invisible.

## Para quien es

- Desarrolladores que quieren trabajar con agentes de IA sin perder control arquitectonico.
- Equipos que quieren estandarizar la forma de iniciar aplicaciones fullstack.
- Proyectos internos, SaaS, dashboards, CRMs, APIs, herramientas operativas o paneles administrativos.
- Cualquier aplicacion que necesite autenticacion, base de datos, frontend moderno y backend REST.

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

## Idea central

No se trata de escribir un prompt gigante. Se trata de disenar el repositorio como un sistema de conocimiento navegable.

El agente debe recibir primero un mapa pequeno y despues abrir solo la documentacion relevante para la tarea.

Este repositorio le da al agente:

- Un mapa corto de instrucciones permanentes.
- Documentos versionados donde buscar contexto profundo.
- Procedimientos reutilizables como skills.
- Criterios de verificacion y definicion de terminado.
- Lugares claros para registrar planes, decisiones y deuda tecnica.

## Que incluye

- `AGENTS.md`: instrucciones base para agentes.
- `ARCHITECTURE.md`: mapa arquitectonico de alto nivel.
- `CLAUDE.md`: memoria equivalente para flujos con Claude.
- `.agents/skills/`: procedimientos reutilizables bajo demanda.
- `.github/copilot-instructions.md`: instrucciones base para GitHub Copilot.
- `.github/instructions/`: reglas especificas por tipo de trabajo.
- `.codex/README.md`: criterio para no mezclar configuracion con conocimiento del proyecto.
- `docs/product/`: producto, dominio, glosario y features.
- `docs/architecture/`: stack, bootstrap, backend, frontend, auth, database, deployment e integraciones.
- `docs/plans/`: planes activos, completados y deuda tecnica.
- `docs/quality/`: definicion de terminado, testing, code review y observabilidad.
- `docs/quality/frontend-checklist.md`: revision visual, funcional, responsive y de accesibilidad antes de cerrar una interfaz.
- `docs/security/`: principios y threat model.
- `docs/generated/`: referencias generadas o derivadas.

## Que no incluye

- Codigo de aplicacion.
- Dependencias.
- Build output.
- Configuracion real de secretos.
- Logica de negocio de ningun dominio especifico.
- Funcionalidades copiadas de un sistema existente.

Solo contiene archivos Markdown y estructura de carpetas.

## Como usarlo en un proyecto nuevo

1. Copia esta estructura en la raiz del nuevo proyecto.
2. Edita `AGENTS.md` con el nombre real del producto y scripts disponibles.
3. Lee `docs/architecture/bootstrap.md` para crear la base tecnica.
4. Completa `docs/product/overview.md`.
5. Crea una carpeta por feature en `docs/product/features/`.
6. Registra trabajos complejos en `docs/plans/active/`.
7. Implementa usando el stack documentado.
8. Actualiza docs junto con el codigo.
9. Mueve planes terminados a `docs/plans/completed/`.
10. Convierte errores repetidos del agente en reglas, tests, linters o skills.

## Flujo recomendado con agentes

1. Pedir al agente que lea `AGENTS.md`.
2. Pedirle que abra solo los documentos relevantes.
3. Para tareas grandes, pedirle un plan en `docs/plans/active/`.
4. Implementar cambios pequenos y coherentes.
5. Ejecutar verificacion.
6. Actualizar documentacion.
7. Registrar decisiones importantes en ADRs.

## Decisiones base del stack

Estas decisiones son intencionales y deben cambiarse solo con un ADR:

- Better Auth para autenticacion.
- PostgreSQL para produccion.
- Prisma para ORM y migraciones.
- pnpm/Corepack como package manager.
- Express.js para REST API.
- Next.js para frontend.
- shadcn/ui y Tailwind CSS para UI.
- React Hook Form + Zod para formularios.
- Axios para integraciones externas server-side.

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
- Las interfaces operativas deben priorizar lectura, comparacion y accion: tablas consistentes, formularios enfocados, navegacion de dos niveles como maximo y feedback mediante estados transitorios.
- Los detalles tecnicos pertenecen al backend, logs o auditoria; la UI muestra lenguaje de negocio y selecciones reconocibles por la persona usuaria.
- El backend debe proteger boundaries: HTTP, auth, env, base de datos e integraciones externas.

## Criterios de interfaz incluidos

El repositorio incorpora criterios reutilizables aprendidos al construir paneles operativos grandes sin convertir cada pantalla en una acumulacion de controles:

- Jerarquia visual y composicion de modulos: `docs/architecture/interface-design.md`.
- Contratos de componentes compartidos: `docs/architecture/component-system.md`.
- Data tables homogeneos: `docs/architecture/data-tables.md`.
- Formularios, modales y flujos de pagina completa: `docs/architecture/forms-and-workflows.md`.
- Toasts, validacion, carga, vacios y errores: `docs/architecture/feedback-and-states.md`.
- Sidebar, header, responsive y dark mode: `docs/architecture/navigation-responsive.md`.
- Checklist de aceptacion frontend: `docs/quality/frontend-checklist.md`.
- Procedimiento para agentes: `.agents/skills/implement-operational-frontend/SKILL.md`.

## Nombre oficial

**agent-ready-app-context**
