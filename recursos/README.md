# Recursos & Plantillas

Plantillas reutilizables para nuevos proyectos con Claude Code.

## Plantillas disponibles

| Archivo | Para qué |
|---------|---------|
| [claude-md-global.md](./plantillas/claude-md-global.md) | Base para `~/.claude/CLAUDE.md` — aplica a todos los proyectos |
| [claude-md-proyecto.md](./plantillas/claude-md-proyecto.md) | Base para el `CLAUDE.md` de cada proyecto específico |
| [skill-template.md](./plantillas/skill-template.md) | Estructura base para cualquier SKILL.md |

## Cómo usar las plantillas

### Para un proyecto nuevo

```bash
# 1. Crea la carpeta del proyecto
mkdir mi-nuevo-proyecto && cd mi-nuevo-proyecto

# 2. Copia la plantilla de CLAUDE.md
cp ruta/a/imperioagentico/recursos/plantillas/claude-md-proyecto.md CLAUDE.md

# 3. Edita con el contexto de tu proyecto
# 4. Crea la carpeta de skills
mkdir -p skills/mi-primer-skill

# 5. Copia la plantilla de skill
cp ruta/a/imperioagentico/recursos/plantillas/skill-template.md skills/mi-primer-skill/SKILL.md
```

### Para el CLAUDE.md global

```bash
# Si no tienes uno todavía
mkdir -p ~/.claude
cp ruta/a/imperioagentico/recursos/plantillas/claude-md-global.md ~/.claude/CLAUDE.md
```
