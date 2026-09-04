---
name: campana-linkedin-ads
description: "Planifica campañas de LinkedIn ad con targeting de audiencia, formatos de ad, diseño de lead gen form, y recomendaciones de presupuesto. Úsalo cuando ejecutes campañas de publicidad B2B en LinkedIn."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Campaña de Anuncios en LinkedIn

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Planificar campaña de LinkedIn advertising de targeting a creative
- Diseñar campañas de lead gen form para generación de leads B2B
- Seleccionar formatos correctos de ad para objetivo de negocio
- Crear estrategia de presupuesto y pujas para ads de LinkedIn

---

## Principio Fundamental

LOS LINKEDIN ADS SON CAROS POR CLIC — CADA CAMPAÑA DEBE APUNTAR A UN DECISION-MAKER ESPECÍFICO CON OFERTA ESPECÍFICA QUE VALGA EL CPM PREMIUM.

---

## Fase 1: Brief de Campaña

### Inputs Requeridos

| Input | Qué Preguntar | Default |
|-------|---------------|---------|
| **Objetivo de campaña** | "¿Cuál es el objetivo? (lead gen, tráfico, conciencia de marca, registros de evento)" | Generación de leads |
| **Audiencia destino** | "¿A quién diriges? (títulos, industrias, tamaños de empresa)" | Sin default — debe ser proporcionado |
| **Oferta** | "¿Qué estás ofreciendo?" | Sin default — debe ser proporcionado |
| **Presupuesto mensual** | "¿Cuál es tu presupuesto mensual de LinkedIn?" | $3,000/mes |
| **Objetivos geográficos** | "¿Qué regiones?" | Estados Unidos |
| **Landing page o lead gen form** | "¿Landing page o LinkedIn native lead gen forms?" | LinkedIn lead gen forms |

---

## Fase 2: Construir Audiencia

### Capas de Targeting

Construye 2-3 segmentos de audiencia para probar:

```
## Segmento de Audiencia 1: [Nombre]
- Job Titles: [Títulos específicos]
- Industries: [Industrias]
- Company Size: [Rangos de empleados]
- Seniority: [Entrada, Senior, Manager, Director, VP, C-Suite]
- Tamaño de audiencia estimado: [Target 50,000-500,000]

## Segmento de Audiencia 2: [Nombre]
- [Combinación de targeting diferente]
```

### Mejores Prácticas de Targeting

- Rango de tamaño de audiencia ideal: 50,000-500,000 para lead gen
- No apiles más de 3 dimensiones de targeting — audiencias demasiado estrechas suben CPM
- Usa exclusiones: competidores, clientes actuales, job seekers
- Matched Audiences: carga listas de clientes para exclusión o lookalikes

---

## Fase 3: Construir Campaña

### Selección de Formato de Ad

| Formato | Mejor Para | Avg CPC |
|---------|----------|---------|
| Single Image | Lead gen, tráfico | $5-12 |
| Carousel | Multi-feature showcase | $4-10 |
| Video | Brand awareness, demos | $6-15 |
| Document | Thought leadership | $3-8 |
| Message/InMail | Ofertas alto-valor, eventos | $0.50-1.00/envío |

### Framework de Copy de Ad

```
## Variación de Ad [A/B/C]

**Formato:** Single Image
**Headline (70 chars máx):** [Headline orientado a beneficio]
**Descripción (100 chars máx):** [Detalle complementario]
**Intro text (600 chars máx):**
[Hook — pregunta o afirmación audaz]
[Reconocimiento del problema — 1-2 oraciones]
[Solución — qué obtienen]
[CTA — paso claro siguiente]

**Botón CTA:** [Descarga / Aprende Más / Registrate]
**Specs de imagen:** 1200x627px, texto minimal en overlay
```

### Diseño de Lead Gen Form (si aplica)

```
## Form de Lead Gen

**Nombre del form:** [Nombre descriptivo]
**Headline (60 chars):** [Value proposition]
**Descripción (160 chars):** [Qué obtienen + urgencia]
**Campos:**
1. Nombre (pre-rellenado)
2. Apellido (pre-rellenado)
3. Email laboral (pre-rellenado)
4. Nombre de empresa (pre-rellenado)
5. [1 pregunta custom máx — mantén fricción baja]
```

---

## Fase 4: Presupuesto y Launch Plan

### Asignación de Presupuesto

```
## Plan de Presupuesto

**Presupuesto mensual:** $[monto]
**Duración de campaña:** [Continuo / Fechas fijas]

### Asignación
- Fase de prueba (Semana 1-2): $[monto] en [X] variaciones de ad
- Optimización (Semana 3-4): Desplaza presupuesto al ganador superior
- Escala (Mes 2+): Aumenta presupuesto diario en combinaciones ganadoras

### Estrategia de Pujas
- Objetivo: Maximum delivery (recomendado para pruebas)
- Cambia a: Target cost después de 50+ conversiones
- Target CPL: $[monto basado en valor de oferta]

### Targets de KPI
| Métrica | Target |
|---------|--------|
| CTR | >0.4% |
| CPL | <$[monto] |
| Lead form completion rate | >10% |
```

---

## Anti-Patrones

- **Targeting demasiado amplio** — "todos los marketers en USA" desperdicia presupuesto
- **Demasiados campos de form** — cada campo arriba de 4 cae tasa de finalización significativamente
- **Ejecutar una variación de ad** — siempre lanza 3-4 variaciones para identificar copy y creative ganador
- **Usar "Aprende Más" para todo** — match el botón CTA a la acción
- **Ignorar la oferta** — usuarios de LinkedIn esperan valor a cambio de info

---

## Recuperación

- **Presupuesto bajo $1,500/mes:** Enfócate en un segmento de audiencia y un formato de ad. LinkedIn requiere presupuestos diarios mínimos.
- **Sin lead magnet u oferta:** Ayuda al usuario identificar activo valioso antes de construir campaña.
- **Audiencia demasiado pequeña (<20,000):** Amplía una dimensión de targeting. Expande de títulos exactos a funciones de trabajo o rango de tamaño de empresa.
- **Sin LinkedIn Company Page:** Una Company Page es requerida. Ayuda al usuario a configurar una antes de proceder.
