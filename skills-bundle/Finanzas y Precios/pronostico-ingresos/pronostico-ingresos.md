---
name: pronostico-ingresos
description: "Proyecta ingresos con múltiples escenarios usando datos históricos y factores de mercado. Úsalo cuando necesites pronosticar ingresos futuros para planificación o reportes."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Pronóstico de Ingresos

## Cuándo usar esta habilidad

Usa esta habilidad cuando necesites:
- Proyectar ingresos para los próximos 3, 6 o 12 meses
- Crear escenarios de ingresos conservador, base y optimista
- Pronosticar ingresos por línea de producto, canal o segmento de cliente
- Construir un plan de ingresos respaldado por datos para presupuestación o comunicaciones con inversionistas

**NO** uses esta habilidad para modelos financieros completos (usa modelo-financiero), pronósticos de gastos o decisiones de precios. Esto está enfocado específicamente en proyección de ingresos.

---

## Principio Central

UN PRONÓSTICO DE INGRESOS ES UN RANGO, NO UN NÚMERO — PRESENTA TRES ESCENARIOS E IDENTIFICA CUÁLES SUPUESTOS LOS SEPARAN.

---

## Fase 1: Datos Históricos

### Entradas Requeridas

| Entrada | Qué Preguntar | Predeterminado |
|---------|--------------|----------------|
| **Ingresos mensuales (últimos 6-12 meses)** | "Comparte tus ingresos mensuales para los últimos 6-12 meses." | Sin predeterminado — debe proporcionarse |
| **Flujos de ingresos** | "¿Cómo generas ingresos? (productos, servicios, suscripciones, única vez)" | Sin predeterminado — debe proporcionarse |
| **Estacionalidad** | "¿Hay patrones estacionales en tus ingresos?" | Sin estacionalidad conocida |
| **Generadores de crecimiento** | "¿Qué impulsa el crecimiento? (marketing, referidos, nuevos productos, expansión)" | Crecimiento orgánico |
| **Cambios planeados** | "¿Algún cambio próximo? (lanzamiento de nuevo producto, aumento de precio, nuevo canal)" | Ninguno planeado |
| **Período de pronóstico** | "¿Cuánto adelante? (3, 6 o 12 meses)" | 12 meses |

**PUNTO DE CONTROL: No continúes sin al menos 3 meses de datos de ingresos históricos.**

---

## Fase 2: Análisis de Tendencias

### Desempeño Histórico

```
## Análisis de Ingresos

### Historial de Ingresos Mensuales
| Mes | Ingresos | Cambio MM | Cambio Interanual |
|-----|----------|-----------|-------------------|
| [Mes] | $[X] | +/-[X]% | +/-[X]% |
| ... | | | |

### Métricas Clave
| Métrica | Valor |
|---------|-------|
| Ingresos mensuales promedio (últimos 6 meses) | $[X] |
| Tasa de crecimiento mensual promedio | [X]% |
| Tendencia de ingresos | Crecimiento / Plano / Declive |
| Mes más alto | $[X] ([Mes]) |
| Mes más bajo | $[X] ([Mes]) |
| Volatilidad de ingresos (desviación estándar) | $[X] |
```

### Ingresos por Flujo

```
### Desglose de Ingresos por Flujo
| Flujo | Promedio Mensual | % Total | Tasa de Crecimiento | Tendencia |
|-------|-----------------|---------|---------------------|-----------|
| [Flujo 1] | $[X] | [X]% | [X]% | ↑↓→ |
| [Flujo 2] | $[X] | [X]% | [X]% | ↑↓→ |
```

---

## Fase 3: Modelo de Pronóstico

### Tres Escenarios

```
## Pronóstico de Ingresos: [Período]

### Supuestos

| Factor | Conservador | Base | Optimista |
|--------|------------|------|-----------|
| Tasa de crecimiento mensual | [X]% | [X]% | [X]% |
| Ingresos de nuevo flujo | $0 | $[X] | $[X] |
| Ajuste estacional | Sí | Sí | Sí |
| Impacto de cambio de precio | Ninguno | Ninguno | +[X]% |
| Factor de churn/pérdida | [X]% | [X]% | [X]% |

### Pronóstico Mensual

| Mes | Conservador | Base | Optimista |
|-----|------------|------|-----------|
| M1 | $[X] | $[X] | $[X] |
| M2 | $[X] | $[X] | $[X] |
| ... | | | |
| M12 | $[X] | $[X] | $[X] |
| **Total** | **$[X]** | **$[X]** | **$[X]** |

### Pronóstico por Flujo de Ingresos (Caso Base)

| Mes | [Flujo 1] | [Flujo 2] | [Flujo 3] | Total |
|-----|-----------|-----------|-----------|-------|
| M1 | $[X] | $[X] | $[X] | $[X] |
| ... | | | | |
```

### Generadores Clave y Riesgos

```
### Qué Separa los Escenarios

**Conservador → Base:** [Diferencia de supuesto clave, ej., "Asume que el nuevo canal de marketing se lanza a tiempo y produce 20 leads/mes en M3"]

**Base → Optimista:** [Diferencia de supuesto clave, ej., "Asume que el trato empresarial se cierra en Q2 añadiendo $5K/mes recurrentes"]

### Riesgos a la Baja
1. [Riesgo] — Impacto: -$[X]/mes — Probabilidad: [Alto/Medio/Bajo]
2. [Riesgo] — Impacto: -$[X]/mes — Probabilidad: [Alto/Medio/Bajo]

### Oportunidades al Alza
1. [Oportunidad] — Impacto: +$[X]/mes — Probabilidad: [Alto/Medio/Bajo]
```

---

## Fase 4: Entregable

```
## Resumen del Pronóstico

**Período de pronóstico:** [X] meses
**Ingresos anuales conservador:** $[X]
**Ingresos caso base:** $[X]
**Ingresos optimista:** $[X]

**Recomendación de planificación:** Presupuesta contra el escenario conservador.
Apunta al caso base. Celebra si alcanzas optimista.

pronóstico/
└── pronóstico-ingresos-[AAAA].md
```

---

## Ejemplo: Negocio de Consultoría ($15K/mes Promedio)

**Historial:** 6 meses de datos, rango $12K-$18K, promedio $15K, 4% crecimiento mensual impulsado por referidos.

**Pronóstico (12 meses):** Conservador $14.5K prom (plano), Base $17.8K prom (4% crecimiento), Optimista $21K prom (7% crecimiento de agregar nuevo servicio). Totales anuales: Conservador $174K, Base $214K, Optimista $252K.

**Generador clave:** El caso base asume mantener tasa de referidos actual. Optimista asume lanzar programa de coaching grupal en M4 añadiendo $3K/mes.

---

## Anti-patrones

- **Proyecciones de línea recta** — los ingresos rara vez crecen en línea recta. Contabiliza estacionalidad, períodos de rampa y mesetas.
- **Pronósticos de número único** — siempre proporciona un rango. Un número único es una mentira o una adivinanza.
- **Ignorar churn y cancelaciones** — si tienes ingresos recurrentes, modela churn. Ingresos nuevos brutos menos churn equivale crecimiento de ingresos neto.
- **Pronósticos sin identificar generadores** — "los ingresos crecerán 10%" no es un pronóstico. "10 nuevos clientes a $1,500/mes de LinkedIn ads" es un pronóstico.
- **Sesgo de sobre-optimismo** — la mayoría de founders pronostican 2-3x lo que realmente ocurre. Usa tasas de crecimiento históricas como base, no objetivos aspiracionales.

---

## Recuperación

- **Menos de 3 meses de datos:** Usa benchmarks de industria y etiqueta claramente el pronóstico como preliminar. Actualiza mensualmente conforme datos se acumulan.
- **Ingresos altamente variables:** Enfócate en promedios finales más que tasas de crecimiento mes a mes. Amplía la brecha entre escenarios conservador y optimista.
- **Nuevo flujo de ingresos sin datos:** Modélalo por separado con una rampa conservadora. No lo incluyas en el caso base hasta que tengas 2-3 meses de datos reales.
- **Ingresos en declive:** Reconoce la tendencia. Modela escenarios para estabilización y recuperación. Identifica cuáles acciones cambian la trayectoria.
