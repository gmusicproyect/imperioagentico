# Instrucciones para agentes que trabajan en este repo

> Este archivo es el equivalente a `CLAUDE.md` (ver `curso-claude-code/clases/clase-04-arquitectura.md`)
> para cualquier agente que no sea Claude Code — Antigravity/Google incluido.
> Si tu agente lee automáticamente un archivo de instrucciones raíz, esto se carga solo.

---

## Qué es este repo

`imperioagentico` es la base de conocimiento del curso Claude Code de Imperio Digital: clases, bonos, skills reutilizables y plantillas. Cada pieza de contenido nuevo debe integrarse siguiendo una estructura fija, no ad-hoc.

---

## Instrucción por defecto para transcripciones nuevas

Cuando recibas una transcripción cruda (de cualquier tema: clase nueva, profundización de una existente, o herramienta/bono específico) para integrarla a este repo:

**Aplica siempre `skills/procesar-transcripcion/SKILL.md`.**

Ese skill contiene:
- La tabla de decisión (Paso 0) para clasificar el contenido: clase nueva / profundización de una clase existente / bono / skill reutilizable extraído
- La estructura exacta a seguir en cada caso (referencia a `skills/transcribir-clase-curso/SKILL.md` para clases)
- Qué índices actualizar (`README.md`, `curso-claude-code/README.md`, `bonos/README.md`, `skills/README.md`)
- El protocolo de entrega: **no hagas commit ni push**, y **no repegues el contenido completo de los archivos en tu respuesta** — repórtale a Claude en 1-2 líneas por archivo qué creaste o modificaste

No hace falta que Juan te repita esta instrucción cada vez. Si te llega una transcripción sin más contexto, asume que aplica este flujo.

---

## Quién aprueba

Claude revisa cada entrega con `git diff` antes de que algo se suba a GitHub. Tu trabajo termina en dejar los archivos correctos en el working tree — no en decidir que están listos para producción.
