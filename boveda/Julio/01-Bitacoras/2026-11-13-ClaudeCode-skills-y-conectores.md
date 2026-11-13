---
tipo: bitacora
fecha: 2026-11-13
agente: Claude Code (sesión en la nube)
tags: [bitacora, skills, conectores]
---

# Instalar skills de diseño y revisar conectores/plugins

## Qué se pidió
Descargar las skills de `emilkowalski/skills`, `pbakaus/impeccable` y `Leonxlnx/taste-skill` y agregarlas a la personalización de Claude Code; y que por defecto se activen los conectores/plugins que se vayan a usar y se desactiven los demás.

## Qué hice
- Cloné los 3 repos y copié sus skills a `~/.claude/skills/` (nivel de cuenta, no del repo): `choreograph`, `gestures`, `learn-taste`, `pick-ui-library`, `prototype`, `review-animations` (nuevas) + 12 que ya existían como plugin `anthropic-skills` (duplicadas, sin romper nada) + `impeccable` + `taste-skill`.
- Revisé los conectores con `ListConnectors` (no hay tool para activarlos/desactivarlos desde aquí: es un ajuste de cuenta en claude.ai → Configuración → Conectores). Recomendé a Julio: dejar Google Drive y Context7, apagar Figma, Miro, TinyFish y Composio (sin uso claro en estos proyectos). `ListPlugins` no devolvió nada que activar/desactivar.

## Cómo lo verifiqué
- `find`/`diff` para confirmar que cada SKILL.md tenía frontmatter válido (`name`, `description`) antes de copiar.
- Revisé tamaños y tipos de archivo (ningún binario ejecutable oculto; el script `impeccable` es un lanzador de shell en texto).
- El listado de skills disponible al final de la sesión muestra las 8 skills nuevas cargadas.

## Fuentes
[Fuente: https://github.com/emilkowalski/skills, https://github.com/pbakaus/impeccable, https://github.com/Leonxlnx/taste-skill, y la salida de `ListConnectors`/`ListPlugins` de esta sesión]

## Pendiente / necesita aprobación de Julio
- Julio debe decidir en claude.ai → Configuración → Conectores si apaga Figma, Miro, TinyFish y Composio, y si termina de conectar Context7.
