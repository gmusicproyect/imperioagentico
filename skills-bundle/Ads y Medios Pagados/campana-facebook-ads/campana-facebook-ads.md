---
name: campana-facebook-ads
description: "Planifica campañas de Facebook/Meta ad con targeting de audiencia, briefs de creative de ad, asignación de presupuesto y estrategia de pruebas. Úsalo cuando ejecutes ads pagados en plataformas Meta."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Campaña de Anuncios en Facebook

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Planificar campaña de Facebook o Instagram advertising de cero
- Definir targeting de audiencia, creative de ad y asignación de presupuesto
- Construir estrategia de pruebas para ad sets, audiencias y creatives
- Crear copy de ad y briefs de creative para múltiples variaciones de ad

---

## Principio Fundamental

LOS FACEBOOK ADS RENTABLES SE CONSTRUYEN EN TRES PILARES: LA AUDIENCIA CORRECTA, UNA OFERTA CONVINCENTE, Y CREATIVE QUE DETIENE EL SCROLL — CONSIGUE LOS TRES CORRECTOS Y EL ALGORITMO HACE EL RESTO.

---

## Fase 1: Brief de Campaña

### Inputs Requeridos

| Input | Qué Preguntar | Default |
|-------|---------------|---------|
| **Objetivo de campaña** | "¿Cuál es el objetivo? (leads, ventas, tráfico, conciencia)" | Sin default — debe ser proporcionado |
| **Oferta** | "¿Qué estás promocionando?" | Sin default — debe ser proporcionado |
| **Landing page** | "¿Dónde envía el ad a las personas?" | Sin default — debe ser proporcionado |
| **Presupuesto** | "¿Cuál es tu presupuesto diario o mensual?" | $20-50/día |
| **Audiencia destino** | "¿Quién es tu cliente ideal?" | Sin default — debe ser proporcionado |
| **Experiencia previa** | "¿Has ejecutado Meta ads antes?" | Sin datos previos |

---

## Fase 2: Arquitectura de Campaña

### Estructura de Campaña

```
## Setup de Campaña

**Nivel de Campaña:**
- Objetivo: [Conversiones / Leads / Tráfico]
- Campaign Budget Optimization: ON
- Presupuesto diario: $[X]

**Ad Set 1: Targeting Basado en Intereses**
- Audiencia: [Targets de interés]
- Edad: [Rango]
- Ubicación: [Países/regiones]
- Budget: 40%

**Ad Set 2: Lookalike Audience** (si datos disponibles)
- Budget: 40%

**Ad Set 3: Retargeting**
- Visitantes de sitio (últimos 30 días) + engaged (últimos 90 días)
- Budget: 20%
```

---

## Fase 3: Creative de Ad

### Variaciones de Copy de Ad (3-5 por ad set)

**Ángulo 1: Problema-Agitar**
- Headline: [Beneficio u outcome]
- Texto primario: [Hook de pain point. Agita. Introduce solución. CTA.]
- Descripción: [Beneficio complementario]
- Botón CTA: [Aprende Más / Registrate / Compra Ahora]

**Ángulo 2: Social Proof**
- Headline: [Resultado o testimonial]
- Texto: ["Cita de cliente." Contexto. CTA.]

**Ángulo 3: Beneficio Directo**
- Headline: [Afirmación clara de oferta]
- Texto: [Qué obtienes. Por qué importa. Cómo obtenerlo.]

---

## Fase 4: Pulido

### Plan de Pruebas

**Semana 1-2: Pruebas de Creative**
- Prueba 3-5 copy de ads uno contra otro
- Misma audiencia, different creative
- Ganador = costo más bajo por resultado

**Semana 3-4: Pruebas de Audiencia**
- Toma creative ganador
- Prueba en diferentes segmentos de audiencia
- Ganador = mejor ROAS o CPA más bajo

**Continuo: Escala Ganadores**
- Aumenta presupuesto 20-30% cada 3-4 días en ganadores
- Mata bajo-desempeño (2x target CPA después de $20+ gastados)
- Introduce creative nuevo cada 2 semanas para combatir fatiga

---

## Anti-Patrones

- **Boosting posts en lugar de ejecutar campañas** — Ads Manager da targeting, pruebas y optimización que Boost no tiene
- **Un ad, una audiencia, un creative** — necesitas variaciones para probar. Comienza con 3-5 creatives mínimo
- **Matar ads demasiado temprano** — da cada ad $20-50 en gasto antes de juzgar
- **Targeting demasiado estrecho** — audiencias bajo 100K a menudo son muy pequeñas para algoritmo Meta
- **Sin retargeting** — audiencias warm (visitantes de sitio, viewers de video) convierten a 3-5x tasa de audiencias frías
- **Ignorar fatiga de creative** — cuando frecuencia excede 3 y CTR cae, tu audiencia ha visto el ad demasiadas veces

---

## Recuperación

- **Sin datos de pixel o lista de clientes:** Comienza solo con targeting basado en intereses. Construye audiencias de retargeting ejecutando campañas de tráfico primero.
- **Presupuesto bajo $10/día:** Enfócate en un ad set con 2-3 variaciones de creative. Pruebas limitadas a presupuestos bajos.
- **CPC alto/CTR bajo:** El creative no está deteniendo el scroll. Prueba nuevos hooks, imágenes, o formatos de video.
- **Buen CTR pero sin conversiones:** La landing page es el problema, no el ad.
- **Cuenta de ad restringida:** Revisa políticas de Meta, apela si apropiado, asegura compliance de landing pages.
