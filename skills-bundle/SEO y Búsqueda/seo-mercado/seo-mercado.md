---
name: seo-mercado
description: Planifica estrategias de SEO para plataformas marketplace con optimización de páginas de categoría, schema de reseñas y enlazado interno. Usa cuando impulses tráfico orgánico a un marketplace.
allowed-tools: Read Write Glob
author: Imperio Digital
version: "1.0"
---

# SEO de Marketplace

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Planificar una estrategia de SEO para un marketplace o plataforma con muchas páginas de listado
- Optimizar páginas de categoría y páginas de listado para búsqueda orgánica
- Implementar datos estructurados (schema markup) para reseñas y productos
- Construir estructuras de enlazado interno que se escalen con el crecimiento del marketplace

**NO** uses este skill para SEO de comercio electrónico de producto único, estrategia de marketing de contenido o auditorías técnicas de SEO. Esto es para estrategia de SEO específica de marketplace.

---

## Principio Fundamental

EL SEO DE MARKETPLACE ES UN JUEGO DE ESCALA — NO ESTÁS OPTIMIZANDO UNA PÁGINA, ESTÁS CONSTRUYENDO PLANTILLAS Y ESTRUCTURAS QUE HACEN QUE MILES DE PÁGINAS RANKEN. LAS PÁGINAS DE CATEGORÍA SON TU ACTIVO DE SEO MÁS VALIOSO.

---

## Fase 1: Briefing

### Información Requerida

| Input | Qué Preguntar | Por Defecto |
|-------|------------|---------|
| **Tipo de marketplace** | "¿Qué vende tu marketplace o conecta?" | Sin defecto — debe proporcionarse |
| **Alcance geográfico** | "¿Local, regional, nacional o global?" | Nacional |
| **Número de listados** | "¿Cuántos listados activos tienes?" | Menos de 500 |
| **Tráfico orgánico actual** | "¿Cuánto tráfico de búsqueda orgánica recibes mensualmente?" | Desconocido |
| **Categorías principales** | "¿Cuáles son tus principales categorías de listado?" | Sin defecto — debe proporcionarse |
| **Competidores en búsqueda** | "¿Quién rankea para las palabras clave que quieres?" | Sin defecto — identifica 3 competidores |

**PUNTO DE CONTROL: Confirma el briefing antes de construir la estrategia.**

---

## Fase 2: Estrategia de Palabras Clave

### Mapeo de Palabras Clave por Tipo de Página

| Tipo de Página | Patrón de Palabra Clave | Ejemplo |
|-----------|----------------|---------|
| **Homepage** | Brand + categoría primaria | "[Plataforma]: Find [categoría] near you" |
| **Páginas de categoría** | [Categoría] + [ubicación/modificador] | "diseñadores freelance en Madrid" |
| **Páginas de sub-categoría** | [Servicio/producto específico] + [modificador] | "diseño de logo para startups" |
| **Páginas de listado** | [Oferta específica] + [nombre del vendedor] | Long-tail, único por listado |
| **Blog/guías** | Palabras clave de intención informacional | "cómo contratar un diseñador freelance" |

### Prioridad de Página de Categoría

Clasifica categorías por:
1. Volumen de búsqueda (búsquedas mensuales para palabra clave de categoría)
2. Competencia (qué tan difícil rankear)
3. Intención comercial (probabilidad de transacción)
4. Densidad de listado (¿tienes suficiente oferta para servir la consulta?)

Enfócate en esfuerzos de SEO en categorías donde tienes oferta fuerte Y demanda de búsqueda.

**PUNTO DE CONTROL: Confirma objetivos de palabras clave y categorías de prioridad antes de escribir planes de optimización.**

---

## Fase 3: Optimizar

### Plantilla de Página de Categoría

Cada página de categoría debe incluir:
- **H1:** Palabra clave de categoría expresada naturalmente
- **Párrafo introductorio (100-150 palabras):** Qué ofrece la categoría, por qué los usuarios deberían explorar aquí
- **Filtros y ordenamiento:** Visible y funcional (buscadores indexan combinaciones de filtro)
- **Tarjetas de listado:** Título, imagen, precio/tarifa, calificación, ubicación
- **Enlaces internos:** Categorías relacionadas y sub-categorías populares
- **Contenido generado por usuarios:** Resumen de reseñas, Q&A si aplica
- **Schema markup:** ItemList para la colección de listados

### Optimización de Página de Listado

- **Fórmula de title tag:** [Título de listado] | [Categoría] | [Nombre de plataforma]
- **Meta descripción:** Auto-generada desde descripción de listado (primeros 155 caracteres)
- **H1:** Título de listado (único, descriptivo)
- **Datos estructurados:** Product, Service o LocalBusiness schema con reseñas
- **Enlaces internos:** Breadcrumbs (Home > Categoría > Sub-categoría > Listado)
- **Listados relacionados:** Sección "Similar [categoría]" para enlazado cruzado

### Recomendaciones de Schema Markup

```
Páginas de categoría: Schema ItemList
Páginas de listado: Schema Product o Service con AggregateRating
Páginas de reseña: Schema Review con autor y calificación
Listados locales: Schema LocalBusiness con coordenadas geo
```

### Estrategia de Enlazado Interno

- **Breadcrumbs:** Cada listado enlaza de regreso a través de jerarquía de categoría
- **Listados relacionados:** Enlaza cruzada listados similares al pie de cada página
- **Enlazado cruzado de categorías:** Enlaza categorías relacionadas desde cada página de categoría
- **Enlaces de pie de página:** Categorías principales enlazadas en todo el sitio
- **Blog a enlaces de categoría:** Páginas de contenido enlazan a páginas de categoría relevantes

### Estrategia de Contenido para SEO

Crea contenido de apoyo que impulse tráfico orgánico a páginas de categoría:
- "Cómo contratar un [profesional de categoría]" → enlaza a página de categoría
- "¿Cuánto cuesta [servicio] en [año]?" → enlaza a página de categoría con datos de precio
- "[X] mejor [categoría] para [caso de uso]" → enlaza a listados individuales
- Guías de comprador, artículos de comparación y contenido cómo hacerlo

---

## Fase 4: Pulir

### 1. Lista de Verificación Técnica de SEO

```
## SEO Técnico de Marketplace

- [ ] Las páginas de categoría tienen title tags y meta descripciones únicos
- [ ] Las páginas de listado generan meta descripciones únicas desde contenido
- [ ] Navegación de breadcrumb está implementada y es visible
- [ ] Schema markup es válido (prueba con Google Rich Results Test)
- [ ] Paginación usa rel="next" y rel="prev" (o scroll infinito con enlaces rastreables)
- [ ] Las páginas de listado duplicadas están canonicalizadas
- [ ] Las combinaciones de filtro que crean páginas delgadas están noindexadas
- [ ] El mapa de sitio XML incluye todas las páginas de categoría y listado
- [ ] La velocidad de carga es menor a 3 segundos (especialmente páginas de categoría)
- [ ] La experiencia móvil es completamente responsive
```

### 2. Métricas de SEO a Rastrear

| Métrica | Herramienta | Frecuencia |
|--------|------|-----------|
| Tráfico orgánico por tipo de página | Google Analytics | Semanal |
| Rankings de palabras clave para páginas de categoría | Ahrefs/SEMrush | Semanal |
| Páginas indexadas | Google Search Console | Mensual |
| Tasa de clics por tipo de página | Google Search Console | Mensual |
| Backlinks adquiridos | Ahrefs | Mensual |

### 3. Lista de Verificación de Calidad

```
## Lista de Verificación de SEO de Marketplace

- [ ] Objetivos de palabras clave mapeados a cada tipo de página
- [ ] Top 10 páginas de categoría optimizadas con H1, intro y schema
- [ ] Fórmula de title tag aplicada en todos los tipos de página
- [ ] Estructura de enlazado interno conecta listados → categorías → homepage
- [ ] Estrategia de contenido soporta 3-5 palabras clave informacionales por trimestre
- [ ] Schema markup implementado para listados y reseñas
- [ ] Problemas de SEO técnico resueltos (duplicados, contenido delgado, velocidad)
- [ ] Mapa de sitio XML enviado y actualizándose automáticamente
- [ ] Métricas de SEO rastreadas semanalmente/mensualmente
- [ ] Rankings de competidores monitoreados para palabras clave de prioridad
```

---

## Ejemplo

**Marketplace:** Servicios de diseño freelance, nacional

**Title de página de categoría:** "Diseñadores Freelance de Logo — Encuentra un Diseñador | [Plataforma]"
**H1 de categoría:** "Diseñadores Freelance de Logo"
**Extracto de intro:** "Explora 120+ diseñadores freelance de logo listos para traer tu marca a la vida. Filtra por estilo, presupuesto y tiempo de entrega. Cada diseñador está verificado y cada proyecto está cubierto por nuestra garantía de satisfacción."

**Contenido de blog apoyando SEO:**
- "¿Cuánto Cuesta Diseño de Logo en 2026?" → enlaza a categoría de diseño de logo
- "Cómo Escribir un Brief de Diseño para un Freelancer" → enlaza a múltiples categorías de diseño

---

## Anti-Patrones

- **Ignorar páginas de categoría** — las páginas de categoría rankean para palabras clave de alto volumen. Los listados individuales rankean para long-tail. Ambos importan, pero las categorías impulsan la mayoría del tráfico.
- **Title tags duplicados** — cada listado generando "Producto | [Plataforma]" como título destruye SEO. Haz los títulos únicos.
- **Páginas de categoría delgadas** — una página de categoría con solo una cuadrícula de listados y sin texto lucharará para rankear. Añade contenido intro, filtros y enlaces internos.
- **Sin schema markup** — los resultados enriquecidos (estrellas, precios, disponibilidad) mejoran dramáticamente las tasas de clics. Implementa schema temprano.
- **Indexando cada combinación de filtro** — "color=blue&size=large&price=low" crea millones de páginas delgadas. Noindex URLs de filtro no esenciales.

---

## Recuperación

- **Muy pocos listados:** Enfócate en SEO impulsado por contenido (blog y guías) hasta que el volumen de listado soporte páginas de categoría fuertes.
- **Compitiendo contra marketplaces masivos:** Apunta a palabras clave long-tail y locales donde los grandes competidores son débiles.
- **Contenido duplicado en listados:** Requiere descripciones únicas de vendedores. Proporciona plantillas que producen output único.
- **Sin experiencia en SEO técnico:** Comienza con optimización de páginas de categoría (titles, H1s, intros) y schema markup. Estos tienen el ROI más alto para esfuerzo.
