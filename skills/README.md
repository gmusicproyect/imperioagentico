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
| [configurar-agente-meta-ads](./configurar-agente-meta-ads/SKILL.md) | Configurar agente CLI de Meta Marketing API (Matías) con One Prompt Setup |
| [aplicar-framework-smart](./aplicar-framework-smart/SKILL.md) | Operar Claude Desktop/Cowork/Code con Skills, MCP, Artifacts, Refine y Test |
| [ejecutar-el-espejo](./ejecutar-el-espejo/SKILL.md) | Ejecutar auditoría forense de sesiones locales con 6 fases, gates y roadmap 30 días |
| [mapear-conocimiento-graphify](./mapear-conocimiento-graphify/SKILL.md) | Construir grafos de conocimiento local con Tree-sitter y Leiden para ahorrar tokens (4.2x) |
| [auditar-operacion-agentica](./auditar-operacion-agentica/SKILL.md) | Auditar consumo de tokens, ROI frente a APIs, salud de memoria y empaquetar skills con El Sueño |
| [produccion-creativa-higgsfield](./produccion-creativa-higgsfield/SKILL.md) | Producir fotos de producto, video cinematográfico y UGC con Higgsfield MCP optimizando créditos |
| [iniciar-proyecto-claude-code](./iniciar-proyecto-claude-code/SKILL.md) | Inicializar y estructurar proyectos en Claude Code con /init, CLAUDE.md conciso y calibración de modelo |
| [crear-claude-skill](./crear-claude-skill/SKILL.md) | Diseñar, redactar y validar skills agénticos efectivos y modulares sin saturar contexto |
| [servidor-local-control-remoto](./servidor-local-control-remoto/SKILL.md) | Configurar y operar máquina local 24/7 (Mac Mini / PC) con Remote Control en el celular |
| [gestionar-sesiones](./gestionar-sesiones/SKILL.md) | Persistir, retomar y estructurar sesiones de Claude Code entre terminal y entornos locales |
| [handoff-claude-design](./handoff-claude-design/SKILL.md) | Importar y convertir diseños de Claude Design en código funcional con Claude Code |
| [gestionar-llm-wiki](./gestionar-llm-wiki/SKILL.md) | Operar y mantener base de conocimiento tipo LLM Wiki (Ingest, Query, Lint, Bulk) |
| [subir-campana-meta-personalizada](./subir-campana-meta-personalizada/SKILL.md) | Subir creativos y campañas a Meta Ads con personalización por país |
| [procesar-transcripcion](./procesar-transcripcion/SKILL.md) | Clasificar e integrar transcripciones crudas (clase, bono, skill) |
| [transcribir-clase-curso](./transcribir-clase-curso/SKILL.md) | Template y reglas de transcripción de clases del curso |
| [sincronizar-estructura-clases](./sincronizar-estructura-clases/SKILL.md) | Sincronizar clases existentes con el template vigente |

---

*Los skills de tus proyectos aparecerán aquí a medida que los crees.*
