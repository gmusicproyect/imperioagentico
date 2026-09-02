# Clase 04 — Arquitectura CLAUDE.md

**Tags:** `Arquitectura` `Memoria` `Proyectos`
**Conecta con:** Clase 03 · Clase 05

---

## Idea central

CLAUDE.md es la memoria persistente de Claude Code. Define quién es el agente, qué puede hacer, cómo debe comportarse y qué herramientas tiene disponibles en cada proyecto.

---

## Global vs Local

| Tipo | Ubicación | Alcance |
|------|-----------|---------|
| **Global** | `~/.claude/CLAUDE.md` | Aplica a todos los proyectos |
| **Local** | `/tu-proyecto/CLAUDE.md` | Solo aplica a ese proyecto |

Los dos se combinan: el global da el contexto base y el local lo sobreescribe o extiende.

---

## Estructura recomendada de CLAUDE.md

```markdown
# Identidad del agente
Eres [nombre]. Tu función es [propósito].

# Contexto del proyecto
[Descripción del proyecto, cliente, objetivo]

# Herramientas disponibles
- [MCP 1]: para [acción]
- [MCP 2]: para [acción]

# Reglas de comportamiento
- [Regla 1]
- [Regla 2]

# Skills disponibles
- /skills/[nombre]/SKILL.md → [para qué]
```

---

## Cuándo usar cada uno

- **Global**: identidad base, estilo de respuesta, herramientas universales
- **Local**: cliente específico, proyecto concreto, restricciones particulares

---

## 🎯 Ejercicio práctico

**Ejercicio 1:** Crea un archivo `CLAUDE.md` en la raíz de tu proyecto siguiendo la estructura recomendada: define la identidad del agente, el contexto de tu proyecto, reglas claras de comportamiento y las secciones para herramientas y skills.

**Ejercicio 2 (avanzado):** Inicia una nueva sesión en Claude Code y pregúntale: "¿Quién eres, cuál es tu objetivo en este proyecto y qué reglas de comportamiento tienes asignadas?". Comprueba que su respuesta refleje exactamente lo que redactaste en tu `CLAUDE.md`.

*Este ejercicio te deja listo el archivo CLAUDE.md local, que servirá como la memoria persistente central de tu proyecto.*

---

## 💡 Tip

Empieza el CLAUDE.md con una línea de identidad clara: `Eres [nombre], un agente especializado en [dominio].` Claude Code usa esto como ancla para todas sus decisiones.

---

## ⚠️ Error común

Poner todo en el CLAUDE.md global y no tener archivos locales. Cuando cambias de proyecto el contexto queda mezclado y Claude Code se confunde.
