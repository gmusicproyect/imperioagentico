# Clase 13 — Segundo Cerebro & RAG con Obsidian

**Tags:** `Obsidian` `RAG` `Memoria` `Segundo Cerebro`
**Conecta con:** Clase 04 · Clase 10

---

## Idea central

Claude Code puede conectarse a una base de conocimiento externa (Obsidian u otro sistema de notas) para recuperar información relevante antes de actuar. Esto es RAG (Retrieval-Augmented Generation) aplicado a flujos agénticos.

---

## El problema que resuelve

Sin memoria externa:
- Claude Code solo sabe lo que está en el contexto actual
- Información de proyectos anteriores se pierde
- Hay que repetir contexto en cada sesión

Con Obsidian + RAG:
- Claude Code busca en tus notas antes de responder
- El conocimiento acumulado de meses está disponible en segundos
- Proyectos y clientes tienen su propia memoria persistente

---

## Arquitectura

```
Obsidian Vault
    ├── /clientes/[cliente].md
    ├── /proyectos/[proyecto].md
    ├── /learnings/[tema].md
    └── /templates/[plantilla].md
         ↓
    MCP de Obsidian / lectura directa de archivos
         ↓
    Claude Code lee el contexto relevante antes de actuar
```

---

## Qué guardar en el segundo cerebro

| Carpeta | Contenido |
|---------|-----------|
| `/clientes/` | Perfil, historial, preferencias, notas de llamadas |
| `/proyectos/` | Objetivo, estado actual, próximos pasos |
| `/learnings/` | Lo que aprendiste de cada proyecto |
| `/prompts/` | Prompts que funcionaron bien |
| `/skills/` | SOPs documentados |

---

## 🎯 Ejercicio práctico

**Ejercicio 1:** Crea en tu proyecto una carpeta `segundo-cerebro/` con subcarpetas `clientes/` y `learnings/`. Añade un archivo `cliente-ejemplo-perfil.md` con datos como: nombre, tono de voz preferido, servicios contratados y restricciones. Pídele a Claude Code: "Consulta `segundo-cerebro/clientes/cliente-ejemplo-perfil.md` y redacta un correo de actualización mensual respetando el tono y las restricciones del cliente".

**Ejercicio 2 (avanzado):** Añade un archivo `learnings/lecciones-aprendidas.md` con 2 reglas aprendidas de proyectos previos. Pídele a Claude Code que genere una propuesta consultando tanto el perfil del cliente como las lecciones aprendidas, y comprueba que cite las fuentes consultadas.

*Este ejercicio deja implementada la estructura de segundo cerebro (RAG) para alimentar a tu agente con contexto persistente.*

---

## 💡 Tip

La clave del RAG efectivo está en nombrar bien los archivos. `cliente-acme-perfil.md` es 100 veces más fácil de encontrar para Claude Code que `notas-reunion-martes.md`.
