# Imperio Digital Skills Bundle — 503 Skills en 20 Categorías

> Descripción oficial de Imperio Digital, adaptada a este repo. **No es contenido del curso ni pasó por el flujo de `procesar-transcripcion`** — son skills ya redactados y listos para usar, entregados como bundle.

Cada skill convierte a Claude en un especialista para una tarea específica de tu negocio digital: marketing, ventas, contenido, operaciones, finanzas, legal y más. 100% en español, listo para usar. No es un curso ni una lista de prompts sueltos — es un arsenal de procesos profesionales "battle-tested", con fases claras, checkpoints de validación y templates listos.

## Qué incluye cada skill

- **Metadata** (nombre, descripción, autor)
- **Cuándo Usar** — situaciones exactas donde aplica
- **Principio Fundamental** — la idea clave detrás
- **Fases de Trabajo** — proceso paso a paso
- **Puntos de Control** — validaciones antes de continuar (no te los saltees, son el mecanismo de calidad)
- **Templates** — plantillas listas para usar
- **Anti-Patrones** — qué NO hacer
- **Recuperación** — cómo salir de problemas si algo se tuerce
- **`casos-de-uso.txt`** (archivo aparte) — 5-6 ejemplos prácticos de aplicación

## En qué se diferencia de `/skills/`

| | `/skills/` (raíz del repo) | `/skills-bundle/` (esta carpeta) |
|---|---|---|
| Origen | Extraídos de las clases y bonos de este curso | Bundle externo de Imperio Digital |
| Formato | Plantilla propia del repo | Formato del bundle: YAML + Fases + Anti-Patrones + Recuperación |
| Cantidad | ~17, específicos a los flujos enseñados aquí | 503, catálogo general de negocio |
| Cómo se usa | Referenciados en tu `CLAUDE.md` de proyecto | Adjuntar el `.md` directo en Claude |

## Estructura

```
skills-bundle/
├── GUIA-INICIO-RAPIDO.txt      → Guía original de uso, ejemplos, FAQ
├── DIRECTORIO-SKILLS.pdf       → Índice completo de los 503 skills
├── [20 categorías]/            → Carpeta por skill: nombre/nombre.md + casos-de-uso.txt
└── Páginas Skool/              → Copys de página por categoría (contenido de comunidad, no skills)
```

## Las 20 categorías (conteo verificado contra los archivos entregados)

| Categoría | Skills | Cubre |
|-----------|--------|-------|
| Contenido y Copywriting | 56 | Blog, copy, guiones, headlines, email |
| Email Marketing y Automatización | 42 | Secuencias, automatización, newsletters, engagement |
| Redes Sociales | 38 | Estrategia, calendario, community management, viralidad |
| Ventas y Embudos | 31 | Funnels, propuestas, high ticket, objeciones, cierre |
| Legal y Cumplimiento | 30 | Contratos, políticas, compliance, términos |
| Operaciones y Sistemas | 30 | SOPs, procesos, automatización, workflows |
| RRHH y Equipo | 29 | Reclutamiento, cultura, evaluaciones, retención |
| Finanzas y Precios | 28 | Modelos financieros, pricing, ROI, forecasting |
| Branding y Diseño | 24 | Identidad visual, voz de marca, naming, estrategia |
| E-commerce y Productos | 24 | Descripciones, lanzamientos, bundles, upsells |
| Eventos y Oratoria | 24 | Webinars, conferencias, lanzamientos, presentaciones |
| Lanzamiento y Crecimiento | 24 | Go-to-market, onboarding, NPS, virality |
| Ads y Medios Pagados | 22 | Campañas, copy de ads, retargeting, A/B testing |
| Analítica y Datos | 22 | Dashboards, KPIs, análisis de conversión, reportes |
| Cursos y Educación | 20 | Diseño de cursos, webinars, talleres, estructura |
| SEO y Búsqueda | 20 | Keywords, auditoría técnica, contenido SEO, clustering |
| Cliente y Consultoría | 18 | Onboarding, propuestas, coaching, follow-up |
| Industrias Específicas | 15 | SaaS, restaurantes, plataformas, verticales |
| IA y Tecnología | 4 | Automatización e integración de IA en tu infraestructura |
| ONG y Comunidad | 2 | Recaudación, impacto social, voluntariado |

*Nota: la página oficial de Imperio Digital indica 504 skills / 57 en Contenido y Copywriting; el conteo real de archivos entregados en este bundle da 503 / 56. Diferencia de 1, sin impacto práctico.*

## Cómo usar un skill

1. Elegí la categoría según lo que necesitás resolver (ver `GUIA-INICIO-RAPIDO.txt` para el mapa por rol: fundador, marketer, operaciones, ventas, producto).
2. Abrí la carpeta del skill que te sirve.
3. Adjuntá el archivo `.md` directo en Claude (claude.ai, Cowork o Code) junto con tu contexto específico.
4. Claude lo lee automáticamente y te guía fase por fase — respondé lo que te pida y respetá los **Puntos de Control**.
5. Resultado esperado: 20-45 minutos por skill, sin necesitar experiencia previa.

### Combinar skills

Podés usar varios skills en un mismo proyecto — ej. para un funnel de webinar: `lead-magnet` (Ventas y Embudos) → secuencia de email (Email Marketing) → landing page (Contenido y Copywriting). Podés adjuntar más de un `.md` a la vez en Claude para proyectos complejos.

### Personalización

Los skills no son inamovibles: editá el `.md` para ajustar tono, agregar campos a las tablas de inputs, o adaptar los templates a tu voz.
