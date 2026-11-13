---
tipo: guia
tags: [claude-code, agentes]
---

# Agentes de Claude Code

Están en `.claude/agents/` del repo. Copia esa carpeta a cualquier proyecto o a `~/.claude/agents/`.

- **director:** divide la tarea, delega eligiendo `haiku`, `sonnet` u `opus`, crea agentes nuevos si faltan, aplica la [[Constitución]], revisa como Calidad y pide aprobación antes de lo irreversible.
- **asesor-de-consumo** (Haiku): antes de una tarea grande, recomienda modelo, esfuerzo y qué delegar.
- **trabajador-economico** (Haiku): tareas simples y mecánicas.
- **auditor-de-sesion** (Sonnet): explica por qué una sesión salió cara y cómo evitarlo.

Aquí sí funcionan las herramientas por MCP (GitHub, Drive y otras).
