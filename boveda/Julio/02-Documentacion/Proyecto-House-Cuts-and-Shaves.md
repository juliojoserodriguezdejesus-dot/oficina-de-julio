---
tipo: proyecto
estado: en espera de que Julio lo asigne
tags: [proyecto, universidad, cliente-interno]
repositorio: https://github.com/juliojoserodriguezdejesus-dot/house-cut-and-shaves
---

# Proyecto: House Cuts & Shaves

Proyecto de la universidad de Julio: una **app web de sistema de citas** para una barbería en Managua. El profesor exige usar un **árbol binario de búsqueda (BST) en Python** (se descartó el grafo). Idioma de interfaz y comentarios: español. El dueño del negocio (el "cliente" del proyecto) no es técnico.

Lo trabaja la [[Oficina-Agentes|oficina]] solo cuando Julio lo pida explícitamente; mientras tanto queda documentado aquí para que el Jefe y el equipo ya sepan de qué proyecto se habla.

## Qué hace
Los clientes crean cuenta y agendan (servicio → estilista → día/hora → adelanto del 50%); estilistas y recepción ven su agenda.

## Estructura
- `backend/` — API en Python (FastAPI + SQLAlchemy). Reglas de negocio en `app/rules.py`, **BST en `app/structures.py`**, uso del BST en `app/main.py` (`occupied_tree`, `free_tree`, `/availability`, `/next-available`). Roles: client, stylist (dayan, lidia), reception (carla).
- `app/` — app Expo / React Native (TypeScript), funciona en celular y web. Pantallas en `src/screens`, componentes en `src/components`.
- `docs/` — guías en PDF para explicar el proyecto al profesor y publicarlo.

## Equipos de la oficina que le corresponden
| Equipo de la oficina | Qué haría en este proyecto |
|---|---|
| Bases de Datos | Tablas `users`, `appointments`, `devices`; el BST se reconstruye en memoria, no se guarda |
| Desarrollo Backend | API FastAPI + SQLAlchemy, reglas en `app/rules.py` |
| Código / Estructuras | El BST en `app/structures.py` — es la pieza que exige el profesor |
| Pantalla (Celular y PC) | La app Expo/React Native funciona en ambos |
| Seguridad | Contraseñas con Argon2; nunca guardar datos de tarjeta |
| Pruebas | `pytest` (13 pruebas) en backend, `npx tsc --noEmit` en la app |
| Calidad / Aprobación | No tocar el BST sin actualizar `tests/test_structures.py`, `demo.py` y la guía PDF |

## Comandos clave
- Servidor: `cd backend && pip install -r requirements.txt && uvicorn app.main:app --reload` (docs interactivos en `/docs`).
- Pruebas: `cd backend && pytest`.
- Demo del BST para la exposición: `python backend/demo.py`.
- App: `cd app && npm install && npx expo start`; chequeo de tipos `npx tsc --noEmit`; web: `npx expo export --platform web`.

## Reglas importantes
- No quitar ni cambiar el BST sin actualizar pruebas, demo y la guía PDF.
- Validaciones duplicadas en TypeScript (`app/src/validate.ts`) y Python (`backend/app/rules.py`) deben coincidir (teléfono nicaragüense de 8 dígitos que empieza con 5/7/8, contraseña 8+ con letras y números).
- Marca: dorado `#EBAC56`, verde `#1C3534`, fondo `#0A0D0F`; fuentes Bodoni Moda y Jost.
- Al terminar cualquier cambio: correr `pytest` y `npx tsc --noEmit`.

## Supuestos pendientes de confirmar con el dueño (del CLAUDE.md del repo)
- Horarios de jueves a domingo son supuestos.
- Duración de citas fija en 30 min (no se conocen las duraciones reales por servicio).
- El pago del adelanto es de demostración; falta pasarela real en córdobas.
- Notificaciones push, términos y privacidad, dominio propio, cancelación/reagendado por el cliente, y un árbol AVL como mejora: todo pendiente.

## Cómo se trabaja
El repo ya trae su propio `CLAUDE.md` con estas mismas reglas para Claude Code. La oficina (Oficina 3D o los agentes de `oficina-de-julio`) solo entra a trabajar en este proyecto cuando Julio dé la orden explícita; hasta entonces, es solo contexto guardado.
