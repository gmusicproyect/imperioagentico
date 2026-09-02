# Skills

Skills reutilizables creados a lo largo del curso y proyectos.

Cada skill está en su propia carpeta con un `SKILL.md` que Claude Code puede leer directamente.

## Cómo agregar un skill nuevo

1. Crea una carpeta con el nombre del skill: `mkdir nombre-del-skill`
2. Copia la plantilla: `cp ../recursos/plantillas/skill-template.md nombre-del-skill/SKILL.md`
3. Completa el SKILL.md con el proceso específico
4. Referencia el skill en el CLAUDE.md del proyecto que lo necesita

## Convención de nombres

Usa nombres descriptivos en kebab-case que indiquen **qué hace** el skill:

```
✅ crear-contacto-ghl/
✅ generar-reporte-meta/
✅ publicar-reel-instagram/
❌ ghl/
❌ meta/
❌ skill-1/
```

## Skills disponibles en este repo

| Skill | Descripción |
|-------|-------------|
| [handoff-claude-design](./handoff-claude-design/SKILL.md) | Importar y convertir diseños de Claude Design en código funcional con Claude Code |
| [gestionar-llm-wiki](./gestionar-llm-wiki/SKILL.md) | Operar y mantener base de conocimiento tipo LLM Wiki (Ingest, Query, Lint, Bulk) |
| [subir-campana-meta-personalizada](./subir-campana-meta-personalizada/SKILL.md) | Subir creativos y campañas a Meta Ads con personalización por país |
| [procesar-transcripcion](./procesar-transcripcion/SKILL.md) | Clasificar e integrar transcripciones crudas (clase, bono, skill) |
| [transcribir-clase-curso](./transcribir-clase-curso/SKILL.md) | Template y reglas de transcripción de clases del curso |
| [sincronizar-estructura-clases](./sincronizar-estructura-clases/SKILL.md) | Sincronizar clases existentes con el template vigente |

---

*Los skills de tus proyectos aparecerán aquí a medida que los crees.*
