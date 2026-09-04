# 🏛️ Imperio Agéntico

Base de conocimiento completa del curso **Claude Code** de Imperio Digital, incluyendo clases, bonos, skills reutilizables y plantillas.

> Documentación estructurada para conectar aprendizajes y construir proyectos reales con IA agéntica.

---

## 📁 Estructura del repositorio

```
imperioagentico/
├── curso-claude-code/          → Módulo principal (16 clases)
│   └── clases/                 → Resumen de cada clase en Markdown
├── bonos/                      → Módulos extra del curso
│   ├── ads-cabrones-ia/        → Pipeline de ads con IA
│   ├── claude-design/          → Prototipado UI y handoff a Claude Code
│   ├── control-remoto/         → Servidor local 24/7 y acceso desde el celular
│   ├── el-espejo/              → Auditoría forense de sesiones y roadmap 30 días
│   ├── gestion-sesiones/       → 5 métodos de sesiones y persistencia
│   ├── go-high-level/          → Integración Claude Code + GHL
│   ├── graphify/               → Mapeo de conocimiento y ahorro de tokens
│   ├── higgsfield/             → Agencia creativa con IA (fotos, video, UGC)
│   ├── meta-ads/               → Agente Ad Manager con Meta API (Matías)
│   ├── motor-agentico/         → Dashboard local de ROI y control
│   └── playwright/             → Automatización de browser
├── skills/                     → Skills reutilizables extraídos del curso (.md)
├── skills-bundle/              → 503 skills listos para usar de Imperio Digital (20 categorías)
└── recursos/plantillas/        → CLAUDE.md global y por proyecto
```

---

## 🗺️ Módulos

### Curso Claude Code — 21 clases

| # | Clase | Temas clave |
|---|-------|-------------|
| 01 | [Ecosistema Anthropic](./curso-claude-code/clases/clase-01-ecosistema.md) | Productos Claude, planes de pricing |
| 02 | [Instalación](./curso-claude-code/clases/clase-02-instalacion.md) | App escritorio, terminal, IDE |
| 03 | [Interfaz & configuración](./curso-claude-code/clases/clase-03-interfaz.md) | Pestaña Code, modelos, razonamiento |
| 04 | [Arquitectura CLAUDE.md](./curso-claude-code/clases/clase-04-arquitectura.md) | Global vs local, memoria persistente |
| 05 | [Skills](./curso-claude-code/clases/clase-05-skills.md) | SOPs reutilizables, estructura SKILL.md |
| 06 | [MCP & conectores](./curso-claude-code/clases/clase-06-mcp.md) | MCP vs API, servidores, autenticación |
| 07 | [Browser & Playwright](./curso-claude-code/clases/clase-07-playwright.md) | Accessibility tree, casos de uso |
| 08 | [Tokens & contexto](./curso-claude-code/clases/clase-08-tokens.md) | Gestión de contexto, compactación |
| 09 | [Permisos & comandos](./curso-claude-code/clases/clase-09-permisos.md) | Modos de sesión, slash commands |
| 10 | [Agentes & subagentes](./curso-claude-code/clases/clase-10-agentes.md) | Ultra como orquestador, paralelismo |
| 11 | [Loops & DAME](./curso-claude-code/clases/clase-11-loops-dame.md) | Framework DAME, objetivos continuos |
| 12 | [Routines, N8N & VPS](./curso-claude-code/clases/clase-12-routines.md) | Automatización, infraestructura |
| 13 | [Segundo cerebro & RAG](./curso-claude-code/clases/clase-13-obsidian.md) | Obsidian, memoria externa |
| 14 | [Proyecto Media Buyer](./curso-claude-code/clases/clase-14-media-buyer.md) | Meta MCP, Hailuo, agente real |
| 15 | [Cierre & siguientes pasos](./curso-claude-code/clases/clase-15-cierre.md) | Freelance, emprendimiento, roadmap |
| 16 | [Resumen final](./curso-claude-code/clases/clase-16-resumen.md) | Mapa completo del ecosistema |
| 17 | [Media Buyer en producción](./curso-claude-code/clases/clase-17-media-buyer-produccion.md) | Personalización por país, research de competencia |
| 18 | [LLM Wiki con Obsidian](./curso-claude-code/clases/clase-18-llm-wiki-obsidian.md) | Memoria infinita sin RAG, Karpathy, 4 operaciones |
| 19 | [Skills en producción](./curso-claude-code/clases/clase-19-skills-en-produccion.md) | Casos reales, meta-skills (Skill Creator) y MCPs |
| 20 | [Masterclass de fundamentos](./curso-claude-code/clases/clase-20-fundamentos-en-vivo.md) | Chat vs Cowork vs Code, demo en vivo, /loop y Q&A |
| 21 | [Framework SMART](./curso-claude-code/clases/clase-21-framework-smart.md) | Metodología integral (Skills, MCP, Artifacts, Refine, Test) |

### Bonos

| Bono | Descripción |
|------|-------------|
| [Ads Cabrones IA](./bonos/ads-cabrones-ia/) | Pipeline automático: Higgsfield + ElevenLabs + Airtable + ffmpeg |
| [Claude Design](./bonos/claude-design/) | Prototipado visual con Opus 4.7 y handoff funcional a Claude Code |
| [Control Remoto](./bonos/control-remoto/) | Tu computador completo en el celular (Mac Mini 24/7 + MCPs) |
| [El Espejo](./bonos/el-espejo/) | Auditoría forense de sesiones con Fable 5 [1M], análisis de hábitos y 4 HTMLs |
| [Gestión de Sesiones](./bonos/gestion-sesiones/) | 5 métodos de persistencia, recuperación y ramificación |
| [Go High Level](./bonos/go-high-level/) | CRM completo desde terminal vía MCP |
| [Graphify](./bonos/graphify/) | Mapeo de conocimiento local, grafo multimodal y reducción de tokens (4.2x) |
| [Higgsfield MCP](./bonos/higgsfield/) | Agencia creativa completa: fotos de producto, video cinematográfico, UGC y thumbnails |
| [Meta Ads 2.0 (Matías)](./bonos/meta-ads/) | Agente Ad Manager con el MCP oficial de Meta (97 herramientas) + Higgsfield |
| [Motor Agéntico](./bonos/motor-agentico/) | Dashboard local de ROI, control de tokens, salud de memoria y El Sueño |
| [Playwright](./bonos/playwright/) | Automatización de browser sin API |

### Skills Bundle

[Imperio Digital Skills Bundle](./skills-bundle/) — 503 skills listos para usar en 20 categorías (Ads, Contenido, Email, Ventas, SEO, Legal, RRHH, y más). Catálogo externo, no pasa por el flujo de transcripción del curso — ver su propio [README](./skills-bundle/README.md) para el detalle y cómo se diferencia de `/skills/`.

---

## ⚡ Inicio rápido

1. Clona el repo: `git clone https://github.com/gmusicproyect/imperioagentico`
2. Navega a la clase que necesites en `curso-claude-code/clases/`
3. Usa las plantillas de `recursos/plantillas/` para nuevos proyectos
4. Copia los skills de `skills/` directamente a tu carpeta de Claude Code
5. Explora `skills-bundle/` para skills listos por categoría de negocio

---

## 🔗 Conexiones entre módulos

```
Clase 01 (Ecosistema) ──→ Bono Claude Design · Clase 20 (Masterclass de Fundamentos)
Clase 04 (CLAUDE.md)  ──→ Clase 05 (Skills) ──→ Skills/
Clase 05 (Skills)     ──→ Clase 19 (Skills en Producción)
Clase 06 (MCP)        ──→ Bono GHL · Bono Higgsfield MCP
Clase 07 (Browser)    ──→ Bono Playwright
Clase 08 (Tokens)     ──→ Bono Motor Agéntico
Clase 09 (Permisos)   ──→ Bono Control Remoto · Bono Gestión de Sesiones
Clase 10 (Agentes)    ──→ Clase 14 (Media Buyer) · Bono El Espejo · Bono Meta Ads
Clase 12 (Routines)   ──→ Bono Ads Cabrones IA
Clase 13 (Obsidian)   ──→ Clase 18 (LLM Wiki) · Bono Graphify
Clase 21 (SMART)      ──→ Clase 05 (Skills) · Clase 06 (MCP) · Clase 11 (DAME)
```

---

*Actualizado: Septiembre 2026 · Imperio Digital · Claude Code*
