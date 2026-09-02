# Clase 05 — Skills

**Tags:** `Skills` `SOPs` `Reutilización`
**Conecta con:** Clase 04 · Clase 12

---

## Idea central

Los Skills son SOPs (procedimientos estándar) escritos en Markdown que Claude Code lee antes de ejecutar una tarea. En lugar de explicar el proceso cada vez, lo escribes una vez y lo reutilizas infinitamente.

---

## Qué es un SKILL.md

Un archivo `.md` que le dice a Claude Code:
1. **Cuándo** usarlo
2. **Qué pasos** seguir
3. **Qué herramientas** necesita
4. **Qué errores** evitar

---

## Estructura de un SKILL.md

```markdown
# [Nombre del Skill]

## Cuándo usar este skill
[Descripción del trigger — cuándo Claude debe leer esto]

## Pasos
1. [Paso 1]
2. [Paso 2]
3. [Paso 3]

## Herramientas requeridas
- [MCP / herramienta]

## Errores comunes
- [Error]: [Cómo evitarlo]

## Notas adicionales
[Contexto extra, variaciones, ejemplos]
```

---

## Dónde guardar los skills

```
/tu-proyecto/
└── skills/
    ├── crear-contacto-ghl/
    │   └── SKILL.md
    ├── publicar-ad/
    │   └── SKILL.md
    └── reportar-metricas/
        └── SKILL.md
```

Referencia en CLAUDE.md: `- /skills/crear-contacto-ghl/SKILL.md → para crear contactos en GHL`

---

## 💡 Tip

Crea un skill después de hacer algo bien 2 veces. Si repetiste un proceso manualmente dos veces, ya vale la pena documentarlo como skill.

---

## ⚠️ Error común

Skills demasiado genéricos que aplican a todo. Un skill efectivo es específico: "publicar-reel-instagram" es mejor que "publicar-contenido".
