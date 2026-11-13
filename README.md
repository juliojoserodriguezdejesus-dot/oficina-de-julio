# Oficinas de Julio

Mi oficina de agentes.

- **Oficina 3D (estilo LEGO):** https://claude.ai/artifact/G78cQyyqqUxTYZ3hyHD5qB (código en `oficina/oficina.html`). Agencia de páginas web con 28 agentes en 12 departamentos (Dirección, Ventas, Atención al Cliente, Marketing, SEO y Contenido, Diseño, Frontend, Backend, Bases de Datos, Seguridad, Calidad, Operaciones). Menú lateral con Oficina, Encargar tarea, Equipo, Bases de Datos, Seguridad, Chat e Historial.
- **Agentes para Claude Code** en `.claude/agents/`: `director`, `asesor-de-consumo`, `trabajador-economico`, `auditor-de-sesion`. Copia esa carpeta a cualquier proyecto (o a `~/.claude/agents/`) para usarlos.

## Documentos y tokens
- **Documentos:** sube PDF, Word, TXT, CSV, Markdown, HTML, JSON o imágenes. Al encargar una tarea eliges cuáles usar y el jefe le pasa a cada agente solo los que necesita.
- **Descargas:** la entrega final se descarga en Word (.docx), HTML o Markdown.
- **Ahorro de tokens:** el jefe elige el modelo de cada paso (rápido, normal o avanzado). En "Uso de tokens" puedes pedir máximo ahorro o máxima calidad. Cada paso muestra el modelo usado y los tokens aproximados.

## Constitución, Calidad y aprobación
- **36 agentes** con ficha: cerebro (modelo de Claude), herramientas, desempeño y memoria propia.
- **Constitución** de 5 reglas que cada agente recibe antes de cada tarea.
- **Equipos** de Pantalla (celular y PC), Servidor, Pruebas, Seguridad, Calidad y Aprobación.
- **Calidad** revisa cada entrega y la devuelve al agente si no cumple (hasta 2 correcciones).
- **Aprobaciones:** al terminar, ves qué hizo cada agente, la nota de Calidad y las acciones irreversibles; tú apruebas o pides cambios.
- **Biblioteca:** bóveda descargable para Obsidian (.zip) con agentes, departamentos, encargos y documentos enlazados.

## Baúl de Obsidian
La carpeta `boveda/Oficinas de Julio/` es una carpeta de notas de Obsidian con la sesión de creación, la guía de la oficina, la constitución, los departamentos y una nota por agente. Cópiala dentro de tu baúl (o usa Obsidian Git).
