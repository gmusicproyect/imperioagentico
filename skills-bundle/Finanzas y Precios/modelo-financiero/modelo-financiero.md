---
name: modelo-financiero
description: "Construye modelos financieros para startups con generadores de ingresos, supuestos de costos y análisis de sensibilidad. Úsalo cuando crees modelos financieros detallados para recaudación de fondos o planificación."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Modelo Financiero

## Cuándo usar esta habilidad

Usa esta habilidad cuando necesites:
- Construir un modelo financiero de abajo hacia arriba para una startup o pequeña empresa
- Crear proyecciones financieras listas para inversionistas con supuestos detallados
- Modelar generadores de ingresos, economía unitaria y flujo de caja
- Ejecutar análisis de sensibilidad en supuestos comerciales clave

**NO** uses esta habilidad para presupuestos simples (usa planificador-presupuesto) ni para pronósticos básicos de ingresos (usa pronóstico-ingresos). Esto es para modelos financieros completos con múltiples supuestos interconectados.

---

## Principio Central

UN MODELO FINANCIERO ES SOLO TAN BUENO COMO SUS SUPUESTOS — CADA NÚMERO DEBE RASTREARSE HASTA UN SUPUESTO ESTABLECIDO QUE PUEDA SER CUESTIONADO, PROBADO Y ACTUALIZADO.

---

## Fase 1: Entradas del Modelo

### Entradas Requeridas

| Entrada | Qué Preguntar | Predeterminado |
|---------|--------------|----------------|
| **Modelo de negocio** | "¿Cómo haces dinero? (SaaS, e-commerce, servicios, marketplace)" | Sin predeterminado — debe proporcionarse |
| **Flujos de ingresos** | "¿Cuáles son tus fuentes de ingresos y precios?" | Sin predeterminado — debe proporcionarse |
| **Métricas actuales** | "¿MRR, usuarios, tasas de conversión, churn actuales?" | Pre-ingresos si no se proporciona |
| **Estructura de costos** | "¿Costos fijos, costos variables, contrataciones planeadas?" | Se construirá desde cero |
| **Plazo del modelo** | "¿12, 24 o 36 meses?" | 24 meses |
| **Propósito del modelo** | "¿Para quién es esto? (planificación interna, seed, Series A)" | Planificación interna |

**PUNTO DE CONTROL: No continúes sin detalles del modelo de negocio y flujos de ingresos.**

---

## Fase 2: Hoja de Supuestos

Todo modelo comienza con una hoja de supuestos documentada.

```
## Supuestos Clave

### Supuestos de Ingresos
| Supuesto | Valor | Fuente/Justificación |
|----------|-------|---------------------|
| MRR inicial | $[X] | Actual |
| Tasa de crecimiento mensual de usuarios | [X]% | [Basado en: histórico, benchmark o objetivo] |
| Tasa de conversión (prueba a pagado) | [X]% | [Fuente] |
| Ingresos promedio por usuario (ARPU) | $[X] | [Precios actuales] |
| Tasa de churn mensual | [X]% | [Histórico o benchmark de industria] |
| Tasa de ingresos de expansión | [X]% | [Estimación de upsell/cross-sell] |

### Supuestos de Costos
| Supuesto | Valor | Fuente/Justificación |
|----------|-------|---------------------|
| Costo de adquisición de cliente (CAC) | $[X] | [Actual o estimado] |
| Margen bruto | [X]% | [Basado en desglose de COGS] |
| Costos fijos mensuales (actuales) | $[X] | [Real] |
| Contrataciones planeadas | [X] personas en mes [X] | [Plan de contratación] |
| Salario promedio totalmente cargado | $[X]/mes | [Tasa de mercado] |
| Gasto en marketing (% de ingresos) | [X]% | [Objetivo] |
```

**PUNTO DE CONTROL: Presenta los supuestos al usuario para validación antes de construir el modelo.**

---

## Fase 3: Construcción del Modelo

### Modelo de Ingresos (De Abajo Hacia Arriba)

```
## Modelo de Ingresos

### Modelo de Cohort Mensual
| Mes | Nuevos Usuarios | Perdidos | Usuarios Activos | MRR | Expansión | MRR Total |
|-----|-----------------|----------|------------------|-----|-----------|-----------|
| M1 | [X] | [X] | [X] | $[X] | $[X] | $[X] |
| M2 | [X] | [X] | [X] | $[X] | $[X] | $[X] |
| ... | | | | | | |
| M24 | [X] | [X] | [X] | $[X] | $[X] | $[X] |

### Resumen de Ingresos Anuales
| | Año 1 | Año 2 |
|--|-------|-------|
| ARR (final) | $[X] | $[X] |
| Ingresos Totales | $[X] | $[X] |
| Crecimiento Interanual | — | [X]% |
```

### Modelo de Gastos

```
## Modelo de Gastos

### Desglose Mensual de Gastos
| Categoría | M1 | M6 | M12 | M18 | M24 |
|-----------|----|----|-----|-----|-----|
| COGS | $[X] | $[X] | $[X] | $[X] | $[X] |
| Personal | $[X] | $[X] | $[X] | $[X] | $[X] |
| Marketing | $[X] | $[X] | $[X] | $[X] | $[X] |
| G&A | $[X] | $[X] | $[X] | $[X] | $[X] |
| **Total Opex** | **$[X]** | **$[X]** | **$[X]** | **$[X]** | **$[X]** |

### Plan de Personal
| Función | Mes de Inicio | Costo Mensual | Propósito |
|---------|-------------|-------------|---------|
| [Función] | M[X] | $[X] | [Por qué se necesita] |
```

### Flujo de Caja y Pista de Despegue

```
## Flujo de Caja

| | M1 | M6 | M12 | M18 | M24 |
|--|----|----|-----|-----|-----|
| Ingresos | $[X] | $[X] | $[X] | $[X] | $[X] |
| Gastos | $[X] | $[X] | $[X] | $[X] | $[X] |
| Flujo de Caja Neto | $[X] | $[X] | $[X] | $[X] | $[X] |
| Saldo de Caja | $[X] | $[X] | $[X] | $[X] | $[X] |
| Pista de Despegue (meses) | [X] | [X] | [X] | [X] | [X] |

**Mes de equilibrio:** M[X]
**Efectivo necesario para alcanzar equilibrio:** $[X]
```

---

## Fase 4: Análisis de Sensibilidad

### Sensibilidad de Variables Clave

```
## Análisis de Sensibilidad

### Impacto de Cambios en Tasa de Crecimiento en ARR M24
| Tasa de Crecimiento | ARR M24 | Pista M24 |
|--------------------|---------|-----------|
| [Base - 3%] | $[X] | [X] meses |
| [Tasa Base] | $[X] | [X] meses |
| [Base + 3%] | $[X] | [X] meses |

### Impacto de Tasa de Churn en ARR M24
| Tasa de Churn | ARR M24 | LTV |
|---------------|---------|-----|
| [Base - 1%] | $[X] | $[X] |
| [Tasa Base] | $[X] | $[X] |
| [Base + 1%] | $[X] | $[X] |

### Resumen de Economía Unitaria
| Métrica | Valor |
|---------|-------|
| CAC | $[X] |
| LTV | $[X] |
| LTV:CAC | [X]:1 |
| Período de recuperación | [X] meses |
| Margen bruto | [X]% |
```

---

## Ejemplo: Startup SaaS Etapa Seed

**Entradas:** $5K MRR, $29/mes ARPU, 8% crecimiento mensual de usuarios, 3.5% churn mensual, $120 CAC, $8K/mes costos fijos.

**Proyección M12:** $14.2K MRR, 490 usuarios activos, $10.5K gastos mensuales, equilibrio en mes 9.
**Proyección M24:** $38.6K MRR, 1,330 usuarios activos, $18K gastos mensuales (añadidas 2 contrataciones), $12K flujo de caja neto mensual.

**Sensibilidad:** Si el churn aumenta a 5%, ARR M24 cae 32%. Si el crecimiento disminuye a 5%, ARR M24 cae 41%. La tasa de crecimiento es la variable más sensible.

---

## Anti-patrones

- **Modelos de arriba hacia abajo** — "capturaremos el 1% de un mercado de $10B" no es un modelo financiero. Construye de abajo hacia arriba desde economía unitaria.
- **Supuestos estáticos** — los costos y tasas de crecimiento cambian con el tiempo. Modela cambios escalonados en contratación, precios y crecimiento.
- **Sin documentación de supuestos** — cada número debe tener justificación. Los supuestos no documentados no pueden validarse.
- **Ignorar churn** — para negocios de suscripción, churn es la variable más importante. Una diferencia del 1% en churn mensual cambia dramáticamente los resultados a 24 meses.
- **Hockey sticks perfectos** — el crecimiento real es irregular. Incluye períodos de rampa realistas para nuevos canales y contrataciones.

---

## Recuperación

- **Negocio pre-ingresos:** Modela desde la primera adquisición de cliente. Establece supuestos claramente y enfatiza el análisis de sensibilidad — los inversionistas saben que los números son inciertos.
- **Sin datos históricos para supuestos:** Usa benchmarks de industria y etiquétalos claramente. Actualiza el modelo mensualmente a medida que datos reales reemplazan supuestos.
- **Modelo demasiado complejo:** Si el usuario está abrumado, simplifica a ingresos, gastos y flujo de caja. Añade complejidad conforme se sienta cómodo.
- **Los números no funcionan:** Muestra cuáles supuestos necesitan cambiar para que el modelo funcione — ARPU más alto, churn más bajo, crecimiento más rápido o costos más bajos. Deja que el usuario decida cuál palanca tirar.
